# Privacy Policy Public URL Deployment

Status: GitHub Pages is connected and the public privacy/support pages are live.

## Required Result

The final URLs must be active, publicly accessible, and non-geofenced.

The final URL must be:

- Publicly accessible without login.
- Active over HTTPS.
- Not a PDF.
- Not geofenced.
- Non-editable by the public.
- Stable enough to paste into App Store Connect and Google Play Console.

## Prepared Files

```text
site/privacy-policy/index.html
site/privacy-policy/privacy-policy.md
site/support/index.html
```

## Selected Hosting Option: GitHub Pages

GitHub Pages is now the selected path.

Prepared workflow:

```text
.github/workflows/privacy-policy-pages.yml
```

Prepared Pages source folder:

```text
site/
```

Live URLs:

```text
https://654k6byhr8-commits.github.io/starbud-adventure-privacy/privacy-policy/
https://654k6byhr8-commits.github.io/starbud-adventure-privacy/support/
```

Completed GitHub setup:

1. Create or connect a GitHub repository.
2. Push this project to the `main` branch.
3. In GitHub repository settings, open Pages.
4. Set Build and deployment source to GitHub Actions.
5. Run the `Deploy privacy policy to GitHub Pages` workflow.
6. Open the deployed `/privacy-policy/` URL and confirm it loads without login.
7. Project files have been updated with the live URLs.

## Other Hosting Options

### Option A: Existing Official Website

Best if the developer already owns a website.

Upload `site/privacy-policy/index.html` to:

```text
https://your-domain.example/privacy-policy/
```

Then update:

```text
PRIVACY_POLICY.md
closed-test/apple-app-store-connect-metadata.md
```

### Option B: Static Hosting Provider

Best if no code repository should be public.

Use a static host such as Cloudflare Pages, Netlify, Vercel, Firebase Hosting, or an object-storage static website. Upload the `site/privacy-policy` folder and point the route to `/privacy-policy/`.

## Current Blocker

No hosting blocker remains for the privacy or support URL. Production release still needs final developer identity and official support contact details.

## After Publishing

Keep these files aligned with the live URLs:

- `PRIVACY_POLICY.md`
- `closed-test/apple-app-store-connect-metadata.md`
- `APPLE_TESTFLIGHT.md` if desired

Then run:

```bash
pnpm apple:testflight:check
pnpm release:check
```
