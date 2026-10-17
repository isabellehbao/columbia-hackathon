# Roar Active

A single-page Columbia campus wellness prototype for Dodge Fitness Center attendance and an administrator-configured outdoor scavenger hunt.

## Run locally

Open `index.html` in a browser. Email/password accounts, gym sessions, leaderboard totals, activity, and photos are stored in that browser's local storage. They do not sync across devices or browsers.

For camera and precise location access, publish with HTTPS (for example, GitHub Pages). The user must grant browser camera and location permissions.

## Publish on GitHub Pages

1. Create a new GitHub repository.
2. Extract this ZIP and upload the files inside `roar-active-github` to the repository root.
3. In the repository, open **Settings → Pages** and publish from the `main` branch and `/ (root)`.

## Included features

- Email/password account creation and login (prototype only; local browser storage).
- Dodge Fitness Center session timer and second-precision credited durations.
- Session ends after the website stays visible for five seconds; those five seconds are excluded.
- Required workout photo at checkout, with live camera capture or image upload.
- Community activity feed with workout photos and timestamps.
- Admin password `12345` unlocks location controls in the current browser.
- GPS check-in within five feet of configured hunt locations, with camera capture or upload.
- Google Maps links for administrator-configured coordinates.
- Leaderboard based on credited gym time.

## Prototype limits

This is a front-end demonstration, not a secure attendance system. ID entry at Dodge is simulated. Accounts, photos, locations, and leaderboard data stay in the current browser; other people can see the feed only when using that same browser. Cross-device sharing requires a backend and shared photo storage. The admin password is present in client code and is not secure for production. Browser visibility and GPS accuracy are not tamper-proof.
