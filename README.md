# DreamWorks Animation Website

A static website showcasing DreamWorks Animation content.

## Deployment to GitHub Pages

### Steps to Deploy:

1. **Push your code to GitHub** (if not already done)
   ```bash
   git add .
   git commit -m "Fix paths for GitHub Pages"
   git push origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Click on **Settings**
   - Scroll down to **Pages** section
   - Under **Source**, select **Deploy from a branch**
   - Choose **main** branch (or your default branch)
   - Select **/ (root)** folder
   - Click **Save**

3. **Wait for deployment:**
   - GitHub will build and deploy your site
   - Your site will be available at: `https://[your-username].github.io/[repository-name]/`
   - If your repository is named `[username].github.io`, it will be at: `https://[username].github.io/`

### Important Notes:

- The `index.html` file is now at the root of the repository (required for GitHub Pages)
- All paths have been converted to relative paths to work with GitHub Pages
- The `.nojekyll` file prevents Jekyll processing (not needed for static HTML sites)

### Troubleshooting:

If you see a 404 error:
1. Make sure `index.html` is in the root directory
2. Check that GitHub Pages is enabled in repository settings
3. Wait a few minutes for the deployment to complete
4. Clear your browser cache and try again
5. Check the repository's **Actions** tab for any deployment errors

## Local Development

To run locally:
1. Install dependencies: `npm install`
2. Run Tailwind CSS watch: `npm run dev`
3. Open `index.html` in your browser
