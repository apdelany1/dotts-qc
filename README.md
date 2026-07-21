# QCapp v11 — Unified Row Entry

This update is ready to upload to the existing `proto-qc` repository.

## New in v11

- Combines Row Details, photos, sample size, and inspection counts into one continuous page.
- Every new row opens at the top and focuses the Pallet ID field.
- Removes the separate **Continue to inspection fields** step.
- Keeps default temperature names, with a pencil button to rename or reset each reading.
- Keeps default Quality and Condition field names, with a pencil button to customize them for the current inspection.
- Renaming a field never changes its stored count or internal field key.
- Custom field names carry into photo defect selectors and report rankings.
- Saves and restores the last scroll position for each inspection row when switching tabs.
- Existing photos, documents, inspections, templates, counts, and report pagination are preserved.

## Deploy

Upload everything in this folder to the root of the GitHub repository and replace the matching files. GitHub Pages will redeploy automatically.

Current site:

```text
https://apdelany1.github.io/proto-qc/
```

After deployment, test with:

```text
https://apdelany1.github.io/proto-qc/?v=11
```

Completely close and reopen an installed iPhone home-screen copy after GitHub finishes deploying.

## Local-only data

Inspection records remain in browser storage. Photos and attached manifest files remain in IndexedDB on that device. They are not uploaded to GitHub or synchronized to another phone. The existing JSON backup does not include photos or attached documents.
