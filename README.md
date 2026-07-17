# QCapp — GitHub Pages PWA

This update keeps the existing offline-first inspection prototype and adds:

- One vertical inspection-count list for every commodity profile
- Citrus fields: Oleo, Scars, Skin Breakdown, Serious Skin Breakdown, Decay, Soft (Mushy), and Soft (Puffy)
- Serious Skin Breakdown is included inside the Skin Breakdown count and is not double-counted in totals
- Avocado fields: Scars, Misshapen, Other, Green, Turning, Brown, Soft, Shrivel, Mold, and Decay

- Editable center-number inputs between the − / + buttons
- Citrus, Avocado, Kiwi, Stone Fruit, and Banana profiles
- One editable **Score** input for each field in profile settings
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

A browser/PWA cannot silently write a camera capture into the iPhone Photos library. QCapp provides **Save to Photos** on each photo, which opens the iOS share sheet when supported. Choose **Save Image**. For a guaranteed Camera Roll copy from the beginning, take pictures in the iPhone Camera app and then use QCapp’s multi-select Gallery button.

## Data

Inspections remain in browser `localStorage`; photos remain in IndexedDB on that phone. Hosting does not synchronize devices. The JSON backup does not include photos.


Version 7 adds three pulp temperature readings and two ambient temperature readings. Each reading accepts Fahrenheit or Celsius and automatically converts the other unit.

Version 8 fixes photo pagination in printed/PDF reports. The photo section starts on a fresh page, prints up to four complete photos per page in a 2x2 layout, and uses contain sizing so portrait and landscape images are never cropped or split across pages.

## v9 workflow safeguards

Autosave-before-navigation, return-to-last-row, in-row photo review and defect linking, one-row-per-sample behavior, generic custom profiles, and access-code reveal for prebuilt templates.
