🔗 LinkClean: Full-Stack URL Optimization Engine

🚀 View Live Application Here By Clicking On This Link (https://linkcleanio.netlify.app)
LinkClean is a full-stack web application architected to sanitize and condense bloated, tracking-heavy URLs into clean, memorable 3-word slugs. Built from the ground up, this project demonstrates end-to-end web development, from designing a responsive client-side interface to deploying a secure, cloud-hosted REST API and database.

🛠️ Technical Architecture
Frontend: Vanilla HTML5, CSS3, JavaScript (Deployed via Netlify)

Backend: Node.js, Express.js (Deployed via Render)

Database: MongoDB Atlas (Mongoose ODM)

Routing: Custom client-side hash routing for instant redirects

🏗️ Development Lifecycle & Stages
Stage 1: Client-Side UI & Logic
The focus was on creating a frictionless user experience. I designed a dark-themed, glassmorphism UI that feels modern and responsive. The core JavaScript logic intercepts the user's raw input, actively strips out known tracking parameters (like utm_source, gclid, fbclid), and generates a unique, randomized 3-word slug before passing the sanitized payload to the backend.

Stage 2: RESTful API Engineering
I engineered a lightweight Node.js/Express backend to handle incoming requests.

Create Route (POST): Validates the incoming sanitized URL, ensures the generated slug is unique, and safely stores the key-value pair in MongoDB.

Retrieve Route (GET): Acts as the redirection engine, querying the database for a specific slug and returning the original destination link.

Stage 3: Cloud Deployment & Database Integration
Transitioned the application from a local development environment to the live internet. This involved deploying the static frontend to Netlify’s global CDN, hosting the Node.js server on Render, and establishing a secure connection to a MongoDB Atlas cluster using environment variables (.env) to protect database credentials.

🚧 Engineering Challenges & Solutions
Building a full-stack application and pushing it to production presented several real-world networking and security challenges:

Challenge: Cross-Origin Resource Sharing (CORS) Blocks * The Issue: Once deployed, the Netlify frontend was completely blocked from communicating with the Render backend due to strict browser security policies preventing unauthorized cross-origin HTTP requests.

The Solution: I diagnosed the network failure via browser developer tools and implemented the cors middleware pipeline within the Express application, explicitly configuring the server to accept cross-origin requests from the client.

Challenge: Cloud Database Network Restrictions

The Issue: The Render cloud server crashed upon deployment because MongoDB Atlas aggressively blocks unknown IP addresses by default, preventing the backend from accessing the database vault.

The Solution: I navigated the MongoDB Atlas security configurations and updated the Network Access rules, implementing a CIDR notation override (0.0.0.0/0) to whitelist the cloud server's dynamic IP address while keeping the cluster credentials secure.

Challenge: Asynchronous Cold Starts

The Issue: Free-tier cloud servers (Render) spin down during inactivity, causing a 20-40 second delay on the very first API request.

The Solution: I engineered the frontend UI to gracefully handle long resolution times, disabling the submit button and rendering a "Processing..." state to provide continuous user feedback while the backend wakes up.
