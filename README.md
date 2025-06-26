#  Friend App – Authenticated CRUD API (Express + JWT)
A simple backend application built with **Node.js** and **Express.js** to perform **CRUD operations** on an in-memory "Friends" object, protected by **JWT and session-based authentication**.

---
##  Features
- **User Authentication** using JWT
- **CRUD operations** on a friends list
- Data stored in-memory (no database)
- Uses `req.body` to handle all input (no query/params)
- **Tested with Postman**
- Secure endpoints — only authenticated users can perform actions

# Project SetUP
## clone Repository

```bash
git clone https://github.com/sushmi-krish/friendCRUD.git
cd friendCRUD

## Install dependencies

```bash
npm install --save

## Start Server

```bash
npm start
The server run on port 8080 by default

---
# API EndPoint
## User Register
.POST/register
```bash
{
"username":"user2",
"password":"password2"
}

*POST//login
```bash
{
"username":"user2",
"password":"password2"
}

*GET/friends
  - Lists all friends hardcoded or added during the session..

* GET/friends/<email>

 - Returns details of the specific friend by email.

*POST/friends
 - ADD new Friend
```bash
{
"email":"andysmith@gamil.com",
"firstName":"Andy",
"lastName":"Smith",
"DOB":"1/1/1987"
}

*PUT/friends/<email>
 - Update the details of the existing friend 
```bash
{"DOB":"1/1/1989"}

*DELETE/friends/<email>
  - DElETE all friend by email
---  
# Authentication Middleware

All /friends routes are protected by middleware that verifies the JWT token stored in the session. Unauthorized requests receive a 403 error.

---
#Testing In Postman
1.Register a new user using /register.
2.Login with /login to generate a session token.
3.Perform CRUD operations on /friends routes with the authenticated session.
4.Screen shots are provided in the Repository 
---
#Notes
* Emails used for friend objects should be fictional (e.g., example@gamil.com) to avoid conflicts.
* JWT token expiration is configurable; default is 1 hour. You can change it (e.g., 60 seconds) for testing. 
---
# Summary
This project demonstrates how to:
 * Secure RESTful API endpoints with JWT & session authentication
 * Implement user registration and login
 * Restrict access to authenticated users only
 * Perform CRUD operations on server-stored data
 * Test API endpoints using tools like Postman

  
