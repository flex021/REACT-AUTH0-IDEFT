# Multi-Frontend SSO Project with Auth0

> **Single Sign-On (SSO) mini-project demonstrating unified authentication across multiple React apps**

[![Live Demo](https://img.shields.io/badge/🚀_Live_Demo-Visit_Here-2ea44f?style=for-the-badge)](https://react-sso-ideft.vercel.app)

## Overview

This project showcases **Single Sign-On (SSO)** using **Auth0** with seamless login/logout across multiple frontends.

**Architecture:**
- **Frontend 1**: React app ([Live Demo](https://react-sso-ideft.vercel.app))
- **Frontend 2**: React app ([Live Demo](https://react-sso-02-ideft.vercel.app))
- **Backend**: Node.js + Express API server ([Render](https://rbac-ideft.onrender.com))

**Key Features:**
- 🔐 Unified authentication across multiple applications
- 🔄 Synchronized logout from all frontends
- 🚀 Independent deployment for frontend and backend
- ⚡ Production-ready SPA with Auth0

## Demo Account

| Email            | Password   |
|-----------------|------------|
| `test-sso@gmail.com` | `test@123` |

Supports **Google, Facebook, GitHub** login.

## Technology Stack

- **Frontend**: React 18.x, Vite, `@auth0/auth0-react`
- **Backend**: Node.js 20.x, Express, Babel
- **Authentication**: Auth0 SSO with JWT
- **Deployment**: Vercel (frontend), Render (backend)

## Setup

**Backend** (`http://localhost:8017`)
```bash
cd backend
yarn install
yarn dev
```

**Frontend 1** (`http://localhost:5173`)
```bash
cd web1-frontend
yarn install
yarn dev
```

**Frontend 2** (`http://localhost:6600`)
```bash
cd web2-frontend
yarn install
yarn dev
```
## Documentation (README full)
👉 [Project Details](./README.full.md)

