# Design System Strategy: The Academic Identity

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Registrar"**

This design system moves away from the generic "tech portfolio" and leans into the tactile, authoritative, yet personal world of academic identification. We are treating the digital space as an archival desk—where professional credentials meet modern editorial flair.

The system rejects the standard "bootstrap" look by utilizing **intentional asymmetry** and **material layering**. We bypass rigid, centered grids in favor of layouts that mimic a physical ID card or an open dossier: information is grouped into dense "data clusters" (stamps, barcodes) contrasted against vast, expansive whitespace. The goal is to make the user feel like they are viewing a verified, high-level clearance document.

---

## 2. Colors & Surface Logic
The palette is rooted in "University Blues" and "Institutional Greys," but executed with a premium, high-contrast finish.

*   **Primary Logic:** Use `primary` (#002045) for high-authority moments—headers, primary actions, and "official" stamps.
*   **The "No-Line" Rule:** Sectioning must never be done with 1px solid strokes. To separate the "Hero" section from "Projects," transition from `surface` (#f7f9fb) to `surface-container-low` (#f2f4f6). Boundary definition comes from tonal shifts, not outlines.
*   **Surface Hierarchy & Nesting:** Treat the UI as a physical stack.
    *   *Base:* `background` (#f7f9fb)
    *   *Section:* `surface-container-low` (#f2f4f6)
    *   *The "ID Card":* `surface-container-lowest` (#ffffff)
    By nesting a pure white card on a slightly grey base, we create a "natural lift" that feels architectural rather than digital.
*   **The "Glass & Gradient" Rule:** For floating navigation or mobile menus, use `surface` with a 70% opacity and a `24px` backdrop blur. Enhance primary buttons with a subtle linear gradient from `primary` (#002045) to `primary-container` (#1a365d) at a 135-degree angle to add "weight" and depth.

---

## 3. Typography: Editorial Authority
We pair the geometric precision of **Space Grotesk** with the utilitarian clarity of **Inter**.

*   **The Display Scale:** Use `display-lg` (Space Grotesk) for name headings. Apply a tight `letter-spacing: -0.04em` to create a "stamped" look.
*   **The Label Logic:** `label-md` and `label-sm` (Space Grotesk) are your most important tools. Use them in all-caps for "metadata"—dates, project categories, or "ID Number" labels. This reinforces the institutional theme.
*   **Body Contrast:** Use `body-lg` (Inter) for project descriptions. The switch from the sharp Space Grotesk to the soft Inter provides a necessary "human" touch to a professional system.

---

## 4. Elevation & Depth
Depth in this system is achieved through light and layering, never through heavy shadows.

*   **Tonal Layering:** To highlight a card, don't reach for a shadow; change the token to `surface-container-highest` (#e0e3e5).
*   **Ambient Shadows:** For the main "ID Badge" components that need to float, use a multi-layered shadow:
    *   `box-shadow: 0 4px 20px rgba(0, 32, 69, 0.04), 0 12px 40px rgba(0, 32, 69, 0.08);`
    Note the use of the `primary` blue tint in the shadow to keep it "academic" rather than "muddy grey."
*   **The "Ghost Border":** If a border is required for a form input, use `outline-variant` (#c4c6cf) at **20% opacity**. It should be felt, not seen.

---

## 5. Components

### The "ID Badge" Card
The core container. Use `surface-container-lowest` (#ffffff) with a `xl` (0.75rem) corner radius.
*   **Header:** Place a small "Digital Chip" icon (using `tertiary_fixed`) in the top right.
*   **Footer:** Use a barcode font or a series of tight vertical lines (using `outline`) to mimic a scannable ID.
*   **Separation:** No dividers. Use a 24px vertical gap between the header and the body content.

### Buttons (The "Official Seal")
*   **Primary:** `primary` background, `on_primary` text. Use `md` (0.375rem) radius. On hover, transition to `primary_container`.
*   **Secondary:** `surface_container_high` background. No border. This should look like it’s "embossed" into the page.
*   **The "Stamp" Action:** A circular button variant using `tertiary` (#321b00) for a "Verified" stamp effect, placed asymmetrically overlapping the edge of a card.

### Inputs & Metadata
*   **Fields:** Use `surface_variant` with a bottom-only "Ghost Border." Labels must be `label-sm` in all-caps.
*   **Status Chips:** Use `secondary_container` with `on_secondary_container` text. These should look like small plastic tabs on a file folder.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme whitespace. A "Student ID" feels important because the information has room to breathe.
*   **Do** use `tertiary` accents (#321b00) sparingly for "Warning" or "Special Edition" content to mimic old-school manila folders or gold-leaf seals.
*   **Do** align text to a strict left-margin "Identity Column," but allow images or "stamps" to break the grid and bleed off-center.

### Don’t:
*   **Don't** use 1px solid black dividers. It breaks the "premium paper" illusion.
*   **Don't** use standard "drop shadows." If it looks like a default Figma effect, it’s wrong.
*   **Don't** center-align long blocks of body text. Academic documents are almost always left-aligned for legibility and "form-filling" aesthetics.
*   **Don't** use vibrant, neon colors. Stick strictly to the "Academic Blue" and "Institutional Grey" tokens to maintain authority.