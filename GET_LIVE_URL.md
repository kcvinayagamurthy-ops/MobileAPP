# 🚀 Get Your Live Website URL in 5 Minutes

## Fastest Way: Deploy to Render.com (FREE)

### Step 1: Push Code to GitHub (2 minutes)

1. **Create GitHub Repository:**
   - Go to https://github.com
   - Click "New repository"
   - Name: `restaurant-website` (or your choice)
   - Set to Public or Private
   - **DON'T** initialize with README
   - Click "Create repository"

2. **Push Your Code:**
   Open Command Prompt/PowerShell in your project folder:
   ```bash
   git init
   git add .
   git commit -m "Restaurant website ready to deploy"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/restaurant-website.git
   git push -u origin main
   ```
   Replace `YOUR_USERNAME` with your GitHub username

---

### Step 2: Deploy on Render (3 minutes)

1. **Sign Up/Login:**
   - Go to https://render.com
   - Click "Get Started for Free"
   - Sign up with GitHub (easiest)

2. **Create Web Service:**
   - Click "New +" → "Web Service"
   - Click "Connect GitHub" (if not connected)
   - Authorize Render
   - Select your `restaurant-website` repository
   - Click "Connect"

3. **Configure Deployment:**
   - **Name:** `restaurant-website` (or your choice)
   - **Root Directory:** (leave empty)
   - **Environment:** `Node`
   - **Build Command:** `cd backend && npm install`
   - **Start Command:** `node backend/server.js`
   - **Instance Type:** `Free` (select from dropdown)
   - Click "Create Web Service"

4. **Wait for Deployment:**
   - Render will build and deploy
   - Takes 2-5 minutes
   - Watch the logs in real-time

5. **Get Your URL:**
   - Once deployed, you'll see: ✅ Live
   - Your URL will be: `https://restaurant-website-XXXX.onrender.com`
   - Copy this URL!

---

## Your Live URLs

Once deployed, you'll have:

- **Customer Page:** 
  `https://restaurant-website-XXXX.onrender.com`

- **Admin Panel:** 
  `https://restaurant-website-XXXX.onrender.com/admin`

- **Preview Page:** 
  `https://restaurant-website-XXXX.onrender.com/preview.html`

---

## Alternative: Railway.app (Also FREE)

1. Go to https://railway.app
2. Click "Start a New Project"
3. Select "Deploy from GitHub repo"
4. Authorize and select your repository
5. Railway auto-detects everything!
6. Wait 2-3 minutes
7. Get your URL from dashboard

---

## Quick Test After Deployment

1. Visit your live URL
2. You should see:
   - ✅ Menu items with images loading
   - ✅ Cart functionality
   - ✅ All 7 items (Idly, Puttu, Poori, Dosa, Coffee, Tea, Vada)
   - ✅ Admin panel accessible at `/admin`

---

## Troubleshooting

### Images Not Loading?
- Check browser console (F12)
- Verify Unsplash URLs are accessible
- Images load from external URLs (that's normal)

### Build Failed?
- Check Render logs
- Verify `backend/package.json` exists
- Ensure Node.js version 14+ is specified

### URL Not Working?
- Wait 2-3 minutes after first deployment
- Free tier spins down after 15 min inactivity
- First load after spin-down takes ~30 seconds

---

## Need Help?

- Check deployment logs on Render/Railway
- Verify all files pushed to GitHub
- Test locally first: `cd backend && npm install && npm start`

---

**🎉 Once deployed, share your URL! Your restaurant website will be live for the world to see!**
