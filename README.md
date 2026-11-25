# Food Rescue Platform
### Connecting Surplus Food with Communities in Need

Food Rescue is a full-stack web application designed to minimize food wastage by connecting food donors, NGOs, and volunteers through a centralized food redistribution platform.

The platform enables individuals, restaurants, and event organizers to list surplus food, allowing verified NGOs to discover nearby donations, coordinate collection, and arrange distribution with the help of volunteers.

By digitizing the food donation lifecycle, Food Rescue aims to improve resource utilization, streamline coordination, and promote transparency in food redistribution.

---

## Key Features

- **Role-Based Authentication:** Dedicated access and dashboards for Admins, Food Donors, NGOs, and Volunteers.
- **Food Donation Management:** Create and manage food listings with quantity, descriptions, expiry details, and location information.
- **Location-Based Matching:** Helps NGOs discover nearby available food donations within a configurable radius.
- **Donation Management:** Enables NGOs to review, accept, and coordinate donation pickups.
- **Volunteer Coordination:** Supports volunteer assignments and pickup and delivery management.
- **Real-Time Notifications:** Socket.io-powered notifications for important donation and delivery updates.
- **Pickup Verification:** OTP-based pickup confirmation with photo verification support.
- **Live Donation Tracking:** Interactive maps using React Leaflet and OpenStreetMap.
- **Admin Dashboard:** User management, NGO verification, and donation monitoring.
- **Impact Dashboard:** Visualizes food-saving statistics and donation-related insights.
- **Feedback and Ratings:** Allows participants to share feedback after completed deliveries.

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Vite |
| Styling | Tailwind CSS |
| Backend | Node.js, Express.js |
| Database | MongoDB, Mongoose |
| Authentication | JWT |
| Real-Time Communication | Socket.io |
| Maps & Geolocation | React Leaflet, OpenStreetMap |
| Data Visualization | Recharts |
| File Uploads | Multer |
| API Integration | Axios |
| Client-Side Routing | React Router |

## System Architecture

The application follows a modular frontend-backend architecture with MongoDB as its primary database.

**Frontend**
- Role-specific user interfaces and dashboards.
- Donation listing and management interfaces.
- API integration and application navigation.
- Interactive maps and data visualizations.

**Backend**
- RESTful API development and request handling.
- Authentication and role-based authorization.
- User, donation, and volunteer management.
- Geospatial donation matching.
- Notification and tracking services.

**Database**
- MongoDB for persistent storage of user profiles, donation records, and notification data.
- Mongoose for schema definition and database operations.

## Project Structure

```text
food-rescue/
│
├── backend/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── uploads/
│   ├── server.js
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── api/
│   │   ├── components/
│   │   ├── context/
│   │   ├── pages/
│   │   └── ...
│   └── package.json
│
├── .gitignore
└── README.md
```

## Installation and Setup

### 1. Prerequisites

Ensure the following tools are installed:

- Node.js (v18 or later)
- npm
- MongoDB Community Server or MongoDB Atlas

### 2. Backend Configuration

```bash
cd backend
npm install
```

Create an environment configuration file:

**Windows PowerShell:**
```powershell
Copy-Item .env.example .env
```

Configure the required environment variables:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

Use the actual variable names defined in `.env.example`.

### 3. Initialize Demo Data

```bash
npm run seed
```

This initializes development demo accounts for the supported user roles.

### 4. Start the Backend

```bash
npm run dev
```

Backend URL: `http://localhost:5000`

Health Check: `http://localhost:5000/api/health`

### 5. Start the Frontend

Open a separate terminal:

```bash
cd frontend
npm install
npm run dev
```

Frontend URL: `http://localhost:5173`

Open the frontend URL in your browser to access the application.

## Demo Accounts

The project provides the following development credentials:

| Role | Email | Password |
|---|---|---|
| Admin | admin@foodrescue.com | admin123 |
| Donor | host@foodrescue.com | host123 |
| NGO | ngo@foodrescue.com | ngo123 |
| Volunteer | volunteer@foodrescue.com | volunteer123 |

**Note:** These credentials are intended for local development and demonstration only. Do not use them in a production environment.

## Application Workflow

1. **Donor(Host) Registration:** Users register and provide the required profile information.
2. **Food Listing:** Donors publish surplus food details, including quantity, expiry, and location.
3. **NGO Discovery:** Verified NGOs explore available donations based on their location.
4. **Donation Acceptance:** NGOs accept suitable donations and coordinate collection.
5. **Volunteer Assignment:** Volunteers are assigned to handle pickup and delivery activities.
6. **Pickup Verification:** OTP-based verification helps confirm successful food collection.
7. **Delivery Completion:** Donation status is updated upon completion of the delivery process.
8. **Impact Monitoring:** The platform provides donation statistics and food-saving insights.

## Future Enhancements

- Responsive and mobile-first user experience.
- Cloud-based image storage integration.
- Advanced analytics and donation reporting.
- Production deployment with enhanced security and scalability.

## Project Objective

The objective of Food Rescue is to establish an efficient digital ecosystem for food redistribution by reducing coordination gaps between donors, NGOs, and volunteers.

Through location-based discovery, structured donation management, and transparent delivery tracking, the platform aims to make surplus food redistribution more accessible, organized, and impactful.
