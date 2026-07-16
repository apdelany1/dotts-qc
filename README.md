# QCapp — GitHub Pages PWA

This update keeps the existing offline-first inspection prototype and adds:

- Editable center-number inputs between the − / + buttons
- Citrus, Avocado, Kiwi, Stone Fruit, and Banana profiles
- HDI Marine guideline reference cards for the commodities covered by the supplied manual
- Three neutral numeric columns in profile settings instead of Good / Fair / Poor labels
- More pallet metadata: grower number, counter mark, package/label, pack date, lot number, and F/NF/I
- Photo renaming after capture
- Multi-select from the photo library
- A per-photo **Save to Photos** share/download action
- QCapp name and home-screen icon

## Update the existing GitHub Pages site

Upload the changed files to the repository root and replace the existing versions:

- `index.html`
- `manifest.webmanifest`
- `sw.js`
- the four files in `icons/`
- optionally `README.md` and `DEPLOYMENT-CHECKLIST.txt`

Commit the changes. GitHub Pages will redeploy automatically. Installed phones may need to fully close and reopen QCapp once or twice for the new service-worker cache to take control.

## iPhone photo limitation

A browser/PWA cannot silently write a camera capture into the iPhone Photos library. QCapp now provides **Save to Photos** on each photo, which opens the iOS share sheet when supported. Choose **Save Image**. For a guaranteed Camera Roll copy from the beginning, take pictures in the iPhone Camera app and then use QCapp’s multi-select Gallery button.

## Guideline limitation

The supplied HDI Marine manual gives defect definitions, qualitative codes, and some firmness/storage thresholds, but it does not provide the complete three-column numeric tolerance table required to fully automate every grade. The app integrates its commodity checklists and fields, while the three numeric columns remain editable. Validate the exact tolerance mapping before official client use.

## Data

Inspections remain in browser `localStorage`; photos remain in IndexedDB on that phone. Hosting does not synchronize devices. The JSON backup does not include photos.
