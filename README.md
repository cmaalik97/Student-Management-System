🎓 Student Management System
A full-stack school management system built as a university project.  
It supports three user roles — Admin, Teacher, and Student — each with their own dashboard and permissions.
This project was developed as part of our university coursework for the React and C# ASP.NET modules.

# Course Instructors

This project was assigned and supervised by:

Mr. Ahmed Mohamed Abdukadir – React Instructor
Mr. Abdinur Abdukadir Hashi – C# ASP.NET Instructor

The project will be evaluated in two parts:

Frontend (React) will be reviewed by Mr. Ahmed Mohamed Abdukadir.
Backend (C# ASP.NET Core) will be reviewed by Mr. Abdinur Abdukadir Hashi.
---
🏗️ System Architecture
```
┌─────────────────────────────────────────────────────────┐
│                     USER (Browser)                      │
└──────────────────────────┬──────────────────────────────┘
                           │ HTTP / HTTPS
┌──────────────────────────▼──────────────────────────────┐
│              REACT FRONTEND  (Vite + Tailwind)          │
│                   hosted on Vercel                       │
└──────────────────────────┬──────────────────────────────┘
                           │ REST API calls with JWT token
┌──────────────────────────▼──────────────────────────────┐
│           C# ASP.NET CORE WEB API (ADO.NET)             │
│                   hosted on Render.com                   │
└──────────────────────────┬──────────────────────────────┘
                           │ SQL queries (SqlConnection)
┌──────────────────────────▼──────────────────────────────┐
│              SQL SERVER DATABASE                        │
│                   hosted on somee.com                    │
└─────────────────────────────────────────────────────────┘
```
---
👥 User Roles
Role	How to get the account	What they can do
Admin	Self-register at `/signup`	Full control — add, edit, delete everything across all 9 tables
Teacher	Admin creates login in Users table → Admin creates Teacher profile	Mark attendance, view own subjects/salary/classes
Student	Admin creates login in Users table → Admin creates Student profile	View own attendance, results, and fee balance only
---
🗃️ Database Tables
Table	Description
`Roles`	Admin / Teacher / Student
`Users`	Login accounts for everyone
`Students`	Student profiles (linked to a User)
`Teachers`	Teacher profiles (linked to a User)
`Classes`	School classes (Grade 9-A, Grade 10-B etc.)
`Subjects`	Subjects taught (linked to a Class and a Teacher)
`Attendance`	Daily attendance records per student
`Fees`	Fee payments per student
`Results`	Exam results per student per subject
---
✨ Key Features
🔐 JWT Authentication — secure login, token expires after 8 hours
👁️ Role-based dashboards — each role sees only what they're allowed to see
📊 Admin dashboard — live summary cards for students, teachers, fees, attendance
📅 Smart attendance — pick date → pick class → only unmarked students appear
💰 Auto fee status — Paid/Partial/Unpaid calculated automatically from amounts
📝 Auto grade — grade calculated from marks when entering results
🚫 Duplicate prevention — attendance, results, and fees block duplicate entries
🌙 Dark mode — toggleable, preference saved between sessions
📱 Responsive — works on mobile, tablet, and desktop
📤 Export — each table exports its own data as JSON or plain text
---
🛠️ Technology Stack
Layer	Technology
Frontend	React 18, Vite, Tailwind CSS
Routing	React Router DOM v6
Forms	React Hook Form (with validation)
HTTP Client	Axios
Backend	C# ASP.NET Core Web API (.NET 8)
Data Access	ADO.NET (SqlConnection, SqlCommand, SqlDataReader)
Authentication	JWT Bearer Tokens + BCrypt password hashing
Database	Microsoft SQL Server
Frontend Host	Vercel (free)
Backend Host	Render.com (free)
Database Host	somee.com (free)
---
🚀 Running the Project 

1.Both repositories

## Frontend
https://github.com/cmaalik97/SMSFrontend

## Backend
https://github.com/cmaalik97/SMSBackend
---

2.Live Demo


## Frontend:
  https://sms-frontend-sooty.vercel.app

## Backend API:
https://smsbackend-bhfp.onrender.com/swagger


📄 Detailed Documentation
Frontend README — React project structure, components, routing
Backend README — C# project structure, API endpoints, ADO.NET pattern

👥 Team Members

Member	Responsibility

Mohamed	UI/UX Design
Shuceyb	Frontend Development
Ahmed	Database Design & SQL
Jibril	LINQ
Abdimalik	Backend Development (ASP.NET Core Web API)
