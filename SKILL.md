---
name: tactile-knit-poster
description: "Generate one 4:5 knit-yarn poster from user copy, or transform a supplied image while preserving its main subject. Use for single raster poster outputs, not HTML, vector, or batches."
---

# Tactile Knit Poster

Create a single portrait poster with a tactile knitted-yarn, embroidered, or fabric-patch look. The output is a finished raster image. This skill has two input modes that share one visual system:

- **Copy-first:** turn supplied copy into one complete poster.
- **Image-first:** preserve the supplied image's main subject, then rebuild the background, material treatment, and poster composition around it.

Read [references/style-system.md](references/style-system.md) when composing the prompt or choosing a layout mode.

## Non-negotiable output contract

- Produce one poster per request, normally in a 4:5 portrait ratio.
- Use the built-in image-generation/editing path for the raster result.
- Treat attached example images as visual inputs for composition, palette roles, typography treatment, and material; do not reduce them to a mood word such as “soft” or “handmade”.
- Pass available visual inputs to the image tool. Do not make the user describe or label them when the tool can inspect them directly.
- Keep the central textile object and surrounding material larger than the readable copy. The poster is a textile badge with typography, not a giant-text poster.
- When a letter border is used, derive its decorative wordmark or letterforms from the user's theme or title; never use an unrelated generic brand-like word.
- If the user requests more whitespace, shrink the complete hero group and keep every element at least 10% farther from each canvas edge than the previous draft.
- Never hard-code sample brand names, logos, dates, or captions from the references.
- In image-first mode, preserve the edit target's existing visible information architecture by default: headers, labels, logos, signatures, captions, footer bars, and text blocks remain part of the poster unless the user explicitly asks to remove or replace them. This rule applies to the edit target, not to style-only reference images.
- Do not turn the task into an HTML/SVG layout, a carousel, or a batch of variants unless the user explicitly changes the scope.
- If the user supplies exact copy, quote it verbatim in the image prompt and preserve its hierarchy. Do not invent important wording.

## Separate visual-input roles before prompting

Do not classify every attached image as an edit target. Assign each image one role:

- **Style input:** an example to learn from. Preserve its visual grammar, not its subject, copy, or branding.
- **Edit target:** the image whose main subject must be preserved and restyled.
- **Supporting insert:** an additional object or texture to incorporate only when the user asks for it.

If the user attaches examples before giving copy, treat them as style inputs and keep the request **copy-first**. Use **image-first** only when the user asks to transform a supplied image or explicitly says to preserve its subject.

## Visual-input analysis

When style inputs are present, choose one primary composition anchor and, at most, one secondary palette/material anchor. Do not average a large set of variants into a vague middle style.

Select visual inputs by visual role, not by attachment order or sample-specific numbering:

- primary anchor: the reference whose overall layout, central hero shape, title scale, and framing are closest to the requested output;
- secondary anchor: the reference whose color relationship, letter border, or textile treatment is most useful to borrow.

If the user has not labeled the images, make this selection yourself. Do not ask the user to identify a primary or secondary image unless the visual inputs are genuinely ambiguous.

Before composing the image prompt, extract and lock:

1. canvas ratio and crop;
2. outer editorial frame, including header and footer zones;
3. central hero bounding box and its visual mass;
4. title placement and hierarchy;
5. text-to-artwork ratio;
6. color roles: background, hero, accent, text, and neutral;
7. stitch direction, relief, camera distance, and lighting.

The prompt must state the composition lock before the mood adjectives. A result with knitted texture but the wrong hero structure, color roles, and information frame is not a successful style match.

## Reference treatment

Determine how much freedom the visual input allows before composing the prompt:

- **Opaque full-poster reference with a background and finished layout:** use a strict reference lock by default. Preserve the canvas ratio, crop, background color, hero bounding box, title scale, information zones, and border logic. Convert the material into knit, yarn, embroidery, or fabric patch, but do not freely add unrelated objects or delete layout elements.
- **Full-poster reference used as a style input:** preserve its structural skeleton and color roles, but replace its wording, logo, dates, and brand identity with the user's content. Do not copy the reference's exact text or branding.
- **Full-poster image used as an edit target:** preserve its visible information architecture and source content by default, including labels, logos, signatures, captions, and footer bars. Repositioning is allowed only within the requested restyle, not silent deletion.
- **Transparent PNG or isolated subject:** use flexible composition. Preserve the subject's silhouette, pose, count, and important colors, then design a new knit background, patch, border, and information layout around it. Add no more than a few relevant micro-elements when they help the theme.
- An explicit user request such as “重新排版”, “重做背景和边框”, or “自由发挥版式” overrides the strict reference lock.

## Route the request

1. If the user supplies copy but no image, use **copy-first**.
2. If the user supplies style inputs plus copy, use **copy-first with visual-input analysis**.
3. If the user supplies an edit target, use **image-first**, whether it is an isolated sticker/illustration or a complete poster.
4. If both style inputs and an edit target are supplied, use the style inputs for composition/material and the edit target for the preserved subject.
5. If an image contains text that must remain exact, ask the user for the text when it is not legible or use the user's supplied transcription; do not guess.

When details are missing, infer a restrained palette and a suitable layout. Ask only when the missing information blocks a useful result.

## Optional editorial information

Top-left metadata, top-right signature marks, and bottom three-part footers are optional content zones, not mandatory decorations.

- If the user supplies the copy, include it accurately.
- If the user does not supply it and does not ask for it, omit the zone or use quiet stitch marks/non-readable texture. Do not force fake headers, logos, or footers into every poster.
- If the user explicitly allows free invention, add only short contextual microcopy related to the subject, such as a season, collection label, or poster category. Keep it secondary and never copy a reference brand.

For **image-first** edits, the rule is different: existing editorial zones in the edit target are preserved by default, even when the user does not transcribe them separately. Keep their presence, relative role, and approximate placement while restyling them as textile elements. Remove, replace, or freely rewrite them only when the user explicitly requests that change. If exact wording matters, ask for or use a user-provided transcription because generated lettering may not be exact.

## Copy-first mode

Parse the input into a small hierarchy before prompting:

- primary Chinese title;
- optional subtitle or explanation;
- optional number/date/label;
- optional brand or signature;
- optional three-part footer.

Choose one central composition from the attached visual inputs and recreate its structural logic: a central patch, badge, or framed hero is required when the visual inputs establish one. Do not make the result merely “text on knitted fabric”. Keep the copy sparse enough for a poster and make the main title the largest knitted element. If no brand or footer is provided, retain the visual system's information zones as quiet space, stitch marks, or restrained non-readable detail rather than fabricating a brand system.

When no visual input is supplied, choose the composition from the user's content rather than applying one fixed template:

- short slogan or compact mood phrase: consider a border badge; use a thematic letter border only when the phrase is short and the border improves the composition;
- concrete person, animal, object, or action: make the subject the central fabric patch and add at most 1–3 small related stitched motifs when they reinforce the theme;
- educational, list, numbered, or typeface-sharing content: use a soft patch or stacked-title layout and do not add a letter border by default;
- seasonal, lifestyle, or abstract themes: use a central patch plus a restrained number of relevant motifs; add a letter border only if it supports the title.

If the user specifies a layout, border, palette, or object, follow that instruction over this inference. Do not add decorative objects merely to fill empty space.

For copy-first color selection, user-provided colors take priority. Otherwise infer a controlled 2–4 color role map: textile background, central subject or patch, accent/border, and optional cream/white neutral. Use the inferred colors as a hierarchy, not as evenly distributed swatches.

Keep the title block restrained: the readable title and subtitle together should normally occupy roughly one-fifth to one-third of the poster height and should not fill the central badge edge-to-edge. Let the patch, fabric fibers, and surrounding letter border carry part of the visual weight.

For the default restrained treatment, keep the main title itself around 15–22% of the canvas height and the subtitle clearly smaller. If the user asks for a smaller title, reduce it by one visual step while preserving legibility and a visible textile field around the glyphs.

When a decorative letter border is present, extract a short thematic wordmark from the subject or title. For example, a spring-walk theme can use a restrained phrase such as “SPRING WALK” or “BREEZY WALK” around the perimeter. Keep it secondary, visually integrated, and relevant; do not introduce a random studio name or unrelated slogan.

## Image-first mode

This is a material restyle with a conditional amount of recomposition, not a filter. Preserve the subject's identity, silhouette, pose, and key recognizable details. Use the reference-treatment rules above to decide whether the layout is locked or flexible.

Default behavior:

- convert the subject into raised yarn, embroidery, or a fabric patch;
- preserve useful source color relationships; for an opaque full-poster reference, keep the reference's background color and color-role hierarchy rather than inventing a new palette;
- for a transparent PNG, choose a central patch or border-badge composition and add only a few relevant micro-elements when useful;
- keep the source's subject as the visual anchor;
- preserve the source poster's visible text blocks, metadata, logos, signatures, and footer structure by default; convert them into the same textile treatment. Treat the wording as approximate unless the user supplies exact copy separately.

Do not add unrelated characters, props, slogans, or sample logos merely to make the image busier.

## Prompt assembly

Build a concise structured image prompt with these fields when useful:

```text
Use case: ads-marketing for copy-first, or style-transfer for image-first
Asset type: one 4:5 portrait poster
Primary request: <the user's request>
Visual inputs: <primary composition anchor; optional secondary palette/material anchor>
Input image: <edit-target role and invariants, for image-first>
Subject: <main title or preserved subject>
Composition lock: <canvas, editorial frame, hero bounding box, chosen mode, title placement>
Reference treatment: <strict full-poster lock, or flexible transparent-subject composition; explicit user override if present>
Source information: <for image-first, preserve existing labels, logo/signature areas, captions, and footer unless explicitly removed>
Style/medium: tactile knitted textile, raised yarn, embroidery, fabric patch
Lighting/mood: soft diffused macro light, gentle textile shadows
Color-role map: background=<...>; hero=<...>; accent=<...>; text/neutral=<...>
Text (verbatim): "<exact copy>"
Text scale: restrained; hero object and textile remain visually dominant
Border logic: <oversized thematic yarn letters wrapping the perimeter, derived from the subject/title when a letter border is used>
Whitespace: <default safe area, or at least 10% more inset on every side when requested>
Background knit: <fine-gauge/thinner yarn background; foreground lettering may remain thicker>
Editorial extras: <omit unless supplied; or short contextual microcopy if free-fill is explicitly allowed>
Constraints: one finished poster; use attached images for visual grammar only; preserve subject in image-first mode
Avoid: flat vector, giant oversized typography, printed-looking text, plain cord border, plastic, chrome, random extra copy, fake logos
```

When attached images are present, keep the user-facing invocation simple. Do not ask the user to explain which image controls composition or color; infer those roles internally. A portable invocation can be only:

```text
$tactile-knit-poster

生成一张 4:5 竖版海报。
主标题：<标题>
副标题：<副标题>
```

Attached images are analyzed automatically. Never expose attachment numbers from one particular example set in the reusable template.

For image-first edits, repeat the invariants in plain language: preserve the main subject; use strict layout/color treatment for an opaque full-poster reference and flexible composition for a transparent PNG; do not remove source information unless asked. For attached style inputs, explicitly say internally: use the images for composition and material; do not copy their text, logo, or brand identity.

## Quality gate

Before returning the result, check:

- the background reads as real knitted fabric at close range;
- the headline looks made from thread or stitched fabric, not a flat digital font;
- the title remains readable and has clear hierarchy;
- the main title is subordinate to the central textile badge and does not overpower the thematic letter border;
- the readable text does not dominate the poster or fill the badge edge-to-edge;
- if a border badge is selected, the border is visibly made from oversized yarn letterforms wrapping around the perimeter, not a generic cord or outline;
- if a letter border is present, its wordmark or letterforms are thematically connected to the user request;
- requested whitespace is visible on all four sides and the hero group is not pressed against the canvas edges;
- the background knit is finer than the foreground lettering when the user asks for a thinner background yarn;
- the composition matches the reference's structural skeleton: header/footer zones, central hero mass, and chosen patch or border logic;
- the color roles match the reference relationship, not merely the individual color names;
- an opaque full-poster reference keeps its background color, major layout, hero mass, and information zones unless the user explicitly requests recomposition;
- a transparent PNG keeps its isolated subject recognizable and adds no more than a few relevant decorative elements;
- in copy-first mode, optional header/footer elements appear only when supplied or explicitly free-filled;
- in image-first mode, existing source header/footer/label/logo zones are not silently deleted;
- the image-first subject is still recognizable;
- the composition has generous margins and a calm editorial balance;
- there is no accidental extra text, watermark, or copied sample branding;
- the result is one portrait poster, not a collage or a set of variants.

If the image only has a knitted texture but lacks the reference's central hero, editorial frame, and color-role relationship, treat it as a failed match and revise the composition before adding more material detail.
