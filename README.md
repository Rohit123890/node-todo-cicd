**Node.js Todo App with CI/CD**

This is a simple Todo list application built with Node.js. It also includes Continuous Integration and Continuous Deployment (CI/CD) setup using Jenkins. This project demonstrates how to create a basic CRUD (Create, Read, Update, Delete) application for managing tasks.

**Prerequisites**

AWS account.

Node js.

Git & Github.

Jenkins.

Docker.

**Features**

Add, view, update, and delete tasks.

Continuous Integration with Jenkins.

Automatic deployment to EC2.

**Installation**

To run this project locally, follow these steps:

Clone the repository:
git clone https://github.com/Rohit123890/node-todo-cicd.git

Navigate to the project directory:
cd node-todo-cicd

Install the dependencies:

sudo apt install nodejs

sudo apt install npm

npm install

node app.js

**Usage**

Add a new task: Enter a task description in the input field and click "Add Task."

View tasks: See the list of tasks on the home page.

Update a task: Click the "Edit" button next to a task to edit its description.

Delete a task: Click the "Delete" button to remove a task.

Continuous Integration and Deployment

This project is set up for continuous integration and deployment using Jenkins. Whenever you push changes to the main branch, Jenkins will automatically build and test the application. If the build is successful, it will deploy the application to EC2.

**Acknowledgments**

This project was inspired by the need for a simple Todo list application.

Thanks to the Node.js community for their great tools and documentation.
