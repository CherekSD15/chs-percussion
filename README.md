# Columbus Percussion app (Solo & Ensemble 2026–27)

An installable web app (PWA) built from the season page. Students add it to their
home screen and it opens full-screen with the Columbus Cardinal icon. It works
offline after the first visit.

## What's in this folder

| File | What it does |
|---|---|
| `index.html` | The app itself (same as the claude.ai season page) |
| `manifest.webmanifest` | Name, icon and colours used when a student installs it |
| `sw.js` | Offline support: saves the app on the phone after the first visit |
| `icons/` | Home-screen icons (iPhone, Android, browser tab) |
| `img/` | Columbus Cardinal logo and the Starry Night painting |
| `cal/` | Rehearsal calendars with alerts: one per student, plus `everyone.ics` |

## Put it online (GitHub Pages, free)

1. Go to github.com/new and create a repository, for example `chs-percussion`.
   On the free plan, GitHub Pages needs the repository to be **public**.
2. Upload everything in this folder (keep the `icons` and `img` folders).
3. In the repository: **Settings → Pages → Build and deployment**,
   source **Deploy from a branch**, branch **main**, folder **/ (root)**. Save.
4. After a minute the app is live at `https://<your-username>.github.io/chs-percussion/`.

## How students install it

- **iPhone (Safari):** open the link → Share button → **Add to Home Screen**.
- **Android (Chrome):** open the link → **Install app** (or menu ⋮ → Add to Home screen).

## Rehearsal reminders

In the app, a student picks their name and taps the **Reminders on your phone** card:

- **iPhone:** **Subscribe (stays updated)** adds their nights to the Calendar app with an
  alert the day before and 2 hours before. If alerts don't show: Settings › Calendar ›
  Accounts › Subscribed Calendars › turn off "Remove Alerts".
- **Android:** **Add to Google Calendar** subscribes in Google Calendar. Alerts:
  Google Calendar › Settings › Columbus Percussion › turn on notifications.

Subscribed calendars refresh on their own (every few hours), so schedule changes reach
students without them doing anything.

## Updating it

Claude rebuilds this folder from the season page, so the page and the app stay the
same: `index.html`, the calendars in `cal/`, and the `VERSION` line in `sw.js` (which
tells phones there's an update) are all regenerated together. Upload the new files and
phones pick up the new version the next time the app is opened with a connection.

## Privacy note

The app shows students' first names only. A public repository means anyone can read
the files, so check that first names and the rehearsal schedule are fine to share under
your district's policy.
