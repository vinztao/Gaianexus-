# Gaianexus Development Setup Guide

## 📋 Prerequisites

- **Node.js** >= 20.0.0
- **npm** >= 10.0.0
- **Docker** and **Docker Compose** (optional, for containerized development)
- **PostgreSQL** >= 16 (if not using Docker)

## 🚀 Quick Start with Docker (Recommended)

### 1. Clone the repository
```bash
git clone https://github.com/vinztao/Gaianexus-.git
cd Gaianexus-
```

### 2. Set up environment variables
```bash
cp backend/.env.example backend/.env
cp frontend/.env.example frontend/.env
```

### 3. Start the services
```bash
docker-compose up
```

The services will be available at:
- **Backend API**: http://localhost:3000
- **Frontend**: http://localhost:5173
- **Database**: localhost:5432

## 🛠️ Local Development (Without Docker)

### Backend Setup

#### 1. Install dependencies
```bash
cd backend
npm install
```

#### 2. Configure environment
```bash
cp .env.example .env
# Edit .env with your database credentials
```

#### 3. Set up PostgreSQL
```bash
# Create database
createdb gaianexus

# Or using psql:
psql -U postgres
CREATE DATABASE gaianexus;
```

#### 4. Start the development server
```bash
npm run dev
```

Backend will run at: http://localhost:3000

### Frontend Setup

#### 1. Install dependencies
```bash
cd frontend
npm install
```

#### 2. Start the development server
```bash
npm run dev
```

Frontend will run at: http://localhost:5173

## 📦 Available Scripts

### Backend
```bash
npm run dev          # Start development server with hot reload
npm run build        # Build TypeScript to JavaScript
npm start            # Run production build
npm run lint         # Run ESLint
npm run type-check   # Check TypeScript types
npm test             # Run tests
```

### Frontend
```bash
npm run dev          # Start Vite development server
npm run build        # Build for production
npm run preview      # Preview production build locally
npm run lint         # Run ESLint
npm run type-check   # Check TypeScript types
npm test             # Run tests
npm run test:ui      # Run tests with UI
```

## 🗄️ Database

### Connection String
```
postgresql://user:password@localhost:5432/gaianexus
```

## 🔗 API Endpoints

### Health Check
- `GET /health` - Server health status
- `GET /api/v1/status` - API status information

### Authentication (Coming Soon)
- `POST /api/v1/auth/register` - Register new user
- `POST /api/v1/auth/login` - Login user
- `POST /api/v1/auth/logout` - Logout user
- `GET /api/v1/auth/me` - Get current user

## 📝 Project Structure

```
Gaianexus-/
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── store/
│   │   ├── types/
│   │   ├── utils/
│   │   ├── App.tsx
│   │   └── main.tsx
│   ├── package.json
│   └── vite.config.ts
├── backend/
│   ├── src/
│   │   ├── controllers/
│   │   ├── services/
│   │   ├── middlewares/
│   │   ├── routes/
│   │   ├── types/
│   │   ├── utils/
│   │   ├── db/
│   │   ├── config/
│   │   └── index.ts
│   ├── package.json
│   └── tsconfig.json
├── docs/
├── .github/workflows/
└── README.md
```

## 🤝 Contributing

Before committing:
1. Run `npm run lint` to check code style
2. Run `npm run type-check` to check TypeScript
3. Run tests: `npm test`

## ❓ Need Help?

Check our [Contributing Guide](../CONTRIBUTING.md) or open an issue on GitHub.
