# React Steps Application
This project is a simple React application that demonstrates the use of state management with the useState hook. The app allows users to navigate through a sequence of steps, each displaying a different message, and dynamically updates the UI based on the current step.

## Features
  Displays three steps with corresponding messages:

      Learn React ⚛️

      Apply for jobs 💼

      Invest your new income 🤑

  Highlights the active step visually using conditional styling.

  Maintains state for:

    Current step (step): Indicates the step the user is on.

    A test object (test): Stores additional data, such as a name.

  Includes navigation buttons to move to the previous or next step.

  Demonstrates best practices for updating state objects.

# Getting Started
## Prerequisites
  Ensure you have the following installed:

    Node.js (>= 12.x)

    npm (or yarn)

## Installation
    1. Clone the repository:
       
       git clone <repository-url>
       
    2. Navigate to the project directory:

cd react-steps-app
Install dependencies:

npm install
# or
yarn install
Running the Application
Start the development server:

npm start
# or
yarn start
Open your browser and navigate to http://localhost:3000.

# Code Overview
State Management
The application uses two state variables:

step: Tracks the current step (1, 2, or 3). Navigation is handled through the handlePrevious and handleNext functions.

test: A state object containing a name property. Demonstrates how to properly update object state using setTest.

# Key Functions
handlePrevious
Decreases the step by 1, ensuring it does not go below 1:

function handlePrevious() {
  if (step > 1) setStep(step - 1);
}
handleNext
Increases the step by 1, ensuring it does not exceed 3. Also updates the name in the test object:

function handleNext() {
  if (step < 3) setStep(step + 1);
  setTest({ name: "Fred" });
}
# Dynamic Styling
The active class is applied conditionally to highlight steps based on the step state:

<div className={step >= 1 ? "active" : ""}>1</div>
Messages
The messages corresponding to each step are stored in an array and dynamically displayed using the step index:

<p className="message">
  Step {step}: {messages[step - 1]} {test.name}
</p>
# Customization
Add more steps: Update the messages array with additional steps.

Modify styles: Update the CSS classes and inline styles for buttons, step indicators, and messages.

# License
This project is licensed under the MIT License. Feel free to use, modify, and distribute it as needed.
