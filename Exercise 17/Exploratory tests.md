# Exploratory testing exercise

This project contains aswers to topics about exploratory testing.

## Observations about the API documentation:
The API should document error responses. All error responses are described as default.
The header correlation-id isn't returned in responses and its descritions could be better detailed in the documentation.

## Test charters

### Charter 1: 
Explore /healthcheck rout to retrieve API info
* Coverage: 
Response 200
Response default
* Goals:
Validate the consistence of retrieved info.
Validate error handling.
* Bugs:
1. When requesting sending app-locale = de_DE, the API response has a null value for "uptime" key.
2. The API returns error code 500 "Internal Server Error" when sending specials characters in correlation-id header.
* Issues:
The documentation doesn't provide details response body.

### Charter 2: 
Explore authentication rout /auth/login - Login DE	
* Coverage: 
Response 200
Response default
* Goals:
Validate the authentication using expected body and header values.
Validate the authentication using not expected body and header values.
Validate the authentication without required parameters.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android, ios are expected.

* Issues:
-

### Charter 3: 
Explore authentication rout /auth/login - Login UK	
* Coverage: 
Response 200
Response default
* Goals:
Validate the authentication using expected header values.
Validate the authentication using not expected header values.
Validate the authentication without required parameters.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.

* Issues:
The documentation doesn't provide any details about the expected response body.

### Charter 4: 
Explore rout /v1/bookings about /v1/bookings
* Coverage: 
Response 200
Response default
* Goals:
Validate the provided bookings using the expected parameters.
Validate the request using not expected header values.
Validate the request missing required headers.

* Bugs:
1. The API is returning the same booking twice.
2. The API returns 200 when sending a request without the required header x-api-key.
3. The API returns 200 when using a not available value in device-os header. According to the documentation only android and ios are expected.

* Issues:
The documentation doesn't provide details about the response body.

### Charter 5: 
Explore rout /v1/bookings/{id} about Booking Info	
* Coverage: 
Response 200
Response default
* Goals:
Validate the authentication using expected header values.
Validate the authentication using not expected header values.
Validate the authentication without required parameters.

* Bugs:
1. The API returns 200 when using a not available value in device-os header. According to the documentation only android, ios are expected.

* Issues:
The documentation doesn't provide details about the response body.

### Charter 6: 
Explore rout /v1/bookings/{id} about Booking Info	
* Coverage: 
Response 200
Response default
* Goals:
Validate the authentication using expected header values.
Validate the authentication using not expected header values.
Validate the authentication without required parameters.

* Bugs:
1. The API returns code 403 "Missing Authentication Token" when requesting with an invalid path.

* Issues:
The documentation doesn't provide details about the response body.


