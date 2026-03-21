# Design System Strategy: The Visionary Builder

## 1. Overview & Creative North Star: "The Monumental Scholar"
This design system is a study in tension: the warmth of a hand-painted Ghibli landscape meeting the cold, sharp precision of a Renaissance sculpture. We are moving away from the "SaaS-ification" of the web. There are no rounded corners here, no soft blue shadows, and no generic cards.

**The Creative North Star: The Monumental Scholar.** 
The interface should feel like a high-end digital broadsheet—an editorial experience where content is treated with the gravity of a stone-carved inscription. We achieve this through "Atmospheric Drama": using high-contrast typography, expansive whitespace (the "Parchment"), and sudden, violent bursts of Crimson to guide the eye. 

The layout is intentionally asymmetrical. Elements should feel "placed" rather than "slotted," utilizing overlapping layers to create a sense of depth and architectural intent.

---

## 2. Colors & Tonal Depth
Our palette is rooted in warmth and depth. The backgrounds are very dark warm near-blacks — not cold grey-blacks. The reds are bright and readable, leaning orange-warm rather than blood-dark. A secondary gold/amber grounds the palette and prevents it from feeling monotone.

### Dark Mode Palette (Primary — Website)

| Token | Hex | Role |
|---|---|---|
| `--bg` | `#0F0D0B` | Primary canvas — very dark warm black |
| `--bg-raised` | `#1C1814` | Raised surfaces (nav, alt sections) |
| `--bg-card` | `#151210` | Card backgrounds |
| `--vermilion` | `#E8503A` | Primary accent — bright warm red-orange |
| `--crimson` | `#C83A26` | Hover state for accent |
| `--gold` | `#D4AA6A` | Secondary accent — warm amber |
| `--t1` | `#F2E8D9` | Primary text — warm parchment |
| `--t2` | `#C4B09A` | Secondary text |
| `--t3` | `#8C7B6A` | Muted text — still legible |
| `--outline` | `#2E2620` | Borders and dividers |

**Key contrast principle:** Accent `#E8503A` on `#0F0D0B` passes WCAG AA for large text. `--t1` and `--t2` maintain strong contrast ratios. `--t3` is used only for decorative labels, never body copy.

### The "No-Line" Rule
**Borders are forbidden for layout sectioning.** To separate a hero from a content area, use a background shift.
*   Alternate between `--bg` and `--bg-card` for major sections.
*   Use `--outline` only for fine rule lines (section headers, table rows).

### Surface Hierarchy & Nesting
Think of the UI as layers of warm volcanic stone.
*   **Base:** `--bg` (#0F0D0B) – The infinite canvas.
*   **Raised:** `--bg-raised` (#1C1814) for nav, interactive cards.
*   **Inset:** `--bg-card` (#151210) for alternate sections.

### Light Mode Reference (Brand Documents Only)
For brand guideline documents and print:
*   **Base:** `#F6F3EA` — warm parchment
*   **Text:** `#1C1C17` — deep charcoal
*   **Accent:** `#AF1014` — deep vermilion (legible on light)

### The "Glass & Crimson" Signature
For floating elements or navigation overlays, use **Glassmorphism**. Apply a background blur (12px–20px) to the `surface` color at 85% opacity. This allows the "Ghost of Tsushima" atmospheric reds to bleed through the UI, softening the rigid structure.

---

## 3. Typography: Sharp & Retro-Futuristic
Typography is the primary visual engine of this system. We pair the aggressive geometry of the future with the legible grace of the present.

*   **Display & Headlines (Space Grotesk):** These must be massive and high-contrast. Use `display-lg` for hero statements. The "Retro-futuristic" vibe comes from the tight tracking (-2% to -4%) and sharp apertures of this typeface. It should feel "monumental."
*   **Body (Manrope):** A clean, modern sans-serif. It provides a neutral resting point for the eyes between the dramatic headlines.
*   **Technical Details (Inter/Monospace):** Use `label-md` for metadata, timestamps, or "visionary" technical specs. This creates the "builder" aesthetic—grounding the grand ideas in technical reality.

---

## 4. Elevation & Depth: Tonal Layering
We do not use shadows to lift elements; we use light and opacity.

*   **The Layering Principle:** To highlight a project in a list, do not add a shadow. Shift its background to `surface-container-highest`.
*   **Ambient Shadows (The Exception):** If an element *must* float (e.g., a modal), use a shadow tinted with `on-surface`. 
    *   *Spec:* `box-shadow: 0 20px 50px rgba(28, 28, 23, 0.05);` 
    *   This mimics natural ambient light hitting a physical object.
*   **The "Ghost Border":** If a button or input requires a boundary, use `outline-variant` (#e4beba) at 20% opacity. It should be felt, not seen.

---

## 5. Components & Primitive Styling

### Buttons: The "Block" Aesthetic
All corners are `0px` (Square). This is non-negotiable.
*   **Primary:** Background `primary` (#af1014), Text `on-primary` (#ffffff). High-contrast and aggressive.
*   **Secondary:** Background `transparent`, Border `px` of `primary` at 30% opacity.
*   **State:** On hover, primary buttons should shift to `primary-container` (#d32f2a) with a slight "lift" (1px vertical translation).

### Cards & Lists: Editorial Grouping
*   **Forbidden:** Divider lines between items.
*   **The Replacement:** Use vertical spacing (`spacing.12` to `spacing.16`) and `label-sm` headers to group content. 
*   **Project Cards:** Use `surface-container-low` as the card base. If an image is present, bleed it to the edges. Text should have generous padding (`spacing.8`).

### Input Fields: Minimalist Precision
*   **Style:** Bottom-border only (`outline-variant` at 40% opacity). 
*   **Focus State:** The border transitions to `primary` (#af1014) and expands to 2px. The label shifts to a monospace `label-sm` to maintain the "technical builder" feel.

### Additional Component: The "Visionary Indicator"
A custom scroll progress bar or "status" chip using a `primary` to `primary-container` linear gradient. This adds a "soul" to the technical layout, referencing the painterly warmth of Ghibli.

---

## 6. Do’s and Don’ts

### Do:
*   **Embrace Asymmetry:** Offset your headlines. Let a 3.5rem headline sit 25% into the grid while the body text sits at 50%.
*   **Use Red as a Scalpel:** Use `primary` only for the most important actions or "blood-like" accents (falling leaf icons, bullet points).
*   **Trust the Whitespace:** Use `spacing.24` (8.5rem) between major sections to let the "Parchment" breathe.

### Don’t:
*   **Never use Border-Radius:** Rounding a single corner breaks the "Renaissance Statue" grandeur.
*   **Avoid Pure Black:** Use `on-surface` (#1c1c17) for text. It’s a deep charcoal that feels more organic and high-end than #000.
*   **No Standard Grids:** Avoid 12-column layouts that feel like a template. Think like a book designer, not a web developer.