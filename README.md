# projectdocumentation

# 1. How To Install React.js On Windows?

### Step 1: Install Node.js And npm
Start by installing the Node.js installer for windows. Visit the official Node.js website and download the LTS version. Once the Installer is downloaded, run it, and follow the prompts, ensuring you don’t change any default settings. Click “Next” until the installation is complete.
![Aspose Words f200e12c-2073-48ff-9c41-ed99252eaf2c 001](https://github.com/user-attachments/assets/2d13e3f2-b0c9-4310-8f4e-986682d89794)


### Step 2: Verify that Node.js npm are installed.
After the installation is complete, you can verify that Node.js and npm are installed by opening a command prompt and running the following commands:
```bash
node --version
```

If the installation is successful, the terminal will display the installed version of Node.js.
```bash
npm --version
```
![Aspose Words f200e12c-2073-48ff-9c41-ed99252eaf2c 002](https://github.com/user-attachments/assets/fbdc5d1b-7559-42ab-b46d-5ec89b8697f8)

If the installation is successful, the terminal will display the installed version of npm.
These commands should display the version numbers for Node.js and npm, respectively.

# 2. How To Run Project?
### Step 1: Open Your Project in an IDE
Open your preferred IDE (e.g., Visual Studio Code) and navigate to the folder where your React app was installed.
![Aspose Words 0004257e-e00a-4b98-b7bb-bfbae20e7c51 003](https://github.com/user-attachments/assets/ff61d9a2-f072-4fc7-848a-900977978364)

### Step 2: Create a New React Project
Now that you have Create React App installed, you can use it to create a new React project. To do this, open a command prompt, go to the directory where you want the project to live, and run the following command:
```bash
npm create vite@latest atsfrontend
```
![Aspose Words 0004257e-e00a-4b98-b7bb-bfbae20e7c51 004](https://github.com/user-attachments/assets/4d24d614-73c7-4a62-8a84-713c9ae6db8f)

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
![Aspose Words 0004257e-e00a-4b98-b7bb-bfbae20e7c51 005](https://github.com/user-attachments/assets/1fad0f4e-94ec-4267-86d5-272ab5a66657)

```bash
npm run dev
```
This command launches the development server, which watches for changes to your project files and automatically reloads the browser when changes are detected.
<br/>
![Aspose Words 0004257e-e00a-4b98-b7bb-bfbae20e7c51 006](https://github.com/user-attachments/assets/e92854c1-a422-44ed-a2cf-4ead47334f9d)

# 3. Port Number

## 1. Purpose of the Port Configuration
The frontend of this project is built using React. By default, React runs on port 3000 during development. This documentation provides guidelines for developers to ensure that the React development server consistently uses port 3000, even if other processes might attempt to occupy this port.

## 2. Project Port Requirements
This project is designed to run only on port 3000 during development. React's development server will be configured to always use port 3000, and developers should ensure no other services are using this port. If the port is already occupied, React will throw an error, and you will need to free up the port.

[http://localhost:3000](http://localhost:3000)

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
Tailwind CSS offers a utility-first approach to styling, which can greatly speed up the development process. It allows you to apply styles directly in your JSX, reducing the need to switch between CSS and JavaScript files.

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
Bootstrap is a popular open-source front-end framework that provides a collection of CSS and JavaScript tools for building responsive, mobile-first websites. It was originally developed by Twitter and is now one of the most widely used frameworks in web development.

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

      const responseBody = await response.json();
      console.log("Response Body:", responseBody);
      let newId = responseBody.id;

      if (response.ok) {
        console.log(loginEmployeeName);

        const emitData = {
          employeeId: newId,
          userType: "Recruiters",
          employeeName: formData.employeeName,
          dateOfJoining: getFormattedDateTime(),
          userName: formData.userName,
          designation: "",
          department: "",
          officialMail: "",
          employeeEmail: "",
          employeeNumber: "",
          officialContactNumber: "",
          alternateContactNo: "",
          dateOfBirth: "",
          gender: "",
          companyMobileNumber: "",
          whatsAppNumber: "",
          emergencyContactPerson: "",
          emergencyContactNumber: "",
          emergencyPersonRelation: "",
          employeePresentAddress: "",
          employeeExperience: "",
          perks: "",
          maritalStatus: "",
          anniversaryDate: "",
          tshirtSize: "",
          lastCompany: "",
          workLocation: "",
          entrySource: "",
          employeeStatus: "",
          lastWorkingDate: "",
          reasonForLeaving: "",
          inductionYesOrNo: "",
          inductionComment: "",
          trainingSource: "",
          trainingCompletedYesOrNo: "",
          trainingTakenCount: "",
          roundsOfInterview: "",
          interviewTakenPerson: "",
          warningComments: "",
          performanceIndicator: "",
          teamLeaderMsg: loginEmployeeName,
          editDeleteAuthority: "",
          linkedInURl: "",
          faceBookURL: "",
          twitterURl: "",
          employeeAddress: "",
          bloodGroup: "",
          aadhaarNo: "",
          panNo: "",
          educationalQualification: "",
          offeredSalary: "",
          jobRole: formData.jobRole,
          professionalPtNo: "",
          esIcNo: "",
          pfNo: "",
          employeePassword: "",
          confirmPassword: "",
          profileImage: null,
          document: null,
          resumeFile: null,
          insuranceNumber: "",
          reportingMangerName: "",
          reportingMangerDesignation: "",
        };
        console.log(emitData);

        toast.success("Employee Data Added Successfully.");
        socket.emit("add_recruiter_event", emitData);
        setFormData({
          employeeId: "0",
          employeeName: "",
          dateOfJoining: "",
          userName: "",
          designation: "",
          department: "",
          officialMail: "",
          employeeEmail: "",
          employeeNumber: "",
          officialContactNumber: "",
          alternateContactNo: "",
          dateOfBirth: "",
          gender: "",
          companyMobileNumber: "",
          whatsAppNumber: "",
          emergencyContactPerson: "",
          emergencyContactNumber: "",
          emergencyPersonRelation: "",
          employeePresentAddress: "",
          employeeExperience: "",
          perks: "",
          maritalStatus: "",
          anniversaryDate: "",
          tshirtSize: "",
          lastCompany: "",
          workLocation: "",
          entrySource: "",
          employeeStatus: "",
          lastWorkingDate: "",
          reasonForLeaving: "",
          inductionYesOrNo: "",
          inductionComment: "",
          trainingSource: "",
          trainingCompletedYesOrNo: "",
          trainingTakenCount: "",
          roundsOfInterview: "",
          interviewTakenPerson: "",
          warningComments: "",
          performanceIndicator: "",
          teamLeaderMsg: "",
          editDeleteAuthority: "",
          linkedInURl: "",
          faceBookURL: "",
          twitterURl: "",
          employeeAddress: "",
          bloodGroup: "",
          aadhaarNo: "",
          panNo: "",
          educationalQualification: "",
          offeredSalary: "",
          jobRole: "",
          professionalPtNo: "",
          esIcNo: "",
          pfNo: "",
          employeePassword: "",
          confirmPassword: "",
          profileImage: null,
          document: null,
          resumeFile: null,
          insuranceNumber: "",
          reportingMangerName: "",
          reportingMangerDesignation: "",
        });
      } else {
        toast.error("Please Fill All Inputs.");
      }
    } catch (error) {
      console.error("Error:", error);
      toast.error("Error occurred while adding employee data.");
    }


```
![Aspose Words 3f0dfcdd-72f5-4fdf-b605-5f61214113ac 008](https://github.com/user-attachments/assets/efffedfe-fd60-40eb-b249-0609be1e5433)

## Component:
1. axios: A popular promise-based HTTP client for the browser and Node.js.
2. toast: Likely a library for displaying notifications to the user, possibly a toast message.
3. socket.io: A library for real-time web communication.


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
const data = await response.json();
setCallingList(data.content);

try {
  // lines updated by sahil karnekar
  let dataToUpdate = {
    callingTracker: {
      ...callingTracker,
      candidateName: callingTracker.candidateName.trim(), // Trim candidateName here
    },
    performanceIndicator: {
      employeeId: employeeId,
      employeeName: loginEmployeeName,
      jobRole: userType,
      candidateName: callingTracker.candidateName.trim(),
      jobId: callingTracker.requirementId,
      salary: convertedCurrentCTC,
      experience: `${lineUpData.experienceYear} years ${lineUpData.experienceMonth} months`,
      companyName: callingTracker.requirementCompany,
      designation: callingTracker.jobDesignation,
      candidateFormFillingDuration: formFillingTime,
      callingTacker: new Date(),
      lineup: new Date(),
      mailToClient: null,
      mailResponse: null,
      sendingDocument: null,
      issueOfferLetter: null,
      letterResponse: null,
      joiningProcess: null,
      joinDate: null,
      interviewRoundList: [],
    },
  };

  dataToUpdate.lineUp = {
    ...lineUpData,
    resume: lineUpData.resume,
  };

  if (userType === "Recruiters") {
    dataToUpdate.callingTracker.employee = { employeeId: employeeId };
  } else if (userType === "TeamLeader") {
    dataToUpdate.callingTracker.teamLeader = { teamLeaderId: employeeId };
  }
  console.log(dataToUpdate);

  const response = await axios.post(
    `${API_BASE_URL}/calling-tracker/${employeeId}/${userType}`,
    dataToUpdate,
    {
      headers: {
        "Content-Type": "application/json",
      },
    }
  );

  // This code is implemented just for testing of socket transmission
  const getFormattedDateTime = () => {
    const now = new Date();
    const year = now.getFullYear();
    const month = now.getMonth() + 1; // Months are 0-based in JavaScript
    const day = now.getDate();

    const hours = now.getHours();
    const minutes = now.getMinutes();
    const period = hours >= 12 ? 'PM' : 'AM';
    const formattedHours = hours > 12 ? hours - 12 : hours === 0 ? 12 : hours;
    const formattedMinutes = minutes < 10 ? `0${minutes}` : minutes;

    const formattedDate = `${year}-${month}-${day}`;
    return `Date: ${formattedDate}, Time: ${formattedHours}:${formattedMinutes} ${period}`;
  };

  const updatedCallingTracker = {
    ...dataToUpdate.callingTracker,
    candidateAddedTime: getFormattedDateTime(),
  };

  if (callingTracker.selectYesOrNo === "Interested") {
    socket.emit("add_candidate", updatedCallingTracker);
  }

  if (response.status === 200 || response.status === 201) {
    // Arshad Attar Added this function to add data from excel and Resume data base and
    // after added in data based delete from excel & resume data base
    // added On Date : 22-11-2024
    if (initialData && initialData.candidateId) {
      if (initialData.sourceComponent === "ResumeList") {
        await deleteResumeDataById(initialData.candidateId);
      } else if (initialData.sourceComponent === "CallingExcelList") {
        await deleteExcelDataById(initialData.candidateId);
      }
    }

    if (callingTracker.selectYesOrNo === "Interested") {
      onsuccessfulDataAdditions(true);
    } else {
      onsuccessfulDataAdditions(false);
    }
    setSubmited(false);
    setLoading(true);
    setShowConfetti(true);
    setResumeSelected(false);
    setTimeout(() => setShowConfetti(false), 4000);
    toast.success("Candidate Added Successfully..");
    setCallingTracker(initialCallingTrackerState);
    setLineUpData(initialLineUpState);
  }
} catch (error) {
  setSubmited(false);
  setLoading(false);
  if (error.response) {
    console.log("Error Response:", error.response);
    toast.error(
      "Error: " + error.response.data.message || "An error occurred"
    );
  } else if (error.request) {
    console.log("Error Request 09 --- :", error.request);
    toast.error("No response received from the server");
  } else {
    console.log("Error Message 09 --- :", error.message);
    toast.error("An error occurred: " + error.message);
  }
} finally {
  setLoading(false);
}

```
![Aspose Words d945a0ba-dd9c-48d5-bad3-b8d911a6f3f6 007](https://github.com/user-attachments/assets/4ede8b61-48c5-4cda-a4c6-d2f030151ea7)

# Functions

**Fetch API**:fetch(url): 
1. Sends a GET request to the API.

**Response Handling**:
1. response.ok: Checks if the response status is in the range 200–299.

2. If the response is not OK, an error is thrown with the HTTP status code.

3. response.json(): Converts the response to a JSON object.

**Set State**: 
1. setCallingList(data.content): Updates the state with the fetched data.

**Axios POST Request**: 
1. axios.post(url, data, config): Sends a POST request to the specified URL.

2. dataToUpdate: The data being sent to the API.

3. headers: Additional HTTP headers (e.g., Content-Type).

**Response Handling**:
1. response.ok: Checks if the response status is in the range 200–299.
2. If the response is not OK, an error is thrown with the HTTP status code.
3. response.json(): Converts the response to a JSON object.
