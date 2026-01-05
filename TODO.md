# Vercel Deployment Checklist

## ✅ Phase 1: Backend Configuration (COMPLETED)
- [x] Modify index.js for Vercel serverless format
- [x] Create vercel.json configuration file
- [x] Update package.json with Vercel scripts

## ✅ Phase 2: Frontend Configuration (COMPLETED)
- [x] Update login.html to use API endpoint instead of static JSON
- [x] Configure static file serving from /public directory

## Phase 3: Build & Deploy
- [ ] Install Vercel CLI globally: `npm i -g vercel`
- [ ] Test deployment locally: `vercel dev`
- [ ] Deploy to production: `vercel --prod`

## Deployment Steps:
1. **Install Vercel CLI** (if not already installed):
   ```bash
   npm i -g vercel
   ```

2. **Login to Vercel**:
   ```bash
   vercel login
   ```

3. **Test locally** (optional):
   ```bash
   vercel dev
   ```

4. **Deploy to production**:
   ```bash
   vercel --prod
   ```

## Environment Variables (Optional):
For better security, set these in Vercel Dashboard:
- `PTERODACTYL_API_KEY` - Your Pterodactyl API key
- `PTERODACTYL_CLIENT_API_KEY` - Your client API key
- `PTERODACTYL_DOMAIN` - Your panel domain
- `TELEGRAM_BOT_TOKEN` - Telegram bot token
- `ADMIN_TELEGRAM_ID` - Admin Telegram ID

## Project Structure:
```
webcpanel/
├── index.js          # Backend (Vercel serverless)
├── vercel.json       # Vercel configuration
├── package.json      # Dependencies
├── public/
│   ├── index.html    # Landing page
│   ├── login.html    # Login page
│   └── dashboard.html # Dashboard
└── README.md
```

## Features:
✅ HTML pages served statically from /public
✅ Backend API routes under /api/
✅ CORS enabled for all origins
✅ Serverless function deployment
✅ Static asset caching configured

## Notes:
- Backend converted to Vercel serverless functions
- Static files served from `/public` directory
- All API routes work under `/api/` path
- Login now uses API endpoint instead of static JSON

