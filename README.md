🔗 LinkClean — Full-Stack URL Optimization Engine

🌐 Live Demo

👉 **Try it here:** https://linkcleanio.netlify.app

---

🚀 Overview

**LinkClean** is a full-stack web application designed to transform long, cluttered, tracking-heavy URLs into clean, memorable **3-word short links**.

The project demonstrates complete end-to-end web development, including:

• Responsive frontend development
• RESTful API design
• Database integration
• Cloud deployment
• URL sanitization & optimization
• Real-world networking and security troubleshooting

---

🛠️ Tech Stack

🎨 Frontend

• HTML5
• CSS3
• Vanilla JavaScript
• Netlify Deployment

⚙️ Backend

• Node.js
• Express.js
• Render Deployment

🗄️ Database

• MongoDB Atlas
• Mongoose ODM

🔄 Routing

• Custom Client-Side Hash Routing

---

🏗️ Project Development Stages

🔹 Stage 1: Frontend UI & URL Processing

• Designed a modern dark-themed glassmorphism interface
• Built a responsive and user-friendly experience
• Automatically removes tracking parameters such as:

* `utm_source`
* `gclid`
* `fbclid`
  • Generates unique randomized 3-word slugs
  • Sends sanitized URLs to the backend API

---

🔹 Stage 2: REST API Engineering

📌 Create Route (POST)

• Validates incoming URLs
• Ensures slug uniqueness
• Stores URL-slug mappings securely in MongoDB

📌 Retrieve Route (GET)

• Fetches original URLs from the database
• Powers instant redirection using generated slugs

---

🔹 Stage 3: Cloud Deployment & Integration

• Deployed frontend globally using Netlify CDN
• Hosted backend services on Render
• Connected application to MongoDB Atlas
• Secured sensitive credentials using environment variables (`.env`)

---

🚧 Engineering Challenges & Solutions

🌍 Cross-Origin Resource Sharing (CORS)

❌ Challenge

The deployed frontend was blocked from communicating with the backend due to browser security restrictions.

✅ Solution

• Diagnosed the issue using browser developer tools
• Implemented Express CORS middleware
• Configured secure cross-origin access between frontend and backend

---

☁️ MongoDB Atlas Network Restrictions

❌ Challenge

The backend failed to connect because Atlas blocks unknown IP addresses by default.

✅ Solution

• Updated Atlas Network Access settings
• Configured CIDR whitelist rules (`0.0.0.0/0`) for cloud deployment
• Maintained security through protected credentials and environment variables

---

⏳ Render Cold Starts

❌ Challenge

Free-tier Render services enter sleep mode during inactivity, causing delays on the first request.

✅ Solution

• Implemented a loading state in the frontend
• Disabled submissions while processing
• Added clear user feedback through a "Processing..." interface

---

✨ Key Features

• URL sanitization and tracking parameter removal
• Randomized 3-word slug generation
• Secure REST API architecture
• MongoDB database persistence
• Responsive glassmorphism UI
• Cloud-hosted production deployment
• Fast redirection system
• Real-world networking and deployment solutions

---

🎯 What This Project Demonstrates

• Full-Stack Development
• REST API Design
• Database Management
• Cloud Deployment
• Debugging & Problem Solving
• Network Security Fundamentals
• Production-Level Project Architecture
