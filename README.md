# hormonia-labs.github.io

The Hormonia org root site, served via GitHub Pages at
`https://hormonia-labs.github.io/`. Hosts two things:

1. **`app-ads.txt`** (repo root) — the IAB authorized-sellers file AdMob crawls
   to verify ad inventory. One file for every Hormonia app (all share one AdMob
   publisher account). Must stay at the domain **root**.
2. **`legal/`** — public legal pages (privacy, terms, account-deletion) for
   every app, linked from store listings.

## Structure
```
app-ads.txt            ← AdMob authorized sellers (domain root — do not move)
index.html             ← landing page (the domain root)
legal/
  flash/
    tnpsc/ gre/ gmat/   ← privacy.html · terms.html · delete-account.html
  docscribe/            ← privacy.html · terms.html · delete-account.html
```

## Live URLs
- https://hormonia-labs.github.io/app-ads.txt
- https://hormonia-labs.github.io/legal/flash/tnpsc/privacy.html
- https://hormonia-labs.github.io/legal/flash/tnpsc/terms.html
- https://hormonia-labs.github.io/legal/flash/tnpsc/delete-account.html

## Adding a new Flash app
Copy an existing exam folder and edit the app name + data specifics:
```
cp -r legal/flash/tnpsc legal/flash/<exam>
```
Point the new app's store-listing **Website** field at
`https://hormonia-labs.github.io` so the shared `app-ads.txt` is crawled for it.
