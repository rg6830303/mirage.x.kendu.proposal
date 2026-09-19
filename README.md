# Mirage, Stadel. × Kendu Entertainment — Run Club Proposal

Static one-page proposal site, hosted on GitHub Pages.

**Live link:** https://rg6830303.github.io/mirage.x.kendu.proposal/

## How it is published

`.github/workflows/pages.yml` builds and deploys the site on every push to
`claude/mirage-kendu-repo-setup-ac3l2b`. It turns Pages on itself
(`configure-pages` with `enablement: true`) and sets the source to *GitHub
Actions*, so the first push is enough to bring the site up.

## Contents

| File | Purpose |
| --- | --- |
| `index.html` | The full self-contained proposal page (styles, scripts and images inline). |
| `run-video.mp4` | Video asset referenced by the page. |
| `vercel.json` | Cache headers, kept for an optional Vercel deploy. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is, without Jekyll processing. |

All asset paths in `index.html` are relative, so the page works from a
subdirectory such as `/mirage.x.kendu.proposal/`.

## Local preview

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```
