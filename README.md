# Topic Manager — Offline-First PWA

An offline-first Progressive Web Application (PWA) built with pure HTML, CSS, and JavaScript using Local Storage persistence.

## Package Contents
- `index.html` — Complete application (UI, styles, LocalStorage state engine, rich text toolbar, combined date/category filters, random practice engine, and JSON `.txt` backup/restore).
- `manifest.json` — Web App Manifest for standalone installation on Android, iOS, tablets, and desktops.
- `sw.js` — Offline Service Worker that caches application assets so the app loads and operates 100% offline.
- `icon-192.png` & `icon-512.png` — App icons for home screen installation.

## How to Run & Install as an Offline PWA

### 1. Local Testing (Desktop / Laptop)
Service Workers require either `https://` or `http://localhost`.
1. Unzip `topic_manager_pwa.zip` into a folder.
2. Open a terminal in that folder and start any static server:
   - Python 3: `python3 -m http.server 8080`
   - Node.js: `npx serve .`
3. Open `http://localhost:8080` in Chrome, Edge, Brave, or Firefox.
4. Click the **Install App** icon in the browser address bar (or the **Install App on Device** button in the sidebar) to install it as a standalone desktop app.

### 2. Installing on Android / Tablet / iOS (GitHub Pages, Netlify, or Local Server)
1. Host the folder on any static HTTPS host (such as GitHub Pages, Cloudflare Pages, Vercel, or Netlify).
2. Open the URL on your Android phone or tablet in Chrome.
3. Tap the menu (**⋮**) -> **Install app** or **Add to Home screen**.
4. Once opened once, the Service Worker (`sw.js`) caches all files for full offline functionality without an internet connection.
