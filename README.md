# Kongkun Chen Personal Website

This repository contains a static GitHub Pages portfolio for Kongkun Chen, a new graduate seeking full-time Machine Learning Engineer, Data Scientist, and Applied ML roles.

The site highlights applied deep learning, scientific computing, CISESS / ESSIC research experience, and the Microwave Super-Resolution Model (MW-SR) project. It uses only HTML, CSS, and a small amount of vanilla JavaScript.

## Website Structure

```text
.
├── index.html
├── projects.html
├── research.html
├── resume.html
├── projects/
│   └── mw-sr.html
├── assets/
│   ├── css/
│   │   └── styles.css
│   ├── js/
│   │   └── main.js
│   ├── images/
│   │   └── mw-sr/
│   └── files/
├── .gitignore
├── .nojekyll
└── README.md
```

## Preview Locally

From the repository root, run:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Publish with GitHub Pages

1. Create or select the GitHub repository that will host the site.
2. Put the website files in the repository root.
3. Commit and push the `main` branch.
4. In GitHub, open **Settings > Pages**.
5. Select **Deploy from a branch**, then choose `main` and `/root`.

For a personal site at `https://USERNAME.github.io`, name the repository `USERNAME.github.io`.

## Edit These First

Search the HTML files for `TODO` and replace these placeholders:

- Email address
- GitHub username and profile URL
- LinkedIn profile URL
- Exact degree, major, graduation date, and optional GPA/honors
- CISESS / ESSIC role title and dates
- PDF resume path
- Project repository link
- Paper draft link
- Final metric table and confirmed experiment results
- Trained-weights link, only if hosted externally
- Exact compiler and data science project names and links

Add the final PDF resume to `assets/files/`, then update the download link in `resume.html`.

## Selected Project Figures

The website includes only three representative, web-sized project figures:

- Per-scene model metric distributions
- Radially averaged PSD comparison
- A representative BT reconstruction and residual inspection view

The full experiment output tree is intentionally excluded.

## Do Not Commit

Do not add raw HDF5 datasets, model weights, checkpoints, cached predictions, logs, virtual environments, or large experiment output folders. The `.gitignore` blocks common forms of these files, but review `git status` before every commit.

Useful checks:

```bash
git status --short
git ls-files | grep -E '\.(h5|hdf5|keras|npz|npy|ckpt)$'
```

## Commit When Ready

```bash
git status
git add .
git status --short
git commit -m "Build machine learning portfolio website"
git push origin main
```

No push is performed automatically by this project.
