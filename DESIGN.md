# Design System Specification

## 1. Overview & Creative North Star: "The Ethereal Navigator"
This design system is built upon the philosophy of **The Ethereal Navigator**. It moves away from the rigid, boxed-in constraints of traditional mobile applications, instead favoring an editorial layout that feels fluid, atmospheric, and intelligently guided. 

By leveraging high-contrast typography scales and intentional asymmetry, the system creates a "Digital Curator" experience. It avoids the "template" look by treating the screen as a continuous canvas rather than a series of isolated slots. Overlapping elements—such as floating AI modules and map interfaces—provide a sense of depth and physical presence, suggesting that the interface is not just a tool, but a sophisticated travel companion.

---

## 2. Color Palette & Surface Architecture
The color strategy utilizes a sophisticated range of blues and architectural neutrals to create a sense of vastness and premium trust.

### Primary & Core Tones
*   **primary-900 (Deep Anchor):** `#001629` — Used for high-authority headings and primary backgrounds.
*   **secondary-500 (Horizon Blue):** `#00658d` — Used for interactive elements and brand accents.
*   **tertiary-accent (Sunlight):** `#ffb870` — Reserved for critical highlights, AI markers, and status indicators.

### Surface Tiers (The Tonal Hierarchy)
*   **surface-bg:** `#f6fafe` (The base canvas)
*   **surface-container-low:** `#f0f4f8`
*   **surface-container-highest:** `#dfe3e7`
*   **surface-lowest (Card White):** `#ffffff`

### The Director’s Rules for Color
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Structural boundaries must be achieved through background shifts (e.g., a `surface-lowest` card sitting on a `surface-container-low` section) or subtle tonal transitions.
*   **The "Glass & Gradient" Rule:** To provide "soul" to the UI, use Glassmorphism for floating modules (AI companion cards). Apply a semi-transparent `surface-lowest` with a 20px backdrop-blur. 
*   **Signature Textures:** For primary CTAs or Hero sections, use a subtle linear gradient transitioning from `primary` (#001629) to `primary_container` (#002b49) at a 135-degree angle.

---

## 3. Typography
The system uses **Plus Jakarta Sans**, a typeface that balances geometric modernism with high-end editorial warmth.

| Token | Weight | Size | Line Height | Letter Spacing | Use Case |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **display-lg** | Bold | 3.5rem | 110% | -0.04em | Impactful Hero / Brand statements |
| **headline-md** | Semibold | 1.75rem | 120% | -0.02em | Main section headers |
| **title-lg** | Medium | 1.375rem | 140% | 0 | Sub-section headings |
| **body-lg** | Regular | 1rem | 160% | 0 | Standard reading text |
| **label-md** | Bold | 0.75rem | 120% | 0.05em | Uppercase category markers |

**Editorial Note:** Always pair `headline-md` (Dark Primary) with `label-md` (Secondary Blue) to create a high-contrast hierarchy that feels intentional and curated.

---

## 4. Elevation & Depth: Tonal Layering
This design system rejects heavy, "dirty" drop shadows. Instead, it conveys hierarchy through the **Layering Principle**.

*   **Tonal Stacking:** Depth is achieved by "stacking" surface tiers. For example, a map (surface-container-high) might hold a "Quick Action" card (surface-lowest). This creates a soft, natural lift without visual noise.
*   **Ambient Shadows:** When a floating effect is required (e.g., the bottom navigation bar), use a shadow tinted with the `on-surface` color: `box-shadow: 0 12px 32px rgba(23, 28, 31, 0.06);`.
*   **The Ghost Border:** If a boundary is necessary for accessibility, use the `outline_variant` token at 15% opacity. Never use 100% opaque borders.

---

## 5. Component Inventory

### Buttons & Interaction
*   **Primary Button:** Deep `primary` background, `xl` (3rem) radius. High-padding (16px 32px) for a luxurious touch.
*   **Selection Chips:** Use `secondary_fixed` background with `on_secondary_fixed_variant` text. Radius set to `full`.
*   **Navigation Items:** Clean, icon-led layouts using `surface_dim` for inactive states and `primary` for active states.

### Cards & Content
*   **Editorial Cards:** Forbid the use of divider lines. Separate content using `space-3` (24px) of vertical whitespace. 
*   **AI Companion Card:** A glassmorphic container with `md` (1.5rem) radius. Features a subtle internal glow using an inner-shadow effect.

### Spacing Scale (8px Base)
*   **space-1:** 8px (Small gaps, label-to-body)
*   **space-2:** 16px (Standard gutter)
*   **space-3:** 24px (Section breathing room)
*   **space-4:** 32px (Hero padding)

---

## 6. Do’s and Don’ts

### Do
*   **Do** use asymmetrical layouts where content slightly overlaps backgrounds to create depth.
*   **Do** prioritize vertical whitespace over horizontal lines to separate sections.
*   **Do** use "Plus Jakarta Sans" in light-tracking caps for `label-sm` to give a premium, metadata-focused feel.
*   **Do** ensure all cards use the `DEFAULT` (1rem) or `md` (1.5rem) corner radius for a friendly, approachable aesthetic.

### Don’t
*   **Don’t** use pure black (#000000) for text. Always use `on_surface` (#171c1f) to maintain visual softness.
*   **Don’t** use 1px solid dividers. They interrupt the flow of the "Ethereal Navigator" North Star.
*   **Don’t** use harsh shadows. If a shadow is visible at first glance, it is too heavy.
*   **Don’t** cram icons. Give each icon at least `space-1` (8px) of internal padding within its touch target.

---

## 7. Grid & Layout Structure
The system employs a **Fluid 4-Column Mobile Grid** with 24px side margins. 

To break the "template" feel, utilize **Feature Breaking**: allow hero images or map modules to bleed to the edge of the screen, while keeping text content strictly within the 24px margins. This creates a high-end editorial feel found in luxury travel magazines.