# Telecom-Domain-Project

 
 
Capstone Project: Telecom Domain Project Requirements 
Project Overview 
Project Name: API Testing for Contact List Application 
 
Domain: Telecom 
Project Description: This project aims to perform comprehensive testing of the APIs provided by the 
https://thinking-tester-contact-list.herokuapp.com/ application. 
 
The testing will cover various endpoints to ensure the functionality and reliability of the APIs. 
Objectives: 
• Verify the correctness and consistency of API responses. 
• Validate authentication and authorization mechanisms (if applicable). 
• Document test cases and results for future reference. 
 
Instructions: 
Follow the API document and test all the test cases in Postman apply the chai library assertion and 
prepare the script in RestAssured & generate the report. 
Testing Flow: 
Add User →Get user profile →Update user →Login user →Add Contact →Get contact list →Get 
contact →Update full contact →Update partial contact →Logout User 
 
Test Case 1: Add New User 
Request Type: POST 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/users 
Request Payload: 
{ 
"firstName": "Test", 
"lastName": "User", 
"email": "test@fake.com", 
"password": "myPassword" 
} 
 
Response validation: 
Test for status code and status message 201 created 
 
 
Token will generate Use the token for further test 
 
Test Case 2: Get user Profile  
Request Type: GET 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/users/me 
Headers: 
Authorization Bearer {{token}} 
Response Validation: 
Test for status code and message 
200 OK 
Test Case 3: Update User 
Request Type: PATCH 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/users/me 
Headers: 
Authorization Bearer {{token}} 
Request Payload: 
{ 
"firstN ame": "Updated", 
"lastName": "Username", 
"email": "test2@fake.com", 
"password": "myNewPassword" 
} 
Validate for status code and message 
200 OK 
Test Case 4: Log In User 
Request Type: POST 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/users/login 
Request Payload: 
{ 
 
 
"email": "test2@fake.com", 
"password": "myNewPassword" 
 
} 
 
Test it in Postman and Get the Token and validate for status code 
200 OK 
Test Case 5: Add Contact 
Request Type: POST 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/contacts 
headers 
Authorization 
Bearer {{token}} 
 
Request Payload 
{ 
"firstName": "John", 
"lastName": "Doe", 
"birthdate": "1970-01-01", 
"email": "jdoe@fake.com", 
"phone": "8005555555", 
"street1": "1 Main St.", 
"street2": "Apartment A", 
"city": "Anytown", 
"stateProvince": "KS", 
"postalCode": "12345", 
"country": "USA" 
} 
 
Validate for 201 Created 
 
 
Test Case 6: Get Contact List 
Request Type: GET 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/contacts 
headers 
Authorization 
Bearer {{token}} 
 
Validate for 200 OK 
 
Test Case 7: Get Contact 
Request Type: GET 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/contacts/ 
headers 
Authorization 
Bearer {{token}} 
 
Validate for 200 OK 
 
Test Case 8: Update Contact 
Request Type: PUT 
End Point: https://thinking-tester-contact-list.herokuapp.com/contacts/ 
headers 
Authorization 
Bearer {{token}} 
Request Payload: 
{ 
"firstName": "Amy", 
"lastName": "Miller",
 
 
"birthdate": "1992-02-02", 
"email": "amiller@fake.com", 
"phone": "8005554242", 
"street1": "13 School St.", 
"street2": "Apt. 5", 
"city": "Washington", 
"stateProvince": "QC", 
"postalCode": "A1A1A1", 
"country": "Canada" 
} 
Validate for Email and 200 OK 
 
Test Case 9: Update Contact 
Request Type: PATCH 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/contacts/ 
headers 
Authorization 
Bearer {{token}} 
Request Payload: 
{ 
"firstName": "Anna" 
} 
 
Validate for first name and 200 OK 
 
Test Case 10: Logout User 
Request Type: POST 
Endpoint: https://thinking-tester-contact-list.herokuapp.com/users/logout 
headers 
Authorization
 
 
Bearer {{token}} 
 
Validate for 200 OK 
 
 
 -------------------------------------------------------------------- END ------------------------------------------------------------ 
 
 
 
 
