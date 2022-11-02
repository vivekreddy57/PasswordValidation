Assignment Report
Problem Statement:
Write a password validation service, meant to be configurable via IoC (using dependency injection engine of your choice). The service is meant to check a text string for compliance to any number of password validation rules. The rules currently known are:
 
1.	Must consist of a mixture of lowercase letters and numerical digits only, with at least one of each.
2.	Must be between 5 and 12 characters in length.
3.	Must not contain any sequence of characters immediately followed by the same sequence.  For example, “clipper123” and “nv123123s both would be invalid due to a repeated sequence of “p” and “123” respectively.



Design:


 



PassWordValidationController: PasswordValidationController is a Rest API controller where client directly gives the password and get the validation result.

PasswordValidationTests: It contains around 37 tests covering all the possible edge cases against to our rule set. Used Junit as a testing framework.

PasswordValidator: PasswordValidator will validate the given password against all the rules.

PasswordValidationResult: It stores the validation result containing success true or false and validation message.




APIs Provided:

validatePassword

Public ResponseEntity validatePassword(String password); 

Input: String password.
Output: ResponseEntity containing success state and validation message.


Tools: IntelliJ with Spring Boot starter project.

Steps In Running the Service:

Download the ZIP file and unzip the folder.

Go to IntelliJ or Eclipse and import the project.

Run the PasswordValidatorApplication and wait for Spring framework to start the tomcat in localhost.

Below the example of console to confirm the service is up and running or not.
 

Once the service is started now our job is to test the service.

Go to Postman and give the local host end point. In my case the endpoint is

http://localhost:8080/api/passwordValidation

If you are running in localhost the end point is same. Give the endpoint and input password as a text and hit send button.

 






SampleOutput:

 

SampleTestResult:

 


CodeCoverageResult:

 


Time Spent: Complete 3 days.


References: 

https://www.youtube.com/watch?v=Ju8EybDDjBk&list=PLd3UqWTnYXOkvuQb1D4wz2BY0XnKRpEiU

https://www.udemy.com/course/microservices-with-spring-boot-and-spring-cloud/learn/lecture/8005574#questions






















