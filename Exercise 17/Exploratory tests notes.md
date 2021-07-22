# Exploratory testing exercise

## Notes:
The API should document error responses. All error responses are described as default.
The header correlation-id isn't returned in responses and its descritions could be better detailed in the documentation.
The API returns code 403 "Missing Authentication Token" when using invalid paths. The message isn't describing the real error.
All requests using special characters for correlation-id header returns error 500 (an example is reported in Charter 1).

## Test charters
The elaborated charters are available in Exercise 17 folder into files: Charter 1, Charter 2, Charter 3, Charter 4, Charter 5 and Charter 6.
