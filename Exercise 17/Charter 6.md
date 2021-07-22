### Charter 6: 
Explore rout /v1/bookings/{id}/weather about weather

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
curl --location --request GET 'https://4s9rh46bpe.execute-api.eu-central-1.amazonaws.com/test//v1/bookings/AR58930/weather' \
--header 'login-token: 1626926835485' \
--header 'x-api-key: 0qNSzqieHI5M36LLgY7Y85Zco0SMXKyr37MIOSAG' \
--header 'device-os: test' \
--header 'app-locale: en_GB'
```
RESPONSE:
```
{
    "weather": [
        {
            "startDate": "2019-05-12",
            "endDate": "2019-05-27",
            "weatherStations": [
                {
                    "id": "WS64353",
                    "city": "Palma",
                    "country": "Spain",
                    "temperatureUnit": "CELCIUS",
                    "speedUnit": "MPH",
                    "weatherData": [
                        {
                            "date": "2019-05-12",
                            "temperatureMin": "15",
                            "temperatureMax": "29",
                            "temperatureWater": "19",
                            "windDirection": "WW",
                            "windSpeed": 10,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-13",
                            "temperatureMin": "17",
                            "temperatureMax": "30",
                            "temperatureWater": "19",
                            "windDirection": "SW",
                            "windSpeed": 6,
                            "chanceOfRain": 0,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-14",
                            "temperatureMin": "24",
                            "temperatureMax": "37",
                            "temperatureWater": "21",
                            "windDirection": "S",
                            "windSpeed": 3,
                            "chanceOfRain": 2,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-15",
                            "temperatureMin": "22",
                            "temperatureMax": "37",
                            "temperatureWater": "22",
                            "windDirection": "SE",
                            "windSpeed": 4,
                            "chanceOfRain": 10,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-16",
                            "temperatureMin": "23",
                            "temperatureMax": "34",
                            "temperatureWater": "22",
                            "windDirection": "SE",
                            "windSpeed": 6,
                            "chanceOfRain": 22,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-17",
                            "temperatureMin": "20",
                            "temperatureMax": "30",
                            "temperatureWater": "22",
                            "windDirection": "E",
                            "windSpeed": 9,
                            "chanceOfRain": 40,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-18",
                            "temperatureMin": "26",
                            "temperatureMax": "35",
                            "temperatureWater": "22",
                            "windDirection": "E",
                            "windSpeed": 5,
                            "chanceOfRain": 34,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-19",
                            "temperatureMin": "26",
                            "temperatureMax": "34",
                            "temperatureWater": "22",
                            "windDirection": "SW",
                            "windSpeed": 5,
                            "chanceOfRain": 20,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-20",
                            "temperatureMin": "27",
                            "temperatureMax": "38",
                            "temperatureWater": "24",
                            "windDirection": "SW",
                            "windSpeed": 2,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-21",
                            "temperatureMin": "22",
                            "temperatureMax": "33",
                            "temperatureWater": "22",
                            "windDirection": "SW",
                            "windSpeed": 10,
                            "chanceOfRain": 12,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-22",
                            "temperatureMin": "18",
                            "temperatureMax": "29",
                            "temperatureWater": "19",
                            "windDirection": "S",
                            "windSpeed": 5,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-23",
                            "temperatureMin": "15",
                            "temperatureMax": "29",
                            "temperatureWater": "18",
                            "windDirection": "SW",
                            "windSpeed": 10,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-24",
                            "temperatureMin": "25",
                            "temperatureMax": "29",
                            "temperatureWater": "19",
                            "windDirection": "SW",
                            "windSpeed": 10,
                            "chanceOfRain": 7,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-25",
                            "temperatureMin": "24",
                            "temperatureMax": "27",
                            "temperatureWater": "20",
                            "windDirection": "W",
                            "windSpeed": 7,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-26",
                            "temperatureMin": "26",
                            "temperatureMax": "34",
                            "temperatureWater": "21",
                            "windDirection": "W",
                            "windSpeed": 10,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        },
                        {
                            "date": "2019-05-27",
                            "temperatureMin": "24",
                            "temperatureMax": "31",
                            "temperatureWater": "19",
                            "windDirection": "W",
                            "windSpeed": 6,
                            "chanceOfRain": 5,
                            "icon": "http://www.tui.co.uk/storage/images/icons/weather/sun.jpg"
                        }
                    ]
                }
            ]
        }
    ]
}
```
* Issues:
The documentation doesn't provide details about the response body.
The success response 204 for no content found isn' documented.

