# 🚀 NestJS Learning Project

A hands-on project exploring **core NestJS concepts** by building real-world style APIs.  
It demonstrates authentication, authorization, database relations, validation, serialization, and testing — the foundations of a **production-ready backend**.
It could be treated as a blueprint while scaffolding any new project. 

---

## 📌 Highlights

- **Authentication & Authorization**
  - Secure signup/signin with password hashing + sessions.
  - Role-based access (Admin vs User) enforced via Guards.

- **Entities, DTOs & Validation**
  - TypeORM entities with One-to-Many relationships.
  - DTOs & Pipes ensure clean, validated, and transformed inputs.

- **Custom NestJS Features**
  - Decorators (`@CurrentUser`) for easy user injection.
  - Interceptors for shaping API responses (hide sensitive fields).
  - Middleware to attach current user before Guards run.

- **Testing**
  - Unit tests with fakes & mocks for isolated logic.
  - End-to-End (E2E) tests using **Jest + Supertest**.

---

## 🗄️ Database Setup (Learning-Friendly)

This project uses lightweight **SQLite databases** to keep the focus on learning the **fundamentals of NestJS** without heavy infrastructure setup.

- **Development DB** → `db.sqlite` (simple and fast for local development).  
- **Testing DB** → `test.sqlite` (auto-wiped during E2E tests for consistent, repeatable results).  

⚡ This structure mirrors **real-world best practices** for DB separation and can be easily extended to **Postgres, MySQL, or cloud databases** in production systems.

---

## 🏗️ Architecture

Request
↓
Middleware → Guards → Interceptors
↓
Controller → Service → Repository → Database



- **Controller** → Defines routes.  
- **Service** → Business logic (auth, reports, validation).  
- **Repository** → Data access (TypeORM).  
- **Entity** → Database schema (User, Report).  
- **Module** → Groups features into reusable units.  

---

## ▶️ How to Run

1. **Install dependencies**
   ```bash
    npm install

2. **Start Dev Server**

    ```bash 
    npm run start:dev

3. **Run Tests**
   ```bash
   # Run unit tests
   npm run test

   # Run end-to-end (E2E) tests
   npm run test:e2e

