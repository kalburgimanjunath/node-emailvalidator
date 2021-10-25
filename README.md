const request = require('request')
const fs = require('fs')

const options = {
method: 'POST',
url: 'https://api.reacher.email/v0/check_email',
headers: {
'content-type': 'application/json',
'authorization': 'test_api_token'
},
body: {
to_email: 'test@gmail.com'
},
json: true
}

request(options, (error, response, body) => {
if (error) throw new Error(error)

console.log(body)
})
