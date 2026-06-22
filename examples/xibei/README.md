# 西北食品品牌 VI 测试

This folder is a compliance test for `$brand-design-skill` after the image-first workflow update.

## Test Brief

User request: 为一个食品品牌（西北地区的）做一个品牌 VI。

## Compliance Status

This environment did not expose an image-generation tool and did not have `OPENAI_API_KEY` configured. According to the updated skill rules, the test must stop before final SVG construction.

The compliant output is therefore:

- [`strategy.md`](strategy.md): concept parsing, Socratic questions, design direction, and image-generation logo prompts
- [`logo-image-prompts.md`](logo-image-prompts.md): ready-to-run prompts for image-generated logo exploration
- `draft-pre-image/`: legacy draft artifacts created before the image-first gate was added; these are not compliant final outputs under the current skill

## Next Step

Generate logo image candidates from `logo-image-prompts.md`, select one direction, then reconstruct the approved visual direction as SVG and build the final HTML VI manual.
