# MRS Mobile

A progressive web app for exploring the [Mixed Reality Service](https://github.com/mpesce/mrs-server/) (MRS) network from your mobile device.

MRS Mobile uses your device's GPS to query nearby MRS registrations and displays any service points found at your location. Point your phone at the world and see what's been registered in mixed reality.

## How It Works

1. **Scan** — Tap to get your current location and query the MRS server for nearby registrations
2. **Watch** — Continuously track your position and automatically re-query as you move
3. **Adjust Range** — Slide to widen or narrow your search radius (10m to 10km, default 250m)

When a hit is found, the top half of the screen shows the raw JSON response and the bottom half displays tappable links to each service point, sorted by distance.

## Getting Started

MRS Mobile is a single-page web app with no build step and no dependencies. Serve it over HTTPS (required for geolocation) and open it in a mobile browser.

```bash
# Clone the repo
git clone https://github.com/mpesce/mrs-mobile.git

# Serve it however you like — any HTTPS-capable web server will do
```

Because it's a PWA, users can install it to their home screen for a full-screen, app-like experience.

## MRS Server

MRS Mobile queries the public MRS server at [owen.iz.net](https://owen.iz.net). API documentation is available at [owen.iz.net/docs](https://owen.iz.net/docs).

The app calls `POST /search` with the device's latitude, longitude, and elevation to find registrations within the selected range.

## Project Structure

```
index.html      — The entire app: HTML, CSS, and JavaScript in one file
manifest.json   — PWA manifest for home screen installation
sw.js           — Service worker for offline caching
icons/          — App icons in all required sizes
CLAUDE.md       — Project instructions
```

## Requirements

- A modern mobile browser with geolocation support
- HTTPS (required by browsers for geolocation access)
- Network connectivity to reach the MRS server

## License

MIT
