### Charter 4: 
Explore rout /v1/bookings about Available bookings

* Coverage: 
Response 200
Response default

* Goals:
Validate the provided bookings using the expected parameters.
Validate the request using not expected header values.
Validate the request missing required headers.
Validate the provided bookings sending differente valid values to device-os and app-locale parameters.

* Bugs:
1. The API is returning the same booking twice when sending request from device-os ios and locale de_DE.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//v1/bookings' \
--header 'login-token: 1626926835485' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'device-os: ios' \
--header 'app-locale: de_DE'
```
RESPONSE:
```
{
    "bookings": [
        {
            "bookingRef": "ADE9452",
            "startDate": "2018-07-06",
            "endDate": "2018-07-22",
            "country": "Italy"
        },
        {
            "bookingRef": "ADE9452",
            "startDate": "2018-07-06",
            "endDate": "2018-07-22",
            "country": "Italy"
        }
    ]
}
```
2. The API returns 200 when sending a request without the required header x-api-key.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//v1/bookings' \
--header 'login-token: 1626926835485' \
--header 'device-os: ios' \
--header 'app-locale: de_DE'
```
RESPONSE:
```
{
    "bookings": [
        {
            "bookingRef": "ADE9452",
            "startDate": "2018-07-06",
            "endDate": "2018-07-22",
            "country": "Italy"
        },
        {
            "bookingRef": "ADE9452",
            "startDate": "2018-07-06",
            "endDate": "2018-07-22",
            "country": "Italy"
        }
    ]
}
```
3. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.
REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//v1/bookings' \
--header 'login-token: 1626926835485' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'device-os: test' \
--header 'app-locale: en_GB'
```
RESPONSE:
```
{
    "bookings": [
        {
            "bookingRef": "AR58930",
            "startDate": "2019-05-12",
            "endDate": "2019-05-27",
            "country": "Spain",
            "lead": {}
        }
    ]
}
```
* Issues:
The documentation doesn't provide details about the response body.
The responses have different body fields when sending the requests using the available app-locale values.
