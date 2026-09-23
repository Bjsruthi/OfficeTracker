# 🚀 Deployment Guide

Deploy your Office Calendar app to multiple platforms - all free!

## 1. GitHub Pages (Recommended & Free)

### Easiest Method - Best for Beginners

**Pros:**
- ✅ Completely free
- ✅ Automatic HTTPS
- ✅ Easy updates via git push
- ✅ Custom domain option
- ✅ No build process needed

**Steps:**

1. Create GitHub repo (see GITHUB_SETUP.md)
2. Push files to main branch:
   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```
3. Go to repo **Settings** → **Pages**
4. Select **main** branch as source
5. Click **Save**
6. Wait 1-2 minutes
7. Your app is live at: `https://USERNAME.github.io/office-calendar/`

**Update manifest.json for GitHub Pages:**
```json
{
  "start_url": "/office-calendar/",
  ...
}
```

**Live in:** ~2 minutes | **Cost:** Free

---

## 2. Netlify (Free Tier)

### Easiest Visual Interface Method

**Pros:**
- ✅ Free tier very generous
- ✅ Automatic deployments
- ✅ Drag & drop upload
- ✅ Great UI
- ✅ Built-in analytics

**Steps:**

1. Go to [netlify.com](https://netlify.com)
2. Click **Sign up** with GitHub
3. Click **New site from Git**
4. Select your GitHub repo
5. Deploy settings:
   - Build command: Leave empty
   - Publish directory: `.` (root)
6. Click **Deploy site**
7. Your app is live at: `https://[random-name].netlify.app`

**Or drag & drop:**
1. Go to netlify.com
2. Drag folder into drop zone
3. Done! Live immediately

**Live in:** < 1 minute | **Cost:** Free (with upgrade options)

---

## 3. Vercel (Free Tier)

### Best Performance

**Pros:**
- ✅ Extremely fast
- ✅ Free tier great for static sites
- ✅ Automatic deployments
- ✅ Built-in CDN
- ✅ Analytics included

**Steps:**

1. Go to [vercel.com](https://vercel.com)
2. Click **Sign up** with GitHub
3. Click **Import Project**
4. Select your GitHub repo
5. Configure:
   - Framework: None (static)
   - Build command: Leave empty
6. Click **Deploy**
7. Your app is live at: `https://[app-name].vercel.app`

**Live in:** ~1 minute | **Cost:** Free

---

## 4. Firebase Hosting (Free Tier)

### Google's Hosting Solution

**Pros:**
- ✅ Free tier generous
- ✅ Google's infrastructure
- ✅ Custom domain easy
- ✅ Analytics included
- ✅ SSL automatic

**Requirements:**
- Node.js installed
- Google account

**Steps:**

```bash
# Install Firebase CLI
npm install -g firebase-tools

# Login to Firebase
firebase login

# Initialize Firebase project
firebase init hosting

# When prompted:
# - Public directory: . (current)
# - Single page app: No
# - Overwrite index.html: No

# Deploy
firebase deploy
```

**Live in:** ~2 minutes | **Cost:** Free

---

## 5. AWS S3 + CloudFront (Free Tier)

### Advanced but Powerful

**Pros:**
- ✅ AWS free tier available
- ✅ Extremely scalable
- ✅ Great for high traffic
- ✅ Advanced options

**Steps:**

1. Create AWS account
2. Go to S3 console
3. Create new bucket: `office-calendar-[random]`
4. Enable static website hosting
5. Upload all files to bucket
6. Set bucket policy for public access
7. Use CloudFront for CDN
8. (Optional) Add custom domain

**Live in:** ~5 minutes | **Cost:** Free tier or minimal

---

## 6. Surge (Free & Simple)

### Quick & Minimal Setup

**Pros:**
- ✅ Super simple
- ✅ One command deploy
- ✅ Free tier good enough
- ✅ Fast and reliable

**Steps:**

```bash
# Install Surge globally (one-time)
npm install -g surge

# Deploy from your folder
surge

# Follow prompts
# - Enter email
# - Enter password
# - Confirm project path
# - Choose subdomain
```

**Live in:** < 1 minute | **Cost:** Free

---

## 7. Self-Hosted (Advanced)

### For VPS or Dedicated Server

**Pros:**
- ✅ Complete control
- ✅ No platform restrictions
- ✅ Can add backend

**Options:**
- DigitalOcean - $5/month
- Linode - $5/month
- Heroku - Free tier removed (paid)
- Vultr - $2.50/month

**Basic Setup:**

```bash
# SSH into your server
ssh user@your-server.com

# Clone your repo
git clone https://github.com/YOU/office-calendar.git

# Start web server
cd office-calendar
python -m http.server 80
```

Or use Nginx/Apache for production.

---

## Comparison Table

| Platform | Free | Setup Time | Performance | Ease | SSL |
|----------|------|-----------|-------------|------|-----|
| GitHub Pages | ✅ | 2 min | Great | Easy | ✅ |
| Netlify | ✅ | 1 min | Excellent | Easy | ✅ |
| Vercel | ✅ | 1 min | Excellent | Easy | ✅ |
| Firebase | ✅ | 3 min | Great | Medium | ✅ |
| AWS S3 | ~Free | 5 min | Good | Hard | ⚠️ |
| Surge | ✅ | <1 min | Good | Very Easy | ✅ |
| Self-Hosted | ⚠️ | 10 min | Variable | Hard | ⚠️ |

---

## Recommended for Different Users

### Beginners
→ **Netlify** or **Surge**
- Simplest to use
- Best UI
- Drag & drop option

### Developers
→ **GitHub Pages** or **Vercel**
- Git-based workflow
- Good performance
- Free and fast

### Advanced Users
→ **Firebase** or **Self-Hosted**
- More control
- Additional features
- Better scalability

---

## Custom Domain Setup

### Connect Your Own Domain

**On Netlify:**
1. Go to Domain settings
2. Add your custom domain
3. Update DNS records (provided)
4. Done!

**On GitHub Pages:**
1. Add to repo settings
2. Add CNAME file in repo:
   ```
   yourdomain.com
   ```
3. Update DNS records with your registrar

**On Vercel:**
1. Add in project settings
2. Update DNS records
3. Automatic SSL certificate

---

## Post-Deployment Checklist

After deployment, verify:

- ✅ App loads correctly
- ✅ Calendar displays
- ✅ Double-tap/click works
- ✅ Office days save
- ✅ Installation prompt appears
- ✅ Offline mode works
- ✅ Mobile responsive
- ✅ HTTPS enabled
- ✅ Icons display

### Test Installation:
```
1. Open app URL
2. Look for "Install" button
3. Click to install
4. Verify on home screen
```

---

## Troubleshooting Deployments

### "HTTPS not working"
- Use Netlify, Vercel, or GitHub Pages (auto HTTPS)
- Contact platform support for custom domains

### "PWA features not working"
- Ensure HTTPS is enabled
- Check service worker registration
- Clear cache and reload

### "App not loading"
- Check all file paths are correct
- Verify index.html exists
- Check manifest.json path in index.html

### "Updates not showing"
- GitHub Pages: Wait 1-2 minutes
- Netlify: Manual redeploy or reconnect
- Vercel: Rebuild from settings

---

## Environment Variables (If Needed)

### For future features with backend:

**Netlify:**
```
Site settings → Build & deploy → Environment
Add variables there
```

**Vercel:**
```
Settings → Environment Variables
Add for different environments
```

---

## Monitoring & Analytics

### GitHub Pages
- Go to Settings → Pages
- See traffic stats

### Netlify
- Dashboard shows analytics
- Bandwidth, visitors, errors

### Vercel
- Built-in analytics
- Performance metrics

---

## Cost Summary

| Scenario | Platform | Monthly Cost |
|----------|----------|--------------|
| Just starting | Netlify | $0 |
| Production | Vercel | $0-20 |
| Scale needed | Firebase | $0-50+ |
| Maximum control | Self-hosted | $5-50+ |

---

## Next Steps After Deployment

1. **Test thoroughly** - Across devices
2. **Share link** - With friends/family
3. **Monitor performance** - Use platform analytics
4. **Get feedback** - Create GitHub issues
5. **Plan features** - What to add next

---

## Security Notes

✅ **Do:**
- Always use HTTPS (all platforms do)
- Keep dependencies updated
- Regularly backup your repo
- Monitor error logs

❌ **Don't:**
- Commit API keys to repo
- Use outdated dependencies
- Share deploy credentials
- Disable HTTPS

---

**Ready to deploy? Choose a platform and go live! 🚀**

Questions? Check README.md or create an issue on GitHub.
