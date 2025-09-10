# Multi-Frontend SSO Project with Auth0

> **Production-ready Single Sign-On implementation across multiple React applications**

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Visit_Here-2ea44f?style=for-the-badge)](https://react-sso-ideft.vercel.app)

## Overview

This project demonstrates enterprise-level **Single Sign-On (SSO)** implementation using **Auth0** with seamless authentication across multiple frontend applications.

**Architecture:**
- Frontend 1: React application ([Live Demo](https://react-sso-ideft.vercel.app))  
- Frontend 2: React application ([Live Demo](https://react-sso-02-ideft.vercel.app))
- Backend: Node.js + Express API server

**Note:** Open both React apps to use the SSO functionality.

**Key Features:**
- 🔐 Unified authentication across multiple applications
- 🔄 Synchronized logout from all connected frontends  
- 🚀 Independent deployment and scaling
- ⚡ Production-ready with live demonstrations

## Technical Implementation

**Backend** (`localhost:8017`)
```bash
cd backend
yarn install
yarn dev
```

**Frontend Applications**
```bash
# Frontend 1 (localhost:5173)
cd web1-frontend
yarn install
yarn dev

# Frontend 2 (localhost:6600)
cd web2-frontend
yarn install
yarn dev
```

> **Note:** Both frontends use identical package.json.

**Technology Stack:**
- **Authentication:** Auth0 with `express-oauth2-jwt-bearer`
- **Frontend:** React 18.3.1, Vite 5.3.1, `@auth0/auth0-react` 2.2.4
- **Backend:** Node.js 20.x, Express 4.18.2, Babel transpilation
- **Database:** NeDB (embedded database)
- **Deployment:** Vercel (frontend), Render (backend)

## Authentication Flow
<div align="center">

<div>
  <img src="https://github.com/user-attachments/assets/8691007b-6977-41ac-ba32-7e72543c7e83" width="320" alt="Auth0 Login" style="display:inline-block; margin:8px;">
  <img src="https://github.com/user-attachments/assets/f0e2915a-ff38-4084-8a78-6064365e04f8" width="320" alt="Web1 Dashboard" style="display:inline-block; margin:8px;">
  <img src="https://github.com/user-attachments/assets/1afba49c-e5ad-420e-a8ef-0d5ed3d5345e" width="320" alt="Web2 Dashboard" style="display:inline-block; margin:8px;">
</div>

*Auth0 Login → Web1 Dashboard → Web2 Dashboard (Same User Authentication)*

</div>


1. User accesses any frontend application
2. Redirect to Auth0 for authentication  
3. Return with valid JWT token
4. Access granted to all connected applications
5. Logout from one application = logout from all

## SSO Notes / Demo

This project uses Auth0 for SSO across multiple React apps.

- Logging into **App 1** creates a session in Auth0.
- **App 2** detects the session on load; a **page refresh** may be needed to sync login.
- This is normal SPA behavior, not a bug.

**Demo Account:**  
- Email: `test-sso@gmail.com`  
- Password: `test@123`  

You can also log in via **Google, Facebook, GitHub**.

- - -

## Project Structure

```
project/
├── backend/           # Express API server
├── web1-frontend/     # React application #1
├── web2-frontend/     # React application #2
└── README.md         # This file
```

## Development & Production Scripts

**Backend Commands:**
```bash
yarn dev             # Development with Babel + Nodemon
npm run build        # Clean + Babel transpilation  
npm run production   # Build + Production server
npm run lint         # ESLint validation
```

**Frontend Commands:**
```bash
yarn dev             # Vite dev server with --host --port 5173
npm run build        # Production build
npm run preview      # Preview production build
npm run lint         # ESLint validation
```

## Key Dependencies

**Backend:**
- `express-oauth2-jwt-bearer` - Auth0 JWT validation middleware
- `nedb-promises` - Embedded database for lightweight data storage
- `cors` - Cross-Origin Resource Sharing configuration
- `babel` - ES6+ transpilation for Node.js compatibility

**Frontend:**
- `@auth0/auth0-react` - Auth0 React SDK for authentication
- `axios` - HTTP client for API communication
- `react-json-view` - JSON data visualization component
- `@vitejs/plugin-react-swc` - Fast React refresh with SWC compiler

**Auth0 Tenant Settings:**
- Callback URLs: Include all frontend URLs
- Web Origins: Include all application origins  
- Logout URLs: Include all frontend logout endpoints

## Configuration Requirements

This project uses **Git Submodules** for modular development:

```bash
# Clone with all submodules
git clone --recurse-submodules <repo-url>

# Update submodule references
git submodule update --remote
git add backend web1-frontend web2-frontend
git commit -m "Update submodule references"
```

## Deployment

- **Backend:** Deployed on Render with auto-deploy from Git
- **Frontends:** Deployed on Vercel with auto-deploy from Git
- **Environment:** Production-ready with proper CORS and security headers

## Business Value

**Problem Solved:** Eliminates need for users to authenticate multiple times across related applications, improving user experience and reducing support overhead.

**Technical Benefits:** 
- Centralized user management
- Scalable authentication system  
- Reduced development complexity for new applications

---

**Note:** This project demonstrates real-world SSO implementation patterns suitable for enterprise applications.
