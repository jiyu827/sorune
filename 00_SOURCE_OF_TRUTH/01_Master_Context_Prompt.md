# Master Context Prompt

> **Highest-authority document.** Every AI and contributor reads this first. If
> documents conflict, this wins, then `02_Architecture_Change_Log.md`, then
> everything else. **Status: DRAFT v1 (Claude-consolidated from existing Sorune
> docs and decisions). Review and adjust, then it stands as canonical.**

## What Sorune is

Sorune is a premium personal-styling app. A user uploads a face photo and a body
photo and answers a short validation quiz; Sorune analyses them and returns a
complete **Style Blueprint** — a small set of signature looks plus the styling,
colour and face guidance behind them. The promise: clarity and confidence, not
endless options.

## Brand

- **Mission:** give everyone a clear, personal styling system they can trust.
- **Vision:** the definitive intelligent styling platform — body, colour, face and complete looks in one place.
- **Positioning:** premium, editorial, intelligent; calm and considered, not trend-chasing.
- **Promise:** fewer, better, confident choices that genuinely suit you.

## Core principles

1. **Clarity Over Complexity**
2. **Guidance Over Rules**
3. **Confidence Over Fashion**
4. **Fewer Better Choices**
5. **Real Value Over Content**

## Sorune aesthetic

Editorial elegance, modern minimalism, timeless femininity, premium restraint.
Palette (cool neutral, defined ladder): Porcelain #F4F5F7, Cloud #DDE0E5, Pewter #9197A1, Graphite #4A4F58, Ink #15171B, with one cool signature accent Plum #5E4F66 (used sparingly) and a Mist #C7D2D7 whisper. The brand stays a neutral canvas so each user's analysed colours are the colour. Type: Cormorant Garamond (headings), Inter (body). Full
detail in `15_BRAND/Design_System.md`.

## Product architecture (the five layers)

> Body Shape + Colour Season + Face Styling + Signature Looks + Style Personality *(future)* = Complete Style Blueprint

- **Body Shape** — five shapes: Hourglass, Pear, Inverted Triangle, Rectangle (incl. Athletic), Apple. Garment categories include Tops, Knitwear, Jackets & Coats, Dresses, Skirts, Jeans, Trousers, Swimwear (necklines sit inside garment categories). See `20_SYSTEMS/Body_Shape_System.md`.
- **Colour Season** — twelve seasons, with palette, metals and combinations. See `20_SYSTEMS/Colour_System.md`.
- **Face Styling** — outputs: Earrings, Necklaces, Sunglasses, Hair Styling, Hair Colour, Hats & Hair Accessories. Hidden variables: Face Shape, Face Size, Feature Scale, Feature Sharpness, Facial Contrast. See `20_SYSTEMS/Face_Styling_System.md`.
- **Signature Looks** — complete looks, not modular garments. See `20_SYSTEMS/Signature_Look_Library.md`.
- **Style Personality** — future layer.

## Recommendation architecture

Every recommendation uses the tiers **Top Pick · Best Styles · Style With Care ·
Your Choice**, ranked **Modern → Stylish → Flattering** (never inverted). The
engine logic is `10_PRODUCT/Recommendation_Engine.md`.

## Onboarding (MVP scope — Decision 002)

Face Photo → Body Photo → AI Analysis → Validation Questions → Results. Photo
analysis of both face and body is in scope.

## Image architecture

Complete-look imagery, not isolated garments. Editorial, brand-palette
backgrounds. See `50_IMAGES/`.

## AI rules

All recommendations are generated from the user's Profile (Body Shape + Colour
Season + Face Styling + preferences) via the Recommendation Engine. Hidden
variables stay behind the scenes; users see finished, warm, plain-language
guidance. No new structure or renaming without a logged decision.

## Future expansion (must inherit this architecture)

Wardrobe Planning, Shopping Assistant, Outfit Builder, Beauty Blueprint, Travel
Packing — all consume the same Profile, tiers and engine.

## What not to change without a logged decision

The five layers; the five body shapes; the twelve seasons; the six face-styling
categories and five hidden variables; the four recommendation tiers; the
Modern → Stylish → Flattering priority; the complete-look principle.
