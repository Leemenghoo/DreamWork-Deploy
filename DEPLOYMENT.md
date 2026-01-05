# GitHub Pages Deployment Guide

## What Was Fixed

1. ✅ Created `index.html` at the root directory (GitHub Pages requires this)
2. ✅ Fixed all absolute paths (`/img/...`, `/src/...`) to relative paths (`img/...`, `src/...`)
3. ✅ Created `.nojekyll` file to prevent Jekyll processing
4. ✅ Updated CSS and JavaScript paths to work from root

## Next Steps to Deploy

### 1. Commit and Push Changes

```bash
git add .
git commit -m "Fix paths for GitHub Pages deployment"
git push origin main
```

### 2. Enable GitHub Pages

1. Go to your GitHub repository
2. Click **Settings** (top menu)
3. Scroll down to **Pages** (left sidebar)
4. Under **Source**, select:
   - **Deploy from a branch**
   - Branch: **main** (or your default branch)
   - Folder: **/ (root)**
5. Click **Save**

### 3. Wait for Deployment

- GitHub will build your site (usually takes 1-2 minutes)
- You'll see a green checkmark when deployment is complete
- Your site URL will be shown in the Pages settings

### 4. Access Your Site

Your site will be available at:
- `https://[your-username].github.io/[repository-name]/`

**Note:** If your repository is named `[username].github.io`, your site will be at:
- `https://[username].github.io/`

## Troubleshooting

### Still seeing 404?

1. **Check the repository name:**
   - If it's not `[username].github.io`, your site is at `https://[username].github.io/[repo-name]/`
   - Make sure you're using the correct URL

2. **Verify files are committed:**
   - Make sure `index.html` is in the root directory
   - Check that all files are pushed to GitHub

3. **Clear browser cache:**
   - Hard refresh: `Ctrl+Shift+R` (Windows/Linux) or `Cmd+Shift+R` (Mac)

4. **Check GitHub Actions:**
   - Go to the **Actions** tab in your repository
   - Look for any deployment errors

5. **Wait a bit longer:**
   - Sometimes it takes 5-10 minutes for changes to propagate

## File Structure

```
generont-project/
├── index.html          ← Main entry point (at root)
├── .nojekyll          ← Prevents Jekyll processing
├── dist/
│   └── output.css
├── img/               ← All images
├── src/
│   ├── css/
│   ├── javascript/
│   ├── movie/
│   ├── tv/
│   └── ...
└── README.md
```

## Important Notes

- All paths are now relative, so the site works whether deployed to root or a subdirectory
- The `.nojekyll` file ensures GitHub doesn't try to process your HTML files with Jekyll
- Make sure your repository is **public** (or you have GitHub Pro for private repos with Pages)
