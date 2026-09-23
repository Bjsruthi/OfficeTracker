# 🚀 GitHub Setup Guide

Complete guide to create a GitHub repository and deploy the Office Calendar app.

## Step 1: Create a GitHub Account (if you don't have one)

1. Go to [github.com](https://github.com)
2. Click **Sign up**
3. Fill in your details and verify your email

## Step 2: Create a New Repository

### On GitHub Website:

1. Click the **+** icon in the top right corner
2. Select **New repository**
3. Fill in the details:
   - **Repository name:** `office-calendar`
   - **Description:** "A beautiful calendar app to track office days"
   - **Visibility:** Public (or Private if you prefer)
   - **Initialize with:** 
     - ✅ Add a README file
     - ✅ Add .gitignore
     - ✅ Choose license (MIT)
4. Click **Create repository**

## Step 3: Clone Repository Locally

```bash
# Open terminal/command prompt
cd path/to/your/projects

# Clone the repository
git clone https://github.com/YOUR_USERNAME/office-calendar.git

# Navigate into the folder
cd office-calendar
```

## Step 4: Add Your Files

Copy these files from the outputs folder into your cloned repository:

```
index.html              ← Rename from office-calendar.html
service-worker.js
manifest.json
icon.svg
package.json
.gitignore
README.md
```

Your folder structure should look like:
```
office-calendar/
├── index.html
├── service-worker.js
├── manifest.json
├── icon.svg
├── package.json
├── .gitignore
└── README.md
```

## Step 5: Commit and Push to GitHub

```bash
# Add all files to git
git add .

# Commit the changes
git commit -m "Initial commit: Add office calendar PWA"

# Push to GitHub
git push origin main
```

## Step 6: Enable GitHub Pages (for free hosting)

1. Go to your repository on GitHub
2. Click **Settings**
3. Scroll down to **Pages** section
4. Under "Source", select **main** branch
5. Click **Save**
6. Wait a few minutes for deployment
7. Your app will be at: `https://YOUR_USERNAME.github.io/office-calendar/`

## Step 7: Update Manifest for Production

If hosting on GitHub Pages, update `manifest.json`:

```json
{
  "start_url": "/office-calendar/",
  ...
}
```

And update `index.html` service worker path if needed.

## Step 8: Make Your First Commit (Complete)

```bash
git add .
git commit -m "Update manifest for GitHub Pages"
git push origin main
```

## 📱 Share Your App

Now you can share your app with others:

### Share Link
```
https://YOUR_USERNAME.github.io/office-calendar/
```

### Add to Phone
1. Open the link in your phone's browser
2. Tap menu → Add to Home Screen

### Add to Desktop
1. Open the link in your desktop browser
2. Click install icon in address bar or menu

## 🔄 Making Updates

To update your app:

```bash
# Make changes to your files locally
# Then:

git add .
git commit -m "Your update message"
git push origin main

# Changes go live automatically (wait ~1 min)
```

## 🔐 Important Notes

### HTTPS Requirement
- PWA features require HTTPS in production
- GitHub Pages provides HTTPS automatically ✅
- Local testing works with HTTP

### Service Worker Updates
- Changes to `service-worker.js` may take time to update
- Users can force refresh (Ctrl+F5 or Cmd+Shift+R)
- Or clear browser cache and reload

### Icons for App Store (Optional)
To distribute on app stores, you'll need:
- App Store: iOS app bundle
- Play Store: Android APK
- Use tools like PWA Builder for conversion

## 📊 Monitoring

### View Traffic
1. Go to **Insights** tab on GitHub
2. View traffic and engagement

### Check Pages Status
1. Go to **Settings** → **Pages**
2. See deployment status and URL

## 🆘 Troubleshooting

### Changes not showing
- Hard refresh: `Ctrl+F5` (Windows) or `Cmd+Shift+R` (Mac)
- Clear cache: Settings → Clear browsing data
- Wait 1-2 minutes for GitHub Pages to update

### Git push rejected
```bash
# Update your local repo first
git pull origin main

# Then try pushing again
git push origin main
```

### 404 Error
- Check repository name matches URL
- Ensure GitHub Pages is enabled in Settings
- Check `index.html` exists in main branch

## 📚 Additional Resources

- [GitHub Docs](https://docs.github.com)
- [GitHub Pages Help](https://pages.github.com)
- [Git Tutorial](https://git-scm.com/doc)
- [PWA Documentation](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps)

## 🎉 Next Steps

1. **Share your repo** - Add to your portfolio
2. **Customize** - Add your own features
3. **Deploy** - Share link with friends
4. **Collect feedback** - Open issues for suggestions

---

Happy coding! 🚀📅
