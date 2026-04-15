```markdown
# Design System Strategy: The Academic Curated Ledger

This design system is a bespoke framework for academic management, designed to transform complex educational data into a high-end editorial experience. Moving beyond the standard "dashboard" aesthetic, this system utilizes tonal layering, sophisticated typography, and intentional white space to create an environment that feels authoritative, trustworthy, and calm.

## 1. Creative North Star: The Scholarly Ledger
The "Creative North Star" for this system is **The Scholarly Ledger**. It envisions the UI not as a digital tool, but as a prestigious archival record. We break the "template" look by using a composition strategy that favors wide margins, asymmetrical data layouts, and high-contrast typographic scales. The goal is to make a data-heavy university system feel as intentional and curated as a premium academic journal.

## 2. Color Theory & Tonal Depth
The palette is rooted in deep, authoritative blues (`primary: #003550`) and professional grays. However, the application is what defines its premium nature.

### The "No-Line" Rule
To achieve a high-end feel, **1px solid borders are strictly prohibited for sectioning.** We do not "box in" data. Boundaries must be defined solely through:
- **Background Color Shifts:** Use `surface-container-low` to define a section against a `surface` background.
- **Tonal Transitions:** Vertical white space combined with subtle color shifts.

### Surface Hierarchy & Nesting
Hierarchy is achieved through "stacked" depth rather than lines.
- **Level 0:** `surface` (#f8f9fa) – The base canvas.
- **Level 1:** `surface-container-low` (#f3f4f5) – Secondary structural regions (e.g., sidebars).
- **Level 2:** `surface-container-lowest` (#ffffff) – Primary content "sheets" or cards. This creates a soft, natural lift.

### The "Glass & Gradient" Rule
For floating elements like modals or relationship mapping nodes, use **Glassmorphism**:
- Apply `surface` colors at 80% opacity with a `20px` backdrop-blur. 
- Use subtle linear gradients for CTAs, transitioning from `primary` (#003550) to `primary-container` (#004d71) to provide "visual soul" and depth that prevents the UI from feeling flat.

## 3. Typography: Editorial Authority
The system pairs **Manrope** (Display/Headline) with **Inter** (Body/Labels) to balance character with extreme readability.

- **Display & Headlines (Manrope):** These are the "editorial" voice. Use `display-md` for high-level stats (e.g., total enrollment) to create a bold, confident statement.
- **Body & Labels (Inter):** Designed for the "Ledger." Use `body-md` (0.875rem) for data table rows to maximize information density without sacrificing legibility.
- **Hierarchical Contrast:** Always pair a `headline-sm` with a `label-md` in `on-surface-variant` to create a clear distinction between "The Title" and "The Metadata."

## 4. Elevation & Depth
We convey importance through **Tonal Layering** rather than traditional drop shadows.

- **The Layering Principle:** Place a `surface-container-lowest` card on top of a `surface-container-high` section. The contrast in lightness provides enough "pop" to signify interactivity.
- **Ambient Shadows:** Only use shadows for high-level floating elements (like popovers). Shadows must be extra-diffused: `blur: 32px`, `opacity: 6%`, using a tint of `on-surface` (#191c1d) to ensure they look like natural light, not digital noise.
- **The Ghost Border:** If a separator is required for accessibility in complex tables, use a "Ghost Border": the `outline-variant` token at **15% opacity**. Never use a 100% opaque border.

## 5. Component Guidelines

### Data Tables (The Ledger)
- **Styling:** Forbid divider lines between rows. Use `surface-container-lowest` for the header row and alternating `surface` and `surface-container-low` for row groups.
- **Padding:** High-end design requires "breathing room." Use `1.5rem` horizontal padding for table cells.

### Relationship Mapping Interfaces
- **Nodes:** Use `surface-container-lowest` with a `2px` "Ghost Border." 
- **Connectors:** Use `outline-variant` at 40% opacity. Use curved Bezier paths rather than straight lines to evoke a more organic, sophisticated feel.
- **Depth:** Nodes should have a subtle `primary` gradient tint on hover to indicate active relationships.

### Forms & Inputs
- **Inputs:** Use the `surface-variant` for the input background with no border. Upon focus, transition the background to `surface-container-lowest` and apply a `primary` "Ghost Border" (20% opacity).
- **Buttons:**
    - **Primary:** Gradient from `primary` to `primary-container`. `rounded-md` (0.375rem).
    - **Secondary:** Transparent background with `on-secondary-container` text. No border.

### Chips & Badges
- **Status Chips:** Use `secondary-container` for neutral states and `primary-fixed` for active academic states. Shapes should be `rounded-full`.

## 6. Do’s and Don'ts

### Do
- **Use Asymmetry:** In student profiles, offset the photo from the name to create an editorial, magazine-style layout.
- **Embrace White Space:** Let data "breathe." If a screen feels cluttered, increase the vertical spacing between surface layers.
- **Use Tonal Shifts:** Always use `surface-container` tiers to define the hierarchy of information.

### Don't
- **Don't use 1px black/gray borders.** This is the fastest way to make a system look "cheap."
- **Don't use heavy shadows.** If the shadow is the first thing you notice, it is too dark.
- **Don't use standard "Alert Red" for everything.** Use the `error` (#ba1a1a) and `error_container` tokens sparingly to maintain the professional, calm aesthetic of the university environment.
- **Don't use dividers in lists.** Use the spacing scale to separate items through proximity and alignment.```