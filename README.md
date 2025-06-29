# 💼 Financial Analytics Dashboard

A professional full-stack web application for financial analysts to visualize, filter, and export transaction data — built with Dockerized backend and an elegant, responsive UI.

---

## 🌐 Deployed Links

- **Frontend**: [https://financial-dashboard-frontend-mocha.vercel.app](https://financial-dashboard-frontend-mocha.vercel.app)
- **Backend**: [https://financial-dashboard-z0nq.onrender.com](https://financial-dashboard-z0nq.onrender.com)

---

## 🎥 Demo Video

[📽️ Watch the Demo](#) <!-- Replace with actual video link when available -->

---

## ✨ Features

### ✅ Authentication
- JWT-based login/signup system
- Secure protected API endpoints

### 📊 Dashboard
- Revenue vs Expense charts using **Recharts**
- Pie charts in analytics
- Separate pages for:
  - Analytics Overview
  - Profile
  - Wallet Overview
  - All Transactions
  - Settings
- SPA functionality with smooth navigation
- Summary metrics include:
  - Total Revenue
  - Expenses
  - Net Balance
  - Investment
  - Average Spending
  - Top Expense Months
- Fully responsive dashboard

### 📁 Transactions Table
- Paginated, searchable, and responsive
- **Multi-field Filtering**: Date, Category, Amount, Status
- **Live Search**: Implemented with **Rebounce**
- **Sorting**: Clickable column headers with indicators

### 📄 CSV Export System
- Modal to configure desired columns
- CSV auto-download via browser
- Clean, properly formatted export

### 🚨 Error Handling
- Alert chips for real-time feedback on errors (API, export, validation)

---

## 🧩 Frontend Tech Stack

- **Framework**: React.js (v19) + TypeScript
- **Build Tool**: Vite (fast dev & optimized build)
- **UI Libraries**:
  - Material UI (`@mui/material`)
  - Ant Design (`antd`)
  - Emotion (`@emotion/react`, `@emotion/styled`)
- **Routing**: React Router DOM (v7)
- **Charts**: Recharts
- **HTTP Client**: Axios
- **Live Search**: Lodash Debounce
- **Date Handling**: Moment Timezone
- **Toasts/Alerts**: React Toastify
- **Icons**: MUI Icons + Ant Design Icons
- **Linting & Quality**:
  - ESLint, `@typescript-eslint`, `eslint-plugin-react-hooks`

---

## 🔧 Backend Tech Stack

- **Language**: TypeScript (Node.js runtime)
- **Framework**: Express.js (v5)
- **Database**: MongoDB (via Mongoose)
- **Authentication**: JWT + Bcrypt.js for secure login
- **CSV Export**: csv-writer
- **Env Handling**: dotenv
- **Dev Tools**: ts-node-dev for hot reloading
- **Containerized with Docker**:
  - Base image: `node:18`
  - Builds TypeScript → JS (`npm run build`)
  - Exposes port `5000`

---

## 📡 API Endpoints

> Base URL: `https://financial-dashboard-z0nq.onrender.com/api`

| Method | Endpoint                         | Description               |
|--------|----------------------------------|---------------------------|
| POST   | `/auth/signup`                   | Register a new user       |
| POST   | `/auth/login`                    | Authenticate and receive JWT |
| GET    | `/transactions/`                 | Get all transactions      |
| GET    | `/transactions/summary`         | Get financial summary data |

All protected routes require the following header:

Authorization: Bearer <your_jwt_token>

yaml
Copy
Edit

---

## 🐳 Docker Setup (Backend Only)

### 🧱 Prerequisites
- Docker installed on your machine: [Install Docker](https://docs.docker.com/get-docker/)
- A `.env` file with:
PORT=5000
MONGO_URI=<your_mongo_connection_string>
JWT_SECRET=<your_jwt_secret>

bash
Copy
Edit

🛠 Setup Instructions
1. Clone the repository and navigate to backend:

bash
Copy
Edit
git clone https://github.com/your-username/financial-dashboard.git
cd financial-dashboard/server
2. Build the Docker image:

bash
Copy
Edit
docker build -t financial-backend .
3. Run the container:

bash
Copy
Edit
docker run -p 5000:5000 --env-file .env financial-backend
Your backend will now be accessible at:
http://localhost:5000

💻 Local Setup Instructions
🧱 Prerequisites
Ensure the following are installed on your system:

Node.js (v18+ recommended)

npm

MongoDB (local or MongoDB Atlas)

Docker (only if you're using the containerized backend)

Git

🚀 Frontend Setup
1. Navigate to the frontend directory:

bash
Copy
Edit
cd financial-dashboard/client
2. Install dependencies:

bash
Copy
Edit
npm install
3. Start the development server:

bash
Copy
Edit
npm run dev
Frontend will run at:
http://localhost:5173

⚙️ Backend (Without Docker)
1. Navigate to backend folder:

bash
Copy
Edit
cd financial-dashboard/server
2. Install dependencies:

bash
Copy
Edit
npm install
3. Start the server in development mode:

bash
Copy
Edit
npm run dev
Backend will run at:
http://localhost:5000

📫 Postman Collection
Test all API endpoints using this Postman collection:
👉 Postman Collection Link <!-- Replace with actual public collection link -->

🧪 Sample Data
To populate your MongoDB instance with sample data:

1. Use the provided sample-data.json file

2. Run this import command:

bash
Copy
Edit
mongoimport --uri "your-mongodb-uri" --collection transactions --file sample-data.json --jsonArray
