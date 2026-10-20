# Almada Attendance — Android & iPhone PWA prototype

This package turns the Almada Attendance prototype into an installable Progressive Web App (PWA).

## Important limitations
- This is still a prototype, not a production-ready shared company attendance service.
- Attendance data is stored in each browser's local storage and does not sync between devices.
- The role selector is only a demo UI, not secure authentication.
- GPS is captured when the user grants permission. This package does not enforce site geofences on a server.
- Selfies are stored locally in the browser in this prototype. Do not use real employee data until secure server storage and access controls are implemented.
- The service worker caches the app shell; it does not make GPS or attendance sync work offline.

## Run locally for testing
Browsers generally require HTTPS or localhost for GPS and service workers. From this folder, run a static web server, for example:
`python -m http.server 8000`
Then open `http://localhost:8000` on the same computer. For testing on phones, host it on an HTTPS website instead.

## Install on Android
1. Host the folder on an HTTPS website.
2. Open the website in Chrome.
3. Use Chrome's menu and choose **Install app** or **Add to Home screen**.
4. Allow location access when asked.

## Install on iPhone
1. Host the folder on an HTTPS website.
2. Open the website in Safari.
3. Tap **Share** → **Add to Home Screen**.
4. Open Almada Attendance from the Home Screen and allow location access.

## Production steps still required
1. Set up secure authentication and role-based permissions.
2. Use a shared server database and API for employees, sites and attendance.
3. Store selfies in private, access-controlled storage with retention rules.
4. Validate GPS and site distance server-side; consider GPS accuracy and spoofing.
5. Add audit logs, backups, HTTPS, privacy notices and appropriate Bahrain data-protection review.
6. Test on current Android and iOS versions and review the browser's camera/location permission behavior.
