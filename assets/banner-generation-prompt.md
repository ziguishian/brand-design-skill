# Banner Generation Prompt

Use this prompt with an image generation model to create `assets/banner.png`.

The preferred visual direction is an open-source launch poster for an AI brand design director: clean white background, bold black headline typography, cobalt-blue action accents, modular UI/process cards, dotted grids, thin connector lines, and a premium productized tool feeling. It should feel closer to a sharp open-source README/product poster than a decorative brand mockup.

```text
Use case: ads-marketing
Asset type: GitHub README top banner, 1600x900
Primary request: Create a premium open-source launch banner for "Brand Design Skill", a Codex skill that turns one rough idea into a complete professional VI brand system and HTML brand manual.
Scene/backdrop: clean white/off-white editorial poster background with faint dot matrices, subtle grid lines, and modular card layout.
Subject: a central product card labeled "AI Brand Design Director" showing a brand-system workflow; surrounding cards show: 01 input idea, 02 AI execution flow, 03 logo exploration grid, 04 VI manual preview, 05 HTML brand manual preview, 06 open-source repository card.
Style/medium: high-end monochrome product poster, Swiss/Apple-like restraint, modern Chinese tech editorial layout, crisp UI cards, premium SaaS documentation aesthetic, not a generic mockup.
Composition/framing: portrait-to-landscape friendly poster composition; oversized bold black Chinese headline at top-left, central large product card, smaller supporting cards around it, dotted blue connector arrows between cards, repo chip near upper-right, footer strip with open-source/license/community cues.
Lighting/mood: bright, minimal, confident, precise, quietly premium.
Color palette: white/off-white, deep black, cool gray, vivid cobalt blue accent (#4353FF) only.
Typography: bold geometric Chinese headline with clean sans-serif English; high contrast, generous spacing, crisp alignment.
Text (verbatim, keep readable and minimal): "我开源了一个 AI 品牌设计总监"; "一句想法 -> 整套 VI"; "AI Brand Design Director"; "ziguishian/brand-design-skill"; "Brand Design Skill"; "Open Source".
Constraints: make all visible text legible; keep the Chinese headline large and accurate; use only the listed text; no fake paragraphs; no random letters; no people; no mascot; no 3D blob; no dark gradient background; no clutter; no watermark.
Avoid: illegible AI text, misspelled Chinese, fake UI gibberish, decorative orbs, neon gradient SaaS look, generic template collage, overly photoreal desk mockups.
```

If the image model cannot reliably render the exact text, generate a clean text-free poster background in this style and overlay the exact text later with HTML/CSS or a graphics editor. Recommended final output: PNG at 1600x900 or larger. Save the final file as `assets/banner.png`, then both README files can continue to reference `assets/banner.png`.

