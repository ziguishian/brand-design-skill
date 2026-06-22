# Conversational Workflow Details

Use this reference whenever the agent is actively guiding a user through brand design. The goal is to prevent skipped steps and make every turn conversational, explicit, and reversible.

## Global Rule

Never silently advance a stage. Every stage has:

- Entry condition
- Agent action
- User-facing response
- Exit condition
- Forbidden actions
- Next decision

If the exit condition is not met, ask for the missing input and stop.

Do not create SVG logos or SVG logo reconstructions. This skill uses image generation for logo exploration, final logo assets, VI applications, and manual visuals.

## No Simulated Consent

Testing the skill is not permission to simulate a whole customer journey. Treat "test this skill", "make a complete VI", "you decide", "generate everything", and "do it all" as real user requests that still require gates.

The agent must never invent user approvals for:

- assumption approval
- route approval for image generation
- candidate selection
- final logo image asset approval
- VI/application image plan approval
- final HTML manual approval

If the user wants the agent to decide, propose named assumptions or a recommendation, then ask for confirmation. Do not treat the agent's own recommendation as the user's approval.

## New Request Rule

For every new brand/logo/VI request, the first response must be Intake or Socratic Interview unless the user has already supplied a complete brief and explicit approval for the current stage.

The first response must not:

- generate images
- create files
- create an HTML manual
- present runnable image prompts as if image generation is already approved
- claim a logo candidate is selected

The first response must end with a specific user action, usually answering questions or approving named assumptions.

## Stage 0: Intake

Entry condition: user gives a brand, logo, or VI request.

Agent action:

1. Summarize the request in plain language.
2. Extract confirmed facts.
3. List missing facts.
4. Determine ambiguity level.
5. Ask Socratic questions.

Exit condition:

- The readiness checklist is complete, or
- The user explicitly authorizes named assumptions.

Forbidden:

- Do not generate images.
- Do not write logo prompts as if ready to generate.
- Do not create final logo assets.
- Do not create HTML manual.

Response template:

```markdown
## Stage
Intake -> Socratic Interview

## What I Understand
<confirmed facts>

## Missing Information
<blocking missing facts>

## Questions
<5-8 focused questions>

## Next Decision
Please answer these questions. I will not generate logo images until the brief is complete or you explicitly ask me to proceed with assumptions.
```

If the user asks for complete delivery immediately, add one sentence: "I can deliver the full VI manual after the approval gates, but I need the design brief decision first."

## Stage 1: Socratic Interview

Entry condition: blocking details are missing.

Question quality rules:

- Ask only questions that change the design outcome.
- Prefer grouped questions: product, audience, taste, logo inspiration, applications, constraints.
- If the user answers partially, ask only the remaining blockers.
- If the user says "you decide", restate assumptions and ask whether to proceed.

Exit condition:

- User answers blocking questions, or
- User explicitly authorizes assumptions.

Forbidden:

- Do not treat silence as approval.
- Do not use broad words like "premium" without asking what kind of premium.
- Do not proceed from an incomplete brief to image generation.
- Do not interpret "full VI", "test", or "complete delivery" as consent to bypass the interview.

## Stage 2: Design Direction Before Images

Entry condition: readiness checklist is satisfied.

Agent action:

1. Summarize confirmed brief.
2. State any approved assumptions.
3. Define the design direction system.
4. Offer 3-5 structurally different image-generation directions.
5. Ask user which directions to generate, or whether to generate all.

Exit condition:

- User says to generate directions.

Forbidden:

- Do not generate images in the same response.
- Do not create final logo assets.

Hard stop: even if the user asked the agent to decide, the agent must first present route options and ask for image-generation approval.

Response template:

```markdown
## Stage
Design Direction Before Images

## Confirmed Brief
<facts + assumptions>

## Design Direction System
<strategy>

## Logo Image Direction Options
1. <direction>
2. <direction>
3. <direction>

## Next Decision
Choose the directions to generate, or say "generate all". I will create image candidates next, then you choose one before final logo image refinement.
```

## Stage 3: Logo Image Generation

Entry condition: user explicitly asks to generate logo images.

Agent action:

1. Generate logo image candidates using image generation.
2. Save project-bound images in the workspace.
3. Show the images.
4. Explain how to evaluate them.
5. Provide a selection menu.

Exit condition:

- User selects, rejects, combines, refines, or asks for recommendation.

Forbidden:

- Do not create SVG.
- Do not create final VI manual in the same response as first image generation.
- Do not assume the prettiest image is approved.
- Do not proceed without a user decision.
- Do not create final logo assets in the same response as first image generation.

Required next-decision menu:

```markdown
## Next Decision
Please choose one:
1. Pick candidate A/B/C/D for final logo image refinement.
2. Ask for a refinement round on one candidate.
3. Combine elements from multiple candidates.
4. Reject all and revise the design direction.
5. Ask me to recommend the strongest candidate and explain why.
```

## Stage 4: Selection and Refinement

Entry condition: generated logo images exist.

User intents:

- Select: document selection and move toward final logo image refinement.
- Refine: run another image generation round.
- Combine: create a new image prompt combining selected features, then generate again.
- Reject: return to Stage 2 and revise strategy.
- Ask recommendation: recommend, explain, then ask for confirmation before final asset generation.

Exit condition:

- User approves one generated direction for final logo image assets.

Forbidden:

- Do not treat a recommendation as approval.
- Do not invent a new logo concept unrelated to the generated/approved candidate.
- Do not create SVG.

## Stage 5: Final Logo Image Assets

Entry condition: one generated image direction is approved.

Agent action:

1. Identify the approved source image and candidate label.
2. Explain what will be preserved and simplified.
3. Generate or edit final raster logo assets.
4. Provide usage notes for image placement, clear space, minimum size, and background control.
5. Ask for final logo image approval.

Final image asset set:

- primary lockup image
- icon/social avatar image
- wordmark-style lockup image if relevant
- monochrome-style image when useful
- inverted/dark-background image when useful
- small-size image when relevant

Exit condition:

- User approves the final logo image assets.

Forbidden:

- Do not create SVG, vector reconstructions, auto-traced files, or code-drawn substitutes.
- Do not start full VI manual until final logo images are approved.

## Stage 6: VI System Expansion

Entry condition: final logo image assets are approved.

Agent action:

1. Propose manual contents based on industry.
2. Identify needed application visuals.
3. Ask whether to generate application images.
4. Stop for approval.
5. Generate imagery only after confirmation when needed.
6. Build the VI system text and assets around approved images.

Exit condition:

- User approves VI structure and application image plan.

Forbidden:

- Do not use generic applications.
- Do not skip brand foundation, imagery, layout, applications, and asset delivery.
- Do not introduce SVG requirements.
- Do not render the HTML manual in the same response that first proposes the VI structure.

## Stage 7: HTML Brand Manual

Entry condition: VI content, final logo images, and application assets are ready or explicitly approved as placeholders.

Agent action:

1. Create HTML/CSS manual.
2. Use approved image assets directly.
3. Use generated images or clearly labeled placeholders.
4. Verify responsive layout and asset paths.
5. Summarize deliverables.

Exit condition:

- Manual is created and verified.

Forbidden:

- Do not ship broken links.
- Do not hide missing images.
- Do not use decorative filler instead of real touchpoints.
- Do not inline SVG logos.

## Handling User Shortcuts

If user says "直接做":

- If no details: ask whether assumptions are allowed.
- If assumptions are allowed: list assumptions first, then ask for assumption confirmation.
- If user confirms assumptions: propose logo image routes and ask which to generate.

If user says "你来决定":

- Recommend assumptions.
- Ask for confirmation.

If user asks for "完整交付" immediately:

- Explain the gated flow briefly.
- Start with missing questions.

If user says "测试这个 skill":

- Do not compress the process.
- Respond exactly as the skill should behave for a real brand client.
- Stop at the first unmet gate.

## Failure Recovery

If the agent accidentally skips a gate:

1. Acknowledge the skipped gate.
2. Mark the artifact as exploratory or regression, not final.
3. Return to the correct stage.
4. Ask for the missing user decision.

If the agent creates an SVG logo, treat it as a regression artifact, do not use it as the final identity source, and return to the image-based stage.
