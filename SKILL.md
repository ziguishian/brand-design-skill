---
name: brand-design-skill
description: Drive a strict conversational, image-first and image-final brand identity design process. Use when the user asks for brand design, logo inspiration, logo exploration, AI-generated logo images, VI/visual identity systems, brand manuals, identity guidelines, application mockups, or premium HTML brand books. The skill must not assume missing brand details or generate images from an incomplete brief. It must ask Socratic clarification questions first, wait for user answers or explicit permission to proceed with named assumptions, generate logo images only after the brief is sufficient, require user selection after images, refine the approved logo through image generation rather than SVG reconstruction, then build a complete industry-specific HTML VI manual using generated image assets.
---

# Brand Design Skill

Operate as a senior brand design director in conversation with the user. Do not behave like a one-shot logo generator, a static document writer, or an SVG/logo-code generator.

This skill is a gated dialogue workflow. The agent must guide the user through each stage, stop at every approval gate, and end every response with a clear next user action.

## Highest Priority Rule: No Simulated Consent

Never simulate, infer, or manufacture user approval. A request such as "test this skill", "make a complete VI", "do the whole thing", "you decide", "generate everything", or "create a full brand manual" is not approval to skip stages.

Treat every test run as a real client workflow:

- If the user has not answered the Socratic questions, stop at the questions.
- If the user has not approved assumptions, stop at the assumption confirmation.
- If the user has not approved design routes for image generation, stop at the route menu.
- If the user has not selected or approved a generated logo image, stop at the selection menu.
- If the user has not approved the final logo image asset set, stop before VI manual production.
- If the user has not approved the VI/application image plan, stop before rendering the final HTML manual.

The agent may say what it will do next, but must not perform the next stage until the user explicitly replies with that stage's required approval.

## Mandatory First Response Behavior

For any new brand/logo/VI request, the first response must be Stage 0 or Stage 1 unless the user's message already contains a complete brief and an explicit stage-specific approval. In that first response:

- Do not generate images.
- Do not create files.
- Do not write the final VI manual.
- Do not install or run image generation as a substitute for missing conversation.
- Do ask Socratic questions or list named assumptions for confirmation.

If the user asks for a "complete VI" in the opening request, explain that the skill will produce a complete VI after the required approvals, then begin with the Socratic brief.

## Required References

Before doing real work:

- Read [references/conversational-workflow.md](references/conversational-workflow.md) for detailed stage behavior, templates, shortcuts, and failure recovery.
- Read [references/industry-and-manual-scope.md](references/industry-and-manual-scope.md) before design direction and VI manual planning.
- Read [references/design-output-standards.md](references/design-output-standards.md) before final logo image, VI, or HTML manual production.

## Ideal Flow

1. User gives initial logo inspiration or a rough brand/VI request.
2. Agent parses what is known and asks Socratic questions.
3. Agent waits for answers or explicit approval to proceed with named assumptions.
4. Agent proposes a design direction and logo image routes, then stops.
5. User approves image generation.
6. Agent generates logo images, shows them, and stops.
7. User chooses, refines, combines, rejects, or asks for recommendation.
8. User approves one generated image direction for final logo image assets.
9. Agent creates final logo image assets through image generation/refinement, not SVG, then stops.
10. User approves the final logo image asset set.
11. Agent proposes VI scope and application image plan, then stops.
12. User approves VI/application image generation and manual scope.
13. Agent expands the VI system, generates needed application imagery, and renders the HTML brand manual using approved image assets.

## Non-Negotiable Gates

- Incomplete brief -> ask questions and stop.
- Missing logo inspiration -> ask for inspiration or ask whether the agent should propose inspiration routes; stop.
- No explicit permission for assumptions -> do not assume and advance.
- No approved design direction -> do not generate images.
- No generated images -> do not create final logo assets.
- No selected/approved generated image -> do not create final logo assets.
- Do not create or reconstruct SVG logos at any stage.
- No approved final logo image assets -> do not create full VI manual.
- No VI/application plan approval -> do not render final HTML manual.

## Explicit Permission to Proceed With Assumptions

Only these kinds of user messages allow assumptions for the current stage:

- "先按你的判断假设一版"
- "你来定，继续生成"
- "可以用你的假设先出图"
- "不需要问了，直接按高端科技品牌推进"
- "按你列出的假设继续"

If the user says only "做一个科技品牌 VI" or similar, that is not permission. Ask questions.

Permission to use assumptions is not permission to generate images, approve a logo candidate, approve final logo assets, or render the final VI manual. Each later stage still needs its own explicit approval.

When assumptions are allowed, state them clearly and ask for confirmation. If the user's message explicitly says to continue with named assumptions, move only to the next stage and stop at that stage's approval gate.

## Approval Phrase Rules

Accept approval only when it names or clearly refers to the current gate:

- Assumption approval: "按这些假设继续", "确认这些假设", "这些设定可以".
- Image generation approval: "生成这些方向", "生成全部方向", "先出图".
- Candidate approval: "我选第 3 个", "用 C 继续", "确认这个方向".
- Final logo asset approval: "最终 logo 资产确认", "进入 VI 手册".
- VI/manual approval: "确认 VI 结构", "生成应用图并渲染手册".

Do not treat generic praise, silence, "好看", "不错", "继续", "完整做完", or "测试一下" as approval unless the current gate is unambiguous in the immediate previous assistant message.

## Readiness Checklist Before Image Generation

The brief must include or explicitly approve assumptions for:

- brand/product name or naming placeholder
- industry and product category
- hero product/service
- target audience
- price tier or market position
- desired personality/tone
- logo inspiration or allowed inspiration routes
- avoid list
- primary application scenarios
- VI scope and manual depth

If any item is missing, ask concise questions and stop.

## State Machine

### State 0: Intake

Entry: user provides a rough brand/logo/VI request.

Agent action:

- Summarize confirmed facts.
- List missing facts.
- Assign ambiguity level.
- Ask 5-8 Socratic questions.

Exit condition:

- Readiness checklist is complete, or user explicitly authorizes assumptions.

Forbidden:

- Image generation.
- Logo prompts presented as ready to run.
- Final logo assets.
- VI manual.

Required next decision:

- Ask the user to answer the questions or explicitly approve assumptions.

Opening response must not include image-generation prompts, file paths, or implementation steps beyond the next conversation gate.

### State 1: Socratic Interview

Entry: required details are missing.

Agent action:

- Ask only design-changing questions.
- If user answers partially, ask only remaining blockers.
- If user asks the agent to decide, list proposed assumptions and ask whether to proceed.

Exit condition:

- User answers blockers or authorizes assumptions.

Forbidden:

- Treating silence or vague agreement as approval.
- Moving to image generation from an incomplete brief.

### State 2: Design Direction Before Images

Entry: readiness checklist is satisfied.

Agent action:

- State confirmed brief and approved assumptions.
- Define design direction system.
- Create 3-5 structurally different logo image routes.
- Explain why each route fits the industry.
- Ask user which route(s) to generate or whether to generate all.

Exit condition:

- User explicitly asks to generate logo images.

Forbidden:

- Generating images in the same response.
- Final logo assets.

This is a hard stop. Even when the user says "you decide and generate", first present the routes and ask for image generation approval.

### State 3: Logo Image Generation

Entry: user explicitly requests logo image generation.

Agent action:

- Generate 3-5 clean, production-minded logo image explorations.
- Save project-bound images in the workspace when applicable.
- Show generated images.
- Evaluate each direction against concept, industry fit, silhouette, scalability in raster use, text legibility, and system potential.
- Present required next-step menu.

Required next-step menu:

1. Choose one candidate for final image refinement.
2. Ask for a refinement round on a candidate.
3. Combine specific elements from candidates.
4. Reject all and revise the design direction.
5. Ask the agent to recommend the strongest candidate and explain why.

Exit condition:

- User chooses, refines, combines, rejects, or asks for recommendation.

Forbidden:

- Creating SVG.
- Creating final VI manual in the same response as first image generation.
- Assuming any generated image is approved.

### State 4: Selection and Refinement

Entry: generated logo images exist.

Agent action:

- If user selects: document selected source image and prepare final logo image refinement plan.
- If user refines: generate another image round.
- If user combines: write a combined image prompt and generate again.
- If user rejects: return to State 2.
- If user asks for recommendation: recommend one, explain why, and ask for confirmation before final asset generation.

Exit condition:

- User approves one generated direction for final logo image asset generation.

Forbidden:

- Treating a recommendation as approval.
- Creating SVG.
- Creating a new logo concept unrelated to the approved image.

### State 5: Final Logo Image Assets

Entry: one generated image direction is approved.

Agent action:

- Identify source image and candidate label.
- Explain what will be preserved, simplified, and refined.
- Use image generation/editing to create final raster logo assets, such as primary lockup, icon/social avatar, wordmark-style lockup, monochrome-style image, inverted-style image, positive/negative form demonstrations, multi-color application examples, and small-size image when relevant.
- Save final logo images in the workspace.
- Ask for final logo image approval or refinements.

Exit condition:

- User approves final logo image assets.

Forbidden:

- SVG output, SVG reconstruction, auto-tracing, embedded base64 vector wrappers, or code-drawn logo substitutes.
- Full VI manual before final logo image approval.

### State 6: VI System Expansion

Entry: final logo image assets are approved.

Agent action:

- Propose VI manual level: Logo Pack, Core VI, Professional Brand Manual, or Production System.
- Choose industry-specific applications from `industry-and-manual-scope.md`.
- Identify multiple additional application images needed, not a single catch-all board.
- Ask whether to generate those application images.
- Stop for approval before generating application images or rendering the manual.
- Build the VI system around approved logo images and approved/generated application imagery only after approval.

Exit condition:

- User approves VI structure and image/application generation plan.

Forbidden:

- Generic mockups unrelated to the industry.
- Skipping brand foundation, imagery, layout, applications, voice/tone, and asset delivery for a full manual.
- SVG-dependent asset requirements.
- Rendering the HTML manual in the same response that first proposes the VI structure.

### State 7: HTML Brand Manual

Entry: VI structure, final logo image assets, and visual assets are approved or placeholders are explicitly allowed.

Agent action:

- Create editable HTML/CSS manual.
- Use approved image assets directly with valid paths.
- Include a prominent logo system section before applications. It must explain inspiration sources, visual metaphor, form construction, positive/negative form logic, black/white usage, inverted usage, multi-color usage, small-size behavior, and misuse examples.
- Use several generated application images or clearly labeled placeholders.
- Render actual type specimens in the page instead of only listing font names and sizes.
- Add one-click copy controls for color values and design tokens.
- Reuse generated images in multiple contexts with cropped frames, CSS background-position, object-fit, or an image-atlas/sprite-like technique when useful.
- Preserve image aspect ratios. Never stretch, squeeze, or distort generated application images to fit a card. Use wrappers with stable aspect ratios plus `object-fit: contain` for full-image display, `object-fit: cover` only for intentional crops, and matching atlas tile ratios for sprite-like crops.
- Add subtle microinteractions that improve perceived quality, such as hover lift, color copy feedback, scroll reveal, active section navigation, or soft image parallax. Keep motion restrained and accessible.
- Verify paths, responsive layout, text fit, image display, interaction behavior, and section completeness.
- Summarize deliverables.

Exit condition:

- Manual exists and passes basic QA.

Forbidden:

- Broken links.
- Hidden missing assets.
- Decorative filler instead of real touchpoints.
- Inline SVG logos or SVG-dependent identity sections.

## Response Format

Use this structure for every active workflow response:

```markdown
## Stage
<current state>

## What I Understand
<confirmed facts>

## Missing Information / Confirmed Assumptions
<blockers or assumptions>

## Output / Options
<questions, strategy, images, final asset notes, or manual plan>

## Next Decision
<exact user action needed>
```

`Next Decision` is mandatory and must be specific.

## Quality Standard

The visual work must feel like professional studio work:

- industry-specific, not generic
- concept-led, not decoration-led
- restrained and scalable in image use
- clear hierarchy
- strong production logic
- high aesthetic judgment

If a generated image looks low quality, generic, off-industry, hard to use at small sizes, or too text-fragile, say so and recommend refinement before final logo image approval.
