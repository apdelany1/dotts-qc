# Dott's Quality Control — GitHub Pages PWA
> **Facelift build:** This version adds a light visual refresh only. Inspection workflow, storage, and grading behavior are unchanged.


This folder is ready to upload to a GitHub repository and publish with GitHub Pages. It contains a static, installable, offline-capable version of the existing Dott's QC prototype.

## Publish it with GitHub Pages

1. Sign in to GitHub and create a new repository. A simple name is `dotts-qc`.
2. Keep the repository **Public** when using GitHub Free.
3. Upload **the contents of this folder** to the repository root. `index.html` must be at the top level, not inside another folder.
4. Open the repository's **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Choose branch **main**, folder **/(root)**, then click **Save**.
7. GitHub will show the published address, normally:
   `https://YOUR-USERNAME.github.io/dotts-qc/`
8. Open the address once on the inspection phone while online. Then install it:
   - Android/Chrome: browser menu → **Install app** or **Add to Home screen**.
   - iPhone/Safari: Share button → **Add to Home Screen**.
9. Test offline mode before field use: open the installed app once, turn on airplane mode, close it, reopen it, and verify that it loads.

## What hosting changes — and what it does not

- GitHub Pages hosts the app files and gives you an HTTPS link.
- The app shell is cached by `sw.js`, allowing the installed app to open offline after its first successful visit.
- Inspections remain in `localStorage` on the browser/device.
- Photos remain in IndexedDB on the browser/device.
- Data does **not** synchronize between devices.
- Browser data can be cleared by the user or operating system. Use **Settings → Export backup** regularly.
- The current JSON backup does not include photos.

## Updating the app

Replace the changed files in the repository and commit them. For changes to cached app-shell files, increment `CACHE_NAME` in `sw.js` (for example, `dotts-qc-shell-v2`) so installed devices discard the previous cache.

## Important prototype warning

This package preserves the current grading implementation. Validate every tolerance, unit, rollup, and grade against the inspector's approved reference process before using the output as an official client report.

## Files

- `index.html` — the complete application
- `manifest.webmanifest` — install name, display mode, colors, and icons
- `sw.js` — offline application-shell cache
- `icons/` — home-screen icons
- `.nojekyll` — tells GitHub Pages to publish the files directly
