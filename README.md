# Museum of Your Visit

A small static web exhibit that turns the current browser session into a temporary museum record.

The page reads browser, device, display, preference, storage, network and session information that is available without permission prompts. Unsupported, empty or unavailable metrics are omitted entirely, so each visit can expose a different set of records.

## Privacy

- No analytics
- No tracking scripts
- No backend or database
- No visitor fingerprint store
- No permission requests for location, camera, microphone, clipboard, Bluetooth, USB, motion sensors or notifications
- Visit information is rendered in the current browser only

The storage checks briefly write and immediately remove a disposable test key solely to verify whether local/session storage is usable. No visit data is stored.

## Export

The **Export** button creates a local `.txt` archive containing only the metrics visible on the page at the moment of export, including the current time-of-visit value.

## Tech

Single-file static HTML/CSS/JavaScript. No framework, dependencies, backend or build step.

## GitHub Pages

Publish from the repository's `main` branch and `/ (root)` folder in **Settings → Pages → Build and deployment**.
