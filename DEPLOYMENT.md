# Deployment Guide for GSW Project Website

## Quick Start: GitHub Pages Deployment

### Step 1: Create GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
   - Name: `gsw-episodic` (or your preferred name)
   - Visibility: Public (required for free GitHub Pages)
   - Do NOT initialize with README (we already have one)

### Step 2: Push to GitHub

```bash
cd /home/shreyas/NLP/SM/gensemworkspaces/gsw-episodic

# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: GSW AAAI 2026 project website"

# Add remote (replace YOUR_USERNAME with your GitHub username)
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gsw-episodic.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** (top menu)
3. Click **Pages** (left sidebar)
4. Under "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: `main`
   - **Folder**: `/ (root)`
5. Click **Save**

### Step 4: Access Your Site

After a few minutes, your site will be live at:
```
https://YOUR_USERNAME.github.io/gsw-episodic/
```

## Optional: Custom Domain

If you want to use a custom domain (e.g., `gsw-memory.com`):

1. Buy a domain from a registrar (Namecheap, Google Domains, etc.)
2. Create a file named `CNAME` in the root directory with your domain:
   ```
   gsw-memory.com
   ```
3. Configure DNS at your registrar:
   - Add an A record pointing to GitHub's IPs:
     - 185.199.108.153
     - 185.199.109.153
     - 185.199.110.153
     - 185.199.111.153
   - Or add a CNAME record for `www` pointing to `YOUR_USERNAME.github.io`

## Updates and Maintenance

### Updating the Website

After making changes:

```bash
git add .
git commit -m "Update: description of changes"
git push
```

GitHub Pages will automatically rebuild and deploy.

### Before Full Release

Remember to update:

1. **ArXiv Link**: Replace placeholder in `index.html`
   ```html
   <a href="https://arxiv.org/abs/XXXX.XXXXX" class="btn">Paper</a>
   ```

2. **Code Repository**: Add link when code is released
   ```html
   <a href="https://github.com/YOUR_USERNAME/gsw-memory" class="btn">Code</a>
   ```

3. **Authors**: Replace "Anonymous" with actual authors in:
   - Citation section
   - BibTeX
   - Meta tags (if you add them)

### Adding Google Analytics (Optional)

If you want to track visitors:

1. Create a Google Analytics account
2. Get your tracking ID
3. Add before `</head>` in `index.html`:
   ```html
   <!-- Google Analytics -->
   <script async src="https://www.googletagmanager.com/gtag/js?id=YOUR_TRACKING_ID"></script>
   <script>
     window.dataLayer = window.dataLayer || [];
     function gtag(){dataLayer.push(arguments);}
     gtag('js', new Date());
     gtag('config', 'YOUR_TRACKING_ID');
   </script>
   ```

## Troubleshooting

### Site Not Loading?
- Wait 5-10 minutes after enabling Pages
- Check Settings → Pages for error messages
- Verify `index.html` is in the root directory

### Images Not Showing?
- Check that image paths are relative (e.g., `figures/main.png`)
- Verify all images are in the `figures/` directory
- Check file extensions match (case-sensitive on Linux)

### Need Help?
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [GitHub Pages Troubleshooting](https://docs.github.com/en/pages/getting-started-with-github-pages/troubleshooting-404-errors-for-github-pages-sites)
