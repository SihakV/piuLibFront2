
# TSU
# TRACKING USAGE OF THE STUDENT IN PARAGON INTERNATIONAL UNIVERSITY


## Description

The TSU (Tracking Student Usage) system is designed to efficiently monitor student entries into the library through the implementation of a user identification mechanism using student ID cards equipped with QR codes.


## Features

1. **User Management:**
   - Registration and authentication of students, head department.
   - Student profile to store relevant information such as studentID, firstname, last name, email, phone number.

2. **Check-In:**
   - Tracking of students entering and leaving the library premises by Paragon.U student ID QR code.
   - Integration with student ID Cards for check-in processes.

3. **Student Tracking:**
   - Recording and maintaining entry records of students visiting the library.
   - Generating reports on student usage for the head of department.

4. **Report Format:**
   - Generate report on table format that contains a list of students from specific department and specific range of time from current week, past two weeks, past one month, past three months, and past sixth months.
   - There are two types of report. Report with library entry of the student only and with both library entry and borrowed book of the student.

5. **Administrative:**
   - Admin dashboard for register and managing student account, scan entry of the student, scan to pick up books, manage borrowed books, and generate reports.

## Software Required

- PgAdmin
- Postman
- Postgres Sql 14


## Installation Guide

- Clone the Backend Repository from the following link: [TSU Backend](https://github.com/SihakV/piuLib)
- Clone the Frontend Repository from the following link: [TSU Frontend](https://github.com/SihakV/piuLibFront2)
- Configure the folder structure as follows:
  ```
  Library-Management-System
   ├── fyp_lms_backend-main
   ├── fyp_lms_frontend-main
   
  ```
- Install the required dependencies for the backend and frontend by running the following commands:

    ```
      cd fyp_lms_backend-main
      npm install
      cd fyp_lms_frontend-main
      npm install

    ```
- Create a database in PgAdmin and restore the database from the backup file provided in the root directory of the backend repository.
- Configure the database connection in the backend by modifying the .env file in the backend repository.
- Configure the backend API URL in the frontend by modifying the env.js file in the frontend repository.
   
   example:

   ```
   const env = {
    api: 'http://127.0.0.1:8001/api/',

    //modify the api url to the backend api url, IF you change the port number or the ip address of the backend api

   };

   ```
- Run the backend server by running the following command in the backend repository:

    ```
    npm start
    ```
   
- Run the frontend server by running the following command in the frontend repository:

   ```
   npm start

   ```

- Open the browser and navigate to the frontend server URL to access the application.
- The default login credentials for the admin are as follows:

  ```
  ID: 1010
  Password: 26IiMa<Y_)
  ```
- you are in!

## Create new Librarian

- Open postman and send a POST request to the following URL:

  ```
  http://"yourbackendapiurl"/api/registerlb
  ```
- Add the following JSON object to the body of the request:

  ```
   { 
      "fullname": "yourname",
      "cardID": "yourid",
      "email": "youremail"
   }
   ```

- Send the request and the new librarian will be created.  




    
