# MERIX LinkHub — implementation and verification

## Delivered

- Self-contained `index.html` (embedded CSS + vanilla JS), plus local derived logo, untouched uploaded original and favicon.
- Three active external social-card HTML links (Instagram, TikTok, Facebook), exactly matching links supplied by the requester.
- Mobile-first editorial layout; desktop asymmetric design; Canvas 2D atmospheric particles; floating logo; CSS chromatic lighting; restrained pointer tilt; staged entrance.
- Built-in sharing: public HTTPS only, native Web Share API with clipboard fallback; local previews show explanatory status instead of copying unsafe `file://` URL.
- Accessibility: semantic HTML, skip link, visible focus, reduced motion, usable links without JavaScript.

## Tested in Chromium

The environment blocks direct browser navigation to `file://` and `localhost` URLs. Browser tests therefore used Chromium's `set_content()` with **unchanged HTML/CSS/JS** and **only the local logo/favicons replaced with equivalent inline image data**. This is a rendered/in-browser functional test, but not an extracted-archive navigation test.

- 360px / 390px / 768px / 1440px: layout renders, no horizontal page overflow, logo decodes, all three correct links present, no uncaught JavaScript page errors.
- Local share button: displays an explanatory message rather than offering to share an unpublishable URL.
- Keyboard Tab: reaches the skip link.
- `prefers-reduced-motion: reduce`: Canvas hidden and card transforms disabled.
- JavaScript disabled: all three social links remain present as ordinary HTML anchors.
- Static asset resolution: both required image resources exist.
- JavaScript syntax: `node --check` passed.

## Not independently verified

- Authenticity/current availability of the user-provided external social profiles; the user supplied those URLs.
- External app redirects and mobile deep-link opening.
- Native Web Share API behavior on the eventual public HTTPS domain.
- Actual `file://` navigation after ZIP extraction (blocked by this automated browser environment; must test locally).
- Formal lab performance and accessibility audit; visual/behavioral smoke tests only.

## Publication

No deployment or GitHub push performed. There is no verified contact email, so none is displayed. Before production, check all three destinations and add approved domain-specific canonical/OG metadata as described in `README.md`.
