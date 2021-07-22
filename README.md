# postman-rest-api-test-sample

This project contains aswers to topics about Postman concepts.

### 1. Please provide your reference number:
001

### 2.  Have you used Postman before?
Yes

### 3. Have you used Swagger before?
Yes

### 4. Get endpoint parameters for Login DE: Using the provided swagger, please tell us all the parameters for Login DE endpoint, including if they are required, type of parameter e.g. header and allowed value(s)
* device-os: required, header, string
* app-locale: required, header, string
* x-api-key: required, header, string
* correlation-id: optional, header, string
* loginBody: required, body, object model(json): {"username": string, "password": string}

### 5. Workspace:
Enables the users to work together sharing and organizing their projects. It facilitates a colaborative work and a better organization of the project under development.

### 6. Collection:
Helps with the organization of the requests. Provides an easier organization of requests and the users can put request from the same context into a collection.

### 7. Environment:
Resource that allows the customization of requests to a specified scope. Is useful for enabling different setups without the need to change information in requests.

### 8. Sandbox and Test Scripts:
* Sandbox: Environment used to execute scripts in Javascript for pre-requests and test for requests. Helps the implementation of scripts providing useful libraries and utilities.
* Tests Scripts: Are scripts in Javascript that run after the response is received. Can be associated with a request, folder or a collection of requests. Allow the user to check if the API is working correctly. Also can be useful to the debugging process.

### 9. Collection Runner:
Is a useful way to run a collection or a subset of it. The user can run using a specific environment and customize the execution with a specific number of interactions, log of responses and definition of time delay. This resource facilitates the automation of test execution.

### 10. Monitor:
Resource that allows the user to run collections at set intervals. Through it is possible to run requests and their tests periodically. Provides detailed dashboards about the API to the user and can help to identify problems in the API.

### 11. Newman:
Allows the user to run postman collections using comand-line instructions. It is useful to integrate the tests to the CI proccess.

### 12. Create necessary Environments - Please create and upload environments based on the following: Kurt Fritze is a DE customer and logs in to their IOS app using their username (test) and password (test), their booking reference is ADE9452. Sam Smith is a UK customer using an android device and their booking reference is AR58930. Once complete, upload the environments.

Results in folder: Exercise 12

### 13. Create a Collection: Create a single collection with all available endpoints. Once complete and you can call each endpoint, upload the collection. If you have made changes to environments, or created globals, please upload them here as well. (Hint: Login endpoints return "login-token" header on successful request).

Results in folder: Exercise 13 and 18

### 14. Did you use the import functionality to create the collection?

Yes

### 15. Reading response results in postman:

Results in folder: Exercise 15

### 16. Analyse and improve testing requirements for the following scenario: A new API has been created to standardise Login endpoint for all markets. The request is now POST only with body parameters: bookingRef, surname, username and password. A new header parameter "appName" has also been added to ensure correct processing of the data. Tester tries to login with each market and closes the testing ticket. What other tests could the tester do to ensure that API is working correctly?

* Try to login sending a valid bookingRef from another user in body
* Try to login sending a valid surname from another user in body
* Try to login sending a login and password from a deleted user
* Try to login sending a bookingRef that was deleted
* Try to login with a non existent "appName" header parameter
* Try to login without the "appName" header parameter
* Try to login using empty "appName" header parameter
* Try to login sending a body with invalid syntax
* Try to login sending a body without mandatory parameters
* Try to login sending a body with duplicated parameters
* Try to login sending a body without a mandatory parameter
* Try to login sending a body with invalid login
* Try to login sending a body with invalid password
* Try to login sending a body with invalid bookingRef
* Try to login sending a body with invalid surname
* Try to login sending a body using not expected data types into parameters

### 17. Test the APIs: Test all of the APIs using Exploratory Testing / Session Based test techniques.

Results in folder: Exercise 17

### 18. Validate headers for all requests:

Results in folder: Exercise 13 and 18




