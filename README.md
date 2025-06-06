# 🎓 EduFlow Backend - AI-Powered Learning Management System API

A comprehensive FastAPI-based backend for an AI-powered Learning Management System. Built with modern Python technologies and AI integrations, providing robust APIs for educational institutions.

## 🚀 Tech Stack

- **FastAPI** - Modern Python web framework
- **PostgreSQL** - Database
- **SQLAlchemy** - ORM
- **Google Gemini AI** - AI Integration
- **OpenAI Whisper** - Voice transcription
- **Stripe** - Payment processing
- **JWT** - Authentication

## ✨ Key Features

### 🤖 AI-Powered APIs

- **Google Gemini Integration**: Intelligent tutoring and question answering
- **OpenAI Whisper**: Speech-to-text capabilities
- **Smart Content Analysis**: AI-driven PDF and document processing
- **Adaptive Learning**: Personalized learning recommendations

### 📚 LMS Core APIs

- **User Management**: Multi-role authentication (Admin, Lecturer, Student)
- **Course Management**: Complete course CRUD operations
- **Assignment System**: File upload, submission, and grading APIs
- **Quiz System**: Dynamic quiz generation and assessment
- **Progress Tracking**: Real-time student progress monitoring

### 💳 Payment & Subscription

- **Stripe Integration**: Secure payment processing
- **Subscription Management**: Free, Pro, and Premium tiers
- **Usage Tracking**: API usage monitoring and limits

### 🔄 Real-time Features

- **WebSocket Support**: Live messaging and notifications
- **Discussion Forums**: Threaded discussion APIs
- **Real-time Updates**: Live progress and activity updates

## 🚀 Quick Start

### Prerequisites

- **Python 3.11+** - Backend runtime
- **PostgreSQL** - Database
- **Git** - Version control

### Installation

1. **Clone the Repository**

```bash
git clone <repository-url>
cd eduflow-backend
```

2. **Setup Virtual Environment**

```bash
# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

3. **Environment Configuration**

```bash
# Copy environment template
cp .env.example .env

# Edit .env with your configuration
# DATABASE_URL=postgresql://user:password@localhost:5432/eduflow
# JWT_SECRET_KEY=your-secret-key
# GEMINI_API_KEY=your-gemini-api-key
# STRIPE_API_KEY=your-stripe-key
# STRIPE_WEBHOOK_SECRET=your-webhook-secret
# OPENAI_API_KEY=your-openai-api-key
```

### Running the Application

```bash
# Activate virtual environment
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Start FastAPI server
python main.py
# 🚀 Backend runs on http://localhost:8000
# 📚 API Documentation: http://localhost:8000/docs
```

## 🚀 Deployment on Render

### Environment Variables

Set these environment variables in your Render dashboard:

```bash
# Required
DATABASE_URL=postgresql://your-db-user:your-db-password@your-db-host:5432/your-db-name
JWT_SECRET_KEY=your-super-secret-jwt-key-here-change-this-in-production
GEMINI_API_KEY=your-gemini-api-key-here
STRIPE_API_KEY=sk_live_your-stripe-secret-key-here
STRIPE_WEBHOOK_SECRET=whsec_your-webhook-secret-here

# Optional but Recommended
OPENAI_API_KEY=your-openai-api-key-here
FRONTEND_URL=https://elearningmanagement.netlify.app
ENVIRONMENT=production
JWT_ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30
REFRESH_TOKEN_EXPIRE_MINUTES=10080
```

### Deployment Steps

1. **Connect Repository**: Link your GitHub repository to Render
2. **Configure Build**: Use `pip install -r requirements.txt`
3. **Set Start Command**: `python main.py`
4. **Add Environment Variables**: Copy the variables above
5. **Deploy**: Render will automatically deploy your application

## 📁 Project Structure

```
eduflow-backend/
├── main.py                    # FastAPI application entry point
├── models.py                  # SQLAlchemy database models
├── database.py                # Database configuration
├── auth.py                    # Authentication & JWT handling
├── logger.py                  # Logging configuration
├── requirements.txt           # Python dependencies
├── .env.example              # Environment variables template
├── .gitignore                # Git ignore rules
└── services/                  # Business logic services
    ├── academic_service.py        # Academic structure management
    ├── communication_service.py   # Messaging & notifications
    ├── discussion_service.py      # Forum discussions
    ├── gemini_service.py          # Google Gemini AI integration
    ├── pdf_service.py             # PDF processing & analysis
    ├── quiz_service.py            # Quiz generation & management
    ├── realtime_service.py        # WebSocket & real-time features
    ├── stripe_service.py          # Payment processing
    ├── user_management_service.py # User & role management
    └── whisper_service.py         # Voice transcription
```

## 📚 API Documentation

Once the backend server is running, explore the comprehensive API documentation:

- **🔗 Interactive API Docs**: http://localhost:8000/docs
- **📖 ReDoc Documentation**: http://localhost:8000/redoc
- **🔍 OpenAPI Schema**: http://localhost:8000/openapi.json

### Key API Endpoints

```
Authentication:
POST /api/login          # User login
POST /api/logout         # User logout
POST /api/register       # User registration

Courses:
GET  /api/courses        # List all courses
POST /api/courses        # Create new course
GET  /api/courses/{id}   # Get course details
PUT  /api/courses/{id}   # Update course

AI Features:
POST /api/ask            # AI-powered question answering
POST /api/upload-pdf     # Upload and analyze PDF
GET  /api/quiz           # Generate AI quiz

Users:
GET  /api/users          # List users (admin only)
POST /api/users          # Create user (admin only)
GET  /api/profile        # Get current user profile
```

## 🔒 Security Features

- **🔐 JWT Authentication**: Secure token-based authentication
- **🛡️ Password Hashing**: bcrypt for secure password storage
- **🌐 CORS Protection**: Configured cross-origin resource sharing
- **✅ Input Validation**: Server-side request validation
- **🍪 Secure Cookies**: HTTP-only cookie configuration
- **🔒 Role-based Access**: Multi-level permission system

## 🧪 Development & Testing

### Database Management

```bash
# View database tables (PostgreSQL)
psql $DATABASE_URL -c "\dt"

# Run database migrations
python -c "from database import create_tables; create_tables()"
```

### Testing

```bash
# Run tests
python -m pytest

# Test specific endpoint
curl -X GET "http://localhost:8000/api/health"
```

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. **Fork the Repository**
2. **Create Feature Branch**: `git checkout -b feature/your-feature-name`
3. **Make Changes**: Follow existing code style and add tests
4. **Test Your Changes**: `python -m pytest`
5. **Submit Pull Request**: Provide clear description

## 📄 License

This project is licensed under the **MIT License**.

## 🆘 Support & Help

- **📚 Documentation**: Check this README and API docs at `/docs`
- **🐛 Bug Reports**: Create an issue on GitHub
- **💡 Feature Requests**: Open a discussion on GitHub

---

**EduFlow Backend - Empowering Education Through AI-Powered APIs** 🎓
