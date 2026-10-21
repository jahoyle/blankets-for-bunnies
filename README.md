# Blankets for Bunnies

A mobile-friendly, build-free event links page based on [the Figma design](https://www.figma.com/design/5BfYXUItZ1voVQx60Lgutn/Sandbox?node-id=551-662).

## Preview locally

Run `python -m http.server 8000 --bind 127.0.0.1` from the repository, then open
`http://127.0.0.1:8000`. No packages, build step, or JavaScript are required.
The supplied Figma artwork is stored locally. The two user-requested image
corrections are described below. The event-site QR code is generated locally,
not fetched from an external QR service.
Relative paths support a GitHub Pages project URL as well as a custom domain.

## Typography

The page uses Aptos Narrow (regular/bold) and QESamRoberts2 when installed,
with system fallbacks; typography varies by device. Consistent typography
would require web-licensed font files or approved alternative web fonts.

The Rabbit Haven, volunteer time, donation, monthly bunny sponsor, Facebook,
Instagram, and Give links use the confirmed destinations. The volunteer and
donation links point to Microsoft's Benevity portal, and Give points to Microsoft
SharePoint; visitors may need to sign in to these services.

About Event opens four pages with Previous/Next navigation and a return to the
links page. Text and blanket steps reflow on narrower screens.
On mobile, transparent side-arrow controls stay at the viewport edges while
scrolling, so readers can navigate without returning to the top or bottom.
The first page's left arrow returns to the home links page. The last page has
only a previous arrow; navigation does not wrap.

| Page | File | Figma node |
| --- | --- | --- |
| Event poster | `about.html` | `547:451` |
| Event information | `event.html` | `649:10332` |
| Blanket instructions | `blanket.html` | `547:483` |
| About Rabbit Haven | `rabbit-haven.html` | `557:1554` |

The last page has a 25-by-23px orange link icon pointing to
`https://www.rabbithaven.org/`, with a 44px touch target.
The separate QR asset, `assets/about/event-site-qr.png`, encodes the approved
event address `https://jahoyle.github.io/blankets-for-bunnies/`. It is retained
for sharing, but no longer displayed on the site. The PNG uses error correction M and a
four-module white quiet zone. If the final hosting address changes, regenerate
the PNG before sharing it.
QR generation/decoding tools are not runtime dependencies.

The step 3 photo's two size digits were corrected locally to read 4-by-4 inches;
the rest of the photo is unchanged. The original is retained as
`assets/about/fleece-corners.png`. Step 6 uses an AI-generated illustration of a
finished blanket, locally retouched to remove the folded corner using the
unfolded portion of the same illustration. It is not a photograph of an actual
event donation. Both image
updates were also applied to the supplied Figma instruction page, preserving
the existing image slots and crop settings.

The footer preserves the supplied icon artwork at its original dimensions,
with equal visible gaps and separate 44px touch targets. The Facebook artwork
is shifted toward Instagram within its target to balance the gaps.

## Hosting and privacy

This repository is public. The page includes `noindex, nofollow` to request that
cooperating search engines not list it; this is **not access control**. Anyone
with its URL can view a published page, and repository contents are public.
Do not put private event information or credentials here.

The live site is hosted at `https://jahoyle.github.io/blankets-for-bunnies/`.
GitHub Pages publishes the root of `main` in this repository; pushes to `main`
automatically update the site. Feature-branch changes are not published until
they reach `main`. There is no expiration date or automatic takedown timer.
