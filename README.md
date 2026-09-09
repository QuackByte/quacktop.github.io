# Quacktop website

Launch page and privacy policy for Quacktop, at https://quackbyte.dev/quacktop/.

## Development

Node 24 or later. Run `npm ci`, then `npm run dev`. `npm run check` checks TypeScript configuration and `.ts` files; `npm run build` compiles the Astro pages. Astro's separate language-service checker currently supports TypeScript 5/6, so it is not installed with TypeScript 7.

Versions verified September 9, 2026: Astro 7.3.2, Vite 8.2.2, TypeScript 7.0.2. Dependencies are locked in package-lock.json.

## Publishing

This repository owns the website source. The existing QuackByte/quackbyte.github.io GitHub Pages workflow checks out this repository, builds it, and includes its output under `/quacktop/`. This preserves the requested URL without renaming the private QuackByte/quacktop application repository or adding a domain.

After pushing website changes, publish with:

```
gh workflow run deploy.yml --repo QuackByte/quackbyte.github.io
```

The organization site's normal deployments also pick up the latest website commit. This repository's workflow checks every push and pull request.

## Launch

Replace the “Coming soon” presentation in src/pages/index.astro with an actual App Store link when the listing is available. Confirm the shipping build's privacy behavior against src/pages/privacy.astro and App Store Connect disclosures before submission.

Screenshots are cropped captures of the running development app from September 9, 2026. Session titles and local project information have been excluded. Source screenshots are not committed. The app icon comes from the app repository. No third-party fonts, analytics, or client-side scripts are loaded.
