# User Management System

## Framework and Language Used

- `Framework` SpringBoot
- `Language` java

## Description
   Welcome to the User Management System repository! This open-source project is a Java-based application built using the Spring Boot framework. The User Management System allows users to manage application users through a set of APIs. With these APIs, users can perform various operations such as adding users, updating user information (including all properties), deleting users, retrieving users by their user ID, and retrieving a list of all users.

## Data flow

  The project is organized into several parts, each serving a specific purpose:

### 1. Controller

  This section houses the `UserController` class, which provides API endpoints for interacting with the User Management System. Here is a list of available endpoints:

- `POST /userMan/Users` : Adds a new user. Accepts a user object in the request body.
- `GET /Users/id/{id}` : Retrieves user information by user ID.
- `GET /userMan/allUsers` : Retrieves a list of all users.
- `PUT /updateUserInfo/{id}` : Updates user information. Accepts user ID and optional parameters for name, username, address, and phone number.
- `DELETE /Users/delete/{ids}` : Deletes a user by user ID.

### 2. Services

The Services section includes a set of service classes that the API Controller class uses to handle user management operations. The list of services includes:

- `addUser` : Adds a new user to the system.
- `getUser` : Retrieves user information by user ID.
- `getAllUser` : Retrieves a list of all users in the system.
- `updateUserInfo` : Updates user information, allowing for changes to name, username, address, and phone number.
- `removeUsers` : Deletes a user by their user ID.

### 3 model :-

  This section contains the `UserManage` class, which represents the core entity of the system. The `UserManage` class includes the following properties:

- `userId` (Integer) : Unique identifier for each user.
- `userName` (String) : User's username.
- `DateOfBirth` (LocalDate) : User's DateOfBirth.
- `email` (String) : User's EmailAddress.
- `phoneNumber` (String) : User's phone number.
- `date` (Date) : user's current date.
- `time` (Time) : user's current time.

### 4.Repository

In this layer data is stored. for storing data I have used database (H2-console).