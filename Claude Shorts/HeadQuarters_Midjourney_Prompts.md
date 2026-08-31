# Head Quarters — Pixar Style Lock + Midjourney Character Prompts

**CANONICAL STYLE, as of this revision: the flat 2D "Nano House Style" section near the bottom of this document.** REPTILE is locked in that style and confirmed working; LIMBIC, CORTEX, DMN, and PFCL already have matching prompts written there, ready to run. The 3D Pixar prompts below (the original draft) produced one genuinely good LIMBIC render but are being kept as reference/alternate only — the flat 2D style better fits the satirical, "South Park of the brain" tone the show is aiming for, and is what's been deliberately chosen for the full cast.

*Paste the Style Lock block at the front of every character prompt below to keep all five visually consistent — same render engine, same lighting, same info-sheet layout. This mirrors the "FINAL.png" character sheets used for The Quadriune, just in a Pixar/3D-cartoon register instead of pseudo-realistic.*

---

## STYLE LOCK (prepend to every prompt)

```
Pixar / DreamWorks-style 3D animated character information sheet, full character turnaround render, soft volumetric studio lighting with warm rim light, subsurface scattering on skin, large expressive eyes, rounded simplified forms, exaggerated friendly proportions, vibrant saturated color palette, clean flat-color UI background panels styled like a friendly dashboard (not military or clinical), bold rounded sans-serif name lockup, small stat-readout graphics, color swatch strip, single dominant prop icon, silhouette icon in corner, high-end animation studio render quality, professional character design sheet, soft ambient occlusion, no text errors, ar 16:9, v 6
```

---

## REPTILE — "THE BRAINSTEM"
**Accent color:** `#8BC34A` (green)

```
[STYLE LOCK] + a squat broad-shouldered cartoon creature built like a fire hydrant with attitude, low center of gravity, stubby powerful legs, oversized forearms, perpetually crouched, skin textured like a well-loved warm leather baseball mitt (not literally scaled or reptilian), wearing a sleeveless hide vest that looks slightly too small, snack visibly stuffed in one pocket, a couple of proud little scars, big blunt teeth in a confident almost-smile, beady alert eyes that read as always-scanning, sitting in a low nest made of repurposed office supplies, green accent color #8BC34A on UI panels and name lockup, name lockup "REPTILE" subtitle "THE BRAINSTEM"
```

---

## LIMBIC — "THE LIMBIC SYSTEM"
**Accent color:** `#EC407A` (pink)

```
[STYLE LOCK] + a round soft plush-toy-proportioned cartoon creature, big saucer eyes on a hair trigger, expressive high eyebrows, wrapped in an oversized cozy cardigan-poncho with sleeves flopping past the hands, slightly static-charged hair as if just startled, clutching a tote bag overflowing with mismatched emergency supplies (flashlight, single mitten, photographs), warm pink and peach color palette, sitting inside a blanket fort, pink accent color #EC407A on UI panels and name lockup, name lockup "LIMBIC" subtitle "THE LIMBIC SYSTEM"
```

---

## CORTEX — "THE NEOCORTEX"
**Accent color:** `#29B6F6` (blue)

```
[STYLE LOCK] + a tall reedy all-elbows cartoon character in an oversized lab coat with double-cuffed sleeves, glasses sliding down the nose with a second pair of reading glasses pushed up on the forehead, three clipped pens in the coat pocket, deliberately-tousled hair, surrounded by floating holographic charts and graphs conjured mid-explanation, an absurdly oversized coffee mug, standing at a clean standing desk with three monitors, cool blue and white color palette, blue accent color #29B6F6 on UI panels and name lockup, name lockup "CORTEX" subtitle "THE NEOCORTEX"
```

---

## DMN — "THE DEFAULT MODE NETWORK"
**Accent color:** `#D8A657` (gold)

```
[STYLE LOCK] + a wispy slightly translucent cartoon character who looks like she is gently drifting rather than standing, oversized cardigan-shawl the color of an old library book, an oversized beret sliding over one eye, holding an open journal, orbited by a soft halo of floating sticky notes and photographs like a tiny solar system of memory, thousand-yard-stare eyes, muted gold and sepia color palette with a soft dreamlike glow, sitting in a dim cozy corner with warm fairy lights, gold accent color #D8A657 on UI panels and name lockup, name lockup "DMN" subtitle "THE DEFAULT MODE NETWORK"
```

---

## PFCL — "THE PREFRONTAL CORTEX"
**Accent color:** `#FFA726` (orange)

```
[STYLE LOCK] + a visibly exhausted cartoon character who is clearly the only adult in the room, slightly rumpled business-casual blazer with sleeves pushed up, reading glasses on a chain being polished, holding a whiteboard marker like a sword in one hand and a half-destroyed stress ball in the other, big expressive explaining-hand-gestures pose, one single visible stress-streak in otherwise tidy hair, standing in front of a whiteboard covered in frameworks with increasingly desperate titles, warm orange and amber color palette, orange accent color #FFA726 on UI panels and name lockup, name lockup "PFCL" subtitle "THE PREFRONTAL CORTEX"
```

---

### Notes for Randy
- Accent colors intentionally match the title-card colors already locked for The Quadriune reel — useful if the two properties ever cross-reference each other, and just good color-coding hygiene either way.
- These prompts assume Midjourney v6 with a still-frame "information sheet" output, same pattern as the `CORTEX FINAL.png` / `PFCL FINAL.png` / `DMN FINAL.png` assets from The Quadriune. If you'd rather generate clean single-pose turnarounds instead of infographic sheets, drop the "information sheet" / "stat-readout" / "UI panel" language from the Style Lock and keep the rest.
- Once you have a FINAL.png per character, send them over and I'll move to the ElevenLabs voice scripts and then the Kling element binding pipeline, same as last time.

---

## ChatGPT / GPT Image — Adapted Prompts

*ChatGPT's image model ignores Midjourney's `--ar` / `--v` flags and tends to do better with plain descriptive sentences instead of comma-stacked keywords. Same five characters, same style, rewritten for that engine.*

**STYLE LOCK (carry this description into every character prompt):**
```
A Pixar/DreamWorks-style 3D animated character information sheet, shown as a full character turnaround render. Soft volumetric studio lighting with a warm rim light, subsurface scattering on the skin, large expressive eyes, rounded simplified forms, and exaggerated friendly proportions. The background is a clean, flat-color UI panel styled like a friendly dashboard, not military or clinical. Include a bold rounded sans-serif name lockup, small stat-readout graphics, a color swatch strip, one dominant prop icon, and a silhouette icon in the corner. Render quality should look like a high-end animation studio's official character design sheet, with soft ambient occlusion and clean, error-free text. Horizontal widescreen composition.
```

**REPTILE — "THE BRAINSTEM"** (accent color: green, #8BC34A)
```
[STYLE LOCK] The character is a squat, broad-shouldered cartoon creature built like a fire hydrant with attitude — low center of gravity, stubby powerful legs, oversized forearms, perpetually crouched. Skin is textured like a well-loved warm leather baseball mitt, not literally scaled or reptilian. He wears a sleeveless hide vest that looks slightly too small, with a snack visibly stuffed in one pocket and a couple of proud little scars. He has big blunt teeth in a confident almost-smile and beady, always-scanning eyes. He sits in a low nest made of repurposed office supplies. Use green (#8BC34A) as the accent color on the UI panels and name lockup. The name lockup reads "REPTILE" with the subtitle "THE BRAINSTEM."
```

**LIMBIC — "THE LIMBIC SYSTEM"** (accent color: pink, #EC407A)
```
[STYLE LOCK] The character is a round, soft, plush-toy-proportioned cartoon creature with big saucer eyes on a hair trigger and expressive high eyebrows. She's wrapped in an oversized cozy cardigan-poncho with sleeves flopping past her hands, and her hair looks slightly static-charged, like she just had a scare. She clutches a tote bag overflowing with mismatched emergency supplies — a flashlight, a single mitten, photographs. The palette is warm pink and peach, and she sits inside a blanket fort. Use pink (#EC407A) as the accent color on the UI panels and name lockup. The name lockup reads "LIMBIC" with the subtitle "THE LIMBIC SYSTEM."
```

**CORTEX — "THE NEOCORTEX"** (accent color: blue, #29B6F6)
```
[STYLE LOCK] The character is tall, reedy, and all elbows, wearing an oversized lab coat with double-cuffed sleeves. His glasses are sliding down his nose, with a second pair of reading glasses pushed up on his forehead, and three pens are clipped to his coat pocket. His hair looks deliberately tousled. He's surrounded by floating holographic charts and graphs conjured mid-explanation, holding an absurdly oversized coffee mug, standing at a clean standing desk with three monitors. The palette is cool blue and white. Use blue (#29B6F6) as the accent color on the UI panels and name lockup. The name lockup reads "CORTEX" with the subtitle "THE NEOCORTEX."
```

**DMN — "THE DEFAULT MODE NETWORK"** (accent color: gold, #D8A657)
```
[STYLE LOCK] The character is wispy and slightly translucent, looking like she's gently drifting rather than standing. She wears an oversized cardigan-shawl the color of an old library book and an oversized beret sliding over one eye, holding an open journal. She's orbited by a soft halo of floating sticky notes and photographs, like a tiny solar system of memory, and her eyes carry a thousand-yard stare. The palette is muted gold and sepia with a soft dreamlike glow, and she sits in a dim cozy corner with warm fairy lights. Use gold (#D8A657) as the accent color on the UI panels and name lockup. The name lockup reads "DMN" with the subtitle "THE DEFAULT MODE NETWORK."
```

**PFCL — "THE PREFRONTAL CORTEX"** (accent color: orange, #FFA726)
```
[STYLE LOCK] The character is visibly exhausted and clearly the only adult in the room. He wears a slightly rumpled business-casual blazer with sleeves pushed up, reading glasses on a chain that he's polishing, and holds a whiteboard marker like a sword in one hand and a half-destroyed stress ball in the other. He's mid-gesture with big, expressive "explaining to a toddler" hand movements, with one single visible stress-streak in otherwise tidy hair. He stands in front of a whiteboard covered in frameworks with increasingly desperate titles. The palette is warm orange and amber. Use orange (#FFA726) as the accent color on the UI panels and name lockup. The name lockup reads "PFCL" with the subtitle "THE PREFRONTAL CORTEX."
```

**Heads-up on ChatGPT specifically:** it sometimes simplifies busy "information sheet" prompts like these into a single clean character pose rather than a full infographic layout, and it's pickier than Midjourney about things like "stress-streak" or sharp-edged props (whiteboard marker "like a sword"). If a generation comes back flattened or missing the UI-panel layout, regenerate and ask explicitly to keep the dashboard background and stat graphics. Otherwise, treat the simplified version as a fine fallback if the full sheet won't render — a clean single-pose turnaround works for the pipeline either way.

---

## Nano "House Style" — Locked Prompts

*Through trial and error on REPTILE, this is the formula that actually works in Nano: flat 2D cartoon color, bold clean outline on the character, thinner linework on background clutter, a soft contact shadow anchoring the character to the floor, one small flat highlight dot on rounded surfaces for volume, and clear front-to-back layering of background objects (some overlapping in front of the character, some pushed back and drawn smaller behind). No photoreal render language anywhere — that's what caused the original schism into realism. REPTILE is the locked reference for this style; the four below are written to match it exactly.*

**STYLE LOCK (carry into every prompt):**
```
A flat-color 2D cartoon illustration in a clean comic/animated-series style — bold consistent black outlines on the main character, thinner linework on background objects, flat color fills with minimal shading, no photorealistic skin or lighting, not 3D rendered, not a photograph. The character has a soft flat-colored contact shadow directly beneath it to anchor it to the ground, and one small flat white highlight dot on rounded surfaces (head, props) to suggest volume without gradient shading. Background clutter is staged with clear front-to-back layering — some objects overlap in front of the character, others are pushed back and drawn slightly smaller behind it. Top-right corner has a bold rounded color-block name lockup with the character name in large bold black text and the subtitle beneath it in smaller black text.
```

**LIMBIC — "THE LIMBIC SYSTEM"** (accent color: pink, #EC407A)
```
[STYLE LOCK] The character is LIMBIC: round, soft, plush-toy proportioned, with big saucer eyes set wide and high, dramatic eyebrows doing most of the emotional expression, a slightly worried half-smile. She wears an oversized cardigan-poncho with sleeves flopping past her hands, in warm pink and peach flat tones. She clutches a tote bag overflowing with mismatched items — a flashlight handle and a photograph corner sticking out. She sits inside a blanket fort: some blankets and pillows overlap in front of her lower body, while string lights and photographs pinned to a back wall are drawn smaller and pushed behind her. Pink (#EC407A) name lockup box, top-right corner, reading "LIMBIC" with subtitle "THE LIMBIC SYSTEM."
```

**CORTEX — "THE NEOCORTEX"** (accent color: blue, #29B6F6)
```
[STYLE LOCK] The character is CORTEX: tall, thin, all elbows, standing in a confident lean. He wears an oversized lab coat with double-cuffed sleeves in cool blue and white flat tones, glasses sliding down his nose, a second pair of reading glasses pushed up on his forehead, three pens clipped to his coat pocket. He holds an absurdly oversized coffee mug. Small flat-colored chart and graph shapes float beside his raised hand, overlapping in front of his sleeve. Behind him, a standing desk with three monitors is drawn smaller and set back, with a corkboard and tangled string visible further back still. Blue (#29B6F6) name lockup box, top-right corner, reading "CORTEX" with subtitle "THE NEOCORTEX."
```

**DMN — "THE DEFAULT MODE NETWORK"** (accent color: gold, #D8A657)
```
[STYLE LOCK] The character is DMN: wispy and slightly soft-edged, in a calm half-drifting pose rather than a firm stance. She wears an oversized cardigan-shawl in muted gold and sepia tones and a beret sliding over one eye, holding an open journal against her chest. A few small sticky notes and photographs float just in front of her shoulder, overlapping her silhouette, while more are scattered smaller and further back near a string of fairy lights against the back wall. Her eyes have a calm, distant half-lidded look. Gold (#D8A657) name lockup box, top-right corner, reading "DMN" with subtitle "THE DEFAULT MODE NETWORK."
```

**PFCL — "THE PREFRONTAL CORTEX"** (accent color: orange, #FFA726)
```
[STYLE LOCK] The character is PFCL: standing with tired but determined posture, clearly the most put-together figure in the room and clearly exhausted by the effort. He wears a slightly rumpled business-casual blazer with sleeves pushed up, in warm orange and amber flat tones, reading glasses on a chain around his neck. He holds a whiteboard marker raised in one hand and a half-dented stress ball in the other, both overlapping in front of his body. Behind him, a whiteboard covered in small diagram shapes and increasingly desperate framework titles is drawn smaller and set back against the wall. One small flat highlight streak in his otherwise tidy hair. Orange (#FFA726) name lockup box, top-right corner, reading "PFCL" with subtitle "THE PREFRONTAL CORTEX."
```

### Notes for Randy
- These four are deliberately written to mirror REPTILE's winning formula line for line — same shadow/highlight/layering instructions, just swapped to each character's visual details from the bible.
- If any of these drift back toward realism, the likely culprit is a noun that reads as "real" to Nano (the way "scars" and "leather" did for REPTILE) — flag it and we'll swap it for a flatter, more cartoon-coded word.
- Once you've got a locked image per character, send them over and we'll move into voice casting and the Kling binding step, same pipeline as before.

---

## World Establishing Shot — Locked Prompt

*This is the wide Control Room shot, the platform all five characters live inside, anchoring the house style at the scene level instead of just per-character. Based on the two Gemini test renders, which nailed the comedic energy (the corkboard conspiracy board, the labeled emergency kit, the framed "Blank Stare" art, the whiteboard frameworks) but had two recurring AI text bugs: garbled readout labels and duplicate floating zone labels. Both are explicitly called out below to fix on the next pass.*

```
A flat-color 2D cartoon illustration in a clean comic/animated-series style — bold consistent black outlines on foreground elements, thinner linework on background clutter, flat color fills with minimal shading, no photorealistic lighting, not 3D rendered, not a photograph.

Wide establishing shot of "The Control Room" — mission control crossed with the world's worst-run open-plan office. The room has five distinct territories, each clearly staged with front-to-back layering and consistent scale:

REPTILE's corner: a low nest made of repurposed office supplies (boxes, cables, an old keyboard), REPTILE sitting in it, a hand-lettered "DO NOT TOUCH" sign nearby. Exactly one "DO NOT TOUCH" sign — do not duplicate it.

CORTEX's station: a standing desk with three monitors, a corkboard behind it with red string connecting exactly two sticky notes, spelled exactly as written and no others added: one reading "Quantum Entanglement" and one reading "Tuesday Afternoon Slump" (double-check the spelling of "Tuesday," it must not be misspelled). A coffee mug sits on the desk. Wall-mounted readout screens show short clean readable labels: "Heart Rate," "Cortisol Surge," "Neural Chatter," each with a simple graph line beneath it. Keep all readout text short and spelled correctly, no garbled words, and do not add any additional sticky notes, labels, or readouts beyond the ones listed here.

LIMBIC's nest: a blanket fort with string lights, family photographs pinned to the inside wall, and a labeled "Emergency Kit" box nearby containing exactly three absurd item labels, each appearing once and only once: "Rubber Duck," "Pickle Jar," and one more invented absurd item of your choosing. No item label may repeat.

DMN's corner: a dim, cozy space with fairy lights, an open journal, floating sticky notes, and one small framed piece of wall art with the readable caption "The Blank Stare."

The Central Table: where PFCL would run meetings — a table with scattered coffee cups and snacks, facing a whiteboard covered in small diagram shapes and a few short, readable increasingly-desperate framework titles like "Ultimate Efficiency v3.0" and "How to Not Implode."

The image must contain exactly five zone labels in total, no more and no fewer, one per character: a single label reading "REPTILE," a single label reading "CORTEX," a single label reading "LIMBIC," a single label reading "DMN," and a single label reading "PFCL." Each of these five words must appear exactly once in the entire image, as a label anchored to that character's own territory. Do not let any of these five words appear a second time anywhere else in the image, including near a different character's territory. All on-image text must be short, legible, and spelled correctly.
```

### Notes for Randy
- The two recurring bugs to watch for on regeneration: garbled readout text ("Unexplained Emetional Bipp" instead of "Emotional Blip") and duplicate zone labels. Both are called out explicitly in the prompt above; if they recur, it's likely a Gemini text-rendering limit rather than a prompt-wording issue, and may need a manual touch-up pass instead of a pure regenerate.
- Once this is locked, it's worth treating as the official background plate, individual character sheets are for casting/binding, this is the platform they all live inside, useful for wides, transitions, or a "tour of the room" cold open shot.
