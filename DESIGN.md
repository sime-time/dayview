# Design System: High-End Editorial & Fashion-Forward

## 1. Overview & Creative North Star: "The Digital Curator"
This design system is built upon the philosophy of **"The Digital Curator."** It rejects the rigid, cookie-cutter structures of traditional web templates in favor of a sophisticated, editorial approach akin to high-fashion mastheads and art gallery portfolios.

The system moves beyond "Standard Minimal" by utilizing **intentional asymmetry** and **typographic tension**. It treats the screen as a physical page where negative space is as important as the content itself. By pairing a high-contrast monochromatic base with electric pink accents, we create a visual language that is both timelessly elegant and aggressively modern.

---

## 2. Colors & Surface Logic
The palette is rooted in a "Piano Key" aesthetic—stark blacks and whites—interrupted by a "Digital Shock" of vibrant pink.

### Color Tokens
- **Primary:** `#000000` (The anchor)
- **Surface (Background):** `#FFFFFF` (The canvas)
- **Surface Container (Low):** `#FAFAFA` (The secondary layer)
- **Accent Pink:** `#FF66C4` (The focal point / call to action)
- **Accent Pink Soft:** `#FFE0F2` (The highlight / hover state)
- **Text Primary:** `#111111` (Deep charcoal for readability)
- **Text Muted:** `#666666` (Low-priority metadata)

### The "No-Line" Rule
To maintain a high-end feel, **1px solid borders for sectioning are strictly prohibited.** Boundaries between sections must be defined through background color shifts (e.g., a `Surface Container Low` block sitting on a `Surface` background) or extreme white space. We define containers by their mass, not their outlines.

### Glass & Gradient Rule
While the base is flat, high-interaction elements (like floating navigation or project overlays) should utilize **Glassmorphism**. Use semi-transparent white backgrounds with a `24px` backdrop-blur to allow the content beneath to bleed through, softening the edges of the high-contrast layout.

---

## 3. Typography
The typographic system relies on the interplay between the romanticism of the serif and the precision of the sans-serif.

| Level | Token | Font Family | Size | Character |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Playfair Display Variable | 3.5rem | Elegant, serif, -2% letter spacing. |
| **Headline** | `headline-md` | Playfair Display Variable | 1.75rem | Used for section titles. |
| **Title** | `title-lg` | Mulish Variable | 1.375rem | Bold, modern, all-caps for impact. |
| **Body** | `body-lg` | Mulish Variable | 1.0rem | High legibility, 1.6 line-height. |
| **Label** | `label-sm` | Mulish Variable | 0.6875rem | Uppercase, 10% letter spacing. |

**Hierarchy Tip:** Always lead with the Serif for "Emotional Content" (Headlines, Quotes) and use the Sans-Serif for "Functional Content" (UI, Navigation, Labels).

---

## 4. Elevation & Depth
In this design system, depth is achieved through **Tonal Layering** rather than heavy drop shadows.

* **The Layering Principle:** Treat the UI as stacked sheets of fine paper. Place a `surface-container-lowest` card on a `surface-container-low` section to create a soft, natural lift.
* **Ambient Shadows:** For floating elements, shadows must be "Ambient." Use a blur value of `40px` to `60px` with an opacity no higher than `4%`. The shadow color should be a tinted black to mimic natural light.
* **The "Ghost Border" Fallback:** If a container requires definition on a white background, use a "Ghost Border": `#EAEAEA` at 40% opacity. Never use a 100% opaque border.
* **Asymmetric Composition:** Break the 12-column grid. Shift hero images 40px off-center. Let text overlap image containers slightly to create a layered, "collage" effect.

---

## 5. Components

### Buttons & Interaction
* **Primary Button:** Solid `#000000`, Text `#FFFFFF`, `9999px` (Pill) radius. On hover, transform to `Accent Pink`.
* **Secondary/Ghost:** `9999px` pill with a `1px` Ghost Border. No fill.
* **The "Magnetic" Cursor:** For the portfolio context, implement a custom cursor that expands into a pink circle when hovering over clickable images or titles.

### Cards & Projects
* **The Card:** `24px` corner radius. Do not use borders. Use a `Surface Container Low` background.
* **No Dividers:** Forbid the use of horizontal lines to separate list items. Use `48px` of vertical white space (padding) to define the end of one item and the start of the next.

### Input Fields
* **Style:** Minimalist. Only a bottom border of `1px` using the `Border` token.
* **Focus State:** The bottom border transforms to `Accent Pink` with a `2px` thickness. Labels should be `label-sm` (uppercase) positioned above the input.

### Signature Component: The "Editorial Reveal"
When scrolling into a new section, utilize a "staggered reveal" where the Serif headline appears first, followed by a slight delay for the body text and imagery. This reinforces the "curated" feel.

---

## 6. Do’s and Don'ts

### Do:
* **Embrace Negative Space:** If a section feels "busy," double the padding. White space is a luxury signal.
* **Mix Alignments:** Align your display text to the left and your body copy to the right for a sophisticated, asymmetric tension.
* **Use High Contrast:** Stick to pure blacks and whites to allow the `Accent Pink` to feel intentional and "loud."

### Don't:
* **Don't Use Default Shadows:** Avoid the standard "Drop Shadow" preset at all costs. It cheapens the editorial look.
* **Don't Use Grids Rigidly:** Do not feel obligated to fill every column. Let elements breathe and sit off-grid.
* **Don't Use Dividers:** Never use a line when white space or a subtle color shift can do the job.
