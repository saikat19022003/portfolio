# Saikat Karmakar — Portfolio

A responsive, multi-page portfolio built with plain HTML, CSS, and vanilla JavaScript. It has no build step, server-side code, or package dependencies.

## Pages and assets

- `index.html` — Home
- `work.html` — Projects
- `about.html` — Profile and skills
- `education.html` — Education and certificates
- `resume.html` — Resume summary and PDF download
- `contact.html` — Contact details and profile links
- `styles.css`, `script.js` — Shared styling and interactions
- `assets/` — Resume PDF and portrait images (WebP with JPEG fallback)
- `.github/workflows/deploy.yml` — Automatic GitHub Pages deployment

All page, stylesheet, script, and asset links are relative, so the site works from a repository subpath as well as a custom domain.

## Preview locally

Open `index.html` in a browser, or run a local static server from this folder:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Publish with GitHub Pages

The included workflow publishes the repository root when a commit is pushed to `main`. For free GitHub Pages hosting, create an empty **public** repository first; the commands below assume the repository name is `portfolio` and the account is `saikat19022003`:

```powershell
cd D:\codex\saikat-portfolio
git init -b main
git add .
git commit -m "Add portfolio website"
git remote add origin https://github.com/saikat19022003/portfolio.git
git push -u origin main
```

Then, in the repository on GitHub, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions**. The workflow will deploy the site after the push. Check the **Actions** tab for a successful “Deploy Portfolio” run and the **Pages** settings for the published address.

For a repository named `portfolio`, the expected address is `https://saikat19022003.github.io/portfolio/`. If you instead name the repository `saikat19022003.github.io`, the expected address is `https://saikat19022003.github.io/`.

## Update the site later

Edit the relevant page or shared asset, then run:

```powershell
git add .
git commit -m "Update portfolio"
git push
```

GitHub Actions will publish the update automatically after the push to `main` completes successfully.
