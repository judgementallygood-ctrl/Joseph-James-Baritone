# Joseph James — baritone site

Plain static site. No build step, no dependencies.

## Files
- `index.html` — the whole site (markup, styles and script in one file)
- `img/` — all photographs. **These must be committed to the repo or the site renders with blank boxes.**

## Deploy to Vercel via GitHub
1. Put both `index.html` and the `img/` folder in the repo root.
2. `git add -A && git commit -m "Add site" && git push`
3. Before pushing, confirm the images are actually staged:
   `git ls-files img/`
   If that prints nothing, the images are not in the repo. Check `.gitignore` for `*.jpg` or `img`.
4. In Vercel: New Project, import the repo, Framework Preset = **Other**, leave build command and output directory empty.

## The one thing that breaks deploys
Vercel builds on Linux, which is case-sensitive. macOS is not.
`img/Field.jpg` referenced as `img/field.jpg` works on your Mac and 404s on Vercel.
Keep every filename lowercase, exactly as it is in this folder.

## Image filenames used by index.html
img/field.jpg
img/street.jpg
img/garden.jpg
img/terrace.jpg
img/smile.jpg
img/press-cardifflife.jpg
img/backstage.jpg
