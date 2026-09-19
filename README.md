# Mirage, Stadel. × Kendu Entertainment — Run Club Proposal

Static one-page proposal site, hosted on GitHub Pages.

**Live link:** https://rg6830303.github.io/mirage.x.kendu.proposal/

## How it is published

Pages has to be switched on once by a repo admin under **Settings → Pages**;
the workflow token is not permitted to create the Pages site. Either source
works, because the site files sit at the root of this branch:

- *GitHub Actions* — `.github/workflows/pages.yml` then builds and deploys on
  every push to `claude/mirage-kendu-repo-setup-ac3l2b`.
- *Deploy from a branch* — pick this branch and `/ (root)`; Pages serves the
  files directly and the workflow skips its deploy steps.

Until Pages is enabled the workflow still runs green: it checks how Pages is
configured and, if there is nothing to deploy to, says so in the run summary
instead of failing.

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
