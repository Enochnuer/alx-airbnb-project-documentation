# Backend Requirements Specification – ALX AirBnB Project

This document outlines the technical and functional requirements for core backend features: **User Authentication**, **Property Management**, and **Booking System**.

---

## 1.  User Authentication

### Objective
Allow users to register, log in, and authenticate securely with role-based access control (guest, host, admin).

### Endpoints
- `POST /api/v1/auth/register`  
- `POST /api/v1/auth/login`  
- `GET /api/v1/auth/me`  
- `POST /api/v1/auth/logout`

### Input/Output
#### Registration
**Request:**
```json
{
  "first_name": "Alice",
  "last_name": "Smith",
  "email": "alice@example.com",
  "password": "Secure123!",
  "phone_number": "+1234567890",
  "role": "guest"
}

response 

{
  "user_id": "uuid",
  "email": "alice@example.com",
  "role": "guest",
  "token": "jwt_token"
}