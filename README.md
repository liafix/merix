# MERIX — Chromatic Motion LinkHub

A static, accessible, mobile-first social link hub for the Slovak student company MERIX.

## Open locally

Extract the ZIP, then open `index.html` in a browser. No installation, package manager, server or build step is required. The three social destinations work even when JavaScript is disabled.

## Social destinations (user-provided)

Update **only the `href` attributes** of the three `<a class="social-card ...">` elements inside the `<!-- SOCIAL LINKS CONFIGURATION -->` section of `index.html`. Their existing URLs were supplied by the requester:

- Instagram: `https://www.instagram.com/merix_sf?psln=dmM4MmpsNHN2NGUx`
- TikTok: `https://www.tiktok.com/@merix_sf?_r=1&_t=ZN-9Aurbr3oSj0`
- Facebook: `https://www.facebook.com/share/1KnEnNTUkM/?mibextid=wwXIfr`

These links are **user-provided**, not independently verified for ownership or external availability. Contact email is intentionally absent because no address was provided.

## Original logo

- `assets/merix-original.png` — untouched uploaded screenshot/logo source.
- `assets/merix-logo.png` — separate derived version with empty margins cropped and near-white backdrop made transparent for web display. The actual coloured symbol is from the uploaded image, not traced or generated.
- `assets/favicon.png` — favicon derived from the same logo.

## Behavior and accessibility

- Semantic HTML, visible keyboard focus, skip link, readable contrast, self-contained inline CSS/JS.
- Adaptive Canvas 2D particles; rendering stops in hidden tabs, and particles/magnetic motion are disabled when `prefers-reduced-motion` is enabled.
- 3D pointer tilt only on fine-pointer desktop devices; regular touch links remain normal.
- The three links are ordinary HTML anchors and remain active without JavaScript.
- The Share button uses Web Share API where supported, otherwise Clipboard API on a **public HTTPS** origin; it does not share `file://` or development addresses. On localhost/file previews it explains that publication is required.
- No analytics, external fonts, tracking scripts, API calls or framework dependencies.

## Before publishing

1. Independently confirm the user-provided social URLs open the intended official profiles.
2. Upload these static files to your approved hosting/domain over HTTPS.
3. Add a verified HTTPS canonical URL and absolute `og:url` and `og:image` values once the domain is known. They are intentionally omitted before deployment.
4. Test links, sharing, and mobile interactions on the published address.
5. Add an email CTA only after a verified contact email is available.

## Known limitations

- Mobile browser external social-app routing depends on the user's OS and social apps.
- Native sharing and clipboard behavior depend on browser support and HTTPS security context.
- Original logo is a raster screenshot; scaling beyond native resolution can reveal mild anti-aliasing.
