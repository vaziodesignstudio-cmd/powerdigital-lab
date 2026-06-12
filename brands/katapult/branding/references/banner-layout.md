# Banner layout reference and production spec — Katapult

Authoritative spec for Katapult ad banners. The **Figma file is the primary source of truth**, above the PDF guidelines. Source: Figma `HgYaoi2oKw63WR0eeGwYhT`, `design-components` (the V1 1:1 and 9:16 templates) and the KAT26014 briefing.

Reference images in this folder: `banner-template-1x1.png`, `banner-template-9x16.png`, `figma-styleguide-overview.png`.

## Source-of-truth values (from Figma, override the PDF)

- Background: `#eaeae8` (warm light gray). Not the PDF's `#f4f4f4`.
- Headline: black `#000000`, font **Aktiv Grotesk SemiBold**. Not Dark Blue, not Oakes Grotesk.
- Accent / logo: Katapult Pink `#ec5370`. (PDF said `#ed5370`; use the Figma value.)
- Disclaimer: Aktiv Grotesk Medium, black.
- Logo: the pink wordmark vector, supplied artwork, never on top of the photo.
- Hero: the hand-holding-phone mockup, a transparent PNG.

Font note: Aktiv Grotesk is licensed and may not load in headless or MCP tooling. When building via tooling, use **Inter** as a stand-in and swap to Aktiv Grotesk in Figma desktop (where it is embedded). Select all text and change the family in one pass.

## Layout zones

Logo, headline (the message), hero mockup, optional disclaimer. The pink uppercase tagline from the template is dropped when a brief tests headline messaging (see KAT26014).

## Composition rules (learned from production)

1. The hero is a transparent PNG, so it must **bleed off a frame edge**, never float with margin all around. Vertical and square formats bleed off the bottom; landscape and short formats bleed off the right (and bottom).
2. Position the hero **high**, right under the headline, so it fills the whitespace. Bigger is better: let the phone dominate the lower two-thirds. In verticals, anchor it to the left (x near 0 or slightly negative).
3. Headline is **confident and large**, scaled to the format. Do not shrink it to tiny sizes on narrow or short pieces. Reference: a 160x600 skyscraper headline reads at about 26px, not 19px.
4. Disclaimer appears on medium and large formats; it is **removed on the smallest leaderboards (320x50 and 728x90)** where it cannot be legible. For those, the legal terms live on the landing page.

## Disclaimer copy (verbatim where used)

> This is an advertisement for a lease-purchase or lease-to-own service. The path to ownership will cost more than the merchant's cash price. Certain items available at participating locations. Not available in MN, NJ, WI, WY.

## IAB sizes (KAT26014 set)

300x250, 300x600, 160x600, 320x480, 480x320, 320x50, 728x90, 970x250. Two messaging iterations per size (V1, V2) = 16 deliverables.

- Vertical (300x600, 160x600, 320x480): logo top-left, headline below, hero high and left-anchored bleeding off the bottom, disclaimer bottom.
- Square / medium rectangle (300x250): logo and headline left, hero bleeding in from the right, disclaimer bottom-left.
- Landscape (480x320, 970x250): text left, hero filling the right and bleeding off right and bottom, disclaimer bottom-left.
- Short leaderboards (728x90, 320x50): logo left, headline beside it, a slice of the phone bleeding from the right, no disclaimer.

## For the agents

- Image Prompt Engineer: reproduce the bleed-and-fill treatment, exact hex values, no filters; the logo is placed artwork, never AI-rendered, never on the photo.
- Ad Creative Strategist: headline carries the tested message; default CTA "Leap Forward" unless a brief says otherwise; carry the disclaimer except on the smallest units.
- Instagram Curator: the 1:1 and 9:16 frames double as Meta creatives.
