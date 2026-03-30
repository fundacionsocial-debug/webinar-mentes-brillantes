# Design System Strategy: The Emotional Sanctuary

### 1. Overview & Creative North Star
This design system is built upon the Creative North Star of **"The Emotional Sanctuary."** Unlike standard utility-first applications, this system is an editorial experience designed to feel like a high-end, private members' club for the mind. We move away from the "template" look by embracing **Atmospheric Depth** and **Intentional Asymmetry**. 

The goal is to reflect emotional intelligence through a layout that "breathes." We achieve this by using oversized white space (from our Spacing Scale), overlapping elements that break the rigid container grid, and a high-contrast typographic scale that mirrors the weight and importance of wisdom.

### 2. Colors: The Tonal Atmosphere
The palette is rooted in the "Deep Blue" of the logo, expanded through Material Design tokens to create a sophisticated, dark-mode-first environment.

*   **Primary (#e9c349):** Our "Rich Gold." Use this for high-impact moments—headings, primary CTAs, and active states. It represents the "Brilliance" within the name.
*   **Surface & Background (#131313):** A "Deep Black" foundation. This provides the "Gymnasium" with a sense of focus and exclusivity.
*   **On-Surface (#e5e2e1):** Our "Creamy White." Use this for all long-form reading to ensure high legibility without the harshness of pure white.

#### The "No-Line" Rule
Designers are prohibited from using 1px solid borders for sectioning. Structural boundaries must be defined solely through background color shifts. For example, a `surface-container-low` section should sit directly on a `surface` background to create a felt, rather than seen, transition.

#### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers.
*   **Base:** `surface` (#131313)
*   **Sectioning:** `surface-container-low` (#1c1b1b)
*   **Floating Elements:** `surface-container-high` (#2a2a2a)
This nesting creates a soft, natural lift that mimics fine paper or layered glass.

#### The "Glass & Gradient" Rule
To elevate the experience beyond flat design, use **Glassmorphism** for floating cards and navigation bars. Apply a `secondary_container` background at 60% opacity with a `backdrop-blur-xl` effect. For Hero sections, utilize a subtle gradient transitioning from `surface` to the deep blue of `secondary_container` to provide visual "soul."

### 3. Typography: The Editorial Voice
Our typography is a conversation between classic wisdom (Serif) and modern clarity (Sans-Serif).

*   **Display & Headline (Noto Serif):** These are the "Authority" levels. Use `display-lg` for hero moments with tight letter-spacing (-0.02em) to evoke a premium editorial feel. Headlines should be treated like book titles—grand and purposeful.
*   **Title & Body (Manrope):** These are the "Clarity" levels. Manrope provides a technical, refined contrast to the Serif. Use `body-lg` for insights and `body-md` for instructional text.
*   **Accents:** Utilize the `label-md` or `label-sm` tokens in all-caps with increased letter-spacing (0.1em) for category tags or "emotional markers."

### 4. Elevation & Depth
In this system, depth is a feeling, not a drop-shadow.

*   **The Layering Principle:** Avoid traditional shadows. Instead, place a `surface-container-highest` card on a `surface-dim` background. This creates a "Tonal Lift" that feels integrated into the architecture of the page.
*   **Ambient Shadows:** If a floating action requires a shadow, it must be extra-diffused. Use a blur of 32px or higher with an opacity of 6% using the `primary` (Gold) color tinted toward black. This mimics natural light reflecting off a luxury surface.
*   **The "Ghost Border" Fallback:** If a container requires a boundary for accessibility, use a "Ghost Border." Apply the `outline-variant` token at 15% opacity. Never use 100% opaque borders; they disrupt the "Sanctuary" atmosphere.

### 5. Components: Refined Primitives

*   **Buttons:**
    *   **Primary:** A solid `primary` (Gold) pill shape (`rounded-full`) with `on_primary` text. Use for the main "Call to Wisdom."
    *   **Secondary:** A "Ghost" style button with a 1px `primary` border at 40% opacity and no fill.
*   **Cards:** Forbid divider lines. Use vertical spacing (Scale `8` or `10`) to separate content. Cards should use `rounded-xl` (1.5rem) to soften the high-contrast aesthetic.
*   **Input Fields:** Minimalist approach. Only a bottom-border using the "Ghost Border" rule. Labels use `label-md` in `primary` (Gold) to guide the user's eye.
*   **Insight Chips:** Small, `secondary_container` capsules with `on_secondary_container` text. Use these to tag emotional states or topics.
*   **The "Progress Thread":** For the "Emotional Gym" tracking, use a thin, `primary` (Gold) gradient line instead of a thick progress bar. It should feel like a delicate gold thread.

### 6. Do's and Don'ts

#### Do:
*   **Embrace Asymmetry:** Place a `display-lg` heading on the left and a `body-md` paragraph slightly offset to the right to create an editorial flow.
*   **Use Gold Sparingly:** Gold is a highlight, not a primary color. Use it for the "spark" of an idea.
*   **Prioritize Breathing Room:** When in doubt, increase the spacing. Use `16` (5.5rem) or `20` (7rem) for section gaps.

#### Don't:
*   **Don't use pure white (#FFFFFF):** It breaks the luxury atmosphere. Always use the Creamy White `on_surface` (#e5e2e1).
*   **Don't use standard shadows:** If the shadow looks like a "default," it is wrong. It must be ambient and tinted.
*   **Don't use 1px solid borders:** Rely on background tonal shifts to define your containers.
*   **Don't crowd the UI:** This is a "Gymnasium for the Emotions"—it needs space for reflection. Overloading a screen with 10+ components is a violation of the system.