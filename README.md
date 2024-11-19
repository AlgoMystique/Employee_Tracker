# Employee Tracker

## Description

The **Employee Tracker** is a command-line application designed to manage a company's employee database. Built using Node.js, PostgreSQL, and Inquirer, this application allows business owners to view and manage departments, roles, and employees in their company. 

The application supports the following functionalities:
- Viewing all departments, roles, and employees.
- Adding new departments, roles, and employees.
- Updating an employee's role.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [License](#license)

## Installation

Follow these steps to set up the application:

### 1. Clone the repository

```
git clone https://github.com/yourusername/employee-tracker.git
cd employee-tracker
```
## 2. Install dependencies

Run the following command to install the necessary dependencies:
```
npm install
```
## 3. Set up PostgreSQL database

Ensure you have PostgreSQL installed on your machine. You can download and install it from PostgreSQL Official Site.

## 4. Create the database and tables

Open PostgreSQL CLI and create a new database:
```
psql -U postgres

CREATE DATABASE employee_tracker;

Run the schema.sql file to create the necessary tables:

psql -U postgres -d employee_tracker -f schema.sql
```

You can populate the database with initial data using the seeds.sql file (optional but useful for testing):
```
psql -U postgres -d employee_tracker -f seeds.sql
```
## 5. Configure the database connection

Make sure your database configuration in db.js matches your PostgreSQL setup (username, password, etc.).
```
const client = new Client({
  host: 'localhost',
  user: 'postgres',  // Change this to your PostgreSQL username
  password: '',      // Add your PostgreSQL password here
  database: 'employee_tracker'
});
```
## Usage
Run the Application
Once everything is set up, you can run the application with the following command:
```
node index.js
```
## Application Menu

You will be presented with a menu of actions:
View All Departments: Displays a list of all departments.
View All Roles: Displays a list of all roles and their associated departments.
View All Employees: Displays a list of employees with their roles, departments, and managers.
Add a Department: Allows you to add a new department.
Add a Role: Allows you to add a new role and assign it to a department.
Add an Employee: Allows you to add a new employee and assign a role and manager.
Update an Employee Role: Allows you to update an existing employee's role.

## Example Workflow

View All Departments: View a list of departments in the company.
Add a Department: Add a new department to the company.
Add a Role: Add a new role to an existing department.
Add an Employee: Add a new employee with a role and manager.
Update an Employee Role: Change the role of an employee.

## Features

Interactive command-line interface using Inquirer.
Integration with PostgreSQL for data persistence.
Ability to manage departments, roles, and employees efficiently.
Flexible for adding and updating employee roles, departments, and job titles.

## Technologies Used

Node.js: JavaScript runtime used to build the application.
PostgreSQL: Relational database used to store data for departments, roles, and employees.
Inquirer: Command-line interface library used to prompt user input.
pg: PostgreSQL client for Node.js to interact with the database.

## License

This project is licensed under the MIT License - see the LICENSE file for details.


