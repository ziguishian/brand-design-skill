# Design Output Standards

Use these standards when producing concrete brand identity artifacts. They support the conversational image-first and image-final workflow in `SKILL.md`.

## Research Baseline

Professional brand guidelines commonly include more than logo/color/type. Public guidance from Canva states that brand identity guidelines should include logos, colors, fonts, images, illustrations, icons, mission, vision, values, voice, tone, formatting preferences, copy guidelines, templates, resources, and points of contact. Frontify breaks professional guidelines into brand core, logo guidelines, color, typography, imagery/iconography, design tokens, voice/tone, social media, templates/applications, and governance.

Use this baseline to avoid underbuilt VI manuals.

## Required Image-First and Image-Final Workflow

Do not create SVG logos. The logo process is image-based from exploration through final asset delivery.

If image generation is unavailable:

1. Produce precise image-generation prompts only after the brief is complete or assumptions are explicitly approved.
2. Ask the user to enable image generation or provide candidate images.
3. Stop before final logo asset creation, VI application images, or final HTML manual visuals.

The final logo must be a refined image asset derived from an approved generated direction, not a direct first-draft invention and not an SVG reconstruction.

## Conversational Gate Checklist

Before moving stages, verify:

- A new brand/logo/VI request received a Socratic intake response first, unless the brief was complete and the current stage had explicit approval.
- "Test this skill", "complete VI", "you decide", or "generate everything" was not treated as consent to bypass gates.
- Intake has enough detail or the user explicitly authorized assumptions.
- Missing brand details triggered Socratic questions instead of image generation.
- The user answered blocking questions or explicitly approved named assumptions before design direction.
- Image generation did not happen in the same response as unanswered intake questions.
- Design routes were presented and approved before image generation.
- Image-generation prompts are industry-specific and structurally varied.
- After image generation, the response gives explicit next-step options: choose, refine, combine, reject, or ask for recommendation.
- Actual generated logo images exist before final logo asset creation.
- User approved or selected a generated direction before final logo asset creation.
- User approved the final logo image assets before the full VI manual.
- Complete/full VI manual requests use `full-vi-manual-outline.md` and render all 21 chapters.
- HTML manual uses approved logo images and appropriate generated application visuals when available.

If any item fails, stop and ask for the missing input.

## Stage QA Checklist

Use this checklist before sending a response or producing an artifact.

### Intake QA

- Did I list what is known?
- Did I list what is missing?
- Did I ask only useful questions?
- Did I stop before image generation?
- Did I provide a clear next decision?

### Design Direction QA

- Is every style choice tied to industry, audience, price tier, and application?
- Are the logo routes structurally different?
- Did I ask permission before image generation?
- Did I avoid final assets?

### Image Generation QA

- Were images generated only after user approval?
- Are directions clean enough for logo use?
- Are directions not just color variations?
- Did I show the image(s)?
- Did I give choose/refine/combine/reject/recommend next options?

### Selection QA

- Did the user actually approve a generated direction?
- Did I document the selected source image?
- If I recommended a candidate, did I ask confirmation before final asset generation?

### Final Logo Image QA

- Is the final logo image based on the selected generated direction?
- Are primary, icon/social, and any needed alternate logo images saved in the workspace?
- Does the logo system include inspiration/source logic, positive and negative form, black/white, inverted, and multi-color usage?
- Does the logo system include a professional specification board with primary logo, dark/light background variants, black/white chips, App Icon variants, clear space, construction grid, geometry/radius callout, and application strip?
- Is text legible and not garbled?
- Does the image work at likely display sizes?
- Are background variants provided when needed?
- Did I ask the user to approve final logo images before VI manual?

### VI QA

- Does the manual scope match the user's request?
- Are applications industry-specific?
- Are imagery/art direction and graphic devices included?
- Are there several application images or clearly separated application scenes instead of only one generic board?
- Are voice/tone and asset delivery included when relevant?
- Did I ask approval before rendering final HTML?
- If the user requested a complete/full VI manual, did I present the 21-chapter structure before final rendering?

### HTML QA

- Are paths valid?
- If this is a complete/full VI manual, are all 21 chapters and every numbered subsection from `full-vi-manual-outline.md` visibly rendered?
- Does the page include a table of contents linking to all 21 chapters?
- Does the page include a final coverage checklist with complete / not applicable / pending asset statuses?
- Are approved logo image assets linked and visible?
- Does the logo section look like a professional VI specification board rather than a decorative gallery?
- Are clear-space, grid, geometry, dark/light background, App Icon, black/white, and application panels visible near the start of the manual?
- Can users copy color values and key design tokens with one click?
- Are font specimens rendered visually in the page, not merely described?
- Are images reused intelligently through crops, repeated frames, CSS background positioning, or atlas/sprite-like sections?
- Are generated images displayed without stretching, squeezing, or unintended aspect-ratio distortion?
- Are microinteractions present but restrained and nonessential?
- Are missing images visibly labeled instead of hidden?
- Is the layout responsive?
- Is text unclipped and non-overlapping?

## Regression Conditions

Treat the output as a regression if any of these happen:

- The first response to a new brand/logo/VI request creates files, images, final assets, or a manual before Socratic intake.
- The agent treats "test this skill", "complete VI", "you decide", or "generate everything" as permission to skip confirmations.
- The agent generates images before asking required questions.
- The agent generates images in the same response that first proposes design routes.
- The agent creates final logo images before initial image exploration and user selection.
- The agent creates SVG logo files or SVG reconstructions.
- The agent skips user selection after showing images.
- The agent treats its own recommendation as user approval.
- The agent creates a full VI manual before final logo image approval.
- The agent renders the final HTML manual in the same response that first proposes the VI/application plan.
- The final HTML for a complete/full VI request omits any of the 21 required chapters.
- The final HTML hides irrelevant sections instead of marking them "Not applicable / 不适用" with reasons.
- The final logo section lacks professional usage panels such as clear space, grid, geometry, background variants, and app icon variants.
- The final manual contains generic applications unrelated to the industry.

When a regression happens, mark the artifact as exploratory or regression, return to the correct stage, and ask for the missing user decision.

## Professional Brand Manual Contents

A complete VI manual should include these sections when relevant to the brand.

For a complete/full VI manual request, `references/full-vi-manual-outline.md` is authoritative. Render all 21 top-level chapters and all numbered subsections. The shorter list below is a conceptual baseline only; it does not replace the required 21-chapter structure.

### 1. Brand Foundation

- Brand name and naming logic
- Brand story or origin
- Mission, vision, values
- Positioning statement
- Target audience and usage occasions
- Personality attributes
- Competitive or category context
- Brand promise and key message

### 2. Design Strategy

- Design direction
- Visual metaphor
- Industry relevance
- Cultural or geographic cues
- Mood keywords with design evidence
- Aesthetic references
- Avoid list

### 3. Logo Image System

- Logo inspiration/source board
- Visual metaphor and concept rationale
- Primary logo image
- Secondary lockup image
- Icon / social avatar image
- Wordmark-style image when useful
- Horizontal and vertical logo image versions
- Positive form demonstration
- Negative form demonstration
- Black-on-white version
- White-on-dark version
- Multi-color version
- Monochrome-style image version when useful
- Inverted/dark-background image version
- Small-size image version
- App/social avatar crop
- Professional VI specification board with clear-space, grid, geometry, black/white, dark/light background, app icon, and application panels

### 4. Logo Usage

- Clear space rule
- Minimum sizes for screen and print
- Placement rules
- Background control
- Co-branding or partner placement, if relevant
- Misuse examples: stretching, recoloring, effects, outlines, low contrast, crowding, rotation, unapproved crops, blurry export, or unapproved lockups

### 5. Color System

- Primary palette
- Secondary palette
- Neutral palette
- Accent colors
- Functional colors, if digital product is relevant
- HEX and RGB values
- CMYK/Pantone guidance when print, packaging, signage, or merchandise matters
- Contrast and accessibility guidance
- Approved color combinations
- Ratio guidance, such as dominant/support/accent proportions

### 6. Typography System

- Primary typeface
- Secondary/body typeface
- Accent typeface, if any
- Fallback fonts
- Type scale
- Font weights by use case
- Line height and spacing rules
- Numerals, units, labels, and legal text rules for packaging or UI
- Licensing notes when specific commercial fonts are recommended

### 7. Imagery and Art Direction

- Photography style
- Illustration style, if used
- Food/product styling rules when relevant
- Lighting, material, composition, crop, and background rules
- Human presence rules
- Approved and disallowed image examples or descriptions
- Image-generation prompts for campaign, packaging, social, and manual visuals

### 8. Graphic Devices

- Patterns
- Texture rules
- Iconography
- Line/stroke rules
- Shape language
- Data or nutrition label styling, if relevant
- Motion principles, if relevant

### 9. Layout System

- Grid system
- Spacing scale
- Alignment rules
- Hierarchy rules
- Margin/safe-zone rules
- Editorial or packaging layout templates
- Digital responsive rules when relevant

### 10. Applications

Choose applications based on the industry, not generic mockups.

For food brands, include:

- package front system
- package back information layout
- flavor or SKU color coding
- ingredient photography direction
- label/seal system
- shipping box or gift box
- e-commerce hero image
- social post system
- shelf strip or retail signage
- menu/storefront only if the brand has retail presence

Other industries should adapt this list to their real touchpoints.

### 11. Voice and Tone

Include when the brand needs customer-facing communication:

- voice principles
- tone by context
- vocabulary
- tagline or messaging examples
- copy do/don't

### 12. Design Tokens and Asset Delivery

Include when digital or implementation use matters:

- color tokens
- type tokens
- spacing tokens
- radius/stroke tokens
- image export sizes and formats
- file naming
- governance and update notes

## Image Generation Standards

Logo exploration images:

- Must be generated before final logo asset creation.
- Must be clean, restrained, and logo-appropriate.
- Must show structurally distinct concepts.
- Must avoid 3D, fake product mockups, over-rendered effects, unreadable tiny text, and generic template aesthetics.
- Must be evaluated for concept, industry relevance, silhouette, scalability in raster contexts, text legibility, and system potential.

Final logo images:

- Must be derived from a user-approved generated direction.
- Must be saved in the workspace, not only in the default generated image folder.
- Should include practical variants when needed: primary, icon/social, dark-background, monochrome-style, positive/negative form, black/white, multi-color, and small-size.
- Must include or be accompanied by a professional logo-system board following `professional-vi-visual-style.md`.
- Must include a visible rationale for the logo's inspiration source and form logic in the final manual, not only a finished mark.
- Must be checked for garbled text, unwanted watermarks, low contrast, broken cropping, excessive detail, and poor small-size readability.
- Should use high-resolution PNG/WebP/JPG as appropriate; PNG is preferred for logos and manual embedding.
- Must not be converted to SVG or traced into vector files.

VI/application images:

- Should be generated after final logo image approval when they help the manual.
- Should usually include several focused scenes, such as product, packaging, ecommerce, social, retail, signage, UI, or campaign, rather than relying on one large application board.
- Must match industry and price tier.
- For food brands, prioritize packaging systems, ingredient/product photography direction, shelf/social/e-commerce visuals, and label systems.
- For product brands, prioritize real product marks, packaging, detail cards, ecommerce thumbnails, social templates, retail/display, instruction/warranty material, and material/finish closeups.

## HTML Brand Manual Standards

- Deliver a complete HTML file with embedded CSS unless the user's environment calls for a framework.
- For complete/full VI requests, render the full 21-chapter structure from `full-vi-manual-outline.md`, including every numbered subsection as visible content.
- Include a table of contents with links to all 21 chapters and a final coverage checklist.
- Do not drop non-core sections such as digital product, motion, office collateral, marketing collateral, digital media, packaging, environment, merchandise, governance, or file delivery. If not relevant, mark them "Not applicable / 不适用" and explain why.
- Use editorial sections with strong hierarchy and generous whitespace.
- Use the professional VI visual language from `professional-vi-visual-style.md`: monochrome-first specification boards, thin dividers, calm grids, bilingual labels, precise measurement diagrams, and restrained application strips.
- Match the aesthetic to the industry and price tier.
- Show approved logo image assets directly.
- Make the logo the primary visual subject in the manual, not just one asset among applications. Include inspiration/source, construction logic, positive/negative form, black/white, inverted, multi-color, clear space, small-size behavior, and misuse guidance.
- The early logo section should include a complete board-style layout: large logo field, dark/light usage, clear space, grid, geometry/radius, black/white, App Icon, and practical applications.
- Use multiple generated application images when available; otherwise include clearly labeled placeholders and prompts only if image generation was unavailable.
- Include one-click copy controls for color values and practical tokens. The control must give visible feedback after copying.
- Render font specimens directly in the page with sample headlines, body copy, numerals, labels, and packaging/legal microcopy. Do not only list font names or sizes.
- Reuse imagery elegantly. It is acceptable to use a single generated board as a visual atlas and crop it into several panels with `object-fit`, `object-position`, CSS background positioning, or an explicit sprite/atlas image.
- Preserve source image proportions. Use a containing frame plus `object-fit: contain` when the full generated image must be visible. Use `object-fit: cover` only for deliberate editorial crops. For sprite/atlas sections, match the visible frame ratio to the source tile ratio so the background is not squeezed.
- Include restrained microinteractions such as hover lift, active navigation, copy feedback, scroll reveal, or subtle image movement. Respect `prefers-reduced-motion`.
- Include industry-specific applications instead of generic decorative cards.
- Make layout responsive, with no overlapping text or clipped labels on mobile.
- Avoid noisy gradients, decorative blobs, generic stock imagery, fake 3D mockups, and template-like filler.
- Do not require SVG assets for the logo system.

## Design Reasoning Standards

Explain decisions through system logic:

- Why this metaphor fits the brand.
- How generated image exploration informed the final logo image assets.
- How composition, color, and typography encode the concept.
- How color and type support the positioning.
- How the identity scales across real touchpoints.
- How the system fits the industry.

Avoid unsupported claims such as "premium", "modern", or "innovative" unless tied to a visible design choice.

## Source Links

- Canva: https://www.canva.com/learn/your-brand-needs-a-visual-style-guide/
- Frontify: https://www.frontify.com/en/guide/brand-guidelines/
