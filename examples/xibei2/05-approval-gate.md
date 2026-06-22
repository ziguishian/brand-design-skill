# 05 Approval Gate

## Current Status

Blocked before final SVG.

The skill requires image-generated logo explorations before SVG construction. This environment has no available image generation tool, so the correct behavior is to stop here.

## Required Inputs Before SVG

At least one of the following must happen:

1. The image-generation prompts in `04-logo-image-prompts.md` are run and candidate logo images are saved into this folder.
2. The user provides generated candidate images.
3. Image generation becomes available in the environment.

## Required User Decision

After candidate images exist, the user must choose one path:

- select one direction as final
- combine specific elements from multiple directions
- reject all and request another image-generation round
- authorize the agent to choose the strongest candidate

## SVG Construction Rules After Approval

Only after approval:

- reconstruct the approved image as pure SVG
- do not trace raster noise literally
- preserve the selected concept, silhouette, and style
- simplify geometry for production use
- create variants: primary lockup, icon, wordmark, monochrome, inverted
- document clear space, minimum size, and misuse rules

## Files To Produce After Approval

- `logo.svg`
- `logo-icon.svg`
- `logo-inverted.svg`
- `vi-system.md`
- `brand-manual.html`
- optional generated application images in `generated/`
