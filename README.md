# 💼 Financial Analytics Dashboard

A professional full-stack web application for financial analysts to visualize, filter, and export transaction data — built with Dockerized backend and an elegant, responsive UI.

## 🌐 Live Demo

- **Frontend**: [your-frontend-url.com](https://your-frontend-url.com)
- **Backend API**: [your-backend-url.com](https://your-backend-url.com)

---

## ✨ Features

### ✅ Authentication
- JWT-based login/logout system
- Secure protected API endpoints

### 📊 Dashboard
- Revenue vs Expense charts using **Recharts**
- Pie/Donut category breakdown
- Summary metrics: Total Revenue, Expenses, Net

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

## 🛠 Tech Stack

### Frontend
- **React.js + TypeScript**
- **Material UI**, **Ant Design**
- **Recharts** for charts
- **Rebounce** for live search
- **Axios**, **React Router**

### Backend
- **Node.js + Express + TypeScript**
- **MongoDB + Mongoose**
- **JWT** Auth
- **CSV Generator** using `json2csv`
- **Dockerized** backend for containerized deployment

---

## 🐳 Docker Setup (Backend)

### Build & Run

```bash
docker build -t financial-backend .
docker run -p 5000:5000 --env-file .env financial-backend
