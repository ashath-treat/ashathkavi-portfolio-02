Ashathkavi Portfolio – Monorepo

This repository contains the complete source code for my personal portfolio website and integrated CMS.
It is built using a modern, scalable architecture designed for long-term maintainability, CI/CD automation, and content-driven workflows.


🚀 Tech Stack

Frontend: React (CRA / Vite optional upgrade)

CMS: Sanity Studio (v3)

Hosting & CI/CD: Azure Static Web Apps + GitHub Actions

Content Delivery: Sanity CDN

Deployment Model: Monorepo with unified build & deploy pipeline


🚀 Project Structure
frontend/   → React app (public website)
studio/     → Sanity Studio (CMS dashboard)
.github/    → GitHub Actions CI/CD pipeline

Live URLs (example)
Component	URL
Frontend	https://your-app.azurestaticapps.net/

Sanity Studio	https://your-app.azurestaticapps.net/studio
🔧 Development
Install dependencies
cd frontend && npm install
cd ../studio && npm install

Run locally (frontend)
cd frontend
npm start

Run locally (Sanity)
cd studio
npm run dev


🚀 Deployment (CI/CD)

Deployment is triggered automatically when pushing to the main branch.

The GitHub Actions workflow:

Builds the frontend

Builds the Sanity Studio

Deploys both to Azure Static Web Apps

You only need to configure AZURE_SWA_TOKEN inside GitHub Secrets.


🧩 Environment Variables
Frontend (frontend/.env.example)
REACT_APP_SANITY_PROJECT_ID=
REACT_APP_SANITY_DATASET=production
REACT_APP_SANITY_API_VERSION=2023-10-01

Sanity (studio/.env)
SANITY_STUDIO_PROJECT_ID=
SANITY_STUDIO_DATASET=production


🔒 Security

Never commit .env files

Use GitHub Secrets for production credentials

Sanity content operations secured via tokens & CORS origins


📄 License

MIT License (optional)


🧑‍💻 Author

Satgunarajah Ashathkavi
Developer & CEO
TealTemplate – “Stabilizing the business blueprint.”