# Body Shape Styling System

> **Status: DRAFT v1 (Claude-drafted from Sorune architecture). Reconcile against the prototype** — where the prototype already encodes rules, the prototype wins; update this doc to match and log it in the Change Log.
>
> **Source of truth:** `00_SOURCE_OF_TRUTH/01_Master_Context_Prompt.md`. Uses the Sorune recommendation tiers and the Modern → Stylish → Flattering priority.

## Purpose

Defines how Sorune turns a user's body shape into garment recommendations. The
Recommendation Engine reads this system, combines it with Colour Season and Face
Styling, and produces the user's Blueprint.

## The five body shapes

Athletic is merged into Rectangle (per Master Context). Shapes are assigned from
the body photo + validation questions.

| Shape | Defining balance |
|---|---|
| **Hourglass** | Shoulders and hips balanced; clearly defined waist. |
| **Pear** | Hips wider than shoulders; waist defined; weight carried below. |
| **Inverted Triangle** | Shoulders/bust wider than hips; straighter waist. |
| **Rectangle** | Shoulders, waist and hips similar; little waist definition (includes Athletic). |
| **Apple** | Weight carried around the midsection; fuller waist; often slimmer legs. |

## Recommendation tiers (used for every category)

- **Top Pick** — the single strongest choice for this shape.
- **Best Styles** — reliably flattering options.
- **Style With Care** — can work with adjustment; note the condition.
- **Your Choice** — neutral; personal preference, no shape penalty.

## Universal styling goal

Every shape is styled to create **balance and a defined vertical line** in a way
that reads Modern first, Stylish second, Flattering third — never the reverse.
We guide, we don't issue rules ("Guidance Over Rules").

## Garment categories covered per shape

Tops · Knitwear · Necklines · Sleeves · Jackets & Coats / Outerwear · Dresses ·
Skirts · Jeans · Trousers · Shorts · Swimwear, plus a **Start Here** priority and
an **Educational Copy** angle.

---

## Hourglass

**Shape summary.** Balanced shoulders and hips with a clearly defined waist. The
styling goal is to follow the natural waistline and avoid anything that hides it.

**Start here priorities.** Define the waist; keep proportions clean; avoid bulk
that squares off the silhouette.

- **Tops — Top Pick:** fitted or semi-fitted that follow the waist (wrap, fitted knit). **Style With Care:** boxy/oversized (hide the waist) — works belted or front-tucked.
- **Knitwear — Best Styles:** fine-gauge, body-skimming; tuck or half-tuck.
- **Necklines — Best Styles:** V-neck, scoop, sweetheart (open the upper body).
- **Sleeves — Your Choice:** most work; avoid heavy structured shoulders that widen the top.
- **Jackets & Coats — Top Pick:** waist-defined (belted, single-button nip, wrap coats). **Style With Care:** boxy/straight cuts — belt them.
- **Dresses — Top Pick:** wrap and fit-and-flare. **Best Styles:** bodycon, sheath.
- **Skirts — Best Styles:** pencil, A-line from the waist, bias.
- **Jeans/Trousers — Best Styles:** high or mid-rise that sit at the natural waist; straight and bootcut.
- **Shorts — Best Styles:** high-rise tailored.
- **Swimwear — Top Pick:** waist-defining one-pieces, high-waist two-pieces.
- **Educational copy:** "Your shape is naturally balanced — the styling job is simply to let your waist show."

## Pear

**Shape summary.** Hips wider than shoulders with a defined waist. Goal: add
visual interest and breadth to the upper body, keep the lower half clean and
elongating.

**Start here priorities.** Draw the eye up; structure the shoulder line; keep
lower-body lines simple and dark/streamlined where wanted.

- **Tops — Top Pick:** detail at the shoulder/neckline (boat necks, structured shoulders, statement sleeves, lighter colours up top). **Best Styles:** tops ending at the hip bone or longer (past the widest point).
- **Knitwear — Best Styles:** texture, horizontal interest, or colour up top.
- **Necklines — Best Styles:** boat, square, off-shoulder (widen the shoulder line).
- **Sleeves — Top Pick:** puff, structured, statement.
- **Jackets & Coats — Best Styles:** structured shoulders; length that clears the hip or hits mid-thigh. **Style With Care:** jackets ending at the widest hip point.
- **Dresses — Top Pick:** fit-and-flare, A-line, wrap (defines waist, skims hip).
- **Skirts — Best Styles:** A-line, full, dark streamlined pencil.
- **Jeans/Trousers — Best Styles:** straight and bootcut to balance the hip; mid/high rise; darker washes if a streamlined look is wanted. **Style With Care:** skinny with a fitted top (emphasises contrast) — balance with volume up top.
- **Shorts — Style With Care:** very short/tight — choose a relaxed tailored cut.
- **Swimwear — Top Pick:** detailed/patterned tops with plain bottoms; higher-cut legs to lengthen.
- **Educational copy:** "We add a little structure and interest up top so your overall silhouette reads balanced top to bottom."

## Inverted Triangle

**Shape summary.** Shoulders/bust broader than hips. Goal: soften the upper body
and add volume and interest to the lower half.

**Start here priorities.** Soften shoulders; add lower-body volume; create a waist.

- **Tops — Top Pick:** softer shoulders, V-necks, simple fabrics that drape. **Style With Care:** structured shoulders, halters, heavy embellishment up top.
- **Knitwear — Best Styles:** fine, draping; avoid chunky shoulder detail.
- **Necklines — Top Pick:** V-neck and scoop (lengthen and narrow the upper body).
- **Sleeves — Best Styles:** set-in, simple; avoid puff/structured shoulders.
- **Jackets & Coats — Best Styles:** single-breasted, soft shoulder, longer line; **Style With Care:** strong-shouldered blazers.
- **Dresses — Top Pick:** fit-and-flare, A-line with detail below the waist.
- **Skirts — Top Pick:** A-line, pleated, full, patterned (add lower volume).
- **Jeans/Trousers — Best Styles:** wide-leg, flare, bootcut, lighter washes and detail below.
- **Shorts — Best Styles:** relaxed, A-line, patterned.
- **Swimwear — Top Pick:** plain supportive tops with detailed/higher-cut bottoms.
- **Educational copy:** "We balance your strong shoulder line by adding a little softness up top and interest below."

## Rectangle (includes Athletic)

**Shape summary.** Shoulders, waist and hips fall in a similar line with little
waist definition. Goal: create the illusion of a waist and curves.

**Start here priorities.** Build a waist; add curve and dimension; use definition
and layering.

- **Tops — Top Pick:** peplum, wrap, ruched, belted; anything that suggests a waist. **Best Styles:** crop/tuck to break the vertical line.
- **Knitwear — Best Styles:** belted or fitted; texture for dimension.
- **Necklines — Your Choice:** broad latitude; scoop/sweetheart add softness.
- **Sleeves — Best Styles:** detail welcome (puff, ruffle) to add dimension.
- **Jackets & Coats — Top Pick:** belted and waist-defined; **Best Styles:** double-breasted for dimension.
- **Dresses — Top Pick:** wrap, belted, fit-and-flare, peplum.
- **Skirts — Best Styles:** full, pleated, A-line, bias; pair with a defined waist.
- **Jeans/Trousers — Your Choice:** most cuts work; high-rise + tuck builds shape.
- **Shorts — Your Choice:** broad latitude; paperbag/belted adds a waist.
- **Swimwear — Best Styles:** cut-outs, belts, colour-blocking to suggest a waist.
- **Educational copy:** "Your frame is a clean canvas — a little waist definition and dimension is all it takes."

## Apple

**Shape summary.** Weight carried around the middle, fuller waist, often slimmer
legs. Goal: elongate the torso, draw attention to legs and neckline, skim the
midsection.

**Start here priorities.** Elongate vertically; create an empire/under-bust line;
show off legs and décolletage; skim, don't cling, at the waist.

- **Tops — Top Pick:** flowing, empire-line, V-neck, longline that skims. **Style With Care:** clingy fabrics at the waist; tight waistbands.
- **Knitwear — Best Styles:** fine, longline, V-neck; layered open cardigans for a vertical line.
- **Necklines — Top Pick:** V-neck and scoop (open and lengthen).
- **Sleeves — Your Choice:** most work; 3/4 length keeps proportions tidy.
- **Jackets & Coats — Best Styles:** open, longline, vertical lines; **Style With Care:** belted-tight-at-waist.
- **Dresses — Top Pick:** empire, A-line, wrap that ties above the natural waist or skims it.
- **Skirts — Best Styles:** A-line, flowing, mid-rise that sits comfortably.
- **Jeans/Trousers — Best Styles:** mid-rise straight and bootcut; show off slimmer legs; avoid tight waistbands.
- **Shorts — Best Styles:** mid-rise tailored that show leg.
- **Swimwear — Top Pick:** one-pieces with ruching/vertical detail; tankinis; high-leg to lengthen.
- **Educational copy:** "We lengthen your torso and put the spotlight on your neckline and legs, keeping everything easy through the middle."

---

## How this feeds the engine

For any garment the user views, the engine looks up the (shape × category) entry
above, assigns the tier (Top Pick / Best Styles / Style With Care / Your Choice),
and combines it with Colour Season and Face Styling per
`10_PRODUCT/Recommendation_Engine.md`. Conflicts are resolved by the engine's
Conflict Resolution Rules.

## Open items to confirm against the prototype

- Exact garment categories and their order (Master lists Tops, Knitwear, Jackets & Coats, Dresses, Skirts, Jeans, Trousers, Swimwear; this doc also details Necklines, Sleeves, Shorts, Outerwear — confirm which are first-class categories).
- Whether "Style With Care" surfaces the adjustment text to users or only internally.
- Any brand-specific rules already encoded in the prototype.
