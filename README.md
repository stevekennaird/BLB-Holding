# Brave Little Books

A quiet, responsive holding page for bravebooks.co.uk. Plain HTML and CSS, with no dependencies or build step.

## Deploy to Vercel

Import this repository into Vercel. `vercel.json` selects the `public` directory as the static output; no framework or build command is needed.

Add `bravebooks.co.uk` (and optionally `www.bravebooks.co.uk`) in the project's **Settings → Domains**, then apply the DNS records Vercel provides.

## Downloads

Add content files to `public/downloads/` and deploy. For example, `public/downloads/sample.pdf` is served at `https://bravebooks.co.uk/downloads/sample.pdf`.

The holding page does not link to this directory. Files are public to anyone with the URL: this is not private storage, so do not upload confidential content. Use the direct file URL rather than `/downloads/`; there is no directory index page.

## Preview locally

From the repository root, run `python3 -m http.server 8000 --directory public` and visit `http://localhost:8000`.