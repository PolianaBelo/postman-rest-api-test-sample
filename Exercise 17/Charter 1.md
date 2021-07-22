### Charter 1: 
Explore /healthcheck rout to retrieve API info

* Coverage: 
Response 200
Response default

* Goals:
Validate the provided response sending differente valid values to device-os and app-locale parameters.
Validate the consistence of retrieved info.
Validate error handling.

* Bugs:
1. When requesting sending app-locale = de_DE, the API response has a null value for "uptime" key.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//healthcheck' \
--header 'app-locale: de_DE' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'Accept: application/json' \
--header 'correlation-id: 123456'
```
RESPONSE:

```
{
    "apiVersion": "1.0.0",
    "market": "DE",
    "status": {
        "health": "HEALTHY",
        "uptime": null
    }
}
```
 
2. The API returns error code 500 "Internal Server Error" when sending specials characters in correlation-id header.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//healthcheck' \
--header 'app-locale: de_DE' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'Accept: application/json' \
--header 'correlation-id: !@#$'
```
RESPONSE:
```
{
    "error": {
        "code": 500,
        "message": "Internal Server Error"
    }
}
```

* Issues:
The documentation doesn't provide details about the expected response body.
