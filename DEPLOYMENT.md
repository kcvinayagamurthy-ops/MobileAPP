# Deployment Guide

This guide will help you deploy the restaurant website to production.

## Quick Deploy Options

### Option 1: Render (Recommended - Easiest)

1. **Create a Render account** at https://render.com

2. **Create a new Web Service:**
   - Click "New +" → "Web Service"
   - Connect your GitHub repository (or push code to GitHub first)
   - Select your repository

3. **Configure the service:**
   - **Name:** restaurant-website (or your choice)
   - **Root Directory:** Leave empty (or specify if in subdirectory)
   - **Environment:** Node
   - **Build Command:** `cd backend && npm install`
   - **Start Command:** `node backend/server.js`
   - **Instance Type:** Free (or paid for better performance)

4. **Environment Variables:**
   - Add if needed: `NODE_ENV=production`
   - PORT will be automatically set by Render

5. **Deploy:**
   - Click "Create Web Service"
   - Wait for deployment to complete
   - Your site will be live at `https://your-app-name.onrender.com`

**Note:** Free tier on Render spins down after 15 minutes of inactivity. First request after spin-down may take ~30 seconds.

---

### Option 2: Railway

1. **Create a Railway account** at https://railway.app

2. **Create a new project:**
   - Click "New Project"
   - Select "Deploy from GitHub repo" (connect GitHub if needed)
   - Select your repository

3. **Configure:**
   - Railway auto-detects Node.js
   - Root directory: Set to project root
   - Build command: `cd backend && npm install`
   - Start command: `node backend/server.js`

4. **Deploy:**
   - Railway will automatically deploy
   - Get your live URL from the service dashboard
   - Add custom domain if needed (paid plan)

---

### Option 3: Heroku

1. **Install Heroku CLI:**
   ```bash
   # Windows: Download from https://devcenter.heroku.com/articles/heroku-cli
   # Or use: npm install -g heroku
   ```

2. **Login to Heroku:**
   ```bash
   heroku login
   ```

3. **Create Heroku app:**
   ```bash
   heroku create your-app-name
   ```

4. **Set buildpack:**
   ```bash
   heroku buildpacks:set heroku/nodejs
   ```

5. **Deploy:**
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git push heroku main
   ```

6. **Open your app:**
   ```bash
   heroku open
   ```

**Note:** Heroku no longer has a free tier. Paid plans start at $7/month.

---

### Option 4: Vercel (Frontend) + Render/Railway (Backend)

**For Backend:**
1. Deploy backend to Render or Railway using steps above
2. Note the backend URL (e.g., `https://api.example.com`)

**For Frontend:**
1. Create Vercel account at https://vercel.com
2. Import your GitHub repository
3. Configure:
   - Framework Preset: Other
   - Build Command: Leave empty
   - Output Directory: `public`
   - Install Command: Leave empty
4. Add Environment Variable: `VITE_API_URL` or update API URLs in JS files
5. Deploy

---

## Pre-Deployment Checklist

- [x] API URLs updated to use `window.location.origin` (already done)
- [x] PORT uses environment variable (already configured)
- [ ] Test locally: `cd backend && npm install && npm start`
- [ ] Verify all images load correctly
- [ ] Test cart functionality
- [ ] Test admin CRUD operations
- [ ] Test sales reports

---

## Environment Variables

These are automatically set by hosting platforms, but you can configure:

- `PORT`: Server port (defaults to 3000, auto-set by hosting)
- `NODE_ENV`: Set to `production` in production

---

## Post-Deployment

1. **Test your live site:**
   - Visit your deployed URL
   - Test menu loading
   - Test adding items to cart
   - Test Pay Now and QR code
   - Test bill printing
   - Test admin panel CRUD operations

2. **Update README:**
   - Add your live URL
   - Update any documentation

3. **Optional - Custom Domain:**
   - Most platforms support custom domains
   - Configure DNS as per platform instructions

---

## Troubleshooting

### Images not loading
- Check if Unsplash URLs are accessible
- Verify CORS settings if using external images
- Check browser console for errors

### API errors
- Verify API URL is correct (should use `window.location.origin`)
- Check server logs on hosting platform
- Ensure backend routes are accessible

### Build fails
- Check Node.js version (requires 14+)
- Verify all dependencies are in `package.json`
- Check build logs on hosting platform

### Port already in use (local)
- Change PORT in `.env` file
- Or kill process using port 3000

---

## Monitoring

- Check hosting platform logs regularly
- Monitor error rates
- Set up alerts if available on your platform
- Monitor API response times

---

## Backup Data

Since we're using JSON files for storage:
- Consider exporting data regularly
- `backend/data/menu.json` - Menu items
- `backend/data/orders.json` - Order history
- For production, consider migrating to a database (MongoDB, PostgreSQL, etc.)

---

## Need Help?

- Check hosting platform documentation
- Review server logs
- Test locally first
- Check browser console for client-side errors

