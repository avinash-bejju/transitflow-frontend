# TransitFlow frontend

React + Vite passenger website. This folder is intended to be its own GitHub repository.

## Local

```powershell
npm install
npm run dev
```

The Vite proxy sends `/api` requests to `http://localhost:8080`. For a hosted API, set `VITE_API_URL` to the backend's public URL followed by `/api` (for example `https://transitflow-api.onrender.com/api`).

## Render

Push this folder as a standalone GitHub repo and create a Blueprint from its `render.yaml`. Set `VITE_API_URL` to the deployed backend URL ending in `/api`. The rewrite in the Blueprint supports React Router deep links. Set the backend's `APP_CORS_ORIGIN` to the static site's exact `https://...onrender.com` URL.
