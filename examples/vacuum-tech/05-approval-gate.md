# 05 Approval Gate

## Current Status

Image candidates exist. The workflow is now waiting for user selection.

Generated image:

- `generated/logo-contact-sheet.png`

## Required User Decision

The user must choose one of these actions before SVG generation:

1. Select a candidate from the contact sheet.
2. Request refinements to one candidate and generate another image round.
3. Combine specific features from multiple candidates and generate another image round.
4. Reject all directions and revise the design strategy.
5. Authorize autonomous selection of the strongest generated direction.

## SVG Is Not Allowed Yet Unless

- a generated direction is selected or approved, and
- the selected direction is documented as the SVG source.

## What To Produce After Approval

- `logo.svg`: primary lockup
- `logo-icon.svg`: standalone mark / app icon
- `logo-wordmark.svg`: wordmark if appropriate
- `logo-inverted.svg`: inverted version
- `vi-system.md`: full identity rules
- `brand-manual.html`: rendered HTML VI manual
- optional generated application visuals under `generated/applications/`

## Vector Reconstruction Requirements

The final SVG must translate the selected image into disciplined geometry. It must not trace raster artifacts, invent a new concept, or skip the selected visual direction.
