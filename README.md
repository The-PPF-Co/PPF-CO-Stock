# The PPF Co. Stock

Stock app for The PPF Co. studio: stock in (with supplier bill PDF reading), B2B sales with client rates, self use, PPF rolls tracked by Roll ID, history, monthly summary and Excel export.

## Files

| File | What it is |
|---|---|
| `index.html` | The live app (uses Firebase) |
| `firebase-config.js` | Your Firebase settings and the owner's email: **edit this** |
| `firestore.rules` | Security rules: paste into Firebase → Firestore → Rules |
| `manifest.json`, `icon-192.png`, `icon-512.png` | App name and icon when added to a phone's home screen |
| `demo.html` | Demo with sample data, no Firebase needed |

## Setup

1. **Firebase project**: console.firebase.google.com → Add project → name `ppfco-stock` → Google Analytics off → Create.
2. **Web app**: Project overview → `</>` (Web) → nickname `ppf-stock` → Register (no Hosting) → copy the `firebaseConfig` values into `firebase-config.js`.
3. **Owner**: in `firebase-config.js` set `ownerEmail` to the owner's email (lowercase).
4. **Sign-in**: Authentication → Get started → enable **Google** (set the support email) and **Email/Password**.
5. **Database**: Firestore Database → Create database → location `asia-south2 (Delhi)` or `asia-south1 (Mumbai)` → Start in **production mode**.
6. **Rules**: Firestore → Rules → replace everything with `firestore.rules`, after changing `owner@example.com` to the owner's email → Publish.
7. **GitHub**: create a public repository `ppf-stock` → Add file → Upload files → upload all files here → Commit.
8. **Pages**: repository Settings → Pages → Deploy from a branch → `main` / `(root)` → Save. The app is at `https://<username>.github.io/ppf-stock/`.
9. **Allow the site in Firebase**: Authentication → Settings → Authorized domains → Add domain → `<username>.github.io`.
10. **First sign-in**: open the app, sign in with the owner's email (you are Admin), then in Settings add the store name, products, B2B clients and the team (email + role).

## Updating

- **App files** (`index.html` etc.): upload the new file on GitHub → Commit. Pages updates in a minute or two.
- **`firestore.rules`**: GitHub does not apply rules. Paste the new rules into Firebase → Firestore → Rules → Publish every time this file changes.

## Good habits

- Download **Summary → Month Excel** at the end of every month and keep it in Google Drive. The free Firebase plan has no automatic backup.
- Never upload a `firebase-config.js` that still says `PASTE` over your filled-in one.
