# QCapp v12 — Paper Form Replacement Workflow

This update is ready to upload to the existing `proto-qc` repository.

## New in v12

- Treats every inspection row as one opened box/sample from a pallet.
- Adds **Not started / In progress / Complete** box statuses and inspection progress.
- Autosaves while the inspector types and shows a **Saved offline** indicator.
- Prevents primary defect counts from assigning the same fruit to more than one defect.
- Adds cut-sample observations to every box.
- Stores packaging and label information once per inspection, with additional packaging options when the lot contains multiple pack types or labels.
- Adds a confirmed **Box 2 from same pallet** workflow and partial pallet-ID matching.
- Imports multiple manifest rows from CSV or modern `.xlsx` files, with flexible column mapping and container filtering.
- Keeps PDF and legacy spreadsheet manifests as attached reference files; a copied table can also be pasted to build rows.
- Keeps grading off by default. When enabled, grading is manual per box using A, B, C, D, or F until the final grading procedure is confirmed.
- Adds a final review screen that flags missing shipment fields and incomplete boxes before the inspection can be completed.
- Allows photos within a row to be reordered.
- Replaces the fragile iPhone download action with a Share-first workflow and a full-size press-and-hold fallback.
- Adds undo after deleting a row or photo.

## Deploy

Upload everything in this folder to the root of the GitHub repository and replace the matching files. GitHub Pages will redeploy automatically.

Current site:

```text
https://apdelany1.github.io/proto-qc/
```

After deployment, test with:

```text
https://apdelany1.github.io/proto-qc/?v=12
```

Completely close and reopen an installed iPhone home-screen copy after GitHub finishes deploying so the new service-worker cache replaces v11.

## Manifest support

- **Build rows directly:** CSV, tab-delimited text, and modern `.xlsx` workbooks.
- **Reference attachment:** PDF, `.xls`, `.xlsx`, CSV, and other supported documents can remain attached to the inspection.
- **PDF or difficult spreadsheet:** copy its table and use **Paste manifest table**.

The importer is deliberately flexible: the inspector confirms which columns contain Pallet ID, Vessel, Container No., Grower, Size, Label/Brand/Mark, Carton Weight, and other available fields.

## Local-only data

Inspection records remain in browser storage. Photos and attached manifest files remain in IndexedDB on that device. They are not uploaded to GitHub or synchronized to another phone. The existing JSON backup does not include photos or attached documents.
