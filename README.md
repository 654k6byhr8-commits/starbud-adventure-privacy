# Starbud Adventure Privacy Policy

This repository publishes the public privacy policy for Starbud Adventure / 星芽冒險團.

Expected GitHub Pages URL:

```text
https://<github-user>.github.io/starbud-adventure-privacy/privacy-policy/
```

## Contents

- `site/privacy-policy/index.html`: public privacy policy page.
- `site/privacy-policy/privacy-policy.md`: editable source copy.
- `.github/workflows/privacy-policy-pages.yml`: GitHub Pages deployment workflow.

## GitHub Setup

1. Create a GitHub repository named `starbud-adventure-privacy`.
2. Push this folder to the repository's `main` branch.
3. In repository Settings > Pages, set Build and deployment source to GitHub Actions.
4. Run the workflow named `Deploy privacy policy to GitHub Pages`.
5. Confirm the public URL loads without login.

After the URL is live, paste it into App Store Connect and update the main game project's `PRIVACY_POLICY.md`.
