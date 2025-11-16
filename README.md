# 3D Models Hub — Client

A React + Vite single-page client application for browsing, uploading and downloading 3D models.

This repository contains the frontend for the 3D Models Hub project, built with React, Vite and TailwindCSS and integrating Firebase for authentication and storage.

**Quick Links**
- **Source**: `src/`
- **Firebase config**: `src/firebase/firebase.config.js`
- **Dev server**: `npm run dev`

**Table of contents**
- [Features](#features)
- [Tech stack](#tech-stack)
- [Project structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Environment / Firebase setup](#environment--firebase-setup)
- [Available scripts](#available-scripts)
- [Linting](#linting)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features

- User authentication (Firebase)
- Add, update and delete 3D model entries
- Browse all models and view model details
- My Models / My Downloads pages
- Client-side routing with React Router
- Notifications with `react-hot-toast` and `react-toastify`

## Tech stack

- React 19
- Vite
- TailwindCSS (+ DaisyUI)
- Firebase (Auth / Firestore / Storage)
- Framer Motion for animations
- React Router for routing
- ESLint for linting

Dependencies shown in `package.json` include `firebase`, `tailwindcss`, `daisyui`, `framer-motion`, `react-router`, `react-hot-toast`, `react-icons`, and `sweetalert2`.

## Project structure

- `src/` — application source
	- `assets/` — static assets (images, icons)
	- `components/` — shared UI components (NavBar, Footer, ModelCard, etc.)
	- `context/` — auth context and provider
	- `firebase/` — Firebase configuration file(s)
	- `layout/` — layouts and pages
	- `router/` — routes and private route wrapper

## Prerequisites

- Node.js (recommended v18+)
- npm (or use `pnpm`/`yarn` if you prefer)

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/Thesachindey/3d-models-hub-client.git
cd 3d-models-hub-client
npm install
```

Start development server:

```bash
npm run dev
```

Open `http://localhost:5173` (Vite default) in your browser.

## Environment / Firebase setup

This project expects a Firebase configuration to be present. Provide your Firebase config in `src/firebase/firebase.config.js`. Example export:

```js
// src/firebase/firebase.config.js
const firebaseConfig = {
	apiKey: "YOUR_API_KEY",
	authDomain: "YOUR_AUTH_DOMAIN",
	projectId: "YOUR_PROJECT_ID",
	storageBucket: "YOUR_STORAGE_BUCKET",
	messagingSenderId: "YOUR_SENDER_ID",
	appId: "YOUR_APP_ID"
};

export default firebaseConfig;
```

Ensure you create a Firebase project and enable Authentication and Firestore/Storage as required by the app features.

## Available scripts

- `npm run dev` — start Vite dev server
- `npm run build` — build production bundle
- `npm run preview` — locally preview production build
- `npm run lint` — run ESLint

Scripts are defined in `package.json`.

## Linting

The project includes ESLint configuration. Run:

```bash
npm run lint
```

Fix issues or follow the lint rules specified in the repo.

## Deployment

Build the production bundle and deploy the `dist/` folder to your static host (Netlify, Vercel, Firebase Hosting, etc.):

```bash
npm run build
```

If using Firebase Hosting, initialize and deploy following Firebase CLI docs.

## Contributing

Contributions are welcome. Please open issues or PRs for bug fixes and improvements. Keep changes focused and add brief descriptions to PRs.

## License

No license specified in `package.json`. Add a `LICENSE` file or set the `license` field in `package.json` if you wish to apply one.

---

