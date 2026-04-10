# Design System Specification: The Empathetic Expert

## 1. Overview & Creative North Star
This design system is built to bridge the gap between clinical precision and human warmth. Our Creative North Star is **"The Digital Sanctuary."** Unlike traditional medical interfaces that feel sterile or overly bureaucratic, this system treats the UI as a calm, breathable environment.

We break the "template" look by utilizing **Environmental Immersion**. This means we do not simply place content on a white background; we use large, sweeping organic shapes (Radii `xl` to `full`) and immersive color blocks to cradle content. We favor intentional asymmetry—such as overlapping image containers and floating action bars—to create a dynamic, high-end editorial feel that suggests a bespoke, high-touch healthcare experience.

## 2. Colors & Tonal Depth
The palette is a sophisticated range of blues and "soft whites" designed to reduce cognitive load and eye strain.

### The "No-Line" Rule
To achieve a premium editorial aesthetic, **designers are prohibited from using 1px solid borders to define sections.** Boundaries must be established through:
*   **Background Shifts:** Transitioning from `background` (#f7f9fb) to `surface_container_low` (#f2f4f6).
*   **Tonal Nesting:** Placing a `surface_container_lowest` (#ffffff) card inside a `surface_container_high` (#e6e8ea) section.

### Surface Hierarchy & Glassmorphism
Treat the UI as a series of physical layers. 
*   **The Foundation:** `background` or `surface`.
*   **The Content Layer:** `surface_container` tiers.
*   **The Floating Layer:** For high-priority navigation or "Book Appointment" bars, use **Glassmorphism**. Apply `surface` at 80% opacity with a `20px` backdrop blur. This allows the soft blues of the background to bleed through, creating a "frosted glass" effect that feels modern and integrated.

### Signature Textures
Avoid "flat" primary buttons. Use subtle linear gradients transitioning from `primary` (#2346d5) at the top left to `primary_container` (#4361ee) at the bottom right. This adds a "soul" to the interactive elements, making them feel tactile and clickable.

## 3. Typography
Our typography pairing balances authority with accessibility.

*   **Display & Headlines (Plus Jakarta Sans):** These are our "Editorial Voices." The geometric yet soft nature of Plus Jakarta Sans provides a modern, expert tone. Use `display-lg` for hero sections to establish immediate confidence.
*   **Body & Labels (Public Sans):** These are our "Functional Voices." Public Sans is used for all reading-heavy content. It is neutral and highly legible, ensuring medical information is accessible to all users.
*   **Intentional Scale:** We utilize a high-contrast scale. A `display-lg` headline should be paired with a `body-lg` or `body-md` subheader to create a clear, authoritative hierarchy that guides the eye.

## 4. Elevation & Depth
In this system, depth is a functional tool, not a decoration. We move away from traditional drop shadows in favor of **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface_container_lowest` card on a `surface_container_low` background creates a natural "lift" through color theory alone.
*   **Ambient Shadows:** Where a shadow is required (e.g., a floating modal), it must be an "Ambient Shadow." 
    *   **Blur:** 40px – 60px.
    *   **Opacity:** 4% – 6%.
    *   **Color:** Use a tinted version of `on_surface` (deep blue-grey) rather than pure black to keep the light source feeling natural and soft.
*   **The "Ghost Border" Fallback:** If a container requires more definition for accessibility, use a **Ghost Border**. This is a 1px stroke using `outline_variant` at **15% opacity**. Never use 100% opaque borders.

## 5. Components

### Buttons
*   **Primary:** `primary` gradient, `full` rounding, `label-md` uppercase or title case. Padding: `16px 32px`.
*   **Secondary:** `surface_container_lowest` with a `Ghost Border`, `primary` text color.
*   **Tertiary:** No background or border. Use `primary` text with an icon (e.g., "View Service →").

### Input Fields
*   **Styling:** Use `surface_container_lowest` backgrounds with `md` (0.75rem) rounding.
*   **States:** On focus, the border should transition to a 2px `primary_fixed` stroke. Labels use `label-md` in `on_surface_variant`.

### Cards & Lists
*   **No Dividers:** Forbid the use of horizontal lines. 
*   **Separation:** Use `48px` to `64px` of vertical whitespace (the Spacing Scale) or subtle background shifts between list items.
*   **Medical Specialty Cards:** Use `surface_container_lowest` with `xl` (1.5rem) rounding. Include a centered `primary_container` tinted icon for a signature look.

### The Floating Appointment Bar
A signature component of this system. It should be a horizontal bar with `full` rounding, utilizing the **Glassmorphism** rule, floating at the bottom of a hero section or the top of the viewport. It uses `surface_container_lowest` at 90% opacity to highlight "Appointment," "Location," and "Specialist" selectors.

## 6. Do's and Don'ts

### Do:
*   **Embrace Whitespace:** If a section feels crowded, double the padding. This system relies on "breathing room" to convey a sense of calm.
*   **Use Soft Geometry:** Images should use `xl` rounding or organic "blob" masks to match the friendly brand personality.
*   **Prioritize Accessibility:** Ensure `on_primary` text always sits on a high-contrast `primary` background.

### Don't:
*   **Don't use pure black:** Use `on_surface` (#191c1e) for text to maintain a premium, softer look.
*   **Don't use sharp corners:** Nothing in this system should be "sharp." Even the smallest components (chips/labels) should have at least `sm` rounding.
*   **Don't use 1px dividers:** They clutter the medical experience. Trust the background colors and whitespace to do the work.