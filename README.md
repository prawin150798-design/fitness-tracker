# Fitness Tracker v3

A simple PWA for functional fitness, fat-loss tracking and Google Sheets storage.

## Files

- `index.html` — complete web app
- `manifest.json` — PWA manifest
- `sw.js` — offline service worker
- `icon-192.png` / `icon-512.png` — PWA icons
- `apps-script/Code.gs` — matching Google Apps Script backend

## Google Sheets

Create these tabs with the exact names:

- `Bodyweight`
- `Measurements`
- `Workouts`
- `Daily habits`
- `Food`

The included Apps Script writes and reads those tabs.

## Deployment

1. Open Google Apps Script.
2. Paste `apps-script/Code.gs`.
3. Set `SPREADSHEET_ID` to your spreadsheet ID.
4. Deploy as a Web App.
5. Execute as yourself.
6. Allow access to anyone who needs to use the app.
7. Put the Web App `/exec` URL into the app's Settings page if it differs from the default.

## GitHub Pages

Upload the files to the repository root and enable GitHub Pages from the `main` branch.

## Sync behavior

- The app stores an offline copy in browser localStorage.
- Saving a weight, measurement, workout, habit or food entry sends it to Google Sheets.
- `Sync Sheets` reads the Google Sheets API and merges remote rows into the local cache.
- If the browser cannot read the Apps Script GET endpoint, the app continues to work locally and POST saving may still work.

## Workout approach

The plan emphasizes functional patterns rather than bodybuilding volume:

- Squat
- Hinge
- Push
- Pull
- Single-leg work
- Carries
- Anti-rotation/core

Progression uses previous weight, reps and RIR as guidance rather than forcing maximal loads.
