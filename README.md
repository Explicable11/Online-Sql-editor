# Online-SQL-editor 🔐

**Interactive SQL Learning Platform with LeetCode-Style Validation**

A full-stack web application that provides an interactive environment for learning SQL through hands-on practice with real-time query execution, intelligent hints, and comprehensive test validation.

[![Live Demo](https://sql.devmachine.space/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js](https://img.shields.io/badge/Node.js-16+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-blue.svg)](https://reactjs.org/)

## 🌟 Features

### Core Functionality
- **📚 Assignment Browser**: Browse 15 carefully crafted SQL assignments (Easy, Medium, Hard)
- **💻 Interactive SQL Editor**: Monaco editor with syntax highlighting and auto-completion
- **⚡ Real-time Execution**: Execute SQL queries against PostgreSQL database instantly
- **🧪 LeetCode-Style Validation**: Comprehensive test case validation with hidden test cases
- **💡 AI-Powered Hints**: OpenAI-powered intelligent hints (with smart fallback system)
- **📊 Sample Data Viewer**: Interactive table schema and sample data exploration

### Advanced Features
- **🎯 Test Case System**: Sample test cases + hidden test cases for comprehensive validation
- **📈 Progress Tracking**: Track query attempts and success rates
- **🔒 Secure Execution**: Sandboxed SQL execution with rollback protection
- **📱 Responsive Design**: Mobile-first design that works on all devices
- **⚡ Performance Optimized**: Fast loading with intelligent caching

## 🛠 Tech Stack

### Frontend
- **React.js** - Modern UI framework
- **Monaco Editor** - Professional code editor
- **Vanilla SCSS** - Custom styling with mobile-first approach
- **Axios** - HTTP client for API communication

### Backend
- **Node.js & Express.js** - Server framework
- **PostgreSQL** - SQL query execution engine
- **MongoDB** - Assignment and progress storage
- **OpenAI API** - Intelligent hint generation
- **Helmet & CORS** - Security middleware

### Validation System
- **Custom OutputValidator** - LeetCode-style test validation
- **Query Sanitization** - SQL injection protection
- **Transaction Safety** - Automatic rollback protection

## 🚀 Live Demo

- **Frontend**: [https://your-username.github.io/ciphersqlstudio](https://your-username.github.io/ciphersqlstudio)
- **API**: Deployed backend with full functionality

## 📋 Prerequisites

- Node.js (v16 or higher)
- PostgreSQL (v12 or higher)
- MongoDB (optional - has in-memory fallback)
- OpenAI API Key (optional - has intelligent fallback)

## ⚙️ Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/your-username/ciphersqlstudio.git
cd ciphersqlstudio
```

### 2. Backend Setup
```bash
cd server
npm install

# Configure environment variables
cp .env.example .env
# Edit .env with your database credentials and API keys
```

### 3. Database Setup
```bash
# PostgreSQL setup
psql -U postgres -f db/setupPostgreSQL.sql

# Seed sample data
npm run seed
```

### 4. Frontend Setup
```bash
cd ../client
npm install
```

### 5. Start Development Servers
```bash
# Terminal 1 - Backend
cd server
npm run dev

# Terminal 2 - Frontend  
cd client
npm start
```

Visit `http://localhost:3000` to access the application.

## 🔧 Environment Configuration

### Server (.env)
```env
# Server Configuration
PORT=5001
NODE_ENV=development

# Database Configuration
MONGODB_URI=mongodb://localhost:27017/ciphersqlstudio
POSTGRES_HOST=localhost
POSTGRES_PORT=5432
POSTGRES_DB=ciphersqlstudio
POSTGRES_USER=your_username
POSTGRES_PASSWORD=your_password

# OpenAI Configuration (Optional)
OPENAI_API_KEY=sk-your-openai-api-key-here

# Security
JWT_SECRET=your-secure-jwt-secret
```

## 🧪 Testing System

### LeetCode-Style Validation
- **Sample Test Cases**: Visible to students for debugging
- **Hidden Test Cases**: Comprehensive validation without revealing solutions
- **Validation Types**:
  - Row count validation
  - Column structure validation
  - Data content comparison
  - SQL syntax requirements
  - Performance constraints

### Example Test Case Structure
```javascript
{
  expectedOutput: [...], // Sample test case
  hiddenTestCases: [
    {
      description: "Should return exactly 5 students",
      expectedRowCount: 5
    },
    {
      description: "Must use JOIN operation",
      requiredOperator: "JOIN"
    }
  ]
}
```

## 📚 Assignment Categories

### Easy (5 Assignments)
- Basic SELECT queries
- WHERE clause filtering
- ORDER BY sorting
- Simple aggregations

### Medium (5 Assignments)  
- JOIN operations
- GROUP BY with HAVING
- Subqueries
- Window functions

### Hard (5 Assignments)
- Complex JOINs with subqueries
- Recursive CTEs
- Advanced analytics
- Performance optimization

## 🔒 Security Features

- **SQL Injection Protection**: Query sanitization and validation
- **Sandboxed Execution**: Transaction-based rollback protection
- **Rate Limiting**: API request throttling
- **CORS Configuration**: Secure cross-origin requests
- **Helmet Security**: HTTP security headers

## 🎨 UI/UX Features

- **Mobile-First Design**: Responsive across all devices
- **Professional Layout**: 30%/40%/30% panel distribution
- **Smart Scrolling**: Only necessary panels scroll internally
- **Visual Feedback**: Color-coded validation results
- **Loading States**: Smooth user experience with proper feedback

## 📊 Performance Optimizations

- **Fast Assignment Loading**: <50ms response times
- **Intelligent Caching**: MongoDB fallback to in-memory data
- **Optimized Queries**: Efficient database operations
- **Lazy Loading**: Components load as needed

## 📁 Project Structure

```
ciphersqlstudio/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── pages/          # Page components
│   │   ├── styles/         # SCSS stylesheets
│   │   └── utils/          # Utility functions
│   └── public/             # Static assets
├── server/                 # Node.js backend
│   ├── controllers/        # Route controllers
│   ├── models/            # Database models
│   ├── routes/            # API routes
│   ├── services/          # Business logic
│   └── db/                # Database configuration
└── README.md
```

## 🔌 API Endpoints

- `GET /api/assignments` - Get all assignments
- `GET /api/assignments/:id` - Get specific assignment
- `POST /api/execute` - Execute SQL query with validation
- `POST /api/hint` - Get AI-powered hint
- `POST /api/save-progress` - Save user progress

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Your Name**
- GitHub: https://github.com/dev-dibyanshu/
- LinkedIn: https://www.linkedin.com/in/dev-dibyanshu/
  
## 🙏 Acknowledgments

- OpenAI for intelligent hint generation
- Monaco Editor for professional code editing experience
- PostgreSQL and MongoDB communities
- React.js ecosystem

---

**Built with ❤️ for SQL learning and education**
