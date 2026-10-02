# Waypoint Ledger

A coordinate journal for your worlds. Snap or pick a screenshot of the debug screen and the
coordinates are read for you, right on your device. Free: no API key, no server, no account.

## Deploy to Vercel

This is a plain static site (a single `index.html`).

- **GitHub:** push this folder to a repo, then in Vercel choose *Add New → Project*, import it,
  pick the *Other* preset and leave the build command empty.
- **Or the CLI:** run `npx vercel` inside this folder.

No environment variables are needed. If you deployed the earlier version, you can delete the
`ANTHROPIC_API_KEY` and `ACCESS_CODE` variables.

## How photo reading works

It uses Tesseract.js, which runs entirely in your browser. The first read downloads the reader
(a few MB) and the browser keeps it, so later reads are faster and photos never leave your phone.

Tips for good reads:
- Screenshots (F2 on Java, or your device's screenshot) work far better than photos of a monitor.
- For photos, get close, fill the frame with the left side of the debug screen, and avoid glare.
- If a read fails or looks wrong, tap "Read again carefully", which tries harder settings.

## Worlds

Tap the world name at the top to switch worlds, add one, or rename it and set its server
address. Each world keeps its own places. When editing a place, you can move it to another world.

## Notes

- Everything is saved in your browser's local storage on each device. Clearing site data
  erases it, and your phone and laptop keep separate ledgers.
- Adding the site to your home screen (Share → Add to Home Screen on iPhone) makes it feel like an app.
