# OE Master Plan 2026 — Source Backup

This archive contains the complete source code and data snapshot for the OE Master Plan 2026 website.

## Requirements

- Node.js 22.13 or newer
- npm

## Open and run locally

1. Extract this archive.
2. Open the extracted folder in VS Code.
3. Open a terminal in the folder.
4. Run `npm ci`.
5. Run `npm run dev`.

The application data used by the website is embedded in `app/workbook-data.ts`. The original Excel workbook is also included at `data/OE_Master_Plan_2026.xlsx`.

## GitHub backup

Create an empty GitHub repository, then run:

```bash
git init
git add .
git commit -m "Backup OE Master Plan 2026"
git branch -M main
git remote add origin YOUR_GITHUB_REPOSITORY_URL
git push -u origin main
```

## Deploy to Vercel

1. Push the folder to GitHub.
2. In Vercel, choose **Add New Project** and import the repository.
3. Keep the detected framework as **Next.js**.
4. Deploy. `vercel.json` instructs Vercel to use the standard Next.js build.

The current admin password is present in the client-side source because the existing website uses browser-side administration. Change it before publishing a public fork if stronger access control is required.

## Deploy with the original Sites/Cloudflare build

The original build remains available through:

```bash
npm run build
npm run start
```

## Backup documentation

- `SOURCE_TREE.txt`: complete folder structure of this backup.
- `SOURCE_CONTENTS.md`: full text content of every readable source/configuration file.
- `FILE_CHECKSUMS.sha256`: SHA-256 checksum of every file.
- `data/OE_Master_Plan_2026.xlsx`: original binary workbook.

Generated dependency and build directories (`node_modules`, `dist`, `.next`) are intentionally excluded. They are reproducible from `package-lock.json`.
