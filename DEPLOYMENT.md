# Deployment Guide for Render

## Prerequisites
1. Your code is pushed to a GitHub repository
2. You have a Render account (free at render.com)

## Step-by-Step Deployment

### 1. Prepare Your Repository
- Make sure all files are committed and pushed to GitHub
- Ensure `best.pt` (your YOLO model) is in the root directory
- Verify `requirements.txt` and `app.py` are updated

### 2. Deploy on Render

1. **Sign up/Login to Render**
   - Go to [render.com](https://render.com)
   - Create account or login

2. **Create New Web Service**
   - Click "New +" button
   - Select "Web Service"
   - Connect your GitHub repository

3. **Configure the Service**
   - **Name:** `car-damage-detection` (or your preferred name)
   - **Environment:** `Python 3`
   - **Build Command:** `pip install -r requirements.txt`
   - **Start Command:** `gunicorn app:app`
   - **Plan:** Free

4. **Environment Variables** (if needed)
   - Add any environment variables in the Render dashboard

5. **Deploy**
   - Click "Create Web Service"
   - Wait for build to complete (5-10 minutes)

### 3. Access Your App
- Once deployed, Render will provide a URL like: `https://your-app-name.onrender.com`
- Your app will be live on the internet!

## Important Notes
- The free tier has limitations (sleeps after inactivity)
- Your model file (`best.pt`) should be under 100MB for free tier
- First request might be slow as the app wakes up

## Troubleshooting
- Check build logs in Render dashboard
- Ensure all dependencies are in `requirements.txt`
- Verify `best.pt` file is in the repository 