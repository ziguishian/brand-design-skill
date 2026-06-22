# Vacuum Tech Brand VI Regression Example

This folder records a previous behavior that is now considered incorrect.

Task:

> 做一个科技品牌，吸尘器的品牌 VI。

## Regression

The agent generated `generated/logo-contact-sheet.png` before the user supplied brand name, target audience, price tier, logo inspiration, avoid list, and application priorities.

Under the current `$brand-design-skill`, this is not compliant. The correct behavior is shown in:

- [`../vacuum-tech2/`](../vacuum-tech2/)

## Why This Is Incorrect

The workflow must first ask Socratic questions and wait for the user's answers, or for explicit permission to proceed with assumptions. Image generation is not allowed from an incomplete brief.

## Preserved Files

The files in this folder are kept as a regression artifact only. Do not use them as the preferred workflow example.
