# FibreConX Joint - Splice Report

Static HTML app for querying the FibreConX ArcGIS joint, splices, cables, fibres, and circuits and exporting a report.

## Publish with GitHub Pages

1. Create a new GitHub repository (preferably **private** if your organisation requires it; check GitHub Pages access settings, as a published Pages site may be publicly accessible even when the repository is private).
2. Upload the files from this folder to the repository root. Keep `index.html` at the top level.
3. In the repository, open **Settings → Pages**. Under **Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then **Save**.
4. Open `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/` when the deployment is complete. The `index.html` file loads automatically. You may also navigate to `/joint-splice-report.html`.
5. For **Sign in to ArcGIS**, the ArcGIS OAuth application (`j61ihett8O71eFQI`) must permit the exact GitHub Pages page URL as a redirect URI. If this is not configured, the app still offers a **temporary token** alternative.

## Operation

- Paste a temporary ArcGIS token into the password-style token field and click **Use token**, or sign in through OAuth if configured.
- Enter a joint name or splice number, then click **Create Report**.
- Use Individual Fibres / Group Tubes-Ribbons and tray controls to inspect results.
- Export CSV to include joint details, cables, and splice schedule. The report creation timestamp is included in cell B1 when opened as a CSV in Excel.

## Notes and security

- This is a **client-side-only** application: no server-side hosting or npm build is required.
- Do not add permanent ArcGIS access tokens, passwords, or secrets to the repository. Temporary tokens entered in the app are held in memory, not committed into these files.
- The site communicates from the visitor's browser to `arcgis.fibreconx.com.au` and loads ArcGIS Maps SDK from `js.arcgis.com`. Users need appropriate network access, permissions, and ArcGIS Server CORS/security policy settings.
- GitHub Pages provides static hosting, not a CORS bypass. If a query is blocked by CORS or network access policy, the ArcGIS server or your hosting approach needs adjustment.
- All displayed joint and fibre details are live responses from your ArcGIS services, not stored data in this repository.
