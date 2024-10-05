# Real-Time Data Synchronization:
This is a solution that enables real-time synchronization of data between a Google Sheet and a specified database (e.g., MySQL, PostgreSQL). The solution detects changes in the Google Sheet and update the database accordingly, and vice versa.

## Architectue of the application:
My application is built using Spring Boot and PostgreSQL, providing robust real-time synchronization between multiple pairs of database tables and Google Sheets. The system architecture includes the following key components:

* **Real-Time Synchronization:**

* *Google Sheets Integration*: I use Google Apps Script to send notifications to my backend whenever changes are made in the Google Sheets. This ensures immediate updates and synchronization with the database.

* _Database Integration_: PostgreSQL functions and triggers are employed to notify the backend of any changes detected in the local database. This setup guarantees that updates in the database are promptly reflected in Google Sheets.

**Dynamic Configuration:**

* _Schema Management_: The application dynamically constructs schemas for both the database tables and corresponding Google Sheets. This automatic configuration simplifies the setup process and ensures consistency between data sources.

* _CRUD Operations_: My system supports full Create, Read, Update, and Delete (CRUD) operations for both Google Sheets and the PostgreSQL database. It seamlessly handles modifications and maintains synchronization across platforms.

* _Trigger and Function Management_: The application dynamically creates necessary triggers and functions for each table, facilitating automated responses to data changes.

**Deployment:**

* _Local Database:_ The PostgreSQL database is currently hosted locally.

* _Remote Access_: The Spring Boot application is exposed to the internet using ngrok, allowing external access and interaction with the application.

## Requirements for the Setup:

* **Java Development Kit (JDK):**

  - Version 11 or newer, as Spring Boot typically supports recent LTS versions.

* **PostgreSQL**
  
* **ngrok**
  - once ngrok has been setup run the following command:
    ```
    ngrok http 8080
    ```
### Application-Setup:
* Visit google marketplace > search for sheets > click on the google sheets api and click enable > click on credentails and add a service account > click on the service account and select keys > create a new key, download it and put the JSON file into the directory right outside the src directory in the project.
* in the application.properties file enter your postgres database name in the url and your postgres username and password.
  
### User-Setup:
* The user has to make a Google Sheet and change access from "Restricted" to "Anyone with the link" and set permissions to "Editor"
* When the user runs the application, they will be prompted with a question if they want to create a new table. If they do want to then they must type yes, else the application will still be running just listening to notifiations.
* When they type yes, they will be asked to enter the sheet id. Then they must enter the google sheet's url
* Then they will be prompted to enter the table name, primary key and column names of the table.
* once the table is created on both the google sheets and the database, copy the App Script given in this repository.
* In the google sheets window click on Extentions > App Script.
* Then paste the Appscrpt there.
* then click on the clock like button on the left
* add a new trigger
   - set the function to "sendnotification" and "notify me immediately"
   - save the trigger
* now the user can use his google sheets and database and synchronisation will start.

### Video:
[**Watch the video**](https://drive.google.com/file/d/1ItHfXC3zhYEcZADYyoaXU_pSkeHIPba5/view?usp=sharing)

