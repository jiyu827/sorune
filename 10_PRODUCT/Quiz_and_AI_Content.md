# Quiz and AI Content

> Merged from two source docs (Quiz v3 + Quiz/UI-Flow v2). Reconcile into a single clean spec when ready.

## Part A — Quiz & AI Content (v3, newest)

=============================

Photo-led onboarding.

Hidden variables: Face Shape, Face Size, Feature Scale, Feature Sharpness, Facial Contrast.

Defines quiz, AI extraction, content generation and output structure.

---

## Part B — UI Flow detail (from Quiz/UI-Flow v2)

======================================

Summary of Changes from v1
--------------------------

Face Styling architecture updated to:\
• Earrings\
• Necklaces\
• Sunglasses\
• Hair Styling\
• Hair Colour\
• Hats & Hair Accessories\
\
Face Styling AI variables updated to:\
• Face Shape\
• Face Size\
• Feature Scale\
• Feature Sharpness\
• Facial Contrast\
\
Onboarding updated from quiz-led to photo-led:\
Face Photo → Body Photo → AI Analysis → Validation Questions → Results

Updated Face Styling Section
----------------------------

Face Styling is generated using:\
Face Shape + Face Size + Feature Scale + Feature Sharpness + Facial Contrast.\
\
User-facing categories:\
1. Earrings\
2. Necklaces\
3. Sunglasses\
4. Hair Styling\
5. Hair Colour\
6. Hats & Hair Accessories

Updated JSON Schema
-------------------

faceStyling:\
- faceShape\
- faceSize\
- featureScale\
- featureSharpness\
- facialContrast\
- earrings\
- necklaces\
- sunglasses\
- hairStyling\
- hairColour\
- hatsAndHairAccessories
