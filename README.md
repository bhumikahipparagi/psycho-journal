# Psycho 🌙 — your journal

A soft, dark, pastel journaling app that works on **macOS, iPad, and iPhone** as an installable web app (PWA). Write, draw with your stylus, or speak — voice notes are saved as audio *and* transcribed live.

## Features
- ✎ **Write** — text entries, with autosaved drafts (close the tab mid-thought, your words survive)
- ✐ **Draw** — pressure-sensitive stylus/Apple Pencil canvas with 6 pastel pens + eraser
- ♪ **Speak** — voice notes stored as audio, transcribed live as you talk
- **Nothing gets lost** — entries live in IndexedDB, persistent storage is requested from the browser, audio is captured in 1-second chunks while recording, and you get one-tap **Backup ↓ / Restore ↑** to a JSON file
- Works **offline** after first load (service worker)

## Deploy to GitHub Pages (≈2 minutes)
1. Create a new repo on GitHub (e.g. `psycho-journal`), keep it public.
2. Upload all the files in this folder (drag & drop works on github.com → "Add file" → "Upload files").
3. Go to **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save.
4. After ~1 minute your app is live at `https://<your-username>.github.io/psycho-journal/`

> ⚠️ Microphone access requires HTTPS — GitHub Pages provides this automatically.

## Install it like a native app
- **iPhone / iPad:** open the URL in Safari → Share button → **Add to Home Screen**
- **macOS:** open in Safari → File → **Add to Dock** (or in Chrome: install icon in the address bar)

## Notes
- Live transcription uses the browser's Speech Recognition (works in Safari 14.5+ and Chrome). If unavailable, the voice note is still saved — only the live transcript is skipped.
- **Cross-device sync (optional):** tap ⚙ in the app, set it up once with a GitHub fine-grained token (access to only your private `psycho-data` repo, permission: Contents read & write), then use "Copy link for my other devices" — opening that link on any device turns sync on there instantly. Entries (including audio) sync automatically after every save and on every launch. Deleting an entry removes it from that device only; the cloud archive keeps everything.
