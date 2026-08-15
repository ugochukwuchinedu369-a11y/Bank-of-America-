# AMERICAN PRIVATE BANK

## Online Banking Platform

A modern, secure, and user-friendly online banking application built with cutting-edge technologies.

### 🎯 Features

- **User Authentication & Account Management**
  - Secure login with JWT tokens
  - Two-factor authentication (2FA)
  - Account registration and profile management
  - Session management

- **Core Banking Operations**
  - View account balance and transaction history
  - Money transfers between accounts
  - External fund transfers
  - Bill payments
  - Recurring payments
  - Statement generation

- **Card Management**
  - Virtual and physical card management
  - Card activation/deactivation
  - Transaction limits configuration
  - Card statement access
  - Fraud alerts

- **Security**
  - End-to-end encryption
  - PCI DSS compliance
  - Fraud detection
  - Secure password management
  - Activity logging and monitoring
  - Multi-factor authentication

- **User Interface**
  - Responsive design (mobile, tablet, desktop)
  - Dark/light mode support
  - Real-time notifications
  - Intuitive dashboard
  - Accessibility compliance

### 🛠️ Tech Stack

**Frontend:**
- React 18+
- TypeScript
- Redux Toolkit (State Management)
- Tailwind CSS (Styling)
- Axios (HTTP Client)
- React Router (Navigation)
- Jest & React Testing Library

**Backend:**
- Node.js with Express.js
- TypeScript
- PostgreSQL (Primary Database)
- Redis (Caching & Sessions)
- JWT (Authentication)
- Nodemailer (Email Notifications)
- Joi (Validation)

**DevOps & Tools:**
- Docker & Docker Compose
- GitHub Actions (CI/CD)
- Jest (Testing)
- ESLint & Prettier (Code Quality)

### 📁 Project Structure

```
american-private-bank/
├── frontend/              # React frontend application
│   ├── src/
│   │   ├── components/    # Reusable UI components
│   │   ├── pages/         # Page components
│   │   ├── store/         # Redux store configuration
│   │   ├── services/      # API services
│   │   ├── utils/         # Utility functions
│   │   ├── styles/        # Global styles
│   │   ├── App.tsx        # Main app component
│   │   └── index.tsx      # Entry point
│   ├── public/
│   ├── package.json
│   ├── tsconfig.json
│   ├── Dockerfile
│   └── .env.example
│
├── backend/               # Express backend API
│   ├── src/
│   │   ├── controllers/   # Request handlers
│   │   ├── models/        # Database models
│   │   ├── routes/        # API routes
│   │   ├── middleware/    # Custom middleware
│   │   ├── services/      # Business logic
│   │   ├── utils/         # Utility functions
│   │   ├── config/        # Configuration
│   │   ├── types/         # TypeScript types
│   │   └── server.ts      # Server entry point
│   ├── tests/
│   ├── package.json
│   ├── tsconfig.json
│   ├── Dockerfile
│   └── .env.example
│
├── database/              # Database scripts
│   ├── init.sql           # Schema initialization
│   ├── migrations/        # Database migrations
│   └── seeds/             # Initial data
│
├── docker-compose.yml     # Docker services orchestration
├── .github/
│   └── workflows/
│       ├── ci-cd.yml      # CI/CD pipeline
│       └── security.yml   # Security checks
├── .gitignore
├── .env.example
└── README.md
```

### 🚀 Getting Started

#### Prerequisites
- Node.js 18+
- Docker & Docker Compose (optional but recommended)
- PostgreSQL 14+ (if not using Docker)
- Redis 7+ (if not using Docker)

#### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/ugochukwuchinedu369-a11y/Bank-of-America-.git
   cd Bank-of-America-
   ```

2. **Setup Environment Variables**
   ```bash
   cp .env.example .env
   # Edit .env with your configuration
   ```

3. **Option A: Using Docker Compose (Recommended)**
   ```bash
   docker-compose up -d
   ```

4. **Option B: Manual Setup**
   ```bash
   # Install frontend dependencies
   cd frontend
   npm install
   npm start
   
   # In another terminal, install backend dependencies
   cd backend
   npm install
   npm run dev
   ```

5. **Database Setup**
   ```bash
   # Run migrations
   npm run migrate
   
   # Seed initial data
   npm run seed
   ```

6. **Access the Application**
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5000
   - API Docs: http://localhost:5000/api/docs

### 📚 API Documentation

API documentation is available at `http://localhost:5000/api/docs` (Swagger/OpenAPI)

#### Key Endpoints

**Authentication:**
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - User login
- `POST /api/auth/refresh` - Refresh token
- `POST /api/auth/logout` - User logout
- `POST /api/auth/2fa/enable` - Enable 2FA
- `POST /api/auth/2fa/verify` - Verify 2FA

**Accounts:**
- `GET /api/accounts` - Get all accounts
- `GET /api/accounts/:id` - Get account details
- `POST /api/accounts` - Create new account
- `GET /api/accounts/:id/transactions` - Get transactions

**Transactions:**
- `POST /api/transactions/transfer` - Transfer funds
- `POST /api/transactions/bill-pay` - Pay bills
- `GET /api/transactions` - Get transaction history
- `GET /api/transactions/:id` - Get transaction details

**Cards:**
- `GET /api/cards` - Get all cards
- `POST /api/cards` - Create new card
- `PATCH /api/cards/:id` - Update card
- `DELETE /api/cards/:id` - Deactivate card

**Users:**
- `GET /api/users/profile` - Get user profile
- `PATCH /api/users/profile` - Update profile
- `POST /api/users/password/change` - Change password

### 🧪 Testing

```bash
# Run all tests
npm run test

# Run tests with coverage
npm run test:coverage

# Run specific test suite
npm run test -- auth.test.ts

# Watch mode
npm run test:watch
```

### 🔒 Security Best Practices

- Never commit `.env` files with sensitive data
- Use HTTPS in production
- Implement rate limiting on API endpoints
- Validate and sanitize all user inputs
- Use parameterized queries to prevent SQL injection
- Regularly update dependencies
- Conduct security audits
- Enable CORS only for trusted origins
- Use security headers (helmet.js)
- Encrypt sensitive data in transit and at rest

### 📝 Environment Variables

See `.env.example` for all available environment variables.

Key variables:
```
NODE_ENV=development
PORT=5000
DB_HOST=localhost
DB_PORT=5432
DB_NAME=apb_db
JWT_SECRET=your_secret_here
REDIS_HOST=localhost
REDIS_PORT=6379
```

### 🤝 Contributing

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit your changes (`git commit -m 'Add amazing feature'`)
3. Push to the branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

### 📄 License

MIT License - See LICENSE file for details

### 🆘 Support & Issues

For issues, bugs, or feature requests, please [create an issue](https://github.com/ugochukwuchinedu369-a11y/Bank-of-America-/issues) on GitHub.

### 👥 Authors

- Your Team @ AMERICAN PRIVATE BANK

---

**Last Updated:** 2026-08-15
**Version:** 1.0.0
