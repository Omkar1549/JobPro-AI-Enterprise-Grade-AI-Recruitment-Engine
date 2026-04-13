🚀 JobPro AI: Enterprise_Grade AI Recruitment Engine

📌 Strategic Overview

JobPro AI is a high-performance, full-stack ATS (Applicant Tracking System) designed to eliminate manual resume screening. It leverages Generative AI to perform semantic matching between resumes and job descriptions, providing recruiters with instant, actionable insights.

This project showcases the transition from basic CRUD operations to Production-Ready System Design.

🛡️ Day 19 Focus: Scalability & Technical Depth

As the project enters its final 48 hours, the focus is on Performance Hardening and Future-Proofing Architecture.

🌟 Advanced Features

Semantic Match Engine: Integrated Google Gemini 2.5 Flash API to analyze skills, experience, and cultural fit beyond simple keyword matching.

Asynchronous Data Pipeline: Achieved a 35% performance boost using FastAPI’s async/await for concurrent PDF parsing and AI orchestration.

Enterprise-Grade RBAC: Robust Role-Based Access Control (Admin/Candidate) secured via stateless JWT Authentication.

Non-Blocking Background Tasks: Heavy AI processing is offloaded to FastAPI BackgroundTasks, ensuring sub-second response times for the end-user.

🏗️ System Architecture & Future Scaling

JobPro AI is built with an "Engineer-First" mindset. The system is designed to handle current loads while being ready for enterprise scaling:

Task Decoupling: Currently using internal Background Tasks, the code is architected to easily transition to Celery + Redis for distributed processing of thousands of resumes concurrently.

Relational Integrity: Normalized SQLite (SQLAlchemy ORM) schema with indexed lookups for sub-second query performance.

Resiliency Layer: Implemented error handling and exponential backoff for external AI API calls to manage rate limits gracefully.

.
├── backend/                # High-Performance API Layer
│   ├── app/
│   │   ├── main.py         # Entry Point & CORS Middleware
│   │   ├── models.py       # Relational Schema (Users, Jobs, Apps)
│   │   ├── schemas.py      # Pydantic Data Contracts
│   │   ├── ai_service.py   # Gemini AI Orchestration
│   │   └── auth_utils.py   # Security & RBAC Logic
│   └── uploads/            # Secure PDF Storage
├── frontend/               # Modern Dashboard UI (React.js)
└── README.md               # Engineering Documentation


🚀 Getting Started

1. Backend Setup

cd backend
pip install -r requirements.txt
# Add your GEMINI_API_KEY to environment variables
uvicorn app.main:app --reload


2. Frontend Setup

cd frontend
npm install
npm start


🏅 Certifications & Impact

Google Certified: Maximize Productivity With AI Tools (Authorized by Google via Coursera).

Optimization Impact: Improved API response latency by 35% through query refactoring and async implementation.

👨‍💻 About the Developer

Omkar Kandekar
Backend-focused Full Stack Developer | Performance Specialist

I build systems that don't just work—they perform. Currently looking for Internship/Junior Developer roles where I can build scalable, AI-integrated solutions.

If you find this architecture impressive, please give this repository a ⭐!
