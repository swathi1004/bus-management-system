🚌 Bus Booking Backend Application
📌 Overview
This is a Bus Booking Backend System built using Spring Boot + MySQL.
It provides REST APIs to manage users, buses, routes, seats, bookings, and payments.

The system follows a layered architecture:

Controller → Service → Repository → Database
🚀 Features
👤 User Module
Register user (unique email)

Login (plain password check)

View users

🚌 Bus Module
Add bus

View all buses

📍 Route Module
Add route

View routes

💺 Seat Module
View seats by bus

🎟️ Booking Module
Book ticket

Cancel booking

💳 Payment Module
Make payment

🏗️ Tech Stack
Backend: Spring Boot

Database: MySQL

ORM: JPA / Hibernate

Build Tool: Maven

Testing Tool: Postman

Lombok: Reduces boilerplate

📂 Project Structure
controller/   → API layer
service/      → Business logic
repository/   → Database access
entity/       → Database mapping
dto/          → Request/Response objects
enums/        → Constant values
exception/    → Global error handling
security/     → JWT (basic)
🗄️ Database Tables
users
buses
routes
seats
bookings
booking_seats
payments
🔄 Backend Flow
Client (Postman)
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
MySQL Database
🔐 Roles
USER

Register/Login

Book tickets

Make payments

ADMIN

Add buses

Add routes

📡 API Endpoints
🔐 Auth
POST /api/auth/register
POST /api/auth/login
👤 Users
GET /api/users
GET /api/users/{id}
🚌 Bus
POST /api/buses
GET  /api/buses
📍 Route
POST /api/routes
GET  /api/routes
💺 Seat
GET /api/seats/{busId}
🎟️ Booking
POST   /api/bookings/book
DELETE /api/bookings/cancel/{id}
💳 Payment
POST /api/payments/pay
⚙️ Setup Instructions
1️⃣ Clone Project
git clone <repo-url>
2️⃣ Configure Database
spring.datasource.url=jdbc:mysql://localhost:3306/bus_booking
spring.datasource.username=root
spring.datasource.password=root
3️⃣ Create Database
CREATE DATABASE bus_booking;
4️⃣ Run Application
mvn spring-boot:run
OR run main class:

BusBookingApplication.java
5️⃣ Test APIs
Use Postman:

http://localhost:8080/api/...
