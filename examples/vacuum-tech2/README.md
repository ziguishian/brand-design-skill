# Vacuum Tech Brand VI Test 2

This folder retests `$brand-design-skill` after tightening the conversational gates.

Task:

> 做一个科技品牌，吸尘器的品牌 VI。

## Correct Behavior

The agent must not generate logo images from this brief yet. The brand name, target audience, price tier, hero product type, logo inspiration, avoid list, and primary applications are incomplete.

The correct output is a Socratic interview and a clear next decision for the user.

## Files

- [`00-expected-response.md`](00-expected-response.md): the correct first response
- [`01-readiness-check.md`](01-readiness-check.md): why image generation is blocked
- [`02-next-step-template.md`](02-next-step-template.md): what the agent should do after the user answers

## Note About Previous Test

`examples/vacuum-tech/` generated a contact sheet too early. It is now treated as a regression example, not the preferred behavior.
