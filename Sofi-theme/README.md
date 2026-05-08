# Sofiś Portfolio — Hugo Site

## Quick start

```bash
# Install Hugo (macOS)
brew install hugo

# Install Hugo (Windows)
winget install Hugo.Hugo.Extended

# Run locally
hugo server -D
# → open http://localhost:1313
```

## Adding a new piece of work

```bash
hugo new work/my-painting-title.md
```

Then open the file in `content/work/` and fill in the frontmatter:

```yaml
title: "My painting title"
image: "https://res.cloudinary.com/your-account/image/upload/yourimage.jpg"
medium: "Gouache on paper"
year: "2025"
size: "A4"
available: true
```

Write a description below the `---` line.

## Changing colours / fonts

Open `themes/elara/static/css/style.css` — all colours are CSS variables at the top:

```css
:root {
  --cream:           #F5EFE4;
  --terracotta:      #C4705A;
  --rose:            #D4A5A0;
  /* etc. */
}
```

## Changing site-wide text

Open `hugo.toml` — the `[params]` section controls the hero headline, tagline, about blurb, and contact email.

## Contact form

The contact form uses [Formspree](https://formspree.io) (free tier is plenty for a portfolio).
1. Sign up at formspree.io
2. Create a form, copy your form ID
3. Open `themes/elara/layouts/contact/single.html`
4. Replace `YOUR_FORM_ID` with your actual ID

## Deploying

Push to `main` — GitHub Actions builds and deploys automatically.
Make sure GitHub Pages is set to deploy from **GitHub Actions** (not a branch) in your repo settings.
