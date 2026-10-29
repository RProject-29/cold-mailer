# Cold Mailer Backend API

An automated cold mailing backend service powered by Express.js, MongoDB, Nodemailer, Cloudinary, and OpenRouter AI.

---

## 🚀 Features

- **Authentication**: JWT-based user authentication and authorization.
- **File Uploads**: Cloudinary integration for handling file attachments/resumes.
- **AI Integration**: OpenRouter AI support for extracting details and crafting personalized cold emails.
- **Email Dispatching**: Automated SMTP mailing with Nodemailer.
- **Vercel Ready**: Configured with `vercel.json` for seamless deployment.

---

## 🛠️ Tech Stack

- **Runtime**: Node.js (ES Modules)
- **Framework**: Express.js
- **Database**: MongoDB (Mongoose)
- **File Storage**: Cloudinary
- **AI Model API**: OpenRouter
- **Email Service**: Nodemailer (SMTP)

---

## 📦 Getting Started

### 1. Prerequisites
- Node.js (v18 or higher recommended)
- MongoDB instance (MongoDB Atlas)
- Gmail SMTP app password or custom SMTP server
- Cloudinary account

### 2. Installation

Clone the repository:
```bash
git clone <repository_url>
cd cold-mailer
```

Install dependencies:
```bash
npm install
```

### 3. Environment Variables Setup

Create a `.env` file in the root directory by copying the `.env.example`:
```bash
cp .env.example .env
```

Configure your credentials in `.env`:
```env
MONGODB_URL=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
CLOUD_NAME=your_cloudinary_cloud_name
CLOUD_API_KEY=your_cloudinary_api_key
CLOUD_API_SECRET=your_cloudinary_api_secret
OPENROUTER_API_KEY=your_openrouter_api_key
SMTP_PASS=your_gmail_app_password
SMTP_USER=your_email@gmail.com
SMTP_PORT=587
SMTP_HOST=smtp.gmail.com
```

### 4. Running the Application

Development mode (with nodemon):
```bash
npm run dev
```

Production mode:
```bash
node index.js
```

The server runs by default on `http://localhost:5000`.

---

## 🛣️ API Endpoints

- **Auth**: `/api/auth`
- **Files**: `/api/files`
- **Mails**: `/api/mails`
