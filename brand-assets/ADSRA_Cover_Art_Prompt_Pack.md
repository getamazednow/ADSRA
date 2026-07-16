# ADSRA — Cover Art Prompt Pack

Photoreal, cinematic, **restrained corporate-consulting** cover art (McKinsey / BCG / Bain feel) for the ADSRA artefacts, locked to the Getamazednow AI brand palette. Paste any prompt below into your image AI (Midjourney, DALL·E 3, Adobe Firefly, Ideogram, etc.). Each is text-free by design so it works as a reusable cover, slide background or section divider.

Once you pick the winners, send them back and I'll crop to the exact ratios, apply the Ink scrim for title legibility, and wire them into the White Paper, Technical Reference and deck via the localisation note.

---

## 1. The house style (reuse on every prompt)

Append this **style block** to any subject line so every image stays on-brand and coherent as a set:

> *Restrained corporate consulting report cover in the style of McKinsey, BCG and Bain — sophisticated, abstract, editorial, minimal, with generous negative space and a single clear conceptual focal element. Photorealistic, cinematic low-key studio lighting, soft volumetric light, shallow depth of field, subtle film grain, premium and calm. Colour palette strictly limited to deep charcoal-teal (#2A363B) background, muted steel-blue (#5FA8CC and #2E7DA6) accents, and a warm muted gold (#A8A17B) highlight used sparingly; soft white key light. Dark, low-key, moody, high detail, 8k.*

**Palette lock (give these to the model if it accepts colours):** background `#2A363B`, deep base `#1C1F21`, accent blue `#5FA8CC` / `#2E7DA6`, gold highlight `#A8A17B`, white key light `#FFFFFF`. No other colours.

**Always avoid (negative prompt):**
> *text, letters, words, logos, watermarks, UI, HUD, neon, cyberpunk, rainbow colours, oversaturation, flat vector, clip-art, cartoon, 3D render look, busy patterns, clutter, stock businesspeople, cheesy waving flags, lens flare overload.*

**Title-safe rule.** Ask for empty negative space where the title goes: **lower-left third** for documents, **left half** for slides. Or generate full-frame and I'll add the Ink scrim on my side.

**Aspect ratios to request:**

| Use | Ratio | Midjourney |
|---|---|---|
| Document cover hero (W2 card) | 16:10 | `--ar 16:10` |
| Slide title background | 16:9 | `--ar 16:9` |
| Favicon / thumbnail crop | 1:1 | `--ar 1:1` |

**Midjourney tail to reuse:** `--ar 16:9 --style raw --stylize 250 --chaos 8 --quality 2`
(Lower `--stylize` = more literal/restrained; raise `--chaos` only if you want more variety across the 4 grid options.)

---

## 2. The concepts (eight, each mapped to ADSRA)

Each concept = a **subject line** + the house style block above + the negative prompt. I've written the subject line in the moody, single-focal, negative-space way that reads as a consulting cover.

### C1 · Sovereign vault
*A single monolithic dark vault door, subtly ajar, isolated in deep charcoal-teal space, one warm gold seam of light tracing its edge, volumetric haze, vast negative space around it.*
Story: control and custody — who can open what. Strong, iconic, boardroom-serious.

### C2 · Sovereign horizon (control plane)
*An abstract minimalist horizon of three luminous horizontal strata dissolving into dark mist — a diffuse upper layer, a single sharp gold dividing line of light, and a solid grounded base — cinematic atmosphere, immense empty sky above for a title.*
Story: cloud/AI above, the sovereign boundary, the controlled foundation.

### C3 · Custody of the keys
*A single elegant machined key resting on a dark brushed-metal surface, dramatic raking gold rim-light, deep shadow, macro shallow depth of field, most of the frame in soft darkness.*
Story: cryptographic sovereignty — control of the keys. Restrained macro-photography cover.

### C4 · Continent of light
*An abstract aerial night view of a landmass rendered only as a soft constellation of faint blue city lights over a dark ocean-like field, seen from high orbit, calm and sparse, faint gold glow at the centre, vast dark space around.*
Story: Australia, elegantly — no literal map outline. (This is the sophisticated version of the earlier attempt.)

### C5 · The seven columns
*A dark modernist architectural interior, a colonnade of seven tall minimalist columns receding into shadow, a single shaft of cool blue light from above and a warm gold glow at the far end, dramatic negative space, fine-art architectural photography.*
Story: the seven sovereignty pillars, told architecturally.

### C6 · Contained flows
*Long-exposure ribbons of soft blue light flowing and curving, then held precisely within an invisible boundary — motion meeting control — against a deep charcoal-teal void, a faint gold containment line, generous darkness.*
Story: data and AI flows, governed and kept in-jurisdiction.

### C7 · Secure ground (texture cover)
*Extreme macro of a dark stone or brushed-titanium surface with a single glowing gold fault-line running through it, and faint embedded blue veins, moody low-key studio light — an abstract premium cover texture with no focal object.*
Story: sovereignty as bedrock. A pure-texture option for section dividers.

### C8 · The sovereign hall
*A moody minimalist data-hall corridor receding symmetrically into darkness, cool blue edge-lighting along the racks, a single warm gold light at the vanishing point, cinematic, restrained, deep perspective with dark negative space up top.*
Story: sovereign infrastructure and operations — serious, institutional.

---

## 3. Platform notes

**Midjourney** — paste `subject line, + house style block --ar 16:9 --style raw --stylize 250 --no text, letters, logos, neon, clutter, vector, cartoon`. Use `--stylize 150–300` for restraint; `--style raw` keeps it photographic rather than illustrative.

**DALL·E 3 / ChatGPT** — it prefers full sentences and ignores `--` params. Write: *"A photorealistic, restrained corporate consulting report cover… [subject]… [house style prose]. Leave the lower-left third empty for a title. No text or logos."* Ask for 16:9 or "wide" explicitly.

**Adobe Firefly** — strong on brand-safe photoreal. Use the subject line, set *Content type = Photo*, add the palette as reference, and use the "Structure/Style reference" with one of my earlier renders if you want the composition held.

**Consistency across the set** — generate C1–C8 with the **same** style block and Midjourney seed (`--seed 1234`) so the eight covers feel like one family.

---

## 4. Handing back

Drop the chosen images into `brand-assets/` (any name). Tell me which artefact each should go on, and I'll:
1. Verify the tone is dark enough for a reversed logo/title (add an Ink `#2A363B` scrim if not).
2. Crop to 16:10 (doc hero) and 16:9 (slide) with the title-safe area preserved.
3. Swap them onto the White Paper, Technical Reference and Executive Briefing covers, and record the choice in `Instructions/Design-System-Localisation.md`.

*Palette and rules source of truth: `Getamazednow AI Design System v1.1/design-tokens.json`. This pack localises image generation for ADSRA only.*
