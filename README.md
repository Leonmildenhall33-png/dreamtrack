# DreamTrack — free iPhone sleep diary

DreamTrack is a lightweight, installable web app (PWA) made with plain HTML, CSS and JavaScript.

## Features
- Log bedtime, wake time, sleep quality and optional notes.
- Automatically calculates duration, including overnight times.
- Seven-night chart, recent history and average sleep duration.
- Set a personal sleep-duration goal.
- Edit and delete entries.
- Export entries as CSV.
- Stores data locally in the browser; no account, subscription or server required.
- Offline caching after the first successful load when hosted over HTTPS.

## Important limitation
This version is a manual sleep diary. A website installed on iPhone cannot reliably detect sleep automatically or continuously monitor sleep stages, heart rate or movement in the background. Those features require native iOS/HealthKit integration and appropriate permissions/hardware. Do not treat this app as a medical device.

## Run locally
For a quick preview, open `index.html` in a desktop browser. For installability and offline support, serve the folder over HTTPS (or localhost for testing).

Example with Python installed:
```bash
cd dreamtrack
python3 -m http.server 8000
```
Then open `http://localhost:8000` on the same computer.

## Put it online for free
1. Create a free account with a static hosting provider such as GitHub Pages or Netlify.
2. Upload the contents of this folder (not just the ZIP).
3. Enable publishing / deploy the site.
4. Open the resulting HTTPS website in Safari on your iPhone.

## Install on iPhone
1. Open the deployed HTTPS website in Safari (not an in-app browser).
2. Tap the Share icon.
3. Choose **Add to Home Screen**.
4. Keep **Open as Web App** enabled if shown, then tap **Add**.
5. Launch DreamTrack from the Home Screen.

## Test checklist
- Add a sleep entry with bedtime 23:00 and wake time 07:00; duration should be 8h 00m.
- Add an entry crossing midnight, e.g. 01:00 to 08:30; duration should be 7h 30m.
- Edit and delete an entry in History.
- Change the goal and confirm it updates on Home and Insights.
- Export CSV and open it in a spreadsheet app.
- Reload the page and confirm entries remain.
- After the first online load, enable airplane mode and test that the cached app opens.

## Privacy
Sleep entries are stored in local browser storage on this device. They are not sent to a server by this app. Clearing Safari website data can erase them, so use CSV export for backups.
