# Vue Node SQLite Starter

A modern full-stack todo application built with Vue 3, Node.js, TypeScript, and SQLite. This project serves as a starter template for building full-stack web applications with a clean separation of concerns and modern development practices.

## 🚀 Features Out of the Box

- **Frontend**: Vue 3 with Composition API and TypeScript
- **Backend**: Node.js with Express and TypeScript
- **Database**: SQLite with better-sqlite3
- **Styling**: Tailwind CSS for responsive design
- **State Management**: Pinia for frontend state
- **HTTP Client**: Axios for API communication
- **Build Tools**: Vite (frontend) and esbuild (backend)
- **Monorepo**: Managed with npm workspaces
- **Type Safety**: TypeScript support across all layers with a `/shared/` folder

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 or higher)
- npm (v7 or higher for workspaces support)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/ProjectDepot/vue-node-sqlite-starter
   cd vue-node-starter
   ```

2. **Install dependencies**

   ```bash
   npm run install:all
   ```

3. **Start development servers**

   ```bash
   npm run dev
   ```

   This will start both the client and server in development mode:

   - Frontend: <http://localhost:3000>
   - Backend: <http://localhost:4000>
   - API: <http://localhost:4000/api/todos>

### 📚 Documentation

A documentation site is available, built with [Vitepress](https://vitepress.dev/).

- **Local Development**: `npm run docs:dev` (opens at <http://localhost:5174>)
- **Production Build**: `npm run docs:build`

## 📁 Project Structure

```text
vue-node-sqlite-starter/
├── client/                   # Vue 3 frontend
│   ├── src/
│   │   ├── components/
│   │   ├── App.vue
│   │   └── main.ts           # Frontend entry point
│   ├── package.json
│   └── vite.config.ts
├── server/                   # Node.js backend
│   ├── src/
│   │   ├── routes/           # API routes
│   │   ├── database.ts       # SQLite setup
│   │   └── index.ts          # Server entry point
│   └── package.json
├── shared/                   # Shared code and types
│   ├── src/
│   │   ├── types.ts          # Shared types
│   │   └── index.ts          # Shared code & exported types
│   └── package.json
├── docs/                     # Documentation site (VitePress)
│   ├── .vitepress/config.mts # VitePress configuration
│   ├── index.md              # Documentation homepage
├── package.json              # Root workspace configuration
└── README.md
```

### Available Scripts

#### Root Level

- **`npm run dev`** - Start both client and server in development mode
- `npm run dev:client` - Start only the client development server
- `npm run dev:server` - Start only the server in development mode
- **`npm run build`** - Build all workspaces for production
- `npm run build:client` - Build only the client
- `npm run build:server` - Build only the server
- `npm run build:shared` - Build only the shared package
- `npm run install:all` - Install dependencies for all workspaces
- `npm run clean` - Clean build artifacts
- **`npm start`** - Start the production server

#### Documentation

- `npm run docs:dev` - Start VitePress development server
- `npm run docs:build` - Build documentation for production
- `npm run docs:preview` - Preview production build locally

## 🔧 Configuration

### Environment Variables

Create a `.env` file in the root directory for environment-specific configuration:

```env
# Server Configuration
PORT=4000
NODE_ENV=development

# Database Configuration
DATABASE_URL=todos.db

# CORS Configuration
CLIENT_URL=http://localhost:3000
```

## 🚀 Production Deployment

1. **Build the application**

   ```bash
   npm run build
   ```

2. **Start the server**

   ```bash
   npm start
   ```

All 3 parts (client, server, shared) are built to and served from `/dist/`.

<!-- ## 🧪 Testing

### Frontend Testing

```bash
cd client
npm run test
```

### Backend Testing

```bash
cd server
npm run test
``` -->

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
