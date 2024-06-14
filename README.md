# Todo List 📆

A practical web application built with Node.js, Express, and MySQL for you to record, view, and manage your tasks. This application supports user authentication, two-factor authentication, subtasks, and email notifications.

## Features

### User Authentication

- **Sign Up:** Users can create an account by providing their name, email, and password.
- **Log In:** Users can log in using their registered email and password.
- **Log In with Facebook:** Users can log in via Facebook.
- **Log Out:** Users can log out of their account.

### Two-Factor Authentication (2FA)

- **Enable 2FA:** Users can enable 2FA for added security.
- **Verify 2FA:** Users must verify their identity using a code from an authenticator app during login.

### Task Management

- **View Todos:** Users can view a list of their tasks with name, due date, and status.
- **Create Todo:** Users can create a new task with details.
- **Edit Todo:** Users can update the details of an existing task.
- **Delete Todo:** Users can delete a task.
- **Subtasks:** Users can add, update, and delete subtasks for each task.

### Notifications

- **Email Notifications:** Users receive email reminders for newly created tasks.

## Project First Look

![Application Screen Shot in GIF](todoList.gif)

## Installation

### Prerequisites

- [Node.js v10.16.0](https://nodejs.org/en/download/)
- [MySQL v8.0.16](https://dev.mysql.com/downloads/mysql/)
- [MySQL Workbench v8.0.16](https://dev.mysql.com/downloads/workbench/)

### Clone the Repository

```sh
$ git clone https://github.com/EgemenErin/ToDo-List
$ cd ToDo-List

Setup Database

Create and use the todo_sequelize database via MySQL Workbench:

DROP DATABASE IF EXISTS todo_sequelize;
CREATE DATABASE todo_sequelize;
USE todo_sequelize;

Setup App

	1.	Create a Facebook account and App:
	•	Facebook Developers
	2.	Create a Facebook App and get the App ID & Secret:

My Apps -> Create App -> Scenario: Integrate Facebook Login -> Settings -> Basic


	3.	Install packages via npm:

$ npm install


	4.	Create .env file:

$ touch .env


	5.	Store API Key in .env file and save:

FACEBOOK_ID=<YOUR_FACEBOOK_APP_ID>
FACEBOOK_SECRET=<YOUR_FACEBOOK_APP_SECRET>
FACEBOOK_CALLBACK=<YOUR_FACEBOOK_REDIRECT_URI>


	6.	Edit password in config/config.json file:

"development": {
  "username": "root",
  "password": "<YOUR_WORKBENCH_PASSWORD>",
  "database": "todo_sequelize",
  "host": "127.0.0.1",
  "dialect": "mysql",
  "operatorsAliases": false
}


	7.	Create models:

$ npx sequelize db:migrate


	8.	Activate the server:

$ npm run dev


	9.	Visit the application:
Open your browser and go to http://localhost:3000

This new README file includes details about the updated features, installation instructions, and prerequisites. Feel free to modify it further if needed!
