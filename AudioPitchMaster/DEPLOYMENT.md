# PitchChanger Pro - Deployment Guide

## Quick Deployment to pitchchanger.app

### 1. Download Project from Replit
- Click the three dots menu (⋯) in Replit file explorer
- Select "Download as zip"
- Extract files to your local machine

### 2. Set Up Neon Database
1. Go to [neon.tech](https://neon.tech) and create account
2. Create new project/database
3. Copy the connection string (format: `postgresql://user:pass@host/db`)

### 3. Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) and sign in
2. Click "New Project"
3. Upload your extracted project folder
4. Vercel auto-detects as Node.js project

### 4. Configure Environment Variables in Vercel
In Vercel Project Dashboard → Settings → Environment Variables:

```bash
DATABASE_URL=postgresql://your_neon_connection_string_here
SESSION_SECRET=generate_random_32_character_string
REPL_ID=your_repl_id_from_replit_url
REPLIT_DOMAINS=pitchchanger.app
VITE_GOOGLE_ADS_ID=G-XXXXXXXXXX  # Optional: Add when you get Google Ads ID
```

### 5. Connect Domain
- Vercel Project → Settings → Domains
- Add `pitchchanger.app`
- Vercel handles SSL automatically

### 6. Database Setup
After deployment, initialize database:
- Go to Vercel Project → Functions
- Run: `npm run db:push`

### 7. Test Your Live Site
Visit `https://pitchchanger.app` and test:
- User authentication (login/logout)
- Audio upload and processing
- All studio features

## Features Ready for Production
✅ User authentication with Replit Auth  
✅ Professional landing page  
✅ 9-tab audio studio interface  
✅ Google Ads tracking integration  
✅ Database persistence  
✅ File upload and processing  
✅ Real-time audio effects  
✅ Project management  
✅ Professional export options  

## Deployment Checklist

### Pre-Deployment
- [ ] Download project from Replit as ZIP
- [ ] Extract files locally
- [ ] Have Neon database connection string ready

### Vercel Setup
- [ ] Upload project to Vercel
- [ ] Add all environment variables
- [ ] Connect pitchchanger.app domain
- [ ] Deploy and test

### Post-Deployment
- [ ] Run database migration: `npm run db:push`
- [ ] Test user authentication
- [ ] Test audio upload and processing
- [ ] Verify all studio features work

### Optional Enhancements
- [ ] Set up Google Ads account and add tracking ID
- [ ] Configure analytics dashboard
- [ ] Set up monitoring alerts

## Support
- Database issues: Check Neon dashboard
- Domain issues: Check Vercel domains settings
- App issues: Check Vercel function logs

Your professional audio studio is ready for users!
