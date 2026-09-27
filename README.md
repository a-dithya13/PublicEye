# PublicEye

> A full-stack civic issue reporting and management platform for reporting, tracking, assigning, and resolving public infrastructure issues.

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/Node.js-Backend-339933?logo=node.js&logoColor=white" alt="Node.js">
  <img src="https://img.shields.io/badge/Express.js-API-000000?logo=express&logoColor=white" alt="Express">
  <img src="https://img.shields.io/badge/MongoDB-Database-47A248?logo=mongodb&logoColor=white" alt="MongoDB">
  <img src="https://img.shields.io/badge/Mongoose-ODM-880000?logo=mongoose&logoColor=white" alt="Mongoose">
  <img src="https://img.shields.io/badge/JWT-Authentication-000000?logo=jsonwebtokens" alt="JWT">
  <img src="https://img.shields.io/badge/Leaflet-Maps-199900?logo=leaflet&logoColor=white" alt="Leaflet">
  <img src="https://img.shields.io/badge/Recharts-Analytics-8884D8" alt="Recharts">
</p>

<p align="center">
  <strong>Report. Track. Resolve.</strong>
</p>

<p align="center">
  A role-based civic issue management system connecting citizens, officers, and administrators through a unified workflow.
</p>
<p align="center">
  
<img src="https://github.com/user-attachments/assets/9c413178-7c79-4c1f-b4eb-cf2cf03494a1"
 alt="PublicEye Dashboard" width="900">
</p>

---

## Overview

PublicEye is a full-stack civic issue reporting and management platform designed to make public infrastructure complaints easier to submit, track, assign, and resolve.

The platform provides separate experiences for **Citizens, Officers, and Administrators**, allowing each role to interact with issues according to their responsibilities.

```text
Citizen
   │
   ├── Report Issue
   ├── Upload Evidence
   ├── Select Location
   └── Track Status
   │
   ▼
Issue Management
   │
   ├── Review
   ├── Assignment
   └── Status Tracking
   │
   ▼
Officer
   │
   ├── Investigate
   ├── Update Progress
   └── Submit Report
   │
   ▼
Administrator
   │
   ├── Monitor
   ├── Assign / Reassign
   ├── Manage Users
   └── Analyse
```

---

## Product Showcase

### Citizen Dashboard

ADD CITIZEN DASHBOARD SCREENSHOT

<p align="center">
  <img width="1917" height="1078" alt="image" src="https://github.com/user-attachments/assets/95134aab-7dcc-4fdf-bd87-d05acb57efbb" 
 alt="PublicEye Citizen Dashboard" width="850">
</p>


### Issue Reporting
<p align="center">
  <img src="[docs/screenshots/report-issue.png](https://static.toiimg.com/thumb/msid-124793154,imgsize-87864,width-400,height-225,resizemode-72/sinkhole-reappears-motorists-suffer-on-perambur-road.jpg)" alt="PublicEye Issue Reporting" width="850">
</p>

### Interactive Map


<p align="center">
  <img  src="https://github.com/user-attachments/assets/677b18c7-415d-4d12-985a-f98fda0cc8ec" 
 alt="PublicEye Interactive Issue Map" width="850">
</p>

### Officer Dashboard


<p align="center">
  <img   src="https://github.com/user-attachments/assets/7b570f27-cf9a-4782-8189-cba4a387ece4" 
 alt="PublicEye Officer Dashboard" width="850">
</p>
-->

### Admin Dashboard



<p align="center">
  <img  src="https://github.com/user-attachments/assets/7ccaa0ee-a5ed-4a01-bf7e-864466deb3b5" 
 alt="PublicEye Admin Dashboard" width="850">
</p>


---

## Core Features

### Citizen

* Secure authentication
* Report civic infrastructure issues
* Upload supporting images
* Select issue locations using an interactive map
* Automatic reverse geocoding
* Public voting on reported issues
* Track issue status
* View submitted reports

### Officer

* View assigned issues
* Review issue descriptions and evidence
* Update issue progress
* Manage issue status
* Submit issue reports
* Access officer-level analytics

### Administrator

* Centralized issue management
* Assign and reassign officers
* Manage users
* Review officer reports
* Monitor issue activity
* View platform analytics

---

## Issue Lifecycle

PublicEye follows a structured issue-resolution workflow:

```text
                 ┌───────────┐
                 │  Pending  │
                 └─────┬─────┘
                       │
                       ▼
                 ┌───────────┐
                 │  Assigned │
                 └─────┬─────┘
                       │
                       ▼
                 ┌─────────────┐
                 │ In Progress │
                 └──────┬──────┘
                        │
                        ▼
                  ┌──────────┐
                  │ Resolved │
                  └──────────┘

                       or

                  ┌──────────┐
                  │ Rejected │
                  └──────────┘
```

This provides a consistent state model across citizens, officers, and administrators.

---

## Location-Based Reporting

PublicEye integrates **Leaflet** and **OpenStreetMap** to support location-aware civic reporting.

Users can:

1. Select an issue location on an interactive map.
2. Capture the geographic coordinates.
3. Convert coordinates into a readable address through reverse geocoding.
4. Associate the location with the submitted issue.

This gives officers more precise information when investigating and resolving reports.

---

## Analytics

The platform uses **Recharts** to provide dashboard-level analytics.

Analytics can be used to understand:

* Issue distribution
* Issue status
* Officer workload
* Resolution activity
* Platform activity



<p align="center">
  <img width="1917"  src="https://github.com/user-attachments/assets/100c73fb-fefc-4644-a4fd-38420b67dd3c" 
alt="PublicEye Analytics" width="850">
</p>


---

## Technology Stack

| Layer             | Technology    |
| ----------------- | ------------- |
| Frontend          | React.js      |
| Routing           | React Router  |
| HTTP Client       | Axios         |
| Maps              | Leaflet       |
| Map Data          | OpenStreetMap |
| Charts            | Recharts      |
| Backend           | Node.js       |
| API               | Express.js    |
| Authentication    | JWT           |
| Password Security | bcrypt        |
| Database          | MongoDB       |
| ODM               | Mongoose      |

---

## Architecture

```text
                         ┌─────────────────────┐
                         │      React.js       │
                         │      Frontend       │
                         └──────────┬──────────┘
                                    │
                                  Axios
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │    Express API      │
                         │      Node.js        │
                         └──────────┬──────────┘
                                    │
                     ┌──────────────┼──────────────┐
                     │              │              │
                     ▼              ▼              ▼
               Controllers      Middleware       Routes
                                    │
                                JWT Auth
                                    │
                                    ▼
                             ┌────────────┐
                             │  Mongoose  │
                             └─────┬──────┘
                                   │
                                   ▼
                             ┌────────────┐
                             │  MongoDB   │
                             └────────────┘

External Services
       │
       ├── OpenStreetMap
       └── Reverse Geocoding
```

---

## Repository Structure

```text
PublicEye/
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── issue-images/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── uploads/
│   ├── utils/
│   ├── app.js
│   └── package.json
│
├── frontend/
│   ├── public/
│   ├── src/
│   │   ├── assets/
│   │   ├── components/
│   │   ├── constants/
│   │   ├── context/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── styles/
│   │   ├── App.jsx
│   │   └── index.js
│   └── package.json
│
└── README.md
```

---

## My Contribution

I contributed to the full-stack implementation of PublicEye, with a focus on connecting the frontend experience, backend services, and civic issue workflows.

### Frontend Development

* Developed and integrated React-based interfaces.
* Worked with React Router for application navigation.
* Integrated REST APIs using Axios.
* Connected dashboard components with backend data.
* Worked with Recharts for analytics and data visualization.
* Integrated location-based functionality using Leaflet.

### Backend Development

* Worked with the Node.js and Express backend.
* Worked across controllers, routes, models, and middleware.
* Integrated JWT-based authentication.
* Worked with MongoDB and Mongoose for application data.
* Connected frontend workflows to backend services.

### Issue Management

* Worked on the citizen issue-reporting workflow.
* Connected issue submission with backend processing.
* Worked on officer assignment and issue-status flows.
* Integrated issue information across different user roles.
* Connected dashboards to the underlying issue-management system.

### Full-Stack Integration

A significant part of the work involved connecting the individual layers into one working application:

```text
React Interface
      │
      ▼
Axios Services
      │
      ▼
Express Routes
      │
      ▼
Controllers
      │
      ▼
Mongoose Models
      │
      ▼
MongoDB
```

---

## Installation

### Prerequisites

Make sure you have:

* Node.js
* npm
* MongoDB
* Git

### Clone the Repository

```bash
git clone https://github.com/a-dithya13/PublicEye.git
cd PublicEye
```

### Backend

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` directory:

```env
PORT=5000
MONGO_URI=your_mongodb_uri
JWT_SECRET=your_jwt_secret
GEOAPIFY_API_KEY=your_geoapify_key
```

Start the backend:

```bash
npm run dev
```

### Frontend

Open another terminal:

```bash
cd frontend
npm install
npm start
```

---

## Environment Variables

Environment files and credentials should not be committed to the repository.

Typical environment files include:

```text
.env
.env.local
.env.production
```

Keep the following values private:

* MongoDB connection strings
* JWT secrets
* Geocoding API keys
* Other application credentials

---

## Development Workflow

```text
              Citizen
                 │
                 ▼
          Create Issue
                 │
       ┌─────────┼─────────┐
       │         │         │
       ▼         ▼         ▼
   Location   Evidence   Details
       │         │         │
       └─────────┼─────────┘
                 ▼
          Issue Created
                 │
                 ▼
          Admin Review
                 │
                 ▼
        Officer Assignment
                 │
                 ▼
          Issue Resolution
                 │
                 ▼
          Citizen Tracking
```

---

## Project Status

PublicEye is a full-stack project exploring how modern web technologies can improve the reporting and management of civic infrastructure issues.

Potential areas for future development include:

* Real-time notifications
* Advanced issue prioritization
* Improved moderation
* Mobile support
* Expanded analytics
* More granular administrative controls

---

## License


