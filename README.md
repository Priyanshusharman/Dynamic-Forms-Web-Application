﻿# Dynamic-Forms-Web-Application
Certainly! Below is the updated README.md file, incorporating the additional details for installation, running the server, and Google Sheets synchronization:

---

# Dynamic Forms Web Application

This web application is developed using the SQL, Express, React, and Node.js stack. It features dynamic forms with form validation, database storage, data synchronization with Google Sheets, and a responsive user interface.

---

## Installation

### Prerequisites

- Node.js and npm installed
- MySQL database server
- Google Sheets API credentials (for synchronization with Google Sheets)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/dynamic-forms-webapp.git
   cd dynamic-forms-webapp
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up MySQL database:

   - Create a MySQL database and update the database configuration in `backend/config/database.js` with your MySQL `user` and `password`.

   ```javascript
   // backend/config/database.js

   module.exports = {
       host: 'localhost',
       user: 'root', // Your MySQL username
       password: 'priyanshu', // Your MySQL password
       database: 'forms_db'
   };
   ```



## How to Run the Application

1. **Start the backend server:**

   ```bash
   nodemon server.js
   ```

2. **Start the React development server:**

   ```bash
   cd client
   npm start
   ```

3. **Open your browser and navigate to `http://localhost:3000` to view the application.**

---

## Functionality Implemented

### Interface:

- Simple user interface with buttons "Form A" and "Form B".
- Clicking each button leads to a form with a dynamic heading ("Form A" or "Form B").

### Form Details:

- Both forms include fields: Name (text input), Country Code (dropdown selection), Phone Number (text input).
- Form validation ensures:
  - Name field is not empty and contains only alphabetic characters (including spaces).
  - Country code is selected from a predefined list of codes.
  - Phone number is numeric and conforms to the format specified by the selected country code.

### Database:

- Uses SQL (MySQL) to store form data.
- Each entry captures form type (A or B), name, country code, and phone number.

### Data Synchronization:

- Implements functionality to connect to an online Excel sheet.
- Includes a "Refresh" button that updates the Excel sheet with new data from the SQL database.
- Synchronization with Google Sheets: [Google Sheet Link](https://docs.google.com/spreadsheets/d/1Zk9ebONjS7cNxE6xjTY92Gf4Cwzo3ErdP8UgNhJ9r4Q/edit#gid=0).

### Additional Features:

- Responsive design for both mobile and desktop views.
- Uses local storage to save form data locally, allowing data persistence across sessions.


## Live Demo video

You can view a live demo video : https://drive.google.com/drive/folders/135A4vIO3VIDmeLs0Lzw2mN6kUWMFoFj9?usp=sharing
