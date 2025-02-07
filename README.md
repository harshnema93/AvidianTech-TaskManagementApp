# Task Management System

## Project Overview

This project is a full-stack web application for managing tasks. It allows users to create, update, track, categorize, and prioritize tasks. The system provides a RESTful API backend built with C# .NET Core and a responsive single-page application frontend built with React.js.

## Features

*   **Task Management:** Create, update, complete, and delete tasks.
*   **Categorization:** Group tasks into categories for better organization.
*   **Prioritization:** Assign priorities (Low, Medium, High) to tasks.
*   **Search and Filter:** Search tasks by title or description, and filter by category or priority.
*   **Responsive UI:** User interface adapts to different screen sizes.
*   **RESTful API:** Backend exposes a RESTful API for task and category management.

## Technologies Used

*   **Backend:**
    *   C# .NET Core
    *   ASP.NET Core Web API
    *   Entity Framework Core
    *   SQL Server
    *   Serilog
*   **Frontend:**
    *   React.js
    *   Axios
    *   CSS
## Setup Instructions

Follow these steps to set up and run the Task Management System.

### Prerequisites

*   [.NET SDK 7.0 (or later)](https://dotnet.microsoft.com/en-us/download)
*   [Node.js](https://nodejs.org/) (with npm)
*   SQL Server (Express Edition or Local instance)

### Backend Setup (TaskManagementApi)

1.  **Clone the repository:**

    ```bash
    git clone [your repository link]
    ```

2.  **Navigate to the Backend Directory:**

    ```bash
    cd TaskManagementApi
    ```

3.  **Update Connection String:**
    *   In the `appsettings.json` file, replace `YourServer`, `YourUserName`, and `YourPassword` with your correct SQL Server credentials.

    ```json
    "ConnectionStrings": {
        "DefaultConnection": "Server=YourServer;Database=TaskManagementDB;User Id=YourUserName;Password=YourPassword;TrustServerCertificate=True"
    }
    ```
4.  **Apply Database Migrations:**

    *   Run the following commands in the `TaskManagementApi` directory:
        ```bash
        dotnet ef migrations add InitialCreate
        dotnet ef database update --framework net8.0
        ```

5.  **Run the Application:**
    *   Run the command
       ```bash
       dotnet run
       ```
    *  The terminal will show the URL that the backend is running on. This will be similar to `https://localhost:5063/api`.

### Frontend Setup (task-management-app)

1.  **Clone the repository:**

    ```bash
    git clone [your repository link]
    ```

2.  **Navigate to the Frontend Directory:**

    ```bash
    cd task-management-app
    ```

3.  **Install Dependencies:**

    ```bash
    npm install
    ```

4.  **Set API Base URL:**
    *  Ensure that `src/api.js` has the correct backend URL and port. Update the `API_BASE_URL` to point to your backend endpoint that you verified above.

    ```javascript
    const API_BASE_URL = 'https://localhost:5063/api'; 
    ```

5.  **Run the Development Server:**

    ```bash
    npm start
    ```

    *   This will start the React development server. App should be accessible at  `http://localhost:5173` (or another port, depending on your configuration).

## Running the Application 

1.  **Start the Backend:**
    * Follow the steps to setup and run the backend
     * Open the terminal in `TaskManagementApi` directory and use the `dotnet run` command. Ensure it is running correctly.

2.  **Start the Frontend:**
    *  Follow the steps to setup the frontend,
      * Open the terminal in `task-management-app` directory and use the `npm start` command. Ensure it is running correctly.

3.  **Access the Application:**
    *   Once both the frontend and backend are running, access the Task Management System through your web browser at the appropriate frontend URL (e.g., `http://localhost:3000`).
4. Set to access Backend.

**Notes:**

*   Make sure to install the .NET SDk, npm, and download an integrated database that is used by the backend. Without all the settings, you may not be able to set this up so double check them!



