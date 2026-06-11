# Shopora - E-Commerce Backend

A Spring Boot based e-commerce backend that supports multi-role access, product management, shopping workflows, and online payments. The project focuses on secure authentication, role-based authorization, and scalable backend design using modern Java technologies.

## Features

* JWT Authentication with Access & Refresh Tokens
* Role-Based Access Control (User, Seller, Admin)
* Email Verification and OTP-based Password Reset
* Product & Category Management
* Seller Onboarding and Approval Workflow
* Shopping Cart and Wishlist Management
* Order Creation and Cancellation
* Stripe Payment Integration with Webhooks
* Cloudinary Media Storage
* Global Exception Handling and Structured API Responses
* Scheduled Jobs for OTP Cleanup and Payment Session Expiry

## Tech Stack

* Java 17
* Spring Boot
* Spring Security
* PostgreSQL
* Stripe
* Cloudinary
* Maven

## System Design

The application follows a layered architecture:

Controller → Service → Repository → Database

Key modules include:

* Authentication & Authorization
* Product Management
* Cart & Wishlist
* Orders
* Payments
* Seller Management

## Authentication Flow

1. User registers and verifies email.
2. User logs in and receives Access + Refresh Tokens.
3. Protected APIs are secured using JWT Authentication.
4. Role-based permissions control access to seller and admin operations.

## Payment Flow

1. User creates an order.
2. Backend creates a Stripe Checkout Session.
3. Stripe processes payment.
4. Webhook updates order payment status.
5. Order is marked as completed after successful payment.

## Learning Outcomes

Through this project I gained hands-on experience with:

* Spring Security and JWT Authentication
* Role-Based Access Control (RBAC)
* Third-party API integrations (Stripe, Cloudinary)
* Exception Handling and API Design
* Scheduled Background Jobs
* Database Modeling with PostgreSQL
* Building production-style REST APIs

## Running the Project

```bash
mvn clean install
mvn spring-boot:run
```

Configure database, JWT, Stripe, Cloudinary, and email credentials in `application.properties` before running the application.

