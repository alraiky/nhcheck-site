# nhcheck.net

The website for **NHCheck** and its first product, **NHCheck Lite** for Android.

Four static pages, one stylesheet, two screenshots. No build step, no framework,
no dependencies — open `index.html` in a browser and it works.

```
index.html        the product, the five checks, how to get it
docs.html         what each check does, the thresholds, the permission
support.html      contact, bug reports, common answers
privacy.html      privacy policy (Google Play requires a reachable URL)
assets/style.css  the app's "Network-Ops Dark" tokens, shared by all four
assets/*.png      screenshots of the Android app
```

## Preview

```bash
python3 -m http.server 4173
```

Then open <http://localhost:4173>.

## Deploy

Published with GitHub Pages from the repository root of `main`. Any other static
host serves the directory as-is — links are relative throughout, so the pages
work from a subpath as well as from a domain root.

## Notes

- English only for now. The app ships English and Arabic; an Arabic mirror would
  be a copy of each page with `dir="rtl"` plus a switch in the top bar.
- Every threshold quoted in `docs.html` is one the app actually applies. When a
  threshold changes in the app, change it here too.
- The store link in `index.html` is a placeholder until the Google Play listing
  is live.
