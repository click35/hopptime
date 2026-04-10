# Hoop Log — Firebase Setup Guide

This app uses Firebase Firestore as its real-time database so players across different devices can see each other on the squad leaderboard. Follow these steps to get it running.

---

## Step 1 — Create a Firebase project

1. Go to [https://console.firebase.google.com](https://console.firebase.google.com)
2. Click **"Create a project"**
3. Enter a project name (e.g. `hoop-log`)
4. Disable Google Analytics (not needed) → click **Create project**
5. Wait for it to finish, then click **Continue**

---

## Step 2 — Set up Firestore Database

1. In the left sidebar, click **Build → Firestore Database**
2. Click **"Create database"**
3. Select **"Start in test mode"** (we'll add security rules later)
4. Choose a location closest to you (e.g. `australia-southeast1` for Australia)
5. Click **Enable**

---

## Step 3 — Register your web app

1. In the left sidebar, click the ⚙️ gear icon → **Project settings**
2. Scroll down to **"Your apps"**
3. Click the **`</>`** (web) icon
4. Enter a nickname (e.g. `hoop-log-web`) — do NOT enable Firebase Hosting
5. Click **"Register app"**
6. You'll see a block of code like this — **copy the `firebaseConfig` object**:

```javascript
const firebaseConfig = {
  apiKey: "AIzaSy...",
  authDomain: "hoop-log.firebaseapp.com",
  projectId: "hoop-log",
  storageBucket: "hoop-log.appspot.com",
  messagingSenderId: "123456789",
  appId: "1:123456789:web:abc123"
};
```

7. Click **Continue to console**

---

## Step 4 — Paste config into index.html

1. Open `index.html` in a text editor
2. Find the section near the top of the `<script>` tag that says:

```
// ══════════════════════════════════════════
// PASTE YOUR FIREBASE CONFIG HERE
// ══════════════════════════════════════════
```

3. Replace the placeholder `firebaseConfig` object with your real one

---

## Step 5 — Add Firestore security rules

1. In the Firebase console, go to **Firestore Database → Rules**
2. Replace the default rules with the contents of `firestore.rules` from this folder
3. Click **Publish**

---

## Step 6 — Deploy to GitHub Pages or Vercel

Upload all files from this folder (index.html, manifest.json, sw.js, icons/) to your hosting platform. The app is ready.

---

## Firestore indexes (if needed)

If you see a Firestore error in the browser console mentioning a missing index, click the link in the error message — it takes you directly to the Firebase console to create the required index with one click.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| "Firebase is not defined" | Check that the Firebase CDN scripts are loading (internet required on first load) |
| Data not syncing | Check the browser console for Firestore permission errors |
| Join code not found | Make sure the coach created the squad first and the code is entered in CAPS |
