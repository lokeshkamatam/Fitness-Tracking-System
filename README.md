Problem Statement:

In today’s fast-paced world, many individuals struggle to achieve their fitness goals due to a lack of personalized guidance, structured workout plans, and expert coaching. Traditional fitness programs often fail to cater to individual needs, leading to low motivation, inconsistent progress, and ineffective training. Additionally, access to professional trainers and accurate fitness tracking is often expensive or inconvenient.

Demo Video:

URL: https://drive.google.com/file/d/1AKtk8advqxXRa0m8e87E5ES__BhetYBk/view?usp=sharing

Solution and complete instructions:

Overview

The Fitness Tracking System is a web-based application that helps users monitor their fitness journey, track workouts, get diet recommendations, and engage in 30-day challenges. The system also incorporates AI-based pose estimation to assist users in evaluating their exercise form using live camera feed.

Features

User Registration: Users can register by entering weight, height, and a unique ID.

BMI Calculation & Diet Recommendations: Provides personalized diet advice based on BMI.

Water Intake Suggestion: Calculates daily recommended water intake.

Exercise Tracking: Users can log gym and yoga workouts.

30-Day Challenges: Includes structured gym and yoga workout challenges.

Live Pose Estimation: AI-powered real-time posture evaluation using a webcam.

Daily Exercise Summary: Displays total workout time per day.

Technologies Used

Backend: Flask (Python)

Database: SQLite

Frontend: HTML, CSS, JavaScript

AI Model: PoseNet (for real-time pose estimation)

Installation & Setup

Prerequisites

Ensure you have the following installed on your system:

Python 3.x

Flask

Flask-SQLAlchemy

TensorFlow.js (for PoseNet)

A working webcam (for AI pose estimation)

AI-Based Pose Estimation:

The AI model used in this project is PoseNet, which detects human body keypoints and evaluates posture. It is integrated using TensorFlow.js to:

Identify key body joints

Analyze user posture

Provide feedback on exercise form

How Pose Estimation Works

The webcam captures a live video feed.

PoseNet processes the video and extracts keypoints (head, shoulders, arms, legs, etc.).

A function evaluates the detected pose and provides corrective feedback based on confidence scores.

Live Camera Access

The system utilizes getUserMedia API in JavaScript to access the user's webcam:

navigator.mediaDevices.getUserMedia({ video: true }) .then(stream => { video.srcObject = stream; }) .catch(error => { console.error("Error accessing camera: ", error); });

Deployment

You can deploy the app on platforms like Heroku or Render:

Deploy on Heroku

Install Heroku CLI:

npm install -g heroku

Login to Heroku:

heroku login

Create a Heroku app:

heroku create fitness-tracker-app

Push the project to Heroku:

git push heroku main

Open the deployed app:

heroku open

Backend Libraries (Python): Flask

Purpose: Web framework for handling HTTP requests, routing, and rendering templates.

License: BSD

Flask-SQLAlchemy

Purpose: ORM (Object Relational Mapper) for managing the SQLite database.

License: MIT

SQLite

Purpose: Lightweight, file-based database for storing user data and exercise logs.

License: Public Domain

Datetime (Python Standard Library)

Purpose: Handling date and time-related operations.

Frontend Libraries (JavaScript & HTML): PoseNet (TensorFlow.js)

Purpose: Real-time pose estimation to analyze workout forms via webcam.

License: Apache 2.0

TensorFlow.js (implied through PoseNet)

Purpose: Machine learning framework in JavaScript for real-time inference.

License: Apache 2.0

Bootstrap (if used in HTML templates)

Purpose: Responsive front-end framework for UI styling.

License: MIT

jQuery (if used for DOM manipulation)

Purpose: Simplifies JavaScript coding for frontend interactions.

License: MIT

APIs & External Integrations: Google PoseNet API (via TensorFlow.js)

Purpose: Real-time body pose detection.

License: Open-source under Apache 2.0

Google Fit API (if integrated in the future)

Purpose: Syncs fitness data from Android devices (optional).

Apple HealthKit API (if integrated in the future)

Purpose: Fetches health-related data from iOS devices (optional).

Database & Storage: SQLite (as mentioned above)

Purpose: Stores user profiles, exercise logs, and daily activity data.

SQLAlchemy ORM

Purpose: Simplifies database operations in Python.

Security & Authentication: JWT (JSON Web Tokens) (if implemented in future)

Purpose: Secure token-based authentication.

License: MIT

OAuth 2.0 (if integrated in future)

Purpose: Authorization framework for third-party access.

Deployment & DevOps Tools Docker (if used)

Purpose: Containerization for easy deployment.

License: Apache 2.0

GitHub Actions / Jenkins (if CI/CD is implemented)

Purpose: Continuous Integration/Continuous Deployment.

Licenses Summary: BSD: Flask

MIT: SQLAlchemy, Bootstrap, jQuery

Apache 2.0: TensorFlow.js, PoseNet

Public Domain: SQLite

Future Enhancements:

Integration with Wearable Devices (Fitbit, Apple Watch, etc.)

AI-driven Personalized Workout Plans

Mobile App for Android & iOS

Advanced pose correction system with feedback animation

Contact

For any queries, contact: 8309589909

Email: lokeshlokee52@gmail.com

GitHub: lokeshkamatam
