# Design System Specification: Industrial Luminescence

## 1. Overview & Creative North Star
### The Creative North Star: "The Architectural Beam"
This design system moves beyond simple "industrial" aesthetics into a realm of **High-End Technical Authority**. Inspired by the precision of architectural lighting and the structural integrity of commercial engineering, the system utilizes high-contrast typography and light-driven depth. 

We break the "standard template" look by utilizing **Intentional Asymmetry**. Large-scale typography is often offset, and imagery should "break" container boundaries to mimic how light spills across a surface. We do not use borders to contain information; we use light (tonal shifts) and shadow (ambient occlusion) to define space.

---

## 2. Colors: Tonal Architecture
The palette is rooted in the deep atmospheric blues of late-evening construction sites, punctuated by the high-visibility "Safety Yellow" and "LED White" of functional illumination.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning or layout containment. Use background color shifts (e.g., a `surface-container-low` section sitting on a `surface` background) to define boundaries. This creates a more sophisticated, seamless industrial feel.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. 
- **Base Layer:** `surface` (#09151a)
- **Nested Content:** Use `surface-container-low` (#111d23) or `surface-container-high` (#202c32) to create "wells" or "platforms" for information.
- **The "Glass & Gradient" Rule:** For floating navigation or high-end product showcases, use Glassmorphism. Apply `surface-bright` (#2f3b41) at 60% opacity with a `20px` backdrop-blur. 

### Signature Textures
Main CTAs and Hero sections should utilize a subtle linear gradient: `primary` (#bdc2ff) transitioning to `primary-container` (#1a237e) at a 135-degree angle. This mimics the "throw" of an LED beam.

---

## 3. Typography: The Editorial Blueprint
We pair **Manrope** (Display/Headline) for its geometric, technical precision with **Inter** (Body/Labels) for its unrivaled legibility in industrial contexts.

| Level | Token | Font | Size | Weight | Intent |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Display** | `display-lg` | Manrope | 3.5rem | 800 | Impactful, architectural statements. |
| **Headline**| `headline-md`| Manrope | 1.75rem | 700 | Authoritative section starts. |
| **Title**   | `title-lg`   | Inter | 1.375rem | 600 | Product names and card headers. |
| **Body**    | `body-md`    | Inter | 0.875rem | 400 | Technical specs and descriptions. |
| **Label**   | `label-md`   | Inter | 0.75rem | 700 | CAPS. High-visibility metadata. |

---

## 4. Elevation & Depth: Tonal Layering
In an industrial lighting system, depth is perceived through the interaction of light and surface, not artificial lines.

*   **The Layering Principle:** Place a `surface-container-lowest` (#041015) card on a `surface-container-low` (#111d23) section. This "recessed" look implies the card is a precision-cut component fitted into a chassis.
*   **Ambient Shadows:** For floating modals, use a shadow with a `40px` blur, `0%` spread, and `8%` opacity. The shadow color must be `on-surface` (#d7e4ec) to simulate the soft bounce of LED light.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use the `outline-variant` (#454652) at **15% opacity**. Never use a 100% opaque border.
*   **Corner Radius:** Use `md` (0.375rem) for functional components (inputs, buttons) and `lg` (0.5rem) for structural elements (cards). This provides a "machined" look that is modern yet sturdy.

---

## 5. Components: The Machined UI

### Buttons
*   **Primary:** Background `secondary` (#f8bd2a), Text `on-secondary` (#402d00). Roundedness: `md`. Use for "Request Quote" or "Install."
*   **Secondary:** Background `transparent`, Ghost Border (15% opacity `outline-variant`), Text `on-surface`. 
*   **Interaction:** On hover, primary buttons should "glow" using a `12px` outer shadow of the `secondary` color.

### Input Fields
*   **Style:** Filled containers using `surface-container-highest` (#2a363d). 
*   **Indicator:** A 2px bottom-bar of `primary` (#bdc2ff) appears only on focus, mimicking a light turning on.
*   **Error:** Use `error` (#ffb4ab) for text and helper icons.

### Cards & Lists
*   **Constraint:** Forbid the use of divider lines. 
*   **Separation:** Separate list items using `spacing-4` (0.9rem) of vertical white space or by alternating background tints between `surface-container-low` and `surface-container-lowest`.

### Technical Chips
*   **Style:** Use `tertiary-container` (#2e3030) with `label-sm` typography. These should look like small, engraved metal plates.

---

## 6. Do's and Don'ts

### Do
*   **Do** use `secondary` (#f8bd2a) sparingly. It is a "safety" color; if everything is yellow, nothing is important.
*   **Do** lean into extreme scale. A `display-lg` headline next to a `body-sm` technical spec creates a high-end, editorial feel.
*   **Do** use the `16` (3.5rem) spacing token for major section breathing room. Industrial doesn't mean crowded.

### Don't
*   **Don't** use standard "Drop Shadows." Use tonal shifts (lighter/darker surfaces) first.
*   **Don't** use pure black (#000000). Always use the `surface` (#09151a) to maintain the deep navy "atmospheric" depth.
*   **Don't** use centered layouts for technical content. Keep it flush-left to maintain a rigorous, "blueprint" feel.