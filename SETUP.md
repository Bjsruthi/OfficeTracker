# 📋 Complete Setup Guide

Full step-by-step guide to set up and deploy the Office Calendar PWA.

## What You're Getting

A **Progressive Web App** that:
- 📱 Installs on phones like native app
- 🖥️ Installs on desktop
- 🌙 Dark theme with purple highlights
- 💾 Works offline
- 📊 Tracks office days
- 🚀 Hosted on GitHub (free)

## Prerequisites

### Absolutely Required:
- ✅ Web browser (Chrome, Firefox, Safari, Edge)
- ✅ GitHub account (free at github.com)

### Recommended (not required):
- ✅ Git installed (for easier updates)
- ✅ Code editor (VS Code, Sublime, etc.)
- ✅ Node.js (for local testing)

---

## Phase 1: Local Testing (5-10 minutes)

### Step 1.1: Download Files

Download all these files to a folder:
```
office-calendar/
├── index.html
├── service-worker.js
├── manifest.json
├── icon.svg
├── package.json
├── .gitignore
├── README.md
├── GITHUB_SETUP.md
├── QUICKSTART.md
└── LICENSE
```

### Step 1.2: Start Local Server

**On Windows (Command Prompt):**
```cmd
cd path\to\office-calendar
python -m http.server 8000
```

**On Mac/Linux (Terminal):**
```bash
cd path/to/office-calendar
python3 -m http.server 8000
```

### Step 1.3: Open in Browser

1. Open your browser
2. Go to: `http://localhost:8000`
3. You should see the calendar with dark theme

### Step 1.4: Test Features

- [ ] Calendar loads with dark theme
- [ ] Weekdays show at top
- [ ] Current month displays
- [ ] Can navigate to other months
- [ ] Double-click a day → turns purple with 🏢
- [ ] Double-click again → removes marking
- [ ] Data persists after refresh
- [ ] Works without internet (offline)

**If something doesn't work:**
1. Check console (F12 → Console tab)
2. Look for red errors
3. Try Ctrl+F5 to hard refresh
4. Try different browser

---

## Phase 2: Prepare for GitHub (10-15 minutes)

### Step 2.1: Create GitHub Account

1. Go to [github.com](https://github.com)
2. Click **Sign up**
3. Create account with email
4. Verify your email

### Step 2.2: Create GitHub Repository

1. Click **+** in top right
2. Select **New repository**
3. Name: `office-calendar`
4. Description: `A dark-themed calendar PWA for tracking office days`
5. Visibility: **Public**
6. **Do NOT** initialize with README (we have our own)
7. Click **Create repository**

### Step 2.3: Install Git (if needed)

**Windows:**
1. Go to [git-scm.com](https://git-scm.com)
2. Download and install
3. Use all default options

**Mac:**
```bash
brew install git
```

**Linux:**
```bash
sudo apt-get install git
```

### Step 2.4: Configure Git

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

---

## Phase 3: Upload to GitHub (5-10 minutes)

### Step 3.1: Initialize Git Repository

```bash
cd path/to/office-calendar
git init
```

### Step 3.2: Add Remote Repository

```bash
git remote add origin https://github.com/YOUR_USERNAME/office-calendar.git
git branch -M main
```

Replace `YOUR_USERNAME` with your actual GitHub username!

### Step 3.3: Add All Files

```bash
git add .
```

### Step 3.4: Commit Files

```bash
git commit -m "Initial commit: Add Office Calendar PWA"
```

### Step 3.5: Push to GitHub

```bash
git push -u origin main
```

You may be asked to authenticate:
- Use your GitHub username and password (or personal access token)

### Step 3.6: Verify on GitHub

1. Go to your repo: `https://github.com/YOUR_USERNAME/office-calendar`
2. You should see all your files
3. Check that `index.html` is there

---

## Phase 4: Enable Hosting (5 minutes)

### Step 4.1: Enable GitHub Pages

1. Go to your repository
2. Click **Settings**
3. Scroll down to **Pages** section
4. Under "Source", select **main** branch
5. Click **Save**
6. Wait 1-2 minutes

### Step 4.2: Get Your Live URL

After waiting:
1. Scroll back to **Pages** section
2. You'll see: "Your site is published at: `https://USERNAME.github.io/office-calendar/`"
3. **This is your live app URL!**

### Step 4.3: Test Live App

1. Open the URL in your browser
2. Verify everything works
3. Test installation prompt

---

## Phase 5: Installation Tests (5-10 minutes)

### Test 5.1: Browser Desktop Install

**Chrome/Edge:**
1. Open your app URL
2. Look for install icon (looks like download arrow in address bar)
3. Click it
4. Choose "Install"
5. Check your desktop/apps

**Firefox:**
1. Right-click the app
2. Click "Install app"

**Safari (Mac):**
1. Click **File** → **Add to Dock**
2. App appears on dock

### Test 5.2: Mobile Phone Install

**Android (Chrome):**
1. Open your app URL on phone
2. Tap menu (three dots)
3. Tap "Install app"
4. Confirm
5. Check home screen

**iPhone (Safari):**
1. Open app in Safari
2. Tap Share button
3. Tap "Add to Home Screen"
4. Name it and tap "Add"
5. Check home screen

### Test 5.3: Offline Testing

1. Open DevTools (F12)
2. Go to **Application** tab
3. Find **Service Workers**
4. Check **Offline** checkbox
5. Try using the app
6. It should still work! ✅

---

## Phase 6: Customization (Optional)

### Customize 6.1: App Name

Edit `manifest.json`:
```json
{
  "name": "My Office Calendar",
  "short_name": "My Calendar",
  ...
}
```

### Customize 6.2: Colors

Edit `index.html` - Find these colors:
```css
/* Change these values */
background: #0f3460;        /* Background color */
#8b5cf6                     /* Purple accent */
#a78bfa                     /* Light purple */
```

### Customize 6.3: App Icon

Replace `icon.svg` with your own icon (must be SVG format)

---

## Phase 7: Share Your App (Done!)

### Share 7.1: Share the Link

Copy your app URL:
```
https://USERNAME.github.io/office-calendar/
```

Share it:
- Send via email
- Post on social media
- Add to portfolio
- Put in GitHub bio

### Share 7.2: Create QR Code

1. Go to [qr-code-generator.com](https://www.qr-code-generator.com)
2. Paste your app URL
3. Generate QR code
4. Share it (easier for mobile install)

### Share 7.3: Documentation

Share these files:
- README.md - Features and usage
- GITHUB_SETUP.md - GitHub instructions
- QUICKSTART.md - Quick start guide

---

## Troubleshooting Checklist

### App not loading
- [ ] All files in same folder
- [ ] Using HTTPS or localhost
- [ ] Check console for errors (F12)
- [ ] Try different browser

### Installation not working
- [ ] Using HTTPS (required for PWA)
- [ ] Service Worker registered (check console)
- [ ] manifest.json path correct in HTML
- [ ] Try after hard refresh (Ctrl+F5)

### Data not saving
- [ ] Localhost not HTTPS (OK)
- [ ] Not in private/incognito mode
- [ ] localStorage not disabled in browser
- [ ] Check browser settings

### GitHub Pages not showing
- [ ] Waited 1-2 minutes after enabling
- [ ] Pushed files with git push
- [ ] index.html is in main branch
- [ ] Settings → Pages shows correct source

---

## What's Next?

### Immediate (Done!)
- ✅ Local testing complete
- ✅ GitHub repository created
- ✅ App is live online
- ✅ Can be installed on devices

### Soon (Nice to have)
- [ ] Custom domain name
- [ ] Share with team/friends
- [ ] Gather feedback
- [ ] Bug fixes

### Future (Advanced)
- [ ] Add more features
- [ ] Sync across devices
- [ ] Export to PDF
- [ ] Mobile app version

---

## File Checklist

Before deploying, ensure you have:

- [ ] `index.html` - Main app
- [ ] `service-worker.js` - Offline support
- [ ] `manifest.json` - Installation config
- [ ] `icon.svg` - App icon
- [ ] `package.json` - Package config
- [ ] `.gitignore` - Git ignore rules
- [ ] `README.md` - Documentation
- [ ] `LICENSE` - MIT License

---

## Command Reference

### Local Testing:
```bash
cd office-calendar
python -m http.server 8000
# Then open: http://localhost:8000
```

### GitHub Upload:
```bash
git init
git remote add origin https://github.com/USERNAME/office-calendar.git
git branch -M main
git add .
git commit -m "Initial commit"
git push -u origin main
```

### Later Updates:
```bash
git add .
git commit -m "Your update message"
git push origin main
```

---

## Support Resources

- **README.md** - Full documentation
- **GITHUB_SETUP.md** - GitHub deployment
- **QUICKSTART.md** - Quick start
- **DEPLOYMENT.md** - Hosting options
- **FILELIST.md** - File descriptions

---

## Estimated Timeline

| Phase | Time | Status |
|-------|------|--------|
| 1. Local Testing | 5-10 min | ⏳ |
| 2. GitHub Setup | 10-15 min | ⏳ |
| 3. GitHub Upload | 5-10 min | ⏳ |
| 4. Enable Hosting | 5 min | ⏳ |
| 5. Installation Tests | 5-10 min | ⏳ |
| 6. Customization | 10-20 min | ✅ Optional |
| **Total** | **40-70 min** | 🎉 |

---

## Success Indicators

You're done when:
- ✅ App loads in browser
- ✅ Dark theme displays correctly
- ✅ Calendar functionality works
- ✅ Double-tap marks days
- ✅ Data saves locally
- ✅ Service worker active
- ✅ App is on GitHub
- ✅ GitHub Pages is live
- ✅ Can install on phone/desktop
- ✅ Installation prompt appears

---

## Congratulations! 🎉

You now have a working PWA!

- 📱 Installable on phones
- 🖥️ Installable on desktop
- 💻 Hosted on GitHub (free)
- 🌙 Beautiful dark theme
- 📊 Tracking office days
- 🔓 Open source (MIT license)
- 📖 Well documented

**Next:** Share your app with the world! 🚀

---

**Questions?** Check the relevant guide:
- Features → README.md
- GitHub → GITHUB_SETUP.md
- Quick start → QUICKSTART.md
- Deployment → DEPLOYMENT.md

**Happy coding! 📅✨**
