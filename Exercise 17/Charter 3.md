### Charter 3: 
Explore authentication rout /auth/login - Login UK
	
* Coverage: 
Response 200
Response default

* Goals:
Validate the authentication using expected header values.
Validate the authentication using not expected header values.
Validate the authentication without required parameters.
Validate the authentication with not registered users.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test/auth/login?bookingRef=AR58930&surname=Smith' \
--header 'app-locale: en_GB' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'Accept: application/json' \
--header 'device-os: test'	
```
RESPONSE:
```
{
    "bookingRef": "AR58930",
    "surname": "Smith"
}
```

* Issues:
The documentation doesn't provide details about the expected response body.
