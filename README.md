# Hoggard Student Council Website

Plain HTML/CSS static site — no build step, no dependencies. Six pages, all
sharing `assets/styles.css`:

- `index.html` — Home
- `activities.html` — Activities
- `classes-seniors.html` / `classes-juniors.html` / `classes-sophomores.html` / `classes-freshmen.html` — Classes (one page per grade)
- `join.html` — Get involved
- `about.html` — About
- `contact.html` — Contact

## Editing content

Every page is plain HTML — open the file, find the text, edit it, save.
Names, event dates, meeting details, and the mission statement are all
placeholders right now; search for phrases like "Name Here" and "Placeholder"
to find what still needs real content.

## Adding real photos

Photo spots currently render as flat gray boxes
(`<div class="photo-slot">...</div>`) inside a sized wrapper. To drop in a
real photo, replace the placeholder div with an image, e.g.:

```html
<div class="hero-photo">
  <img src="assets/img/officers-2026.jpg" alt="Student Council officers" style="width:100%; height:100%; object-fit:cover;">
</div>
```

Put image files in `assets/img/` (create the folder) and keep filenames
lowercase with hyphens.

## Colors

The Coastal palette (navy, Columbia blue, plus teal/gold/coral accents) is
defined once as CSS variables at the top of `assets/styles.css` — change a
value there to retint the whole site.

## Deploying

`.github/workflows/deploy.yml` publishes this site to GitHub Pages on every
push to `main`. One-time setup: in the repo's **Settings → Pages**, set
"Source" to **GitHub Actions**.
