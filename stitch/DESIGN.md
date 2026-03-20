# Design System Specification: Industrial Editorial Excellence

## 1. Overview & Creative North Star
### Creative North Star: "The Architectural Monolith"
This design system rejects the "template-heavy" look of standard corporate sites. Instead, it draws inspiration from modern structural engineering and premium architectural blueprints. The aesthetic is **Architectural Monolith**: characterized by heavy-duty typographic scales, intentional asymmetric white space, and a feeling of immense physical scale.

By leveraging high-contrast color shifts and raw, industrial photography, we create an experience that feels as solid as the concrete the company produces. We move beyond "web pages" and into "digital infrastructure," using the UI to mirror the strength, precision, and high capacity of Turkish industrial excellence.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the materials of the trade—anthracite steel, cured concrete, and high-visibility safety accents.

### Color Roles
*   **Primary (#030813):** Used for deep, authoritative backgrounds and primary text.
*   **Secondary (#944b00):** Our "Controlled Vivid Orange." This is the spark of machinery; use it sparingly for critical CTAs and high-priority highlights.
*   **Surface Tiers:** Use `surface-container-lowest` (#ffffff) to `surface-container-highest` (#dde2f3) to build depth.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. High-end industrial design is about mass and volume. Define boundaries strictly through background color shifts. A `surface-container-low` section should sit adjacent to a `surface` background to create a clean, modern break without the clutter of "lines."

### Surface Hierarchy & Nesting
Treat the UI as a series of cast concrete slabs.
*   **Layer 1 (Base):** `surface` (#f9f9ff).
*   **Layer 2 (In-set Content):** `surface-container-low` (#f1f3ff).
*   **Layer 3 (Interactive Cards):** `surface-container-lowest` (#ffffff).
By nesting these, you create a "recessed" or "extruded" look that feels engineered rather than drawn.

### Signature Textures
Use subtle gradients (e.g., `primary` to `primary-container`) on large hero areas. This mimics the way light hits polished anthracite or brushed metal, adding a "soul" to the digital interface that flat hex codes cannot achieve.

---

## 3. Typography
We utilize a pairing of **Manrope** for Display/Headings to provide a structural, geometric feel, and **Inter** for Body/Labels to maintain engineering precision and readability.

*   **Display LG (Manrope, 3.5rem):** Reserved for hero headlines. Use tight letter-spacing (-0.02em) to mimic the density of industrial branding.
*   **Headline MD (Manrope, 1.75rem):** For major section titles. These should feel like "stamped" metal.
*   **Title LG (Inter, 1.375rem):** Bold, clean, and functional.
*   **Body MD (Inter, 0.875rem):** Our workhorse for technical specs and descriptions.
*   **Label SM (Inter, 0.6875rem):** High-contrast, all-caps for metadata or "Machine IDs."

**Editorial Tip:** Use massive `display-lg` headings that intentionally overlap background transitions or "break" the grid slightly to create a high-end, bespoke editorial feel.

---

## 4. Elevation & Depth
In this system, depth is a function of light and material, not "dropshadow.png."

### The Layering Principle
Achieve lift through tonal shifts. Place a `surface-container-lowest` card on a `surface-dim` background. This creates a soft, natural lift that feels like a physical object in a studio.

### Ambient Shadows
When a floating element (like a modal) is required:
*   **Blur:** 40px - 60px.
*   **Opacity:** 4% - 8%.
*   **Color:** Use a tinted version of `on-surface` (#161c27) rather than pure black.

### The "Ghost Border" Fallback
If accessibility requires a container boundary, use the `outline-variant` token at **15% opacity**. It should be felt, not seen.

### Glassmorphism & Depth
For floating navigation or overlays, use `surface-container-lowest` with an 80% opacity and a `backdrop-filter: blur(12px)`. This allows the "industrial site photography" to bleed through the UI, keeping the user grounded in the physical world of construction.

---

## 5. Components

### Buttons
*   **Primary:** `secondary` background (#944b00) with `on-secondary` text. **Radius:** `md` (0.375rem). No shadow; use a 2px "inset" top-light on hover to simulate a physical switch.
*   **Secondary:** `primary` background (#030813). Bold, authoritative, and heavy.
*   **Tertiary:** Transparent background with `primary` text and a `0.7rem` bottom padding to act as an "underline" indicator.

### Input Fields
*   **Style:** No full borders. Use a `surface-container-high` background with a 2px `outline` bottom-stroke. This mimics engineering forms and blueprint layouts.

### Cards & Lists
*   **The Divider Forbid:** Never use horizontal rules. Separate list items using the spacing scale (e.g., `spacing-4` / 1.4rem) and subtle alternating background tints (`surface` vs `surface-container-low`).

### Industry-Specific Components
*   **The "Capacity Gauge":** A custom progress bar using `secondary` (orange) against a `primary-container` (navy) track to show concrete mix ratios or delivery statuses.
*   **The Technical Spec Grid:** A multi-column layout for product data using `label-md` for headers and `title-sm` for values, separated by massive white space (`spacing-8`).

---

## 6. Do's and Don'ts

### Do:
*   **DO** use photography as a structural element. Crop industrial photos of concrete pours into large, vertical rectangles that span multiple sections.
*   **DO** lean into "Over-Sizing." If a title feels big, make it bigger.
*   **DO** use `spacing-20` (7rem) between major sections to let the "engineering" breathe.

### Don't:
*   **DON'T** use rounded corners above `xl` (0.75rem). We are building with concrete and steel, not plastic.
*   **DON'T** use "Generic Blue." Every navy must be the deep, anthracite `primary` (#030813) or `primary-container` (#1a202c).
*   **DON'T** use centered layouts for everything. Use the left-heavy, asymmetric "Blueprint Grid" to create a sense of movement and scale.

---

## 7. Spacing Scale Implementation
Standardize all layouts using the provided scale.
*   **Containers:** Use `spacing-16` (5.5rem) for internal section padding.
*   **Gaps:** Use `spacing-3` (1rem) for tight technical data; `spacing-6` (2rem) for standard UI groupings.

*End of Document*