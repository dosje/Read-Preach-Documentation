# Read & Preach user docs

Jekyll site on GitHub Pages (minima theme), live at https://docs.read-preach.com.
Pushing `main` to the remote **`docs-repo`** (not `origin`) publishes the site.

**Always pull before editing** (`git pull --ff-only docs-repo main`): the iOS and Android CI push
screenshot commits ("[UPD] iOS/Android screenshots X.Y.Z") straight to `main`.
`assets/screenshots/` is used by www.read-preach.com. Never move, rename or delete files there.

## Structure

- One set of pages for iPhone/iPad **and** Android. Platform-specific content goes in
  "iPhone & iPad" / "Android" subsections or is tagged *(iPhone & iPad)* / *(Android)*.
- Three languages, always changed together: `docs/` (EN), `de/docs/` (DE, "du"), `fr/docs/` (FR, "vous"),
  plus `index.md`, `de/index.md`, `fr/index.md`.
- Navigation comes from `header_pages` in `_config.yml`.
- `questions.json` is fetched by both apps. Never move or rename it.
- Minimum versions: iOS 18.2, Android 8.0.
- NW Publisher may be named in these docs (not in store texts or screenshots).
- Google Play: link only the generic https://play.google.com/store/apps until the app is public,
  then https://play.google.com/store/apps/details?id=jd.readandpreach. Never mention APK downloads.

## Versioning

- The docs always describe the newest version. No per-version copies.
- New features get a tag line under their heading in `features.md`:
  `*Available from iOS x · Android y*` (DE `*Verfügbar ab iOS x · Android y*`,
  FR `*Disponible à partir d'iOS x · Android y*`). Small changes get an inline tag `*(iOS x · Android y)*`.
- iOS and Android have their own version numbers. Do not try to align them.

## When an app version is released

The app sessions own their release notes. This repo only reads them.

| Source | iOS (`read&preach/dev`) | Android (`read&preach-android/main`) |
|---|---|---|
| Full changes | `CHANGELOG.md` | `CHANGELOG.md` |
| User-facing notes (EN/DE/FR) | `release/X.Y.Z/whats-new.md` | `release/X.Y.Z/store-text.md` |

Steps:

1. Read the version's CHANGELOG entry and release notes. Store notes leave out NW Publisher,
   so check the CHANGELOG for anything missing.
2. Update `docs/whats-new.md` + `de/` + `fr/`: newest first, in the right platform section,
   with month and year. Turn "coming soon" into the release month. Versions that were never released
   on their own are merged into the next released one.
3. Update `features.md`, `faq.md`, `getting-started.md` and `installation.md` where behaviour or
   UI labels changed. Take UI labels from the app string files
   (iOS `Read & Preach/Read & Preach/{en,de,fr}.lproj/Localizable.strings`, Android `app/src/main/res/values{,-de,-fr}/strings_app.xml`).
4. Add or adjust *Available from* tags for new features.
5. Commit as `[UPD] <platform> X.Y.Z released: … (EN/DE/FR)` and ask before pushing.
