# VYBE — free iPhone music player

VYBE is a local-first Progressive Web App. It plays audio files you import from your device; it does not stream Spotify/Apple Music catalogues.

## Files
- `index.html` — complete app
- `manifest.json` — install metadata
- `service-worker.js` — offline app-shell cache
- `icons/` — app icon assets

## Publish free with GitHub Pages
1. Create a **public** GitHub repository named `vybe`.
2. Upload all files and the `icons` folder, preserving the folder structure.
3. Open repository **Settings → Pages**.
4. Choose **Deploy from a branch**, branch `main`, folder `/ (root)`, then Save.
5. Wait for the published URL shown on the Pages screen.

## Install on iPhone
1. Open the published URL in **Safari** (not an in-app browser).
2. Tap Share → Add to Home Screen.
3. If offered, enable **Open as Web App**.
4. Tap Add.

## Use
- Tap **Add** in Library or **Import your music** on Home.
- Choose audio files from Files. VYBE stores the selected files in browser IndexedDB on this device.
- Tap a song to play; tap the mini-player to open Now Playing.
- Use Playlists to create playlists and add imported tracks.
- Export/import VYBE playlist backups as JSON.

## Notes and limitations
- No account, subscription, paid API, or server is used.
- Local audio files stay in this browser's storage. Clearing Safari website data, removing the PWA, or browser storage eviction may remove them. Keep original files backed up in Files.
- Browser playback formats vary. MP3, M4A/AAC, WAV and some OGG/FLAC files are supported depending on iOS version and codec.
- Background audio and lock-screen controls are browser/iOS-dependent. Safari PWA playback may pause under system memory or power policies; this is not equivalent to a native audio app.
- The app does not extract embedded ID3 artwork or full tags in this first version; filenames are used as track titles. Metadata editing/artwork can be added later.
- The demo SoundHelix sample is online-only and requires internet. Attribution: “SoundHelix Song 1 by T. Schürger (soundhelix.com)”. It is not included in the offline cache.
- Spotify and Apple Music playlists cannot be fetched directly without their services' authentication/API permissions. Recreate playlists in VYBE or import a VYBE JSON backup.
