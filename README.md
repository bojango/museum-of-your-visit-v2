# Museum of Your Visit

A small static web exhibit that turns the current browser session into a temporary museum record.

The page reads browser, device, display, preference, network and session information exposed by the current browser. Unsupported, empty or unavailable metrics are omitted entirely, so each visit can expose a different set of records.

## Restricted metrics

A deliberately subtle **Do not press** control lets the visitor explicitly opt in to additional browser permissions. Depending on browser support and the permissions granted, the exhibit can add:

- Precise location and related movement/location data
- Device orientation
- Clipboard text
- A single locally captured camera still
- Bluetooth device information selected through the browser chooser
- USB device information selected through the browser chooser

Bluetooth and USB access always uses the browser's own device-selection flow where supported. Unsupported or denied capabilities are simply omitted.

## Privacy

- No analytics
- No tracking scripts
- No backend or database
- No visitor fingerprint store
- No visit data is transmitted by the site
- Permission-based data is requested only after explicit visitor interaction
- Camera capture is reduced to one local still image and the camera stream is stopped immediately afterwards
- Location is rendered locally without third-party map tiles
- Visit information remains in the current browser session only

## Export

The main **Export** button creates a full-length local image of the current exhibit, attempting PNG first and falling back to SVG where necessary. The **TXT** button creates a local text archive containing the currently displayed metrics, including any permission-based or connected-hardware details that were added.

## Tech

Static HTML, CSS and JavaScript. No framework, backend, database or build step.

## GitHub Pages

Publish from the repository's `main` branch and `/ (root)` folder in **Settings → Pages → Build and deployment**.
