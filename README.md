# Elevatr

An AI-powered platform that helps students discover and track **scholarships, fellowships, internships, and grants** using intelligent matching and personalized recommendations.

**Live Demo:** d2kr25z71q8y4g.cloudfront.net

---

# Project Overview

Elevatr is designed to solve a major problem faced by students: discovering the **right opportunities at the right time**. Many scholarships, internships, and fellowships go unnoticed because students cannot efficiently search through thousands of listings.

Elevatr uses **AI-powered matching and conversational assistance** to analyze a student's profile and recommend the most relevant opportunities.

Students simply create a profile with their:

* Degree
* Field of study
* Skills
* Interests

The platform then automatically recommends opportunities with **match scoring and eligibility insights**.

---

# Key Features

### AI Opportunity Matching

Matches students with relevant internships, scholarships using **Amazon Bedrock AI models**.

### EL – AI Assistant

A conversational assistant that helps students:

* Discover opportunities
* Understand eligibility
* Get guidance on applications

### Deadline Tracker

Tracks application deadlines in:

* Calendar view
* List view

Helps students avoid missing important application dates.

### Live Opportunity Discovery

Students can explore opportunities beyond recommendations using search and filters.

### Profile Builder

Students create detailed profiles and receive AI-powered analysis for better matching.

### Password Reset System

Email-based password reset for secure account recovery.

---

# Tech Stack

## Frontend

* React
* React Router
* Create React App

## Backend

* Node.js
* Express.js

## AI

* Amazon Bedrock
* Amazon Nova

## Database

* Amazon DynamoDB

## Cloud Infrastructure

| Service           | Purpose                                |
| ----------------- | -------------------------------------- |
| Amazon EC2        | Runs the Express backend server        |
| Amazon S3         | Hosts the built React frontend         |
| Amazon CloudFront | Global CDN for frontend delivery       |
| Amazon Bedrock    | AI matching and opportunity generation |
| Amazon Nova       | Powers the EL conversational assistant |
| Amazon DynamoDB   | Stores user profiles and deadlines     |

---

# Project Structure

```
Elevatr/

frontend/
 └── src/
     └── components/
         ├── AIAssistant.js
         ├── Dashboard.js
         ├── Deadlines.js
         ├── LandingPage.js
         ├── Login.js
         ├── Navbar.js
         ├── OpportunityCard.js
         ├── ProfileBuilder.js
         └── Signup.js

backend/
 └── server.js
```

---

# Getting Started

## 1. Clone the Repository

```bash
git clone https://github.com/kshrax/Elevatr.git
cd Elevatr
```

---

## 2. Install Dependencies

```bash
cd frontend
npm install

cd ../backend
npm install
```

---

## 3. Configure Environment Variables

Create a `.env` file inside **backend/**

```env
PORT=5000
CLIENT_URL=http://localhost:3000
SERVER_URL=http://localhost:5000

AWS_REGION=us-east-1
AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret

```

Create a `.env` file inside **frontend/**

```env
REACT_APP_API_URL=http://localhost:5000
```

---

## 4. Run the Project Locally

### Start Backend

```bash
cd backend
node server.js
```

### Start Frontend

Open a new terminal:

```bash
cd frontend
npm start
```

Open in browser:

```
http://localhost:3000
```

---
# Deployment Architecture

Frontend:

React → Build → Amazon S3 → CloudFront CDN

Backend:

Node.js + Express → Amazon EC2

AI Layer:

Amazon Bedrock → Opportunity Matching + AI Assistant

Database:

Amazon DynamoDB → User Profiles + Deadlines

