# Ecommerce Demo
## Full Stack E-commerce Platform (User Web + Admin Panel)

منصة تجارة إلكترونية متكاملة مكوّنة من:
- User Web لواجهة العملاء
- Admin Panel لإدارة المتجر
- Backend لإدارة العمليات والبيانات

---

## Live Demo

- User Web: https://ecommerce-demo-brown.vercel.app/
- Admin Panel: https://ecommerce-demo-4eafc.web.app/

> هذه نسخة Demo بدون Domain مخصص، لذلك بعض خدمات البريد المرتبطة بالتحقق لا تعمل كما هو موضح بالأسفل.

---

## Architecture Overview

يتكوّن النظام من ثلاث طبقات رئيسية:

1) Backend API  
2) User Web (Frontend)  
3) Admin Panel (Dashboard)

كل جزء مبني بتقنية مختلفة لتحقيق أفضل أداء حسب وظيفته.

---

## Backend

**Technology**
- Node.js
- Express.js
- MongoDB
- Redis

**Hosting**
- Railway

**Responsibilities**
- Authentication & Authorization
- Product, Category, Brand, Variant Management
- Orders Management
- Coupons & Discounts
- Paymob Payment Integration
- Email Verification & Resend
- Google Sign-In
- Notifications
- Contact & Banner Management
- Logging & Security Layers

**Storage**
- Images stored on Cloudflare R2

---

## User Web (Frontend)

**Technology**
- Next.js (SSR)
- Responsive Design
- Arabic / English

**Hosting**
- Vercel

**Main Features**
- Product browsing, search, and filtering
- Product variants (color, storage, etc.)
- Cart & Checkout
- Account management
- Order tracking
- Coupon usage
- Paymob card / wallet payment
- Dynamic banners and contact info from backend

---

## Admin Panel (Dashboard)

**Technology**
- Flutter Web App

**Hosting**
- Firebase Hosting

**Main Features**
- Dashboard analytics
- Full product management
- Variant types and variants control
- Categories & brands management
- Orders workflow control
- Coupons system
- Posters & banners control
- Contact info & locations management
- Notifications system

---

## Authentication System

- Email/Password Sign Up
- Google Sign-In (OAuth)
- Email Verification
- Resend Verification Email

> ملاحظة: خدمة التحقق عبر البريد وميزة Resend تعتمد على وجود Domain مخصص وإعدادات DNS صحيحة. في نسخة الـ Demo الحالية لا تعمل هذه الجزئية بسبب عدم ربط Domain.

---

## Payment Integration

- Paymob (Card / Wallet)
- Secure payment processing
- Order status tracking after payment

---

## Infrastructure & Services

| Service            | Provider        | Purpose                          |
|--------------------|-----------------|----------------------------------|
| Backend Hosting    | Railway         | Node.js API, MongoDB, Redis     |
| User Web Hosting   | Vercel          | Next.js SSR Frontend            |
| Admin Hosting      | Firebase        | Flutter Web Admin Panel         |
| Image Storage      | Cloudflare R2   | Product and banner images       |

---

## Database Design (MongoDB)

يتم تخزين:
- Users
- Products
- Variants & Variant Types
- Categories & Brands
- Orders
- Coupons
- Banners & Posters
- Contact Information
- Logs

---

## Security

- Encrypted passwords
- JWT Authentication
- Rate Limiting
- CSRF & XSS Protection
- Secure payment flow
- Activity logging

---

## Order Flow

1. العميل يتصفح المنتجات من User Web
2. يختار المتغيرات ويضيف للسلة
3. يتم الدفع عبر Paymob
4. Backend يسجل الطلب في MongoDB
5. الطلب يظهر في Admin Panel
6. الإدارة تحدّث حالة الطلب
7. العميل يتابع حالة الطلب من حسابه

---

## Tech Stack Summary

- Backend: Node.js / Express / MongoDB / Redis
- User Web: Next.js
- Admin Panel: Flutter Web
- Storage: Cloudflare R2
- Payments: Paymob
- Hosting: Railway / Vercel / Firebase

---

## Author

Mohamed Ghabour
