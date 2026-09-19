# HustleHub Legal and Compliance Web Portal

This repository contains the official, publicly hosted legal and Google Play Store compliance documents for **HustleHub** at Meru University of Science and Technology (MUST).

Maintained by: **KDroiders of MUST Innovation Club**  
Official Contact: **kotlin.hustlehub@gmail.com**

## Pages Included
- **Landing Hub**: `index.html` (`/`)
- **Privacy Policy**: `privacy.html` (`/privacy`)
- **Terms of Service**: `terms.html` (`/terms`)
- **Account and Data Deletion Portal**: `delete-account.html` (`/delete-account`)
- **Vercel Configuration**: `vercel.json` (enables clean URLs and security headers)
- **Styling**: `styles.css` (professional, responsive design without emojis)
- **Branding**: `logo.png`

---

## Deploying to Vercel

### Option 1: Vercel Dashboard (Recommended)
1. Commit and push this repository to GitHub:
   ```bash
   git add .
   git commit -m "feat: updated legal docs, e2ee privacy policy, and brand assets"
   git push origin dev
   ```
2. Go to the [Vercel Dashboard](https://vercel.com/new).
3. Click **Import Project** and select this GitHub repository (`hustlehub-legal`).
4. Keep the default settings (Framework: **Other**, Root Directory: `./`).
5. Click **Deploy**.

### Option 2: Vercel CLI
```bash
npx vercel
npx vercel --prod
```

---

## Google Play Console Compliance URLs

Once deployed to Vercel (e.g. `https://<your-project>.vercel.app` or your custom domain):

| Requirement | Google Play Console Field | URL |
| :--- | :--- | :--- |
| **Privacy Policy** | App content &rarr; Privacy policy | `https://<your-domain>/privacy` |
| **Account Deletion** | App content &rarr; Data safety &rarr; Delete account URL | `https://<your-domain>/delete-account` |
| **Terms of Service** | Store listing / in-app Help | `https://<your-domain>/terms` |

---

## Android App Integration

Once your Vercel URL is live, update lines 69–70 in `HelpScreen.kt` inside the `kotlin-hustlehub` Android project:

```kotlin
private const val TERMS_URL = "https://<your-domain>/terms"
private const val PRIVACY_URL = "https://<your-domain>/privacy"
```
