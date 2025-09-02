# Multi-Frontend SSO Project with Auth0

## Overview
This is a **small project demonstrating Single Sign-On (SSO)** using **Auth0** with:

- **Backend**: Node.js + Express  
- **Frontends**: 2 React apps to test SSO  

Structure:
- `backend` → API server (local: http://localhost:8017)  
- `web1-frontend` → React frontend #1 (local: http://localhost:5173 / live: [React SSO IDEFT](https://react-sso-ideft.vercel.app))  
- `web2-frontend` → React frontend #2 (local: http://localhost:6600 / live: [React SSO 02 IDEFT](https://react-sso-02-ideft.vercel.app))  

Goal: demonstrate knowledge of **multi-frontend SSO**.

---

## Features

- **SSO with Auth0**: login once, access multiple frontends.  
- **Logout sync**: logging out from one frontend logs out user from the other.  
- **Independent deployment**: backend and frontends deployed separately.  

---

## How It Works

1. User visits Web1 or Web2.  
2. Frontend redirects to Auth0 for authentication.  
3. After login, user can switch between Web1 and Web2 **without logging in again**.  
4. Logging out from one frontend triggers logout on the other automatically via Auth0.

---

## Setup

### Backend

```bash
cd backend
yarn install
yarn dev

Runs on http://localhost:8017

### Frontend (Web1 / Web2)
```bash
cd web1-frontend  # or web2-frontend
yarn install
yarn dev
