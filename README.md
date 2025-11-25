# Generative Semantic Workspaces

**Project Website for AAAI 2026 Paper**

## Structured Episodic Memory for Next-Gen RAG

This is the official project website for our AAAI 2026 paper on Generative Semantic Workspaces (GSW), a neuro-inspired framework that builds structured, interpretable representations of evolving situations for episodic memory in Large Language Models.

### Key Highlights

- **State-of-the-art** F1-score of 0.850 on EpBench
- **20% improvement** in recall on complex queries
- **51% token reduction** compared to next-best baseline
- **Biologically-inspired** architecture (hippocampus + neocortex)

### Website Structure

```
gsw-episodic/
├── index.html              # Main project page
├── assets/
│   └── css/
│       └── style.css       # Styling
├── figures/                # Paper figures and diagrams
└── README.md              # This file
```

### Local Development

Simply open `index.html` in your browser to view the site locally.

### Deployment to GitHub Pages

1. Create a new repository on GitHub named `gsw-episodic` (or your preferred name)
2. Initialize git and push:

```bash
cd gsw-episodic
git init
git add .
git commit -m "Initial commit: GSW project website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/gsw-episodic.git
git push -u origin main
```

3. Enable GitHub Pages:
   - Go to repository Settings → Pages
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Save

Your site will be available at: `https://YOUR_USERNAME.github.io/gsw-episodic/`

### Updates

- **Paper**: ArXiv link to be added upon publication
- **Code**: Repository link to be added when ready for release

### Citation

```bibtex
@inproceedings{gsw2026,
  title={Generative Semantic Workspaces: Structured Episodic Memory for Next-Gen RAG},
  author={Anonymous},
  booktitle={Proceedings of the AAAI Conference on Artificial Intelligence},
  year={2026}
}
```

### License

MIT License - See repository for details
