# Beauty From Ashes Counseling Services: website

Static site (HTML/CSS with a little JavaScript). No build step is needed to host it. All asset paths are relative, so it works at
`https://orehruoy.github.io/beautfyfromashescs/` and later at the root of a custom domain.

## Quick edits
- **Online booking link (one line):** `js/config.js` → `window.BFA_BOOKING_URL = "";`
  Paste Lauren's Headway direct booking link (Headway provider portal → Settings → Profile) between the quotes.
  Every "Book" button then opens it in a new tab, and the "coming soon" box on `contact.html#book` hides itself.
  While it's empty, Book buttons go to `contact.html#book` (call/email to schedule).
- **Insurance checker list:** `js/insurance-data.js`. Update `updated: "..."` and add/remove entries in `plans`
  (`also` = other names people might type). The checker runs entirely in the visitor's browser; nothing is sent anywhere.

## Page content
Pages are generated from `build.py`, which is kept outside this repo (in the bot workspace at
`/workspace/bfa-counseling/src/build.py`). Run `python3 build.py` to regenerate the `.html` files, or edit the HTML directly for small fixes.

## Preview mode (current)
- Every page has `<meta name="robots" content="noindex, nofollow">`, and `robots.txt` disallows all crawlers.
- A small "Preview" badge appears in the corner.
- At launch: set `PREVIEW = False` in build.py and rebuild, add a `CNAME` file, and point DNS (not done yet).

## Files
- `index.html`, `about.html`, `services.html`, `insurance.html`, `faq.html`, `contact.html`, `404.html`
- `assets/site.css`, `assets/fonts/`, `assets/img/`
- `js/config.js`, `js/insurance-data.js`, `js/checker.js`, `js/site.js`
- `robots.txt`, `.nojekyll`, `favicon-96.png`, `apple-touch-icon.png`
