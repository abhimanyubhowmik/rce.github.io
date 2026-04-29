# Uncertainty-Aware Relative Compliance Estimation of Wind-Excited Plant from Monocular Video

**ICRA 2026 Workshop**  
Abhimanyu Bhowmik, Jan Behrens, Robert Babuška  
Czech Technical University in Prague · Delft University of Technology

🔗 **Live site:** https://abhimanyubhowmik.github.io/rce.github.io/  
📄 **Paper:** [`static/paper/ICRA26_Workshop.pdf`](static/paper/ICRA26_Workshop.pdf)

---

## View locally

### Option 1 — Python (no install needed)

```bash
cd rce-website
python3 -m http.server 8000
```

Then open **http://localhost:8000** in your browser.  
> Use a local server (not `file://`) so that videos and fonts load correctly.

### Option 2 — Node.js `serve`

```bash
npx serve .
```

### Option 3 — VS Code Live Server

Install the **Live Server** extension, right-click `index.html` → *Open with Live Server*.

---

## Edit the website

| What to change | File |
|---|---|
| Content, sections, text | `index.html` |
| Typography, colours, layout | `static/css/index.css` |
| Navbar burger JS | `static/js/index.js` |
| Videos | `static/videos/` |
| Images / plots | `static/images/` |
| Paper PDF | `static/paper/` |

---

## Deploy to GitHub Pages

### First-time setup

1. **Create the GitHub repository** (public):

   ```bash
   gh repo create abhimanyubhowmik/rce.github.io --public --source=. --remote=origin --push
   ```

   Or create it at https://github.com/new, then:

   ```bash
   git remote add origin git@github.com:abhimanyubhowmik/rce.github.io.git
   git push -u origin main
   ```

2. **Enable GitHub Pages** — go to  
   *Settings → Pages → Source → Deploy from branch → `main` / `/ (root)`*  
   and click **Save**.

   The site will be live at **https://abhimanyubhowmik.github.io/rce.github.io/** within ~1 minute.

   Or via CLI:
   ```bash
   gh api repos/abhimanyubhowmik/rce.github.io/pages \
     --method POST \
     -f source='{"branch":"main","path":"/"}'
   ```

### Push updates

```bash
git add -A
git commit -m "Update website"
git push origin main
```

GitHub Pages rebuilds automatically on every push to `main`.

---

## File structure

```
rce-website/
├── index.html              ← Main page
├── README.md
└── static/
    ├── css/
    │   └── index.css       ← Custom styles
    ├── js/
    │   └── index.js        ← Navbar JS
    ├── images/             ← Result plots and overlays
    ├── videos/             ← Demo videos (mp4)
    └── paper/              ← PDF of the paper
```

---

## Dependencies (all via CDN — no install required)

| Library | Purpose |
|---|---|
| [Bulma 0.9.4](https://bulma.io/) | Responsive CSS framework |
| [Font Awesome 6.4](https://fontawesome.com/) | Icons |
| [Academicons](https://jpswalsh.github.io/academicons/) | arXiv / paper icons |
| [jQuery 3.5.1](https://jquery.com/) | Navbar mobile toggle |
| Google Fonts | Google Sans, Noto Sans |
