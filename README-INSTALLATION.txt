SEVA SADAN BOOKING MANAGER — BRANDED PWA LAUNCHER PROTOTYPE

CONTENTS
- index.html: branded launch page using the Trust logo
- manifest.webmanifest: PWA name and install icons
- sw.js: basic service worker for local launcher assets
- icons/: app icons and Trust logo

IMPORTANT LIMITATION
This is a separate branded launcher/prototype, not a replacement for the existing Apps Script app. The Open Booking Manager button links to the current deployment:
https://script.google.com/macros/s/AKfycbxtAeWu1rY6Ub0xAhbUq8CbKWmQ-dlp13XFaE3lDmQmsmutHTZ9DXyHOvnk0k2JVlZroQ/exec
It does not bypass Google sign-in, deployment access settings, or the application's role checks. It also does not yet prove that every booking operation works through a PWA. The booking system opens at its existing Google Apps Script URL, which may open in a browser context on some phones.

PUBLISH USING GITHUB PAGES
1. Sign in to GitHub and create a NEW repository named `seva-sadan-booking-launcher`.
2. Keep this repository separate from the Apps Script project. Upload the files and folders in this ZIP to the repository root (not the ZIP file itself).
3. If GitHub asks about visibility, note that GitHub Pages on GitHub Free generally requires a public repository. This launcher contains no customer records or secrets, but its app link will be visible publicly. Do not upload Apps Script source, spreadsheet exports, user lists, credentials, or customer data.
4. In repository Settings → Pages, choose publishing from the `main` branch and `/ (root)`, then Save.
5. Wait for GitHub Pages to publish. GitHub will show the resulting HTTPS address, typically `https://YOUR-ACCOUNT.github.io/seva-sadan-booking-launcher/`.
6. Open that address on one Android phone in Chrome and one iPhone in Safari. Verify the logo, app title, install/shortcut steps, Google sign-in and role permissions. Do not distribute widely until checked.
7. Android: Chrome menu → Install app or Add to Home screen. iPhone: Safari Share → Add to Home Screen.

SECURITY AND BACKEND PRESERVATION
- Do NOT edit or redeploy the existing Apps Script project for this prototype.
- Do NOT change the current spreadsheet, Users_Roles tab, deployment URL, or permissions.
- This static page is only a launcher; it is not an authentication layer. Access control must continue to be enforced by Apps Script.
- A PWA on a free GitHub Pages URL is not guaranteed to keep the Google Apps Script app fully inside standalone mode. If the Google app opens in the browser, that is a platform limitation, not proof of broken backend.
- Do not put sensitive data or secrets in this public static site.
