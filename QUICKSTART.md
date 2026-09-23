# 🏃 Quick Start Guide

Get the Office Calendar running on your machine in minutes!

## Prerequisites

You only need a **web browser** - no installation required!

Optional: Node.js (for convenient local server)

## Option 1: Run Immediately (Easiest)

### On Windows:
1. Download all files to a folder
2. Open Command Prompt in that folder
3. Run:
```cmd
cd path\to\office-calendar
python -m http.server 8000
```
4. Open `http://localhost:8000` in your browser

### On Mac/Linux:
```bash
cd path/to/office-calendar
python3 -m http.server 8000
```
4. Open `http://localhost:8000` in your browser

## Option 2: Using Node.js

```bash
# Install http-server globally (one-time)
npm install -g http-server

# Run from your app folder
cd path/to/office-calendar
http-server -p 8000
```

Open `http://localhost:8000`

## Option 3: Using Python (Recommended for Beginners)

Python is often pre-installed on Mac/Linux.

### Check if Python is installed:
```bash
python --version
# or
python3 --version
```

### Run the server:
```bash
cd path/to/office-calendar
python -m http.server 8000
```

## Option 4: Using PHP

If you have PHP installed:

```bash
cd path/to/office-calendar
php -S localhost:8000
```

## After Starting Server

1. Open your browser
2. Go to: `http://localhost:8000`
3. The app should load with the dark theme

## Testing PWA Features

### Test Offline Mode:
1. Open DevTools (F12)
2. Go to **Application** tab
3. Check **Service Workers**
4. Click **Offline** checkbox
5. The app should still work!

### Test Installation:
1. Look for **Install** button in address bar
2. Or right-click → "Install app"
3. Follow prompts to install

### Test Local Storage:
1. Open DevTools (F12)
2. Go to **Application** → **Local Storage**
3. Mark some office days
4. Your data is persisted under key: `officeDays`

## File Structure Explanation

```
office-calendar/
├── index.html              # Main PWA file (load this in browser)
├── service-worker.js       # Makes app work offline
├── manifest.json           # Installation info
├── icon.svg               # App icon
├── package.json           # NPM config
├── README.md              # Documentation
└── GITHUB_SETUP.md        # GitHub instructions
```

## Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Hard Refresh | Ctrl+F5 (Windows) or Cmd+Shift+R (Mac) |
| DevTools | F12 |
| Toggle Dark Mode | Browser settings |
| Clear Cache | Ctrl+Shift+Del (Windows) or Cmd+Shift+Del (Mac) |

## Common Issues

### "Port already in use"
Change port number:
```bash
python -m http.server 8001  # Use 8001 instead
```

### "Service Worker not working"
- Use HTTP (localhost) - localhost doesn't need HTTPS
- Check DevTools Console (F12) for errors
- Try incognito mode to bypass cache issues

### "App not loading"
- Ensure you're in the correct folder
- Check that `index.html` exists
- Make sure all files are in same folder
- Try different port: 8001, 8002, etc.

## Next Steps

1. ✅ Run the app locally
2. ✅ Test marking office days
3. ✅ Test offline mode
4. ✅ Try installing as app
5. ✅ Follow GITHUB_SETUP.md to upload to GitHub

## Need Help?

1. Check README.md for features and troubleshooting
2. Check GITHUB_SETUP.md for deployment
3. Look at browser console (F12) for errors
4. Try a different browser

---

**Happy tracking! 🏢📅**
