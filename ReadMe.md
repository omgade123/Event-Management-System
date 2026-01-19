# Event Management System

## Description

This project is an **Event Management System**, designed to facilitate the organization and management of events. It features a web-based interface for user interaction and a robust backend for data processing.

## Technologies Used

### Frontend
*   HTML
*   CSS
*   JavaScript

### Backend
*   Java (JDK 17)
*   Spring Boot (v3.4.5)
*   Spring Data JPA
*   Spring Security
*   REST APIs

### Database
*   MySQL

## Prerequisites

Before you begin, make sure you have the following installed:
*   **Eclipse IDE** (Enterprise Edition recommended) or **IntelliJ IDEA**
*   **MySQL Workbench** (for the database)
*   **VS Code** (for frontend development)
*   **Live Server Extension for VS Code** (for running HTML files locally)

## Step 1: Backend Setup Instructions

### Import the Backend Project into Eclipse
1.  Open **Eclipse IDE** and click on **File > Import**.
2.  Choose **Existing Maven Projects**, then browse and select the `event-main/event-main` folder in your project directory (where the `pom.xml` is located).
3.  Import the project into Eclipse.

### Configure MySQL Database
1.  Open **MySQL Workbench**.
2.  Create a new schema (database) named `event`. You can do this by running the following SQL command:
    ```sql
    CREATE DATABASE event;
    ```
    *(Note: No SQL dump file was found, so the application is expected to generate the schema or it must be created manually.)*
3.  Open the `src/main/resources/application.properties` file in Eclipse.
4.  Update the MySQL username and password if they differ from the defaults:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/event
    spring.datasource.username=your_username
    spring.datasource.password=your_password
    ```

### Run the Backend Application
1.  In **Eclipse**, go to the **Package Explorer** and navigate to the package `com.capgemini.event`.
2.  Locate the main application class (e.g., `EventApplication.java` or similar).
3.  Right-click on this class and choose **Run As > Java Application**.
4.  The backend server will start running and should be accessible at `localhost:8080`.

## Step 2: Frontend Setup Instructions

### Install Required Extensions in VS Code
Make sure you have the **Live Server** extension installed in VS Code.

### Open Frontend in VS Code
1.  In **VS Code**, open the `login` folder.
2.  Navigate to the `login.html` file.
3.  Right-click on the file and select **Open with Live Server** to run the frontend in your browser.
4.  The frontend will open on a local server (usually at `localhost:5500`).

## Step 3: How to Run the Project

1.  **Running the Backend**:
    *   Ensure MySQL is running and the `event` database exists.
    *   Run the Spring Boot application from Eclipse.
    *   Verify it is running at `localhost:8080`.

2.  **Running the Frontend**:
    *   Open `login/login.html` in VS Code.
    *   Use Live Server to launch the page.

## Troubleshooting

*   **Database Connection Issues**: Double-check the `application.properties` file for correct URL, username, and password. Ensure the MySQL service is running.
*   **Port Conflicts**: If port 8080 is in use, change `server.port` in `application.properties`.
*   **Frontend-Backend Communication**: Ensure the backend is running before interacting with the frontend.
