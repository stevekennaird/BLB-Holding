# Brave Little Books

A quiet, responsive holding page for bravebooks.co.uk. Plain HTML and CSS, with no dependencies.

## Deploy to Vercel

Import this repository into Vercel. `vercel.json` selects the `public` directory as the static output and copies the root `img-style-test.html` into it during the build; no framework is needed.

Add `bravebooks.co.uk` (and optionally `www.bravebooks.co.uk`) in the project's **Settings → Domains**, then apply the DNS records Vercel provides.

## Image style survey

The root `img-style-test.html` is served at `/image-style-test-survey` through a Vercel rewrite. Edit the root file to update the survey.

## Downloads

Add content files to `public/downloads/` and deploy. For example, `public/downloads/sample.pdf` is served at `https://bravebooks.co.uk/downloads/sample.pdf`.

The holding page does not link to this directory. Files are public to anyone with the URL: this is not private storage, so do not upload confidential content. Use the direct file URL rather than `/downloads/`; there is no directory index page.

## Preview locally

From the repository root, run `python3 -m http.server 8000 --directory public` and visit `http://localhost:8000`.

To preview the survey without generating build output, run `python3 -m http.server 8001` from the repository root and visit `http://localhost:8001/img-style-test.html`. The `/image-style-test-survey` rewrite only applies on Vercel.