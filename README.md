                                              Backend (Spring Boot)

Overview:
----------
This backend service is built with Spring Boot. It provides REST APIs to manage user data loaded from a pipe-separated text file (userData.txt). 

The service supports:
---------------------
--> Fetching all users
--> User login authentication

User data includes login time calculation based on login start and end timestamps.

Technologies:
--------------
--> Java 17
--> Spring Boot
--> Lombok
--> Maven (build tool)

Setup & Run:
--------------
a)Clone the repository.
b)Make sure userData.txt is located in src/main/resources.

Build the project using:
------------------------
--> mvn clean install

Run the application:
---------------------
--> mvn spring-boot:run

The API will be available at http://localhost:8080/api/users.

Endpoints:
----------
--> GET /api/users — Returns list of all users.
--> POST /api/users/login — Accepts JSON body with username and password; returns user data if authenticated.

Project Structure Summary:
--------------------------

Backend:
---------
--> model — User and Login data models
--> repository — Reads user data from text file
--> service — Business logic for user management
--> controller — REST API endpoints

Notes:
-------
--> User data is read from a static text file.
--> Passwords are stored in plain text for simplicity (not recommended for production).
--> Time online is calculated as the difference between login and logout timestamps.

