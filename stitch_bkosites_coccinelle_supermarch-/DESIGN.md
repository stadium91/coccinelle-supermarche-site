```markdown
# Design System Document: The Digital Curator

## 1. Overview & Creative North Star

This design system is built to transform the mundane task of grocery shopping into a curated, editorial experience. Our Creative North Star is **"The Digital Curator"**—a philosophy that treats every product as a masterpiece and every layout as a gallery wall. 

For 'Coccinelle Supermarché', we reject the rigid, boxy constraints of traditional e-commerce. Instead, we embrace **Intentional Asymmetry** and **Broken Grids**. This system is tailored for an expatriate audience that values "terroir," quality, and a sophisticated aesthetic. We move away from "stock" layouts by using overlapping elements, organic clipping masks, and dramatic typographic scales to create a sense of movement and premium heritage.

---

## 2. Colors: 'The Fresh Garden' Palette

The palette is grounded in the organic world, using high-contrast tones to guide the eye without the need for structural scaffolding.

### The "No-Line" Rule
**Explicit Instruction:** You are prohibited from using 1px solid borders to define sections or containers. Boundaries must be defined solely through background shifts. For example, a `surface_container_low` section sitting against a `surface` background provides all the separation a premium user needs.

### Surface Hierarchy & Nesting
Depth is achieved through tonal layering rather than lines.
- **Surface (#FAF9F6):** The canvas. Use this for the primary background to maintain a "Creamy White" editorial feel.
- **Surface-Container-Low (#F4F3F1):** Use for large, secondary content blocks (e.g., a "Chef’s Selection" section).
- **Surface-Container-Highest (#E3E2E0):** Use for small, interactive elements or "nested" cards that need to pop against a lower-tier surface.

### The "Glass & Gradient" Rule
- **Navigation:** Must use `surface` at 80% opacity with a `24px` backdrop-blur. This creates a "frosted glass" effect that allows the rich imagery of produce to bleed through as the user scrolls.
- **Signature Polish:** Use subtle gradients transitioning from `primary` (#A80017) to `primary_container` (#CE2029) for hero buttons. This adds a "weighted" feel that flat colors cannot replicate.

---

## 3. Typography: The Editorial Voice

We pair the dramatic, high-contrast **Noto Serif** with the functional, modern **Manrope** to balance heritage with efficiency.

- **Display-LG (Noto Serif, 3.5rem):** Reserved for hero statements. Use with `on_surface` or `primary` to command immediate attention.
- **Headline-MD (Noto Serif, 1.75rem):** For section titles. These should often be placed off-center or overlapping an image mask to break the grid.
- **Body-LG (Manrope, 1rem):** Used for product descriptions and editorial copy. The generous line-height of Manrope ensures readability for our expatriate demographic.
- **Label-MD (Manrope, 0.75rem, All Caps):** Use for category tags (e.g., "ORGANIC", "IMPORTED"). Increased letter spacing (0.05em) is encouraged here to evoke luxury branding.

---

## 4. Elevation & Depth: Tonal Layering

Traditional shadows are too heavy for a "Fresh" aesthetic. We communicate depth through **Tonal Stacking**.

- **The Layering Principle:** To lift a card, do not add a shadow. Place a `surface_container_lowest` (#FFFFFF) card on a `surface_container_low` (#F4F3F1) background. The subtle shift in hex value creates a "natural lift."
- **Ambient Shadows:** Only use shadows for floating modals or global navigation. Use a blur of 40px-60px with the color `on_surface` at 4% opacity. It should look like a soft glow, not a dark smudge.
- **The "Ghost Border" Fallback:** If accessibility requires a border (e.g., an input field), use the `outline_variant` token at 20% opacity. Never use 100% opaque lines.

---

## 5. Components

### The Organic Aperture (Imagery)
All lifestyle photography must use **Organic Clipping Masks**. Avoid rectangles. Use "leaf" or "produce-blob" shapes with the `xl` (3rem) or `full` roundedness scale. This mimics the irregular beauty of nature.

### Buttons: The Tactile Interaction
- **Primary:** Background: `primary_container` (#CE2029). Typography: `on_primary` (White). Shape: `full` roundedness.
- **Secondary:** Background: `secondary_fixed_dim` (#A4D393). Typography: `on_secondary_fixed` (#022100).
- **State Change:** On hover, shift the background to a subtle gradient or increase the `surface_tint` intensity.

### Cards & Lists: The No-Divider Approach
- **Product Cards:** No borders. Use `surface_container_low` for the card body. Use an organic mask for the product image that "breaks" the top edge of the card.
- **Lists:** Do not use horizontal lines between items. Use `2rem` (lg) of vertical whitespace to separate list items. This creates a spacious, "unhurried" shopping experience.

### Input Fields
- **Style:** Minimalist. Only a bottom "Ghost Border" (outline-variant at 20%). 
- **Focus State:** The bottom border transitions to `primary` (#A80017) at 2px thickness. 

---

## 6. Do's and Don'ts

### Do:
- **Embrace White Space:** If a layout feels "full," remove an element. The expatriate luxury market responds to breathing room.
- **Asymmetric Balance:** Balance a large Noto Serif headline on the left with a small, organic-masked image shifted slightly off-grid on the right.
- **Color Context:** Use `tertiary` (#674B47) for secondary text to keep the "Deep Earth Brown" warmth throughout the experience.

### Don't:
- **No Sharp Corners:** Never use a `0px` radius. Even the most "structured" element should have at least `sm` (0.5rem) rounding to remain organic.
- **No Pure Black:** Avoid #000000. Use `on_surface` (#1A1C1A) for all "black" text to maintain the soft, creamy tone of the system.
- **No Grids for Grids' Sake:** Do not force elements to align perfectly to a 12-column grid. Let elements "float" and overlap to create the Digital Curator aesthetic.

---

**Director’s Final Note:** This system is about the *restraint* of color and the *intentionality* of space. Treat the `surface` as the most important element on the page. If the background feels like fine paper, you have succeeded.```