# Face Styling Recommendation Library

> **Status: DRAFT v1 (Claude-drafted from Sorune architecture). Reconcile against the prototype.**
> Companion to `Face_Styling_System.md`. This is the lookup the engine reads to
> produce face-styling recommendations in each of the six categories, using the
> tiers **Top Pick · Best Styles · Style With Care · Your Choice**.

## How to read this

Each category lists the styling levers and what to recommend by the relevant
hidden variable (Face Shape, Scale, Sharpness, Contrast). The engine selects the
entries matching the user's variables and ranks them Modern → Stylish → Flattering.

## 1. Earrings

**Levers:** shape, length, scale, metal.
- **Round / Oblong faces — Top Pick:** angular or elongating drops (round) vs. studs/short rounds (oblong to add width).
- **Square / Sharp features — Best Styles:** hoops, curved, organic shapes to soften.
- **Heart — Top Pick:** teardrop / wider-at-base.
- **Scale:** delicate features → fine studs/threaders; bold features/large face → statement drops/hoops. Tiny pieces on a large face are **Style With Care**.
- **Contrast:** high → bold stones/colour; low → tonal/metal-only.

## 2. Necklaces

**Levers:** length, neckline interaction, pendant scale.
- **Round / shorter neck — Top Pick:** longer (V/Y) necklaces to lengthen. **Style With Care:** chokers.
- **Long / oblong — Best Styles:** shorter, layered, or collar lengths to add width.
- **Scale:** match pendant scale to feature scale and to the garment neckline (see Body Shape necklines).
- **Coordinate** with the top's neckline from `Body_Shape_System.md` so the engine doesn't recommend a pendant that fights the neckline.

## 3. Sunglasses (frames)

**Levers:** frame shape, width, scale.
- **Round — Top Pick:** angular/rectangular/geometric frames.
- **Square — Top Pick:** round/oval frames to soften.
- **Heart — Best Styles:** bottom-heavy or rounded frames; light colours.
- **Oblong — Best Styles:** taller/wider frames to shorten the face.
- **Rule of width:** frames should be as wide as (or slightly wider than) the widest part of the face. Narrow frames on a large face are **Style With Care**.

## 4. Hair Styling

**Levers:** volume placement, length lines, fringe.
- **Round — Top Pick:** height at the crown, length past the chin, side parts; **Style With Care:** blunt chin-length bobs that widen.
- **Square — Best Styles:** soft layers around the jaw, waves; **Style With Care:** blunt jaw-length cuts.
- **Heart — Best Styles:** volume at the jaw (lobs, layers ending below the chin); side-swept fringe.
- **Oblong — Top Pick:** width at the sides, fringe to shorten; **Style With Care:** long straight centre-part length.
- **Diamond — Best Styles:** fullness at forehead and jaw; chin-length styles.
- **Scale/Sharpness:** softer features suit waves; sharp features carry sleek/blunt lines.

## 5. Hair Colour

**Levers:** depth, warmth, contrast — coordinate with **Colour Season**.
- Driven primarily by `Colour_System.md` (undertone, value, contrast). The face system adds: keep hair-to-skin contrast in line with **Facial Contrast** (high-contrast people carry bold colour shifts; low-contrast suit tonal, blended colour).
- **Style With Care:** colour choices that push the user far outside their season's contrast level.

## 6. Hats & Hair Accessories

**Levers:** brim/scale, proportion to face size.
- **Scale:** match brim and accessory scale to Face Size — large face carries wide brims (Top Pick); small face → smaller proportions, wide brims are **Style With Care**.
- **Shape:** structured/angular for soft faces wanting definition; rounded/soft for sharp faces wanting softness.

## Conflicts

When a face-styling pick conflicts with a Colour or Body recommendation (e.g.
metal/colour), defer to the engine's Conflict Resolution Rules in
`10_PRODUCT/Recommendation_Engine.md`.
