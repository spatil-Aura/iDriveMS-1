# iDriveMS Landing Redesign

Static site: three pages, no build step required.

- `index.html` — landing page
- `contact.html` — contact page
- `login.html` — sign in / create account page
- `support.js` — shared runtime the pages depend on (must stay next to them)
- `assets/` — images, video, and logos the pages reference

## Run locally

No build tools needed — any static file server works:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/index.html`.

## Deploy to Vercel

1. Push this folder to a GitHub repository (root of the repo, not a subfolder).
2. On [vercel.com](https://vercel.com), **Add New → Project**, import the repo.
3. Framework preset: **Other** (no build command, no output directory override needed).
4. Deploy.

`vercel.json` pins `cleanUrls`/`trailingSlash` off so `login.html` and `contact.html` are served at those exact paths, matching the links used in the pages.
