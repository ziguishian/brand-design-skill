# Professional VI Visual Style

Use this reference when creating final logo image assets, VI system boards, and HTML brand manual visuals. The target quality is a professional brand identity guideline board, not a decorative showcase.

## Visual Direction

Prefer a disciplined monochrome-first specification style:

- off-white or white background
- deep black primary mark
- cool gray supporting lines and annotations
- restrained accent color only when needed for hierarchy
- generous whitespace
- thin divider lines
- precise grid overlays
- bilingual labels when useful: English title plus Chinese subtitle
- specification panels instead of decorative cards

The work should feel like a senior designer's VI presentation board: quiet, exact, geometric, and production-aware.

## Required Logo System Board

For final logo image assets or a complete VI manual, create or render a prominent logo system board that includes:

- large primary logo image on a clean light field
- dark background application
- light background application
- black/white color chips with HEX labels
- App Icon variants, including light, dark, and circular crop when relevant
- clear space diagram with x-based measurement
- grid construction diagram
- geometry or radius detail callout
- small application strip, such as business card, notebook, bag, packaging, social icon, or product surface
- short bilingual rationale explaining form logic and production use

If generated image assets cannot cover every panel, render the missing panels in HTML/CSS as specification diagrams while keeping the logo itself image-based.

## Source Preservation Rule

The professional VI board must explain the approved logo; it must not redesign it.

- Use the user-selected candidate image as the source of truth.
- Keep the mark's silhouette, negative space, proportions, stroke/weight relationships, angle/curve logic, and distinctive features unchanged.
- Grid, geometry, clear-space, app icon, and background panels should be drawn around or behind the approved image.
- Do not "improve" the mark to fit a cleaner grid unless the user explicitly approves a shape change.
- Do not recreate the logo from a text-only prompt for the board. Use the approved image asset directly or an image edit/reference workflow that preserves it.

## Board Composition

Use a structured board layout:

- left column: title, category, concept rationale, short Chinese explanation
- center: oversized primary logo image with generous breathing room
- top/right panels: dark/light background variants and clear space
- mid/right panels: grid and geometry
- bottom strip: black/white, app icon, and physical/digital applications

Avoid page sections that look like random marketing cards. Every panel should teach a rule.

## HTML Manual Translation

When translating this visual direction into HTML:

- Use section dividers, measured grids, and compact bilingual labels.
- Make the logo system feel like a technical specification board.
- Use CSS grid for equal-height panels and stable ratios.
- Render clear-space and grid diagrams with CSS lines or raster images, but never reconstruct the logo as SVG.
- Use CSS-only measurement guides, dotted grid overlays, and x labels around approved logo images.
- Keep backgrounds quiet and reduce decorative gradients.
- Prefer black/white/neutral systems for logo rules, then introduce brand color in the color chapter.

## Image Generation Prompt Pattern

When generating a logo system or VI board image, use this prompt pattern:

```text
Use case: logo-brand
Asset type: professional VI specification board
Primary request: Create a professional brand identity guideline board for <brand>, focused on the approved logo system.
Style/medium: monochrome-first premium VI manual board, precise Swiss grid, bilingual labels, quiet Apple-like restraint, production-ready design specification.
Composition/framing: wide board with large primary logo on the left/center, dark background and light background variants, clear-space diagram, grid construction, geometry/radius callout, black/white color chips, app icon variants, and a bottom strip of real application mockups.
Color palette: white/off-white, black, cool gray, restrained brand accent only.
Text: keep labels short and readable; use bilingual headings such as "Logo System 标志系统", "Clear Space 安全空间", "Grid 标准制图", "Geometry 几何规范", "Application 应用系统".
Constraints: logo must remain image-based; clean alignment; no fake paragraphs; no clutter; no 3D mascot; no decorative gradients; no random UI.
Source preservation: use the approved logo image as the source of truth; preserve its silhouette, negative space, proportions, stroke/weight relationships, and angle/curve logic exactly; create specification panels around the mark, not a redesigned mark.
Avoid: generic moodboard, advertising poster, excessive color, warped mockups, illegible tiny text, fake brand manual filler.
```

## Quality Bar

Treat output as below standard if:

- the logo is only shown once without construction or usage rules
- the manual lacks clear-space, grid, geometry, background, and App Icon demonstrations
- applications dominate before the identity rules are explained
- the page looks like a marketing landing page rather than a usable VI standard
- labels are decorative instead of specifying how to use assets
- the board changes the approved mark while trying to make the grid or geometry cleaner
