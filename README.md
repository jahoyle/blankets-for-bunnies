# Blankets for Bunnies

A mobile-friendly, build-free event links page based on [the Figma design](https://www.figma.com/design/5BfYXUItZ1voVQx60Lgutn/Sandbox?node-id=551-662).

## Preview locally

Run `python -m http.server 8000 --bind 127.0.0.1` from the repository, then open
`http://127.0.0.1:8000`. No packages, build step, or JavaScript are required.
All image assets are local, unmodified exports from the supplied Figma frame.
Relative paths support a GitHub Pages project URL as well as a custom domain.

## Content still needed before launch

- Confirm the final subtitle; the current text is the Figma placeholder.
- Supply the text for the planned About Event page.
- Supply the destinations for Facebook, Instagram, and Give.
- Supply web-licensed Aptos Narrow (regular/bold) and QESamRoberts2 font files
  or approve alternative fonts. Currently the page uses these fonts when
  installed, with system fallbacks; typography varies by device.

The Rabbit Haven, volunteer time, donation, and monthly bunny sponsor buttons
use the confirmed destinations. The volunteer and donation links point to
Microsoft's Benevity portal; visitors may need to sign in there.

Unconfigured links intentionally have no `href`. They expose their unavailable
state to assistive technology and a native tooltip on hover. To activate each
link in `index.html`, add the confirmed `href` and remove `role`, `tabindex`,
`aria-disabled`, `aria-describedby`, and the unavailable `title`. Keep the social
links' `aria-label`. Remove the shared pending-links description and its remaining
references after all destinations are configured.

The footer preserves the supplied icon artwork at its original dimensions.
Its targets are spaced farther apart than the mockup so each has a separate
44px touch target.

## Hosting and privacy

This repository is public. The page includes `noindex, nofollow` to request that
cooperating search engines not list it; this is **not access control**. Anyone
with its URL can view a published page, and repository contents are public.
Do not put private event information or credentials here.

GitHub Pages has not been enabled, and there is no automatic deployment workflow,
expiration date, or takedown timer. Once content and destinations are approved,
merge the implementation and enable Pages for the root of `main` in this
repository's settings. Until then, use local previews only.
