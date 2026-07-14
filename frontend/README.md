# Gaianexus Frontend

Modern React + TypeScript frontend for the Gaianexus collaborative platform.

## 🚀 Quick Start

### Prerequisites
- Node.js >= 20.0.0
- npm >= 10.0.0

### Installation
```bash
cd frontend
npm install
```

### Development
```bash
npm run dev
```

The app will be available at `http://localhost:5173`

### Build
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## 📁 Project Structure

```
src/
├── components/        # Reusable React components
├── pages/            # Page components
├── services/         # API services and utilities
├── store/            # Zustand state management
├── types/            # TypeScript type definitions
├── utils/            # Helper functions
├── App.tsx           # Root component
├── main.tsx          # Entry point
└── index.css         # Global styles
```

## 🛠️ Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build
- `npm run lint` - Run ESLint
- `npm run type-check` - Check TypeScript types
- `npm test` - Run tests
- `npm run test:ui` - Run tests with UI

## 🎨 Technologies

- **React 18** - UI library
- **TypeScript** - Type safety
- **Vite** - Build tool
- **React Router** - Client-side routing
- **Axios** - HTTP client
- **Zustand** - State management
- **Tailwind CSS** - Utility-first CSS
- **Vitest** - Testing framework

## 🔧 Configuration

### Environment Variables
Create `.env` file from `.env.example`:
```bash
cp .env.example .env
```

Key variables:
- `VITE_API_BASE_URL` - Backend API URL
- `VITE_APP_NAME` - Application name
- `VITE_ENABLE_DEBUG` - Debug mode

## 📚 Documentation

- [Development Setup Guide](../docs/SETUP.md)
- [Architecture](./ARCHITECTURE.md) (coming soon)
- [Contributing Guidelines](../CONTRIBUTING.md)

## 🤝 Contributing

We welcome contributions! Please check our [Contributing Guide](../CONTRIBUTING.md).

Before committing:
1. Run `npm run lint` to check code style
2. Run `npm run type-check` to check TypeScript
3. Run tests: `npm test`

## 📄 License

See [LICENSE](../LICENSE) file for details.
