# Luis Juarez — Personal Portfolio

A responsive personal portfolio for **Luis Juarez Corral**, a Computer Science student at The University of Texas at El Paso. Built with **HTML and CSS only** and ready for GitHub Pages.

The design uses a warm cream background, forest green typography, lime accents, custom SVG/CSS project illustrations, and a responsive layout. There is no JavaScript, build step, package installation, or API key.

## What's included

- Introduction and internship availability
- Three projects: Wayve, a character-level language model, and AI Dyno Finance
- Expandable project details using native HTML `<details>` elements
- UTEP technology support experience
- Education, skills, and student leadership
- Email, LinkedIn, GitHub, and résumé links
- Keyboard focus styles, a skip link, and reduced-motion support
- Locally hosted fonts, so the design does not depend on a font CDN

## Files in the downloadable package

| File | Purpose |
| --- | --- |
| `index.html` | All portfolio content, navigation, and SVG illustrations |
| `index.css` | Colors, typography, spacing, layout, and responsive rules |
| `assets/Luis-Juarez-Resume.pdf` | Downloadable résumé |
| `assets/favicon.svg` | Browser tab icon |
| `assets/portfolio-sans.woff` | Noto Sans regular font |
| `assets/portfolio-sans-bold.woff` | Noto Sans bold font, used for emphasized text |
| `assets/FONT-LICENSE.txt` | Font attribution and license |
| `.nojekyll` | Keeps GitHub Pages from applying Jekyll processing |

The hosted development checkout keeps the website inside `dist/`. The downloadable package puts `index.html`, `index.css`, and `assets/` at its root so it can directly replace your current GitHub Pages files.

## Preview locally

Unzip the package and open `index.html` in your browser. All site assets use relative paths, so the page also works inside a GitHub Pages project folder such as `/MyPortfolio2/`.

For a local server, open a terminal in the extracted folder and run:

```bash
python3 -m http.server 8000
```

On Windows, if `python3` is unavailable:

```powershell
py -m http.server 8000
```

Then open `http://localhost:8000`.

## Update your existing GitHub Pages portfolio

Your repository is `EmmanuelJuarez2811/MyPortfolio2`.

1. Unzip the package.
2. Open your `MyPortfolio2` repository on GitHub.
3. Choose **Add file → Upload files**.
4. Upload `index.html`, `index.css`, `README.md`, `.nojekyll`, and the entire `assets` folder to the repository root. Replace the existing `index.html` and `index.css`.
5. Commit the changes.
6. In **Settings → Pages**, confirm the publishing source is **Deploy from a branch** and select the branch containing those files, with **/(root)** as its folder. If Pages already uses a workflow, retain that workflow and ensure it publishes these root files.
7. Wait for the GitHub Pages deployment to finish, then open your existing portfolio URL:

   https://emmanueljuarez2811.github.io/MyPortfolio2/

If hidden files are omitted by your file picker, add `.nojekyll` through GitHub's **Add file → Create new file** option. The page contains no Jekyll-specific files, so the portfolio also works without it.

### Using Git instead

If you already have a local checkout, copy the extracted files into it, then run:

```bash
git add index.html index.css README.md assets .nojekyll
git commit -m "Redesign portfolio with resume projects and experience"
git push
```

The source package does not update your GitHub repository automatically. The separately hosted preview is independent of GitHub Pages.

## Customize it

### Change the content

Edit `index.html`. Main section anchors are:

| Anchor | Section |
| --- | --- |
| `#home` | Introduction |
| `#projects` | Selected work |
| `#experience` | Work experience |
| `#about` | Background, skills, and leadership |
| `#contact` | Contact links |

Your existing `#experience` link remains supported. The old template's empty Certificates section has been replaced with verified education and leadership content.

To add a project, duplicate an `<article class="project project-small">` inside `.project-grid`, then edit its title, description, tags, and `<details>` content. Project-specific repository links were not guessed; add them when you have the correct URLs.

### Change colors

Edit the variables at the top of `index.css`:

```css
:root {
  --paper: #f5f4ec;
  --ink: #173d30;
  --muted: #646b60;
  --line: #dcded2;
  --lime: #d4ed8b;
  --white: #fffef8;
}
```

### Update the résumé or contact details

Replace `assets/Luis-Juarez-Resume.pdf` with your updated PDF using the same filename. If you rename it, update every résumé link in `index.html`.

Search `index.html` for these values when changing your contact details:

- `lejuarezcorral@miners.utep.edu`
- `https://linkedin.com/in/eljuarez`
- `https://github.com/EmmanuelJuarez2811`

The email buttons open the visitor's email application. They are not a contact form and do not send messages automatically.

## Content and illustrations

The main factual source is `Luis_Juarez_Resume_1E26.pdf`. The additional résumé, `Resume_Luis_Juarez_3Q26.pdf`, was reviewed for context; speculative outcomes and unsupported performance claims from that version were not added to the site.

Project visuals are original SVG/CSS illustrations, not screenshots of the actual applications. The project details distinguish the Wayve prototype, model training results, and small Dyno learning evaluation from broader claims. The illustrative model code is a visual explanation, not runnable Python.

## Fonts and ownership

Noto Sans is included under the SIL Open Font License; see `assets/FONT-LICENSE.txt`. Georgia and system serif fonts are used for italic headlines. The portfolio does not redistribute Georgia.

Personal information, project descriptions, and the résumé belong to Luis Juarez Corral. No open-source license is assigned to those materials by this package.

## Quick check after editing

- Open the site on a phone and on a desktop.
- Check the navigation and each expandable project section.
- Download the résumé and confirm it is the intended version.
- Check your email, GitHub, and LinkedIn links.
- Use Tab and Enter to move through the page with the keyboard.
