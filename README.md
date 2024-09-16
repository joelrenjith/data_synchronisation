[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/AHFn7Vbn)
# Superjoin Hiring Assignment

### Welcome to Superjoin's hiring assignment! 🚀

### Objective
Build a solution that enables real-time synchronization of data between a Google Sheet and a specified database (e.g., MySQL, PostgreSQL). The solution should detect changes in the Google Sheet and update the database accordingly, and vice versa.

### Problem Statement
Many businesses use Google Sheets for collaborative data management and databases for more robust and scalable data storage. However, keeping the data synchronised between Google Sheets and databases is often a manual and error-prone process. Your task is to develop a solution that automates this synchronisation, ensuring that changes in one are reflected in the other in real-time.

### Requirements:
1. Real-time Synchronisation
  - Implement a system that detects changes in Google Sheets and updates the database accordingly.
   - Similarly, detect changes in the database and update the Google Sheet.
  2.	CRUD Operations
   - Ensure the system supports Create, Read, Update, and Delete operations for both Google Sheets and the database.
   - Maintain data consistency across both platforms.
   
### Optional Challenges (This is not mandatory):
1. Conflict Handling
- Develop a strategy to handle conflicts that may arise when changes are made simultaneously in both Google Sheets and the database.
- Provide options for conflict resolution (e.g., last write wins, user-defined rules).
    
2. Scalability: 	
- Ensure the solution can handle large datasets and high-frequency updates without performance degradation.
- Optimize for scalability and efficiency.

## Submission ⏰
The timeline for this submission is: **Next 2 days**

Some things you might want to take care of:
- Make use of git and commit your steps!
- Use good coding practices.
- Write beautiful and readable code. Well-written code is nothing less than a work of art.
- Use semantic variable naming.
- Your code should be organized well in files and folders which is easy to figure out.
- If there is something happening in your code that is not very intuitive, add some comments.
- Add to this README at the bottom explaining your approach (brownie points 😋)
- Use ChatGPT4o/o1/Github Co-pilot, anything that accelerates how you work 💪🏽. 

Make sure you finish the assignment a little earlier than this so you have time to make any final changes.

Once you're done, make sure you **record a video** showing your project working. The video should **NOT** be longer than 120 seconds. While you record the video, tell us about your biggest blocker, and how you overcame it! Don't be shy, talk us through, we'd love that.

We have a checklist at the bottom of this README file, which you should update as your progress with your assignment. It will help us evaluate your project.

- [x] My code's working just fine! 🥳
- [x] I have recorded a video showing it working and embedded it in the README ▶️
- [x] I have tested all the normal working cases 😎
- [ ] I have even solved some edge cases (brownie points) 💪
- [x] I added my very planned-out approach to the problem at the end of this README 📜

## Got Questions❓
Feel free to check the discussions tab, you might get some help there. Check out that tab before reaching out to us. Also, did you know, the internet is a great place to explore? 😛

We're available at techhiring@superjoin.ai for all queries. 

All the best ✨.

## Developer's Section
# Architectue of the application:
My application is built using Spring Boot and PostgreSQL, providing robust real-time synchronization between multiple pairs of database tables and Google Sheets. The system architecture includes the following key components:

**Real-Time Synchronization:**

*Google Sheets Integration*: I use Google Apps Script to send notifications to my backend whenever changes are made in the Google Sheets. This ensures immediate updates and synchronization with the database.

_Database Integration_: PostgreSQL functions and triggers are employed to notify the backend of any changes detected in the local database. This setup guarantees that updates in the database are promptly reflected in Google Sheets.

**Dynamic Configuration:**

_Schema Management_: The application dynamically constructs schemas for both the database tables and corresponding Google Sheets. This automatic configuration simplifies the setup process and ensures consistency between data sources.

_CRUD Operations_: My system supports full Create, Read, Update, and Delete (CRUD) operations for both Google Sheets and the PostgreSQL database. It seamlessly handles modifications and maintains synchronization across platforms.

_Trigger and Function Management_: The application dynamically creates necessary triggers and functions for each table, facilitating automated responses to data changes.

**Deployment:**

_Local Database:_ The PostgreSQL database is currently hosted locally.

_Remote Access_: The Spring Boot application is exposed to the internet using ngrok, allowing external access and interaction with the application.

[Watch the video](https://drive.google.com/file/d/1ItHfXC3zhYEcZADYyoaXU_pSkeHIPba5/view?usp=sharing)

