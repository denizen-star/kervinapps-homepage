# KervinApps Homepage - Deployment Guide

## 📦 Backup Created
**Location:** `/Users/kervinleacock/Documents/Development/kervinapps-backup-20251011-191506.tar.gz`
**Date:** October 11, 2025
**Size:** ~30KB

To restore from backup:
```bash
cd /Users/kervinleacock/Documents/Development
tar -xzf kervinapps-backup-20251011-191506.tar.gz -C KervinApps-restored/
```

## 🗂️ Current File Structure

```
/KervinApps/
├── index.html                          # Main homepage (Dark Nordic Fusion)
├── pathfinders.html                    # Pathfinders Learn More
├── optimizer.html                      # Optimizer Learn More
├── toronto-guide.html                  # Toronto Guide Learn More
├── community-builder.html              # Community Builder Learn More
├── financial-planner.html              # Financial Planner Learn More
├── job-hunting.html                    # Job Hunting Follow-ups Learn More
└── scheduling-gay-run-club.html        # Scheduling Gay Run Club Learn More
```

## 🚀 Deployment Steps to kervinapps.com

### Option 1: Netlify Deployment (Recommended)

1. **Initialize Git Repository** (if not already done):
   ```bash
   cd /Users/kervinleacock/Documents/Development/KervinApps
   git init
   git add .
   git commit -m "Initial commit: Dark Nordic Fusion homepage"
   ```

2. **Push to GitHub:**
   ```bash
   # Create a new repo on GitHub called "kervinapps-homepage"
   git remote add origin git@github.com:denizen-start/kervinapps-homepage.git
   git branch -M main
   git push -u origin main
   ```

3. **Deploy to Netlify:**
   - Go to https://app.netlify.com
   - Click "Add new site" → "Import an existing project"
   - Choose GitHub and select `kervinapps-homepage` repository
   - Build settings:
     - Build command: (leave empty - it's just HTML)
     - Publish directory: `/`
   - Click "Deploy site"

4. **Configure Custom Domain:**
   - In Netlify: Site settings → Domain management
   - Add custom domain: `kervinapps.com`
   - Follow DNS configuration instructions
   - Netlify will automatically provide HTTPS

### Option 2: Manual Deployment

If you have FTP/SFTP access to kervinapps.com:
1. Upload all `.html` files to your web server's root directory
2. Ensure `index.html` is set as the default page
3. Configure HTTPS if not already enabled

## 🔗 Subdomain Preservation

Your existing subdomains will remain intact:
- ✅ pathfinders.kervinapps.com
- ✅ optimizer.kervinapps.com
- ✅ to-guide.kervinapps.com
- ✅ sxp.kervinapps.com

These are separate deployments and won't be affected by the main site update.

## ✨ What's Deployed

### Main Homepage Features:
- Dark Nordic Fusion design
- 12 slow-moving animated background shapes
- Glassmorphic cards with frosted glass effect
- 4 categories: Networking, Lifestyle, Productivity, Planning
- 7 applications showcased
- Responsive design
- Dark mode by default

### Learn More Pages:
- Individual detailed pages for each app
- Same Dark Nordic Fusion styling
- No emojis (professional look)
- Animated background shapes
- Glassmorphic cards

## 🎨 Design Details

**Color Palette:**
- Background: #1a1d23 (dark blue-gray)
- Cards: rgba(36, 41, 49, 0.6) with 20px blur
- Text: #e4e6eb (light gray)
- Shapes: Various grays (#6b7a8f, #7a8a9f, #5a6a7f, #8a9aaf)
- Borders: rgba(255, 255, 255, 0.1)

**Animations:**
- Shape movement: 25-36 second cycles
- Card hover: Subtle lift and glow
- Tab transitions: Smooth fade
- All animations are GPU-accelerated

## 📊 Performance

- No external dependencies (uses Tailwind CDN)
- Lightweight: ~50KB total (all HTML files)
- Fast load times
- Mobile-optimized
- SEO-friendly static HTML

## 🔧 Maintenance

To update content:
1. Edit the relevant `.html` file
2. Test locally: `python3 -m http.server 3509`
3. Commit changes: `git add . && git commit -m "Update: description"`
4. Push: `git push`
5. Netlify will auto-deploy (if using Netlify)

## 📞 Support

If you need to make changes:
- Edit HTML files directly (they're well-commented)
- Colors, animations, and content are all in the `<style>` tags
- All glassmorphic effects use `backdrop-filter: blur()`
- Shape positions can be adjusted in the CSS

---

**Last Updated:** October 11, 2025
**Design:** Dark Nordic Fusion
**Status:** Ready for deployment

