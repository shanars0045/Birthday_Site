# Deploying Birthday Website to Vercel

## Step 1: Prepare Your Project
1. Create a folder for your project (if not already done):
   ```
   d:\Rohan\Intern\birthday-site\
   ├── birthday.html (rename from birthday.html to index.html)
   ├── Main.jpeg
   ├── Happy-Birthday.mp3
   ├── 20231103_142945.jpg
   ├── IMG-20231104-WA0084.jpg
   ├── IMG-20231104-WA0090.jpg
   ├── Snapchat-67298281.jpg
   └── WhatsApp Image*.jpeg (9, 10, 11, 12)
   ```

2. **Important**: Rename `birthday.html` to `index.html` so Vercel serves it as the main page.

## Step 2: Initialize Git Repository
```powershell
cd d:\Rohan\Intern\birthday-site
git init
git add .
git commit -m "Initial commit: Birthday website"
```

## Step 3: Create GitHub Repository
1. Go to https://github.com/new
2. Create a new repository (e.g., `birthday-website`)
3. Do NOT initialize with README
4. Copy the commands shown and run in PowerShell:
```powershell
git remote add origin https://github.com/YOUR-USERNAME/birthday-website.git
git branch -M main
git push -u origin main
```

## Step 4: Deploy on Vercel
### Option A: Via GitHub (Easiest)
1. Go to https://vercel.com
2. Click "Sign Up" → Choose "Continue with GitHub"
3. Authorize Vercel to access your GitHub
4. Click "New Project"
5. Select your `birthday-website` repository
6. Click "Import"
7. **Project Settings** (leave defaults, just click "Deploy")
8. Wait for deployment (usually 30 seconds)
9. Your site will be live at: `https://YOUR-PROJECT-NAME.vercel.app`

### Option B: Via Vercel CLI
1. Install Node.js from https://nodejs.org (if not installed)
2. Install Vercel CLI:
```powershell
npm install -g vercel
```

3. Deploy:
```powershell
cd d:\Rohan\Intern\birthday-site
vercel
```

4. Follow the prompts:
   - Link to existing project? → No
   - Set up and deploy? → Yes
   - Which scope? → Your personal account
   - Link to existing project? → No
   - Project name? → birthday-website
   - Directory? → ./ (current)
   - Override settings? → No

5. Your site will be deployed!

## Step 5: Custom Domain (Optional)
1. In Vercel dashboard, go to your project
2. Settings → Domains
3. Add your custom domain
4. Follow DNS configuration instructions

## Step 6: Updates & Redeployment
After making changes:
```powershell
git add .
git commit -m "Update: describe your changes"
git push origin main
```
Vercel automatically redeploys!

## Troubleshooting

### Images not loading?
- Ensure all image filenames match exactly (case-sensitive)
- Use relative paths: `Main.jpeg` not `./Main.jpeg`

### Audio not playing?
- Verify `Happy-Birthday.mp3` is in the same folder as `index.html`
- Check browser console (F12 → Console) for errors

### Site not updating?
- Clear browser cache (Ctrl+Shift+Delete)
- Wait 2-3 minutes for Vercel to rebuild
- Check deployment status in Vercel dashboard

## Access Your Live Site
- GitHub Pages: `https://YOUR-USERNAME.github.io/birthday-website/`
- Vercel: `https://YOUR-PROJECT-NAME.vercel.app/`

---

**Questions?** Check Vercel docs: https://vercel.com/docs
