# Bento Harmony: Design System

### 1. Overview & Creative North Star
**Creative North Star: The Glass Curator**
Bento Harmony is a high-end editorial interface that prioritizes airy transparency and structured modularity. It departs from the rigid, boxed-in layouts of traditional dashboards by employing a "Bento Box" philosophy—where information is organized into organic, semi-transparent vessels that appear to float over a soft, atmospheric background. The aesthetic is defined by "Deep Softness": the intersection of sharp, modern typography and diffused, glass-like surfaces.

### 2. Colors
Bento Harmony utilizes a palette of soft periwinkle, muted slate, and warm accents to create a calm yet productive environment.

- **Primary Role:** `#8B93FF` (Periwinkle) acts as the primary driver for progress, active states, and call-to-actions.
- **The "No-Line" Rule:** Sectioning must never be done with 1px solid dark borders. Use `rgba(255, 255, 255, 0.8)` for "Ghost Borders" or rely entirely on background shifts between `surface` and `surface_container`.
- **Surface Hierarchy:** 
    - **Background:** `#F8F9FA` with a subtle multi-stop radial gradient for depth.
    - **Base Surface:** `rgba(255, 255, 255, 0.6)` with a 16px backdrop blur.
    - **Hovered Surface:** `rgba(255, 255, 255, 0.8)` to indicate interactivity.
- **Accent Tones:** Use "Mint" (`#A6E3E9`), "Peach" (`#FFD3B6`), and "Lemon" (`#FFF1DC`) for secondary categorization and priority markers.

### 3. Typography
The system uses **Plus Jakarta Sans** as the primary typeface, supported by **Outfit** for headlines to provide a geometric, modern edge.

- **Display (32px):** Used for primary page titles (e.g., "Dashboard"). Bold weight with -0.02em letter spacing.
- **Headline (1.25rem - 1.5rem):** Semi-bold. Used for card titles and section headers.
- **Body (1rem / 0.875rem):** High readability for content and descriptions. Use `#7077A1` for muted secondary body text.
- **Label (13px):** All-caps with 0.05em tracking for metadata, dates, and small tags.

### 4. Elevation & Depth
Depth in Bento Harmony is achieved through **Tonal Layering** and optical physics rather than heavy drop shadows.

- **The Layering Principle:** Stack `glass-panel` elements over the background. Floating elements should use a `backdrop-filter: blur(16px)` to create a sense of physical material.
- **Ambient Shadows:** 
    - **Level 1 (Default):** `0 24px 48px -12px rgba(139, 147, 255, 0.15)`. This is a wide, diffused shadow with a hint of the primary brand color to simulate light passing through colored glass.
    - **Level 2 (Active/Hover):** `0 8px 16px -4px rgba(139, 147, 255, 0.2)`.
- **Glassmorphism:** All containers must feature a semi-transparent white background and a subtle white outline (`rgba(255, 255, 255, 0.5)`) to catch the light at the edges.

### 5. Components
- **Bento Cards:** 24px corner radius. Must include `backdrop-filter` and the signature wide shadow.
- **Interactive Chips:** 9999px (Pill-shaped) with low-opacity primary backgrounds (`rgba(139,147,255,0.1)`).
- **Buttons:** 
    - **Primary:** Solid `#8B93FF` with white text and a specific glow shadow: `0_4px_12px_rgba(139,147,255,0.4)`.
    - **Ghost:** Transparent background with hover states that increase opacity to 80%.
- **Progress Indicators:** Circular "Focus Rings" should use a 12px stroke width with rounded caps and a high-contrast periwinkle stroke over a 40% opaque white track.

### 6. Do's and Don'ts
- **Do:** Use asymmetrical layout groupings to create visual interest.
- **Do:** Use color blocks (vertical bars) on the left of cards to indicate priority or status.
- **Don't:** Use pure black (`#000000`) for text; use `#2D3250` for better integration with the glass aesthetic.
- **Don't:** Apply shadows to every element; only to the primary "vessels" containing the content.
- **Don't:** Use sharp corners. The minimum radius for any container is 12px, with the standard being 24px.