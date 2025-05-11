# Feedback-Management-System
A web-based application designed to collect, manage, and analyze user feedback for continuous improvement in services or products
The Feedback Management System is a web application that allows users to submit feedback and view all feedback entries. The project is built with a Node.js backend using Express and TypeScript and a React frontend using TypeScript. The backend manages the feedback entries, and the frontend provides a user interface for submitting and viewing feedback.

Cloning Instructions
git clone https://github.com/exclusiveabhi/feedback-system.git
Setup Instructions
Backend Setup
Navigate to the backend directory:

cd feedback-management-system/backend
Install dependencies:

npm install
Install CORS type definitions:

npm install @types/cors --save-dev
Start the server:

For development, you can use ts-node to run TypeScript directly:

npx ts-node src/index.ts
Alternatively, you can compile the TypeScript code to JavaScript and run it with Node.js:

npx tsc
node dist/index.js
Verify the server is running:

Open your browser or use a tool like Postman to navigate to http://localhost:3000/feedback. You should see an empty array (since there are no feedback entries initially).

Frontend Setup
Navigate to the frontend directory:

cd ../frontend
Install dependencies:

npm install
Start the React application:

npm start
Verify the application is running:

Open your browser and navigate to http://localhost:3001. You should see the feedback form and a list (which will be empty initially).

Backend Code Details
src/index.ts: Entry point of the server.
src/controllers/feedback.controller.ts: Handles API routes.
src/services/feedback.service.ts: Contains business logic.
src/models/feedback.model.ts: Defines the Feedback model.
Frontend Code Details
src/components/FeedbackForm.tsx: Form for submitting feedback.
src/components/FeedbackList.tsx: Displays a list of feedbacks.
src/App.tsx: Main application component.
Additional Notes
The backend uses an in-memory data structure to store feedback entries.
The frontend uses Axios for API communication.
The backend uses CORS middleware to allow cross-origin requests from the frontend.
API Endpoints
Retrieve All Feedback Entries
URL: /feedback
Method: GET
Response: Returns an array of all feedback entries.
Submit New Feedback
URL: /feedback
Method: POST
Body: { name: string, feedback: string }
Response: Adds a new feedback entry and returns the updated list of feedback.
Example Usage
Submitting Feedback
Send a POST request to http://localhost:3000/feedback with the following body:

{
    "name": "Abhishek",
    "feedback": "Great !"
}
