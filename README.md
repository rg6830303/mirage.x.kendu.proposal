# Mirage, Stadel. × Kendu Entertainment — Run Club Proposal

Static one-page proposal site, hosted on GitHub Pages.

**Live link:** https://rg6830303.github.io/mirage.x.kendu.proposal/

## How it is published

`.github/workflows/pages.yml` runs on every push to
`claude/mirage-kendu-repo-setup-ac3l2b`. It stages `index.html`, the video and
`.nojekyll`, then force-pushes them to the `gh-pages` branch, which is what
GitHub Pages serves.

**One manual step is needed once.** Creating a Pages site for the first time is
refused for the Actions token (`Resource not accessible by integration`), so
open **Settings → Pages** and set the source to **Deploy from a branch →
`gh-pages` / (root)**. After that every push deploys with no further
intervention.

To remove even that step on a fresh repo, store a personal access token with
the `pages` scope as the `PAGES_TOKEN` secret; the workflow then enables Pages
on its own.

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
