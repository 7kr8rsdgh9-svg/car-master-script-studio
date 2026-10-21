# Car Master — Script Studio

A mobile-friendly, browser-only automotive video script generator. No build tools, server, API key, analytics or paid AI integration are needed.

## Features

- Short-form (30–45 seconds), Social standard (45–60 seconds), Full showcase (75–90 seconds).
- English voice-over and timed camera shot list, based only on the supplied vehicle details.
- Adjustable tone, British or American English, and speaking pace.
- Automatic local draft saving, named saved vehicles, JSON import/export.
- Copy, share and text-file exports.
- A prepared refinement prompt to copy into ChatGPT. This is a manual handoff, not a live AI connection.
- A manifest and service worker for home-screen use and cached app-shell access after an initial successful online load.

## Privacy and accuracy

The application processes vehicle details in the browser. Projects are stored in localStorage on that browser, not in this repository and not synced between devices. Export backups before clearing website data. Use only a public business contact in scripts. The hosting provider may log ordinary website requests.

No real vehicle data is bundled. The demo is fictional. Information is not independently verified. The generator omits blank fields and may shorten or exclude lower-priority sections to fit the selected format. If too little information is provided, it reports a shorter duration rather than fabricating facts. Rehearse to check actual delivery time.

## Hosting

This repository is ready for static hosting; uploading it does not by itself publish a website.

### Render

Create a **Static Site** using this repository and its `main` branch.

- Build command: `echo 'Car Master is ready'`
- Publish directory: `.`
- Auto-deploy: enabled
- No environment variables, API keys or database required.

Use the actual HTTPS address returned by Render after deployment succeeds. The app works both at a domain root and under a subdirectory.

### GitHub Pages (alternative)

In repository **Settings → Pages**, select **Deploy from a branch**, branch **main**, folder **/(root)**, then save. Do not use a predicted address as proof of a successful deployment; check the Pages status first.

## Development and testing

`index.html` contains the app, styles and JavaScript. `manifest.webmanifest`, `icon.svg` and `sw.js` provide app-shell installation/caching support. No dependency installation or build is required.

Local checks covered JavaScript syntax; Chromium UI interactions at 320, 375, 390, 430 and 1280-pixel widths; three distinct script formats; consistent shot timing; local-save logic with a storage test double; import/export; ChatGPT prompt preparation; and safe rendering of HTML-like input. These are not physical iPhone/Safari tests. Storage, sharing and installation depend on browser support and permissions.
