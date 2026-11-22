# Bazinga

Bazinga is building mobile games. This repository contains the studio's
responsive, motion-led website as a dependency-free static site.

## Preview locally

From the repository root, run:

```sh
python3 -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000) in a browser.

## Publish with GitHub Pages

1. Push the repository to GitHub.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, select **Deploy from a branch**.
4. Choose the `main` branch and `/(root)` as the folder, then save.

GitHub Pages serves the root-level `index.html`; no build step or dependencies
are required.
