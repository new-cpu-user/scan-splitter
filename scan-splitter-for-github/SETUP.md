# Getting Scan Splitter onto everyone's phone

## 1. Put it on GitHub Pages (you do this once)

1. Go to github.com and create a new repository — call it something like
   `scan-splitter`. Public is fine: the code has zero personal data in
   it, since every scan is processed on the visitor's own device and
   never uploaded anywhere. Nothing about your family's documents is
   ever exposed by making this repo public.
2. Upload the contents of the `scan-splitter/` folder from this package
   — `index.html`, `manifest.json`, and the `icons/` folder — to the
   root of that repo. Easiest way: on the repo's GitHub page, click
   "Add file" → "Upload files", drag in the folder contents, commit.
3. Go to the repo's Settings → Pages. Under "Source", choose the
   `main` branch and `/ (root)` folder, then save.
4. GitHub gives you a URL, typically:
   `https://<your-username>.github.io/scan-splitter/`
   It takes a minute or two to go live the first time.
5. Open that URL yourself and confirm it loads and works, exactly like
   the version you already tested.

To update it later (a bug fix, a new feature): just upload the changed
files to the same repo, overwriting the old ones. GitHub Pages
redeploys automatically within a minute or so.

## 2. Share the link with your family

Send them the `https://<your-username>.github.io/scan-splitter/` link
however's easiest — text, WhatsApp, email. No account, no login, no
app store needed.

## 3. Add it to the home screen (each person does this once, on their own device)

**iPhone / iPad (Safari):**
1. Open the link in Safari (must be Safari, not Chrome, for this to work on iOS).
2. Tap the Share icon (square with an arrow, bottom of the screen).
3. Scroll down and tap "Add to Home Screen".
4. Tap "Add". It now behaves like a regular app icon — opens full-screen, no browser bar.

**Android (Chrome):**
1. Open the link in Chrome.
2. Tap the ⋮ menu (top right).
3. Tap "Add to Home screen" or "Install app" (wording varies by Android version).
4. Confirm. It installs like a proper app, with its own icon.

**Mac / Windows (Chrome or Edge):**
1. Open the link.
2. Click the install icon in the address bar (a little monitor-with-arrow icon), or the ⋮ menu → "Install Scan Splitter".
3. It opens in its own window from then on, separate from your regular browser tabs.

Once installed this way, it opens with a real app icon and its own
window, separate from regular browser tabs — no more re-typing or
re-finding the link. It still needs an internet connection each time
to load the page itself (it fetches a few small library files from a
CDN on open), but nothing about the documents you scan is ever sent
anywhere — all of that happens on the device, after the page has
loaded. If offline use ever actually matters to you (patchy wifi
somewhere), that's a solvable follow-up — just flag it and I'll add
proper offline caching rather than guessing at it now.
