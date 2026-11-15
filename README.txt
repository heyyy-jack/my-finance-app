MY FINANCE — FIREBASE PUSH ENABLED PWA

Files:
- index.html
- service-worker.js
- manifest.json
- icons/

DEPLOYMENT
1. Upload the contents of this folder to a static HTTPS host (Firebase Hosting is suitable).
2. Open the HTTPS site in Chrome on Android.
3. Add it to the Home screen and open the installed app.
4. Open Settings > Notifications > Enable push notifications.
5. Copy the device registration token shown in the app.
6. In Firebase Console > Messaging, create a test message and send it to that registration token.

IMPORTANT
- The VAPID key is a public key and is used by the browser to register for FCM.
- Never publish a Firebase service-account private key or admin credentials in this folder.
- This setup registers the device and displays incoming FCM messages.
- To send automatic budget alerts while the app is closed, a trusted backend/cloud function must send FCM messages. This PWA does not upload transaction records, and it cannot calculate private local spending while closed on a server.
- Firebase project configuration values and API keys in a web app are client configuration, not service-account secrets. Configure Firebase authorized domains and security rules as needed.
