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

- The pages describe **1.4 (versionCode 21)**. The mobile link shipped with it,
  so the privacy policy carries the mobile network — the operator, the radio and
  signal, the band, and the identities of the cells in range — and the location
  section covers all three uses of the permission, as the in-app disclosure now
  does. The first check is titled "Wi-Fi status" on Wi-Fi and "Link status" off
  it, which is why the pages name both.
- The **store listing has not been updated for 1.4**: `android-lite/play/listing/`
  still describes 1.3, and its What's new block is the 1.3 one. The site is ahead
  of the listing until that is written.
- English only for now. The app itself ships six languages (English, Arabic,
  Spanish, Urdu, Portuguese, French); an Arabic mirror of this site would be a
  copy of each page with `dir="rtl"` plus a switch in the top bar.
- Every threshold quoted in `docs.html` is one the app actually applies. When a
  threshold changes in the app, change it here too.
- `privacy.html` is what Play's User Data policy is judged against, so it has to
  keep describing the app exactly. `android-lite/play/policy-review.md` in the
  app repository is where that is checked each release.
- The screenshots come from `android-lite/play/graphics/screenshots-phone/en-US/`
  (1, 7 and 8), cropped of their letterboxing and halved to 540 wide. They are
  demo captures: the LAN names are `Device-NN` stand-ins, never real hostnames.
- The listing is live, and `index.html` and `docs.html` link to it:
  `https://play.google.com/store/apps/details?id=com.nhcheck.lite`. There is no
  App Store link because the iOS build is not published.
