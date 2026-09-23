# 📅 Office Calendar App

A beautiful, dark-themed calendar app to track your office days with double-tap marking and purple highlighting. Works offline, installable on phone and desktop!

## ✨ Features

- 🌙 **Dark Theme** - Beautiful dark UI with purple accents
- 📱 **PWA Ready** - Install as an app on your phone or desktop
- 🖱️ **Double-Tap Marking** - Double-click/tap any day to mark as office day
- 🏢 **Office Day Tracking** - See your office days with 🏢 emoji
- 💾 **Auto-Save** - Automatically saves to browser storage
- 📊 **Monthly Stats** - Track office days per month
- ⚡ **Offline Support** - Works completely offline with service worker
- 🎨 **Responsive Design** - Works on phone, tablet, and desktop

## 🚀 Quick Start

### Option 1: Use Directly
1. Download all files to a folder
2. Serve the folder using any HTTP server:
   ```bash
   # Using Python 3
   python -m http.server 8000
   
   # Using Node.js
   npx http-server
   
   # Using PHP
   php -S localhost:8000
   ```
3. Open `http://localhost:8000` in your browser

### Option 2: Desktop Installation
1. Open the app in your browser
2. Click the address bar menu (three dots)
3. Select **"Install app"** or **"Add to desktop"**
4. Choose your installation location

### Option 3: Mobile Installation

**iOS (iPhone/iPad):**
1. Open the app in Safari
2. Tap the Share button (box with arrow)
3. Tap **"Add to Home Screen"**
4. Name your shortcut and tap **"Add"**

**Android:**
1. Open the app in Chrome
2. Tap the menu (three dots)
3. Tap **"Install app"** or **"Add to Home Screen"**
4. Confirm installation

## 📁 File Structure

```
office-calendar/
├── index.html              # Main PWA app file
├── service-worker.js       # Service worker for offline support
├── manifest.json           # PWA manifest file
├── icon.svg               # App icon (SVG)
├── README.md              # This file
├── .gitignore             # Git ignore file
└── package.json           # Project metadata
```

## 🛠️ Development

### Requirements
- Node.js (optional, for development server)
- Modern web browser with PWA support

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/office-calendar.git
cd office-calendar

# Install dependencies (if using npm)
npm install

# Start development server
npm start
```

### Running Locally
```bash
# Using npm
npm run serve

# Using Python
python -m http.server 8000

# Using http-server (if installed)
http-server
```

Then open `http://localhost:8000` in your browser.

## 📦 PWA Features

This app is a Progressive Web App that includes:

- **Service Worker** - Offline functionality and caching
- **Web Manifest** - App installation and metadata
- **Responsive Design** - Works on all screen sizes
- **App Icons** - Multiple icon sizes for different platforms
- **Installable** - Can be installed like a native app

### Service Worker
The service worker caches all necessary files and allows the app to work offline. It will automatically update when you refresh the app.

## 🎨 Customization

### Change Colors
Edit the CSS color values in `index.html`:
- Primary Purple: `#8b5cf6`
- Background: `#0f3460`
- Text: `#e0d5ff`

### Change App Name
Update these files:
1. `manifest.json` - Change `name` and `short_name`
2. `index.html` - Change `<title>` tag
3. `index.html` - Change `apple-mobile-web-app-title`

### Add Custom Icon
Replace `icon.svg` with your own icon (SVG format recommended)

## 🔄 How It Works

### Marking Office Days
1. **Double-click** (desktop) or **double-tap** (mobile) any day
2. The day turns **purple** with a 🏢 emoji
3. Your selection is saved automatically to browser storage

### Data Storage
- All office days are stored in your browser's `localStorage`
- Data persists even after closing the app
- Clearing browser data will reset your calendar

## 📱 Browser Support

| Browser | Desktop | Mobile |
|---------|---------|--------|
| Chrome | ✅ | ✅ |
| Firefox | ✅ | ✅ |
| Safari | ✅ | ✅ |
| Edge | ✅ | ✅ |
| Opera | ✅ | ✅ |

## 🐛 Troubleshooting

### App Won't Install
- Make sure you're using HTTPS (required for PWA in production)
- Check if your browser supports PWA installation
- Clear browser cache and try again

### Service Worker Not Working
- Check browser console for errors (F12)
- Ensure `service-worker.js` is in the same folder as `index.html`
- Try clearing site data and refreshing

### Data Not Saving
- Make sure localStorage is enabled in your browser
- Check if private/incognito mode is disabled
- Try a different browser

## 📄 License

MIT License - Feel free to use this project for personal or commercial use.

## 🤝 Contributing

Contributions are welcome! Please feel free to:
- Report bugs
- Suggest features
- Submit pull requests
- Improve documentation

## 👨‍💻 Author

Created with ❤️ for tracking office days efficiently

## 📞 Support

If you encounter any issues or have questions:
1. Check the troubleshooting section
2. Open an issue on GitHub
3. Check browser console for error messages

## 🎯 Future Features

- [ ] Export calendar to PDF
- [ ] Share office schedule with team
- [ ] Multiple calendar views (week, year)
- [ ] Custom notifications
- [ ] Sync across devices
- [ ] Dark/Light theme toggle
- [ ] Multiple calendar support

---

**Happy tracking! 🏢📅**
