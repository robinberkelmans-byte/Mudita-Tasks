# Task PWA — Setup

A minimal Google Tasks entry app. One field, one button.

## What you need

- Somewhere to host 3 files (GitHub Pages is free and easy)
- A Google account
- ~15 minutes

---

## Step 1 — Host the files

Upload `index.html`, `manifest.json`, and `sw.js` to any static host.

**GitHub Pages (recommended):**
1. New repository → upload the three files
2. Settings → Pages → Source: main branch
3. Your URL will be `https://yourusername.github.io/repositoryname`

---

## Step 2 — Create a Google OAuth credential

1. Go to [console.cloud.google.com](https://console.cloud.google.com)
2. Create a new project (or use an existing one)
3. APIs & Services → Enable APIs → search **Google Tasks API** → Enable
4. APIs & Services → Credentials → Create Credentials → OAuth 2.0 Client ID
5. Application type: **Web application**
6. Under **Authorised redirect URIs** → add your hosted URL exactly
   (e.g. `https://yourusername.github.io/repositoryname/`)
7. Click Create → copy the **Client ID**

---

## Step 3 — Connect the app

1. Open your hosted URL in Firefox on the Mudita
2. Tap **Connect Google Tasks**
3. Paste your Client ID → tap Connect
4. Log in with Google → authorise
5. Done — you're in

From this point on: open app → type → tap Add → close.

---

## Notes

- The app stores a refresh token locally. It silently renews itself.
  You should not need to log in again.
- To add to home screen in Firefox: menu → Install / Add to Home Screen
- If you ever need to disconnect: clear site data in Firefox settings
- The app works offline — tasks queued while offline are not yet supported
  (this is a future addition if needed)
