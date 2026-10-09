# SapphireIQ Airbnb Clone — Full Stack

A complete Airbnb-style listings and booking platform based on the supplied SapphireIQ project guide.

## Stack
- Frontend: React + Vite, React Router, Axios, Leaflet/React-Leaflet
- Backend: Node.js + Express, Mongoose, JWT, bcryptjs
- Database: MongoDB
- Maps: Leaflet + OpenStreetMap (no paid Maps key required)

## Modules implemented
1. Backend foundation: users, listings, bookings, reviews, CRUD APIs, JWT auth, role checks.
2. Listings & search: live API, keyword search, location/type/price/guest filters, responsive cards.
3. Booking flow: date selection, server-side overlap validation, price calculation, cancellation.
4. Maps/reviews/host dashboard: listing map, review aggregation, host listing management, guest reviews.
5. Deployment/polish: environment variables, production build, API health check, responsive UI, image lazy loading.

The PDF explicitly calls for these five modules and a React frontend + Express API + Maps API structure. See the supplied guide pages 3–9. fileciteturn0file0L43-L54

## Run locally

### 1. MongoDB
Start MongoDB locally, or create a MongoDB Atlas database.

### 2. Backend
```bash
cd backend
cp .env.example .env
npm install
npm run seed
npm run dev
```
Backend runs on `http://localhost:5000`.

### 3. Frontend
Open another terminal:
```bash
cd frontend
cp .env.example .env
npm install
npm run dev
```
Frontend runs on `http://localhost:5173`.

### Demo accounts after seeding
- Host: `host@example.com` / `Password123!`
- Guest: `guest@example.com` / `Password123!`

## Production
Build the frontend with `npm run build`. The backend can be deployed to Render/Railway/Fly.io and the frontend to Vercel/Netlify. Set `VITE_API_URL` in the frontend deployment to the backend URL.

## Notes
- This implementation uses Leaflet/OpenStreetMap for the map requirement, so no paid map API key is needed.
- Image URLs are stored as normal listing fields to keep the project simple and deployment-friendly.
- Booking conflict prevention is enforced on the server, not only in the UI.
