# Merry Grantmas

A festive single-page site that collects the Grant family's holiday songs and playlists in one place. It highlights the latest song “Ting-a-ling,” links out to streaming playlists, and preserves a songbook of past originals.

## Features
- **Featured track player:** Custom play/pause button controlling the bundled `ting-a-ling.mp3` audio with accessible labels.
- **Past years songbook:** Scrollable list of prior Grant family holiday tracks with track lengths and outbound links.
- **Playlist buttons:** Quick links to Bandcamp, Apple Music, TIDAL, and Spotify playlists.
- **Festive presentation:** Decorative lights, snow, ribbons, and a Grant family photo (`assets/img/grantmas.jpg`).

## Project structure
```
index.html         # Static page with styles, layout, and minimal JS for the player
assets/
├─ audio/          # Audio assets (e.g., ting-a-ling.mp3)
└─ img/            # Images (e.g., grantmas.jpg)
```

## Running locally
This is a static site—no build step required. Open `index.html` directly in a browser or serve the directory locally (for reliable audio loading) with any static server, for example:

```bash
python -m http.server 8000
```

Then visit [http://localhost:8000](http://localhost:8000) and enjoy the tunes.
