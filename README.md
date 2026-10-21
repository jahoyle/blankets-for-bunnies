# Blankets for Bunnies

A mobile-friendly, build-free event links page based on [the Figma design](https://www.figma.com/design/5BfYXUItZ1voVQx60Lgutn/Sandbox?node-id=551-662).

## Preview locally

Run `python -m http.server 8000 --bind 127.0.0.1` from the repository, then open
`http://127.0.0.1:8000`. No packages, build step, or JavaScript are required.
The supplied Figma artwork is stored locally and unmodified. The event-site QR
code is generated locally, not fetched from an external QR service.
Relative paths support a GitHub Pages project URL as well as a custom domain.

## Content still needed before launch

- Supply web-licensed Aptos Narrow (regular/bold) and QESamRoberts2 font files
  or approve alternative fonts. Currently the page uses these fonts when
  installed, with system fallbacks; typography varies by device.

The Rabbit Haven, volunteer time, donation, monthly bunny sponsor, Facebook,
Instagram, and Give links use the confirmed destinations. The volunteer and
donation links point to Microsoft's Benevity portal, and Give points to Microsoft
SharePoint; visitors may need to sign in to these services.

About Event opens four pages with Previous/Next navigation and a return to the
links page. Text and blanket steps reflow on narrower screens.

| Page | File | Figma node |
| --- | --- | --- |
| Event poster | `about.html` | `547:451` |
| Event information | `event.html` | `649:10332` |
| Blanket instructions | `blanket.html` | `547:483` |
| About Rabbit Haven | `rabbit-haven.html` | `557:1554` |

The last page's QR code encodes the approved address
`https://jahoyle.github.io/blankets-for-bunnies/`. It is also a clickable link.
It will not lead to the event page until GitHub Pages is published.
The PNG uses error correction M and a four-module white quiet zone, and is
displayed at 164px so it remains scannable. If the final hosting address changes,
regenerate the PNG and update its link and alternative text in `rabbit-haven.html`.
QR generation/decoding tools are not runtime dependencies.

The supplied instruction design has one content discrepancy: step 3 says to cut
4-by-4-inch corners, while its reference photo shows a 5-by-5-inch template.
Both are preserved from Figma pending clarification.

The footer preserves the supplied icon artwork at its original dimensions,
with equal visible gaps and separate 44px touch targets. The Facebook artwork
is shifted toward Instagram within its target to balance the gaps.

## Hosting and privacy

This repository is public. The page includes `noindex, nofollow` to request that
cooperating search engines not list it; this is **not access control**. Anyone
with its URL can view a published page, and repository contents are public.
Do not put private event information or credentials here.

GitHub Pages has not been enabled, and there is no automatic deployment workflow,
expiration date, or takedown timer. Once content and destinations are approved,
merge the implementation and enable Pages for the root of `main` in this
repository's settings. Until then, use local previews only.
