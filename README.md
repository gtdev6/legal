# GT Dev Apps — legal & support pages

Static GitHub Pages site with the privacy policy, terms of use, in-app purchase info and support page for each app.

Live at **https://gtdev6.github.io/legal/**

## Rebound

| Page | URL | Where it goes |
|---|---|---|
| Privacy Policy | https://gtdev6.github.io/legal/rebound/privacy/ | App Store Connect → App Privacy; Play Console → Policy → App content → Privacy policy; in-game Settings |
| Terms of Use | https://gtdev6.github.io/legal/rebound/terms/ | App description / in-game Settings |
| In-App Purchases | https://gtdev6.github.io/legal/rebound/purchases/ | Optional link from the store screen |
| Support | https://gtdev6.github.io/legal/rebound/support/ | App Store Connect → Support URL; Play Console → Store settings → Website |
| Marketing | https://gtdev6.github.io/legal/rebound/ | App Store Connect → Marketing URL (optional) |

## Changing the contact email

The pages use `support@example.com` as a placeholder. Replace it everywhere:

```bash
grep -rl 'support@example.com' . | xargs sed -i '' 's/support@example\.com/you@yourdomain.com/g'
```

## Adding another app

1. Copy `rebound/` to a new folder (e.g. `myapp/`) and edit the text: app name, the logo letter, what data the SDKs collect, and what is sold.
2. If the app has **auto-renewing subscriptions**, the terms page and the paywall must state: subscription name and length, price per period, that payment is charged to the Apple ID / Google account at confirmation, that it renews automatically unless cancelled at least 24 hours before the period ends, how to manage/cancel it in account settings, and free-trial terms. Link both Privacy Policy and Terms of Use from the paywall and the App Store description.
3. Add a card for it in the root `index.html`.
4. Commit and push; Pages redeploys in about a minute.

## Local preview

```bash
python3 -m http.server 8000
```
