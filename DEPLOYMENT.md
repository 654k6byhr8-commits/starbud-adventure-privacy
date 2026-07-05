# Privacy Policy Public URL Deployment

Status: page is ready, public hosting is not connected.

## Required Result

The final URL must be an active, publicly accessible and non-geofenced URL.

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

Expected URL shape:

```text
https://<github-user>.github.io/<repo>/privacy-policy/
```

Required GitHub setup:

1. Create or connect a GitHub repository.
2. Push this project to the `main` branch.
3. In GitHub repository settings, open Pages.
4. Set Build and deployment source to GitHub Actions.
5. Run the `Deploy privacy policy to GitHub Pages` workflow.
6. Open the deployed `/privacy-policy/` URL and confirm it loads without login.
7. Replace `TODO public URL` in project files with the live URL.

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

This workspace has no configured git remote and no GitHub CLI, so Codex cannot publish the page without one of these:

- A target hosting provider.
- A GitHub repository remote with Pages enabled.
- A domain/hosting account where this file should be uploaded.
- Permission to install/use a deployment CLI and complete login/authorization.

## After Publishing

Replace `TODO public URL` with the live URL in:

- `PRIVACY_POLICY.md`
- `closed-test/apple-app-store-connect-metadata.md`
- `APPLE_TESTFLIGHT.md` if desired

Then run:

```bash
pnpm apple:testflight:check
pnpm release:check
```
