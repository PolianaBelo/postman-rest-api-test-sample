### Charter 2: 
Explore authentication rout /auth/login - Login DE
	
* Coverage: 
Response 200
Response default

* Goals:
Validate the authentication using expected body and header values.
Validate the authentication using not expected body and header values.
Validate the authentication without required parameters.
Validate the authentication with not registered users.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.
REQUEST:
```
curl --location --request POST 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test/auth/login' \
--header 'device-os: test' \
--header 'app-locale: de_DE' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--data-raw '{
  "username": "test",
  "password": "test"
}'
```
RESPONSE
```
{}
```

* Issues: -
