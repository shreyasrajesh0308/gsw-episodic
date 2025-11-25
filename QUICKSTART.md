# GSW Website Quick Start

## What You Have

✅ Complete project website for your AAAI 2026 paper
✅ Minimal academic design (distill.pub inspired)
✅ All key results and tables included
✅ Figures from your paper
✅ Ready for GitHub Pages deployment

## Directory Structure

```
gsw-episodic/
├── index.html              # Main website
├── assets/
│   └── css/
│       └── style.css       # Styling
├── figures/                # Paper figures (PNG)
│   ├── main.png           # Main architecture diagram
│   ├── overview3.png      # QA pipeline
│   └── ...                # Other figures
├── README.md              # Project README
├── DEPLOYMENT.md          # Detailed deployment guide
└── QUICKSTART.md          # This file
```

## Deploy in 3 Steps

### 1. Create GitHub Repo
```bash
# On GitHub: Create new repository "gsw-episodic" (public)
```

### 2. Push Code
```bash
cd /home/shreyas/NLP/SM/gensemworkspaces/gsw-episodic
git init
git add .
git commit -m "Initial commit: GSW project website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gsw-episodic.git
git push -u origin main
```

### 3. Enable GitHub Pages
- Go to repo Settings → Pages
- Source: Branch `main`, Folder `/ (root)`
- Save

**Your site will be live at:** `https://YOUR_USERNAME.github.io/gsw-episodic/`

## Before Going Live

Update these in `index.html`:

1. **ArXiv link** (line ~26):
   ```html
   <a href="https://arxiv.org/abs/YOUR_ARXIV_ID">Paper</a>
   ```

2. **Authors** (when de-anonymizing):
   - Replace "Anonymous" in citation section
   - Update BibTeX

3. **Code link** (when ready):
   ```html
   <a href="https://github.com/YOUR_USERNAME/gsw-memory">Code</a>
   ```

## Local Preview

```bash
# Option 1: Direct open
open index.html  # macOS
xdg-open index.html  # Linux

# Option 2: Local server (better)
python3 -m http.server 8000
# Then visit: http://localhost:8000
```

## What's Included

### Content
- ✅ Abstract and motivation
- ✅ Architecture overview
- ✅ Key results (F1: 0.850, 20% recall improvement, 51% token reduction)
- ✅ Performance tables by query complexity
- ✅ Token efficiency comparison
- ✅ How It Works section (Operator + Reconciler)
- ✅ BibTeX citation

### Design
- ✅ Clean, minimal academic style
- ✅ Responsive (mobile-friendly)
- ✅ Professional typography
- ✅ Highlighted metrics
- ✅ Properly formatted tables
- ✅ Figure captions

## Customization

### Colors
Edit `assets/css/style.css` (lines 9-15):
```css
:root {
    --primary-color: #2c3e50;    /* Headings */
    --accent-color: #3498db;     /* Buttons, highlights */
    /* ... */
}
```

### Adding Sections
Add after any `</section>` tag in `index.html`:
```html
<section id="new-section">
    <h3>New Section Title</h3>
    <p>Content here...</p>
</section>
```

## Support

- **Full deployment guide**: See [DEPLOYMENT.md](DEPLOYMENT.md)
- **GitHub Pages docs**: https://docs.github.com/en/pages
- **Issues**: Create a ticket in your repo

## Next Steps

1. ✅ Deploy to GitHub Pages
2. ⏳ Add ArXiv link when paper is published
3. ⏳ Add code repository link when ready
4. ⏳ Share on Twitter/LinkedIn
5. ⏳ Update with authors when de-anonymized

---

**Note**: Keep the code private in `gsw-memory/` until your second paper is ready. The website can be public now as it only contains the AAAI paper content.
