# TouchGrass116

TouchGrass116 is a Columbia campus fitness prototype for Dodge Fitness Center workout sessions and an outdoor scavenger hunt.

## Run with shared accounts and leaderboard

Requires Node.js 20 or later. From the repository folder, run:

```sh
npm start
```

Open `http://localhost:3000`. The included Node server stores account credentials (salted scrypt hashes) and workout records in `data/records.json`. Workout photos and session times are public through the leaderboard. Account emails and password hashes are not included in the public session response.

To make the leaderboard shared across people and devices, deploy this Node app to a host that supports Node.js and persistent disk storage. Keep the `data` directory on that persistent disk. GitHub Pages alone only hosts static files and cannot run this API; opening `index.html` directly also uses browser-local demo data instead of shared accounts.

For camera and precise GPS access, serve the app over HTTPS and allow the user to grant browser permissions.

## Upload to GitHub

1. Create a new repository on GitHub.
2. Extract this ZIP and upload the files inside `roar-active-github` to the repository root.
3. Deploy the Node app using the hosting provider's Node service instructions. Set its start command to `npm start` and attach persistent storage for `data/`.

## Features

- Email/password account creation and sign-in with in-dialog error feedback. A valid sign-in closes the dialog.
- Public leaderboard showing all users' gym totals, session durations, timestamps, and confirmation photos.
- Dodge Fitness Center session timer, credited to the second. The session ends if the website remains visible for five seconds; those five seconds are excluded.
- Required workout photo at checkout, captured by camera or image upload.
- Admin password `12345` unlocks administrator controls in the browser.
- Admin-configured outdoor hunt locations with GPS verification within five feet, camera/upload photo check-in, and Google Maps links.

## Prototype limitations

Building ID check-in is simulated. The five-second visibility rule and GPS checks are browser-based and can be evaded or inaccurate. Admin access and scavenger-hunt settings are still browser-local. This is not production-ready for real Columbia credentials or attendance decisions. A real deployment should add managed authentication, authorization for admin changes, privacy/retention rules for public photos, and monitored persistent storage.
