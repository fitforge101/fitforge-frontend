🔗 **Central Documentation:** [https://github.com/fitforge101/fitforge-app-docs](https://github.com/fitforge101/fitforge-app-docs)

# Frontend Application

## Overview
The `fitforge-frontend` repository contains the React-based Single Page Application (SPA) for the FitForge platform. It serves as the main interactive portal for users to track their workouts, nutrition, and chat with the AI assistant.

## Features
*   Responsive, fast SPA built with React 18.
*   Client-side routing via React Router DOM.
*   API integration using Axios communicating with the Envoy API Gateway.
*   Lightning-fast development server powered by Vite.

## Tech Stack
*   Vite
*   React
*   React Router DOM
*   Axios

## Setup Instructions
1.  **Install Dependencies:**
    ```bash
    npm ci
    ```
2.  **Run Development Server:**
    ```bash
    npm run dev
    ```

## Environment Variables
*   `VITE_API_GATEWAY_URL` (Required: Points to the Envoy Ingress Gateway)

## Folder Structure
```text
.
├── Dockerfile
├── package.json
├── vite.config.js
└── src/
    ├── App.jsx
    ├── main.jsx
    ├── components/
    ├── pages/
    └── services/
```

## Deployment
The application is packaged as static assets within an Nginx Docker container (`Dockerfile`). It is deployed to Kubernetes via Helm charts and is the only service in the FitForge ecosystem configured with an HPA to auto-scale based on CPU/Memory usage.
