# 🎓 Student Management System
A full-stack school management system built as a university project.  
It supports three user roles — Admin, Teacher, and Student — each with their own dashboard and permissions.
This project was developed as part of our university coursework for the React and C# ASP.NET modules.

# Course Instructors
This project was assigned and supervised by:
#### Mr. Ahmed Mohamed Abdukadir – React Instructor
#### Mr. Abdinur Abdukadir Hashi – C# ASP.NET Instructor

---
# 🏗️ System Architecture
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
# 👥 User Roles
### Role	How to get the account	What they can do
1) Admin	Self-register at `/signup`	Full control — add, edit, delete everything across all 9 tables
2) Teacher	Admin creates login in Users table → Admin creates Teacher profile	Mark attendance, view own subjects/salary/classes
3) Student	Admin creates login in Users table → Admin creates Student profile	View own attendance, results, and fee balance only
---
# 🗃️ Database Tables
## Table	Description
1) `Roles`	Admin / Teacher / Student
2) `Users`	Login accounts for everyone
3) `Students`	Student profiles (linked to a User)
4) `Teachers`	Teacher profiles (linked to a User)
5) `Classes`	School classes (Grade 9-A, Grade 10-B etc.)
6) `Subjects`	Subjects taught (linked to a Class and a Teacher)
7) `Attendance`	Daily attendance records per student
8) `Fees`	Fee payments per student
9) `Results`	Exam results per student per subject
---
# ✨ Key Features
* 🔐 JWT Authentication — secure login, token expires after 8 hours
* 👁️ Role-based dashboards — each role sees only what they're allowed to see
* 📊 Admin dashboard — live summary cards for students, teachers, fees, attendance
* 📅 Smart attendance — pick date → pick class → only unmarked students appear
* 💰 Auto fee status — Paid/Partial/Unpaid calculated automatically from amounts
* 📝 Auto grade — grade calculated from marks when entering results
* 🚫 Duplicate prevention — attendance, results, and fees block duplicate entries
* 🌙 Dark mode — toggleable, preference saved between sessions
* 📱 Responsive — works on mobile, tablet, and desktop
* 📤 Export — each table exports its own data as JSON or plain text
---
# 🛠️ Technology Stack
## Layer	Technology
1) Frontend	React 18, Vite, Tailwind CSS
2) Routing	React Router DOM v6
3) Forms	React Hook Form (with validation)
4) HTTP Client	Axios
5) Backend	C# ASP.NET Core Web API (.NET 8)
6) Data Access	ADO.NET (SqlConnection, SqlCommand, SqlDataReader)
7) Authentication	JWT Bearer Tokens + BCrypt password hashing
8) Database	Microsoft SQL Server
9) Frontend Host	Vercel (free)
10) Backend Host	Render.com (free)
11) Database Host	somee.com (free)
---

# 🚀 Running the Project 

## 1. Both repositories
### Frontend:  https://github.com/cmaalik97/SMSFrontend
### Backend:  https://github.com/cmaalik97/SMSBackend
---

## 2. Live Demo
### Frontend: https://sms-frontend-sooty.vercel.app
### Backend API: https://smsbackend-bhfp.onrender.com/swagger

# 👥 Team Members

##   Member	      |  Responsibility
###  Mohamed      |  UI/UX Design
###  Shuceyb      |  Frontend Development
###  Ahmed	      |  Database Design & SQL
### Jibril        |  ADO.net
### Abdimalik     |  Backend Development (ASP.NET Core Web API)