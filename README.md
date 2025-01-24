# Project Documentation

# 1. How To Install React.js On Windows?

### Step 1: Install Node.js And npm
### Step 1: Install Node.js And npm

Start by installing the Node.js installer for Windows. Visit the [Node.js official website](https://nodejs.org/) and download the LTS version. Once the installer is downloaded, run it, and follow the prompts, ensuring you don’t change any default settings. Click “Next” until the installation is complete.
![Npm](https://github.com/user-attachments/assets/8fdafbc8-4499-4ebc-bd4d-17189d8803d1)


### Step 2: Verify that Node.js npm are installed.
After the installation is complete, you can verify that Node.js and npm are installed by opening a command prompt and running the following commands:
```bash
node --version
```

If the installation is successful, the terminal will display the installed version of Node.js.
```bash
npm --version
```
![Version](https://github.com/user-attachments/assets/01ce4967-1297-463c-8d23-ef489ffba116)

If the installation is successful, the terminal will display the installed version of npm.
These commands should display the version numbers for Node.js and npm, respectively.

# 2. How To Run Project?
### Step 1: Open Your Project in an IDE
Open your preferred IDE (e.g., Visual Studio Code) and navigate to the folder where your React app was installed.
![IDE](https://github.com/user-attachments/assets/01d2c8dc-5cd2-419f-b9c1-dc4856cad775)

### Step 2: Create a New React Project
Now that you have Create React App installed, you can use it to create a new React project. To do this, open a command prompt, go to the directory where you want the project to live, and run the following command:
```bash
npm create vite@latest atsfrontend
```
![Npm command](https://github.com/user-attachments/assets/6c035137-3e0b-4ba4-a01c-0262f702b654)

Replace “atsfrontend” with the desired name for your project. Create React App will create a new directory with the specified name and generate a new React project with a recommended project structure and configuration.
### Step 3: Start The Development Server
Once the project is created, head over to the project directory by running the following command in the command prompt:
```bash
cd atsfrontend
```
Replace “atsfrontend” with the name of your project directory. Now, start the development server by running the following command:
```bash
npm install
```
![Start server](https://github.com/user-attachments/assets/da0327d2-85df-4724-ad0d-e0d32ea2a71c)

```bash
npm run dev
```
This command launches the development server, which watches for changes to your project files and automatically reloads the browser when changes are detected.
<br/>
![Page](https://github.com/user-attachments/assets/a3b4ebd5-0952-48a8-afd2-278e10c3934a)

# 3. Port Number

## 1. Purpose of the Port Configuration
The frontend of this project is built using React. By default, React runs on port 3000 during development. This documentation provides guidelines for developers to ensure that the React development server consistently uses port 3000, even if other processes might attempt to occupy this port.

## 2. Project Port Requirements
This project is designed to run only on port 3000 during development. React's development server will be configured to always use port 3000, and developers should ensure no other services are using this port. If the port is already occupied, React will throw an error, and you will need to free up the port.

`http://localhost:3000`

## 3. Troubleshooting
- **Port Conflict:** If port 3000 is already in use by another application, you will need to free up the port or modify the configuration to use a different one.
- **Firewall Issues:** Ensure that your firewall or network settings are configured to allow traffic on port 3000 for local development.

This command launches the development server, which watches for changes to your project files and automatically reloads the browser when changes are detected.
# Project Structure

```
atsfrontend
│
├── atsfronted
│     ├── public
│     │     ├── files
│     │     │        ├── calling_Tracker_format.xlsx
│     │     │        ├── Lineup_Tracker_format.xlsx
│     ├── src
│     │     ├── AddCandidate
│     │     │        ├── CallingTrackerForm.jsx
│     │     │        ├── employeeMasterSheet.jsx
│     │     │        ├── UpdateSelfCalling.jsx
│     │     ├── App.css
│     │     ├── App.jsx
│     │     ├── index.css
│     │     ├── main.jsx
│     ├── .eslintrc.cjs
│     ├── .gitignore
│     ├── index.html
│     ├── package-lock.json
│     ├── postcss.config.js
│     ├── README.md
│     ├── tailwind.config.js
│     ├── vite.config.js
│     ├── vite.config.js.timestamp-1724634013512-4fb99d3a1e7c6.mjs
│     ├── vite.config.js.timestamp-1724634013512-6473bf87f809d.mjs
│
└── README.md
```

# App.jsx

In a React application, `App.jsx` is a central component file that typically serves as the entry point for rendering the main application. It acts as the root component of your React app and often contains the core structure and layout of the application.

## Key Points about App.jsx in React:

### 1. Default Component:

In React apps created with Create React App, `App.jsx` is automatically included as the main component. It is usually rendered by `index.js` and acts as the parent component for other components.

### 2. Component Structure:

`App.jsx` is a functional or class-based React component. It defines the primary structure of your app and integrates other components.

### 3. Purpose:

`App.jsx` is typically used to:

- Define the layout and structure of the app.
- Integrate and manage state (often using tools like React's `useState` or `useReducer`).
- Serve as the central hub to load and nest other child components.
- Implement routing using tools like `react-router`.

# CSS

## 6.1 Tailwind CSS
<a href="https://tailwindcss.com/" target="_blank" >Tailwind</a> CSS offers a utility-first approach to styling, which can greatly speed up the development process. It allows you to apply styles directly in your JSX, reducing the need to switch between CSS and JavaScript files.

### The Tailwind CSS configuration file (`tailwind.config.js`)
```js
/** @type {import('tailwindcss').Config} */
export default {
  content: ["./index.html", "./src/*/.{js,ts,jsx,tsx}"],
  theme: {
    extend: {
      colors: {
        primary: 'var(--primary-color)', // Use CSS variable for the primary color
      },
    },
  },
  plugins: [],
};
```
### Key Features of Tailwind CSS:
- **Utility-First:** Use pre-made classes in HTML/JSX for styling (e.g., padding, colors) instead of custom CSS.
- **Customizability:** Easily adjust Tailwind settings to fit your project's unique design.
- **Responsive Design:** Simplifies creating designs that work on different screen sizes using classes like `sm:`, `md:`, `lg:`.
- **No Pre-made UI:** Gives you full control to design your UI without predefined components.
### Example

```js
import React from 'react';

function Button() {
  return (
    <button className="px-4 py-2 bg-blue-500 text-white rounded-lg hover:bg-blue-700">
      Click Me
    </button>
  );
}

export default Button;
```
### In this example:
- `px-4` adds padding to the left and right of the button.
- `py-2` adds padding to the top and bottom.
- `bg-blue-500` sets the background color.
- `text-white` makes the text color white.
- `rounded-lg` applies rounded corners.
- `hover:bg-blue-700` changes the background color on hover.
## 6.2 Bootstrap
[Bootstrap](https://getbootstrap.com/) is a popular open-source front-end framework that provides a collection of CSS and JavaScript tools for building responsive, mobile-first websites. It was originally developed by Twitter and is now one of the most widely used frameworks in web development.

The following two lines of code are used to import Bootstrap styles and JavaScript functionality into a React project:
```js
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/js/bootstrap.js';
```
### Example

```js
import React from 'react';
import 'bootstrap/dist/css/bootstrap.css';

function App() {
  return (
    <div className="container">
      <h1 className="text-center text-primary">Hello, Bootstrap!</h1>
      <p className="text-muted">This is a simple example of Bootstrap styling in React.</p>
      <button className="btn btn-success">Click Me</button>
    </div>
  );
}

export default App;
```
### Component Use:
- `container`: Centers the content with padding.
- `text-center`: Centers the text.
- `text-primary`: Makes the text color blue (Bootstrap's primary color).
- `text-muted`: Makes the text color gray.
- `btn btn-success`: Styles the button with a green background.



# Component Information

### 1. Component Purpose and Overview:
The purpose of this component is to manage the Calling Tracker Form functionality. It is responsible for fetching data, submitting new data, and updating the calling tracker. The component also integrates with APIs, handles socket transmissions, and shows success/error notifications to the user.

### Example Code:

```jsx
// App.jsx
import CallingTrackerForm from "./CallingTrackerForm";
export default function App() {
  return (
    <div>
      <CallingTrackerForm/> 
    </div>
  );
}
```


### CallingTrackerForm.jsx

```javascript
try {
     
      
    axios.post(
        ${API_BASE_URL}/calling-tracker/${employeeId}/${userType},
        dataToUpdate,
        {
          headers: {
            "Content-Type": "application/json",
          },
        }

```
<img src="https://github.com/user-attachments/assets/17b629ae-9bfe-43f4-a034-79875c882f4a" width="900">

## Dependencies:
1. <a href="https://www.npmjs.com/package/axios" target="_blank">Axios</a>: A popular promise-based HTTP client for the browser and Node.js.

## Request Body:
2. **dataToUpdate** (Object): This object contains the data to be sent in the request body. The data is typically in JSON format and can include various fields related to the calling tracker (e.g., call count, duration, etc.).





# API Fetching in React

API fetching in React means getting data from an external source, like a server or database, using an API (a way to communicate between systems). When you make a request to an API, you ask for information, and the API sends it back to your React app.

## Why use API fetching in React?

1. **Get Dynamic Data**: Your app can show real-time data, like the latest news, weather, or user information, by fetching it from an API.
   
2. **Organize Code Better**: The app gets data from a backend (like a server), while React focuses on showing it to users. This keeps your code clean.

3. **Save Data**: You can send or receive data to/from a server. For example, if a user fills out a form, you can send that data to be saved.

4. **Load Data in the Background**: React can fetch data without freezing the page, so users can still interact with the app while the data loads.
## Example of API Fetching

```javascript
const response = await fetch(
  `${API_BASE_URL}/calling-lineup/${employeeId}/${userType}?searchTerm=${searchTerm}&page=${page}&size=${size}`
);
if (!response.ok) {
  throw new Error(`HTTP error! Status: ${response.status}`);
}
```
![Api](https://github.com/user-attachments/assets/3113931a-1d56-4148-a084-57b9ed51466b)

## Dependencies
- **fetch**: A native JavaScript function to make HTTP requests. It returns a `Promise` that resolves to the response of the request.

## Request Format
- The request is made to the calling lineup API endpoint with dynamic segments (`employeeId` and `userType`) as part of the URL.
- Query parameters (`searchTerm`, `page`, `size`) are appended to the URL to provide filtering and pagination capabilities.
