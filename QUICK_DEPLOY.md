# 🚀 Quick Deploy to Production

## Fastest Way: Render.com (Free)

### Step 1: Push to GitHub
```bash
git init
git add .
git commit -m "Initial commit - Restaurant website"
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

### Step 2: Deploy on Render

1. **Sign up/Login** at https://render.com (free account)

2. **Create Web Service:**
   - Click "New +" → "Web Service"
   - Connect your GitHub account
   - Select your repository

3. **Settings:**
   - **Name:** `restaurant-website` (or your choice)
   - **Root Directory:** (leave empty)
   - **Environment:** `Node`
   - **Build Command:** `cd backend && npm install`
   - **Start Command:** `node backend/server.js`
   - **Instance Type:** `Free`

4. **Click "Create Web Service"**

5. **Wait 2-5 minutes** for deployment

6. **Your site is live!** 🎉
   - URL: `https://your-app-name.onrender.com`
   - Customer page: `https://your-app-name.onrender.com`
   - Admin panel: `https://your-app-name.onrender.com/admin`

---

## Alternative: Railway.app (Also Free)

1. Go to https://railway.app
2. Sign up/login
3. Click "New Project" → "Deploy from GitHub repo"
4. Select your repository
5. Railway auto-detects everything!
6. Wait for deployment
7. Done! Get your URL from the dashboard

---

## ✅ What's Already Configured

- ✅ API URLs automatically use your domain (no hardcoding)
- ✅ Server uses environment PORT
- ✅ All deployment files created (Procfile, render.yaml)
- ✅ .gitignore configured
- ✅ Package.json with correct scripts

---

## 🧪 Test Locally First (Optional)

```bash
# Install dependencies
cd backend
npm install

# Start server
npm start

# Visit http://localhost:3000
```

---

## 📝 Notes

- **Free tier on Render:** Spins down after 15 min inactivity (first load ~30 sec)
- **Railway:** More consistent performance on free tier
- **Custom domain:** Available on both platforms (paid plans)

---

## 🆘 Issues?

- Check server logs on hosting platform
- Verify all files are pushed to GitHub
- Ensure Node.js 14+ is specified
- Check browser console for errors

---

**That's it! Your restaurant website is ready to go live! 🎊**

