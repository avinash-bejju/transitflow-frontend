# TransitFlow frontend

React + Vite passenger website. This folder is intended to be its own GitHub repository.

## Local

```powershell
npm install
npm run dev
```

The Vite proxy sends `/api` requests to `http://localhost:8080`. For a hosted API, set `VITE_API_URL` to the backend's public URL followed by `/api` (for example `https://transitflow-api.onrender.com/api`).

## Railway

This repository includes a Dockerfile and Caddy configuration for Railway. Create a Railway service named `frontend` from this repository, set the build variable `VITE_API_URL` to `https://${{backend.RAILWAY_PUBLIC_DOMAIN}}/api`, and deploy. The Caddy server listens on Railway's `PORT` and falls back to `index.html` for React Router routes. Set the backend's `APP_CORS_ORIGIN` to this service's exact public URL.

Railway's free trial includes a one-time $5 credit for up to 30 days. The Free plan then includes $1 of monthly resource usage; Hobby starts at $5/month and includes $5 of usage, with additional usage billed separately. See [Railway pricing](https://docs.railway.com/pricing/plans).
