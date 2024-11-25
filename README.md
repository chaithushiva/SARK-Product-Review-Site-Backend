# SARK Product Review Site - Backend

This Project is Developed as a part of course CS5610. It is Developed by Kaushik Boora, Rahul Reddy Baddam, Sai Sriker Reddy Vootukuri and Abhishek Kumar.
This Repository contains the code for the Backend of SARK Product review site.

## About

SARK Product review site is a website where users can lookup for products and rate them, developed using NodeJS, ExpressJS, JWT, MongoDB technologies on the Backend.
The site essentially uses a Free Open API service that provides product information. This product Information can be stored on Database. This site assumes there are 3 types of users, Customer, Dealer and Admin.
For the Frontend Code of this project Please visit [SARK Product Review Site - Frontend](https://github.com/BooraKaushik/SARK-Product-Review-Site-Frontend)

## Features

This Project Provides the following RESTful APIs,
| API Name | Path | HTTP Verb | Description |
| -------- | ---- | --------- | :---------- |
| Create User | /api/users | POST | Creates a User by taking in info such as first name, last name, email etc. Example body: <pre>{<br>"confirmPassword": "Kaushik@123",<br>"dateOfBirth": "2022-04-11",<br>"email": "kaushik.boo97@gmail.com",<br>"firstName": "Kaushik",<br>"lastName": "Boora",<br>"password": "Kaushik@123",<br>"phone": "(857) 230-5227",<br>"type": "Customer",<br>"address":{<br>"addressLine": "10 Buckley Ave Apt 1",<br>"addressLine2": " mnbh",<br>"city": "Jamaica Plain",<br>"state": "Massachusetts",<br>"zipcode": "02130-2293"}<br>}</pre> |
| Login | /api/login | POST | Logs a user in and sends JWT token back to the user. For authenticated routes this token must be sent in header for authorizaion. Example body:<pre>{<br> "email":"kaushik.boo97@gmail.com",<br> "password":"Kaushik@123"<br>}</pre> |
| Unique Email | /api/uniqueEmail | POST | This API checks if a given username is already in the DB. |
| Update User Info | /api/updateusers | PUT | This API updates the user information. |
| Fetch All Users | /api/all-users | POST | This is an authenticated route, Reqires the id of the user sent in the body. All user info is returned if the user requesting data is an admin. |
| Remove a particular user | /api/remove-users | DELETE | This is an authenticated route, Reqires the id of the requesting user sent as id and id of user to be deleted as delid in the body. A user is deleted if the user requesting is an admin. |
| Add a review | /api/add-review | POST | This is an authenticated route and requires user id sent in the body |
| Add a like | /api/add-like | POST | This is an authenticated route and requires user id sent in the body |
etc..

## Running the project

Follow the below steps to run the project

1. Clone the Directory.
2. Make sure the MongoDB instance is running.
3. In a terminal move to the cloned directory. Execute the following command `npm start`. This will start the Backend on port 4300.
