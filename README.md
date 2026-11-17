# Beauty From Ashes Counseling Services: website (preview)
Static HTML/CSS/JS. No build step is needed to host this; pages are generated from `build.py` kept in the bot workspace.

- **Booking link (one-line swap):** `js/config.js` → `window.BFA_BOOKING_URL = "";` Paste Lauren's Headway direct booking link there.
- **Insurance list:** `js/insurance-data.js` (update `updated` date + `plans`).
- **Preview mode:** pages carry `noindex` and robots.txt disallows all. Remove these at launch.
