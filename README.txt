MY FINANCE — UPDATE BASED ON YOUR NEW INDEX FILE

Included:
- index.html: your newly uploaded version, preserved unchanged
- service-worker.js: Firebase background push handler plus offline caching

Upload/replace these two files in the ROOT of your existing GitHub repository.
Do not delete or replace manifest.json or the icons folder.

After GitHub Pages deploys:
1. Open the installed My Finance app while online.
2. Open Settings > System notifications > Enable.
3. Allow notifications.
4. Copy the device token shown in Settings.
5. Use Firebase Console > Messaging to send a test message to that token.

Notes:
- This package does not include any service-account private key.
- FCM push delivery requires a sender (Firebase Console for testing; trusted backend/Cloud Function for automatic scheduled or budget-triggered messages).
- Existing local data key myFinance_v1 is preserved in index.html.


MINIMAL iOS-STYLE ICON UPDATE
Replace icons/icon-192.png, icons/icon-512.png, and icons/icon-512-maskable.png with the versions in this ZIP.
Keep manifest.json and all other files unchanged. After deployment, remove and reinstall the PWA on your phone to refresh its launcher icon.


LATEST UI UPDATE
The index.html in this package is the latest UI file supplied by the user. It replaces the previous index.html while keeping the Firebase service worker, manifest, and minimal iOS-style app icons from the existing package.
Upload/replace the files in the repository root and icons folder as applicable. Do not delete existing manifest.json or other required assets.
