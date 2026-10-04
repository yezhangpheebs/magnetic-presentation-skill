---
name: artifact-template-magnetic-presentation
description: "Create a presentation using the 磁场计划专属演示 Magnetic Presentation template and its retained reference file. Use when the user selects this template, names 磁场计划专属演示 Magnetic Presentation, or explicitly invokes $artifact-template-magnetic-presentation. 为客户决策层创建公司介绍、投标、概念提案和完整设计汇报；使用黑白灰骨架、项目主题色、观点型主标题、结论先行叙事，以及图纸、效果图与技术证据递进。"
---

# 磁场计划专属演示 Magnetic Presentation

Create a presentation from this template. Keep the reference file unchanged.

## Workflow

1. Read `artifact-template.json` and resolve its paths relative to this skill directory.
2. Load [@presentations](plugin://presentations@openai-primary-runtime) and invoke its reference/template workflow with the retained file.
3. Treat the user's prompt and available sources as the content input. Do not invent facts merely to fill a template slot.
4. Clone or import the reference instead of replacing its visual system with generic defaults.
5. Render and verify the finished presentation, then return the final artifact.

## Fidelity

Preserve source slides, layouts, masters, typography, geometry, images, charts, tables, and recurring slide chrome.

User instructions control requested content and explicit deviations. The retained reference controls layout and formatting where the user has not requested a change.

## How the reference is organized

The reference is a page-family library. A template page is followed by one or more pages showing how that family has been used in real projects.

- Slides 1–5: usage instructions. Read them, but exclude them from finished client decks.
- Slides 6–8: three cover templates.
- Slide 9: cover example reference.
- Slides 10–13: four distinct contents-page templates.
- Slide 14: contents-page example reference.
- Slides 15–26: section, concept, evidence, and technical template families.
- Slide 27: example reference for the preceding technical-relation family.
- Slides 28–29: light and dark option templates.
- Slide 30: example reference for the preceding option family.
- Slides 31–33: audience, process, and context templates.
- Slide 34: example reference for the preceding concept-system family.
- Slides 35–39: plan, drawing, axonometric, and spatial-option templates.
- Slide 40: example reference for the preceding spatial-option family.
- Slide 41: program and area schedule template.
- Slide 42: drawing-analysis example reference.
- Slides 43–48: schedule, technical, synthesis, and closing templates.

Use example references as visual grammar: they demonstrate image density, cropping, title hierarchy, spacing, and intended finish. Do not automatically duplicate example references into a client deliverable. Select the editable template that precedes the example, then adapt it to the user's project.

## Core communication rule

For every important body slide, make the main title the page's primary viewpoint, judgment, conclusion, or argument. Do not default to a topic label such as “平面图”, “效果图”, “项目背景”, or “方案对比”.

Use three levels when the content supports them:

1. A small navigation label identifies the section or page type, such as `设计方案 / 空间效果`.
2. The main title states the point the audience should accept.
3. The drawing, image, table, chart, or short explanation proves that point.

The complete sequence of main titles should be readable as a concise summary of the whole presentation. Use descriptive titles only for covers, contents, section dividers, pure drawing appendices, and other reference-only pages.

Keep each body slide focused on one major claim. Prefer a natural sentence a presenter would say aloud. Avoid slogans, vague nouns, and repeated title formulas.

## Default design-report structure

For a design presentation, default to:

`cover → concept proposition → design strategy → detailed design for each space → drawings and spatial evidence → optional synthesis → brand closing`

The contents page should normally contain only:

1. 概念主张
2. 设计策略
3. 空间详细设计

Do not add “项目理解”, “实施计划”, or “下一步建议” by default. Use them only when the user explicitly requests them or the project genuinely needs those decision topics.

Choose one of the four retained contents templates on slides 10–13. Use slide 14 only to understand how a contents page may be completed; do not insert it as project content.

The numbered divider and image divider on slides 15–16 are alternative treatments for “概念主张”. Select the one that suits the deck; do not automatically place both in a finished presentation.

For a numbered section divider, follow retained slide 15 exactly: the Arabic number is the dominant visual element and the Chinese chapter label is much smaller beneath it. Preserve this proportion, spacing, and centered geometry. Change the numeral and chapter label only.

## Presentation modes

Choose one of two modes before selecting slides.

### Complete design presentation

Use for concept proposals and full design presentations:

`cover → concept proposition → design strategy → spatial sequence → detailed design for each space → technical and drawing evidence → optional synthesis → brand closing`

### Short result-led report

Use when the design is already mature and the audience mainly needs to review the result. Target roughly 12–18 slides:

`theme cover → program/area schedule → plan series → full-bleed rendering series → optional synthesis → brand closing`

Do not add background analysis, implementation planning, or next-step pages merely to lengthen a design report.

## Page systems

### Cover family

Choose one cover template from slides 6–8 according to the available evidence:

- Use the minimal cover when the project name and proposition should lead.
- Use the title-and-image cover when one key image is available.
- Use the centered image cover for a formal design-proposal opening.

Use slide 9 only as a visual reference for possible completed-cover outcomes.

### Plan series

Use the retained first-plan and continuation-plan pages as a pair.

- The first page establishes the drawing section and states what the plan achieves.
- Continuation pages keep the drawing scale, title zone, floor label, footer, and page number fixed.
- Repeating the same structure across several floors is intentional.
- Replace the drawing placeholder with a plan, map, circulation drawing, axonometric drawing, or technical evidence.

#### Multi-floor scale and alignment — hard rule

When a project contains multiple vertically related floors, treat their plan drawings as one coordinated series rather than fitting each floor independently.

- Keep every floor plan at exactly the same drawing scale across slides. A first-floor plan must not appear smaller and a second-floor plan larger merely because their outlines or source-image bounds differ.
- Use one shared drawing frame, one scale factor, one rotation, one crop/padding rule, and one slide position for the entire floor sequence.
- Establish the common frame from the largest required floor extent, then apply it unchanged to every other floor. Allow intentional whitespace around a smaller floor instead of enlarging it to fill the page.
- Align floors by a real shared datum whenever available: structural grid, column line, core, stair, lift, façade line, building origin, or another stable architectural reference. Do not center each image independently by its own visible bounding box.
- Normalize source drawings onto equal-size transparent canvases before placing them when different exports have inconsistent margins.
- Keep the floor label, title zone, footer, page number, and drawing viewport fixed so that consecutive slides can be mentally overlaid.
- Before delivery, compare the consecutive floor-plan slides as an overlay or flick sequence and verify that shared cores, grids, and boundaries do not jump.

Only break the shared scale for an explicitly identified detail enlargement or when the drawings are genuinely unrelated. Label an enlargement clearly as “局部放大” or with its stated scale, and do not present it as another page in the same continuous floor-plan sequence.

### Full-bleed spatial evidence

Use the retained light or dark full-bleed result pages for renderings and strong photographic evidence.

- The image is the main evidence and should occupy the full canvas.
- Keep a small section label and a prominent viewpoint title.
- When a plan is available, use the bottom-right locator card to show viewpoint and direction.
- Keep locator scale and safe margins identical across a continuous sequence.
- A single space may use two or three consecutive views: overall view first, operational or secondary view next, detail last.
- Remove the locator when it does not help the audience understand spatial position.

### Program and area schedule

Use the retained native table for floor, function, area, quantity, scope, or other project indicators.

- The title must explain what the allocation means, not merely say “指标表”.
- Replace all bracketed sample values with verified project data.
- Do not invent values or retain unused rows.

## Visual system

- Preserve the black, white, and warm-gray base.
- Use cyan and gold as optional accents, not mandatory project colors.
- Derive the active project color from its visual identity or key imagery when appropriate.
- Keep the Magnetic Project mark restrained.
- Prefer one dominant visual composition over collections of cards.
- Do not absorb project-specific robots, technology-blue styling, client marks, or industry imagery from the retained examples.
