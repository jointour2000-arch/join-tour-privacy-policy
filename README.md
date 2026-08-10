# Join Tour — Privacy Policy

This repo contains only the public Privacy Policy page for the **Join Tour** app
(`com.jointour.app`), meant to be hosted via GitHub Pages so it can be submitted
to Apple (App Store Connect → App Privacy → Privacy Policy URL) and Google Play.

The content in [`index.html`](index.html) was generated from an audit of the
app's actual data collection (auth, bookings, saved bank cards, reviews, and
Firebase Cloud Messaging push notifications) as of August 2026. Update it
whenever the app starts collecting new categories of data (e.g. if you add
location, camera, or a real third-party payment processor).

## 1. Create the GitHub repo and push

`gh` wasn't authenticated in the environment this was generated in, so push it
yourself:

```bash
cd /Users/davit/Desktop/flutter_projects/join-tour-privacy-policy

git init
git add -A
git commit -m "Add Join Tour privacy policy"
git branch -M main

# Create the repo on GitHub (pick one):
# A) via gh, once you're re-authenticated:
gh auth login -h github.com
gh repo create join-tour-privacy-policy --public --source=. --remote=origin --push

# B) or manually: create an empty PUBLIC repo named
#    "join-tour-privacy-policy" at https://github.com/new, then:
git remote add origin https://github.com/<your-username>/join-tour-privacy-policy.git
git push -u origin main
```

The repo **must be public** for GitHub Pages (on the free plan) and for Apple
to be able to fetch the URL.

## 2. Enable GitHub Pages

1. On GitHub, go to the repo → **Settings → Pages**.
2. Under "Build and deployment", set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` / `(root)`, then **Save**.
4. Wait ~1 minute, then your Privacy Policy will be live at:

   ```
   https://<your-username>.github.io/join-tour-privacy-policy/
   ```

## 3. Use the link

Paste that URL into:

- **App Store Connect** → App Privacy → Privacy Policy URL
- **Google Play Console** → App content → Privacy policy (if you publish there too)

## Keeping it up to date

If you add features that collect new data (camera, location, a real payment
gateway, analytics/ads SDKs, etc.), update `index.html` and push again —
GitHub Pages redeploys automatically on every push to `main`.
