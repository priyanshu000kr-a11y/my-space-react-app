# My Space — React Blog Platform

**Author:** Priyanshu Kumar  
**Tech Stack:** React, Vite, Firebase Authentication, Cloud Firestore, React Router, react-hot-toast

> A production-inspired blog/content platform built with React, Firebase Authentication and Cloud Firestore.

## Why this project?

My Space demonstrates more than a static React UI. It separates public content from administrative workflows and uses Firebase as the backend service.

## Features

### Public experience

- Responsive landing page
- Blog post catalogue
- Search across title, excerpt and content
- Individual post pages
- Empty/loading/error states
- Accessible form labels and buttons

### Authentication

- Firebase email/password authentication
- Login/logout flow
- Session persistence through Firebase Auth
- Protected admin route

### Admin

- Create blog posts
- Delete posts
- Real-time Firestore updates
- Form validation
- Success/error toast notifications

### Engineering

- React Router
- Reusable UI components
- Firebase service module
- Environment-variable configuration
- Git-safe `.env` handling
- Production build script
- Clear project structure

## Architecture

```text
React UI
  │
  ├── Router
  │    ├── Home
  │    ├── Post Detail
  │    ├── Login
  │    └── Protected Admin
  │
  ├── Firebase Auth
  │
  └── Cloud Firestore
       └── posts collection
```

## Tech Stack

- React
- Vite
- React Router
- Firebase Authentication
- Cloud Firestore
- react-hot-toast
- CSS

## Project Structure

```text
my-space/
├── README.md
├── package.json
├── .env.example
├── .gitignore
├── index.html
└── src/
    ├── firebase.js
    ├── main.jsx
    └── style.css
```

## Installation

```bash
npm install
npm run dev
```

Open the local Vite URL shown in the terminal.

## Firebase Setup

1. Create a Firebase project.
2. Create a Web App.
3. Enable Email/Password Authentication.
4. Create a Cloud Firestore database.
5. Copy the Web App configuration.
6. Create `.env` from `.env.example`.
7. Add the Firebase values to `.env`.

Example:

```env
VITE_FIREBASE_API_KEY=...
VITE_FIREBASE_AUTH_DOMAIN=...
VITE_FIREBASE_PROJECT_ID=...
VITE_FIREBASE_STORAGE_BUCKET=...
VITE_FIREBASE_MESSAGING_SENDER_ID=...
VITE_FIREBASE_APP_ID=...
```

**Never commit `.env`.**

## Firestore Data Model

Collection:

```text
posts/{postId}
```

Document:

```json
{
  "title": "My First Post",
  "excerpt": "A short introduction.",
  "content": "Full post content...",
  "createdAt": "serverTimestamp"
}
```

## Authorization Note

The demo uses an admin email check in the React application so the portfolio can demonstrate protected UI routing.

For a real production deployment, authorization should also be enforced server-side through Firebase Security Rules and/or custom claims. Client-side checks alone must never be treated as the security boundary.

## Build

```bash
npm run build
npm run preview
```

## Suggested Deployment

The Vite build can be deployed to a static hosting provider such as Firebase Hosting, Vercel or Netlify after configuring environment variables.

## Future Improvements

- Rich-text/Markdown editor
- Edit post workflow
- Image uploads with Firebase Storage
- User roles with Firebase custom claims
- Server-side pagination
- Post slugs
- Comments
- Like/bookmark functionality
- Automated tests
- CI/CD

## Author

**Priyanshu Kumar**

This repository is part of Priyanshu Kumar’s software development / machine learning portfolio.
