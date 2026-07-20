# QCapp v10 — GitHub Pages PWA

This update is ready to upload to the existing `proto-qc` repository.

## New in v10

- Replace Document ID with a **Manifest / reference** field.
- Attach PDF, XLS, XLSX, or CSV files to an inspection for offline access.
- Rename each pulp and ambient temperature reading while retaining live Fahrenheit/Celsius conversion.
- Categorize photos during review.
- Cut Sample photos receive **Seed count (%)** and freeform internal-condition remarks.
- Defect photos retain optional field/count mapping; unrelated photo types do not show those controls.
- The camera workflow can immediately open the iPhone share sheet with the original file. iOS still requires the user to choose **Save Image**.
- **+ Row** shortcut appears in the Pallets area. Every new row is blank, opens at the top of Row Details, and focuses the Pallet ID field.
- New rows no longer copy labels or metadata from the prior row.
- Existing autosave, return-to-last-row, PDF photo pagination, templates, photos, and inspection data are preserved.

## Deploy

Upload everything in this folder to the root of the GitHub repository and replace the matching files. GitHub Pages will redeploy automatically.

Current site:

```text
https://apdelany1.github.io/proto-qc/
```

After deployment, test with:

```text
https://apdelany1.github.io/proto-qc/?v=10
```

Completely close and reopen an installed iPhone home-screen copy after GitHub finishes deploying.

## Local-only data

Inspection records remain in browser storage. Photos and attached manifest files remain in IndexedDB on that device. They are not uploaded to GitHub or synchronized to another phone. The existing JSON backup does not include photos or attached documents.
