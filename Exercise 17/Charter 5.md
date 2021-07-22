### Charter 5: 
Explore rout /v1/bookings/{id} about Booking Info

* Coverage: 
Response 200
Response default

* Goals:
Validate the provided info using expected parameters values.
Validate the provided info using not expected parameters values.
Validate the provided info without required parameters.
Validate the provided info sending differente valid values to device-os and app-locale parameters.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.

REQUEST:
```
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//v1/bookings/AR58930' \
--header 'login-token: 1626926835485' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'device-os: test' \
--header 'app-locale: en_GB'
```
RESPONSE:
```
{
    "bookingRef": "AR58930",
    "status": "pre",
    "startDate": "2019-05-12",
    "endDate": "2019-05-27",
    "flights": [
        {
            "flightOperator": "TUI",
            "departureDatetime": "2019-05-12T23:10:00+00:00",
            "departureAirport": "LTN",
            "arrivalDatetime": "2019-05-13T00:40:00+01:00",
            "arrivalAirport": "PMI",
            "type": "INBOUND"
        },
        {
            "flightOperator": "TUI",
            "departureDatetime": "2019-05-27T18:20:00+01:00",
            "departureAirport": "PMI",
            "arrivalDatetime": "2019-05-27T20:00:00+00:00",
            "arrivalAirport": "LTN",
            "type": "OUTBOUND"
        }
    ],
    "accomodation": [
        {
            "id": "AC45934",
            "name": "Hotel de la palma",
            "country": "Mallorca",
            "startDate": "2019-05-13",
            "endDate": "2019-05-27",
            "rooms": [
                {
                    "roomType": "ECO_LIGHT",
                    "guests": [
                        {
                            "fullName": "Sam Smith",
                            "firstName": "Sam",
                            "lastName": "Smith",
                            "lead": false
                        },
                        {
                            "fullName": "Debby Smith",
                            "firstName": "Debby",
                            "lastName": "Smith",
                            "lead": false
                        }
                    ],
                    "roomNumbers": [
                        "6B"
                    ]
                }
            ]
        }
    ]
}
```
* Issues:
The documentation doesn't provide details about the response body.
