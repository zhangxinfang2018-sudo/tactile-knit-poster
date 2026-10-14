# Tactile Knit Poster Style System

Use this reference to shape the visual prompt. It describes the reusable grammar observed in the supplied examples; it is not a request to reproduce their exact brand, copy, or logo.

## Visual-input selection

When the user provides several attached images, select one image as the **primary composition anchor** and optionally one as the **secondary palette/material anchor**. Choose the primary anchor by structural similarity to the requested poster, not by color alone. Do not blend all examples into a generic average.

Use feature-based selection:

- choose the primary reference by matching the overall layout, central hero silhouette, title scale, and framing;
- choose the secondary reference by matching the needed color relationship, letter-wrapped border, stitch treatment, or contrast;
- if one reference already supplies both, use it alone;
- if the user labels references in natural language, follow those labels; otherwise infer the roles from the images.

Visual-input selection must be portable. Do not rely on attachment order, temporary filenames, or sample-specific numbers in reusable prompts or skill examples.

For every reference set, identify:

- full-bleed crop and safe margins;
- top-left and top-right information zones;
- central hero bounding box and its silhouette;
- bottom metadata/footer rhythm;
- title scale, line breaks, and position;
- ratio between readable typography and the surrounding textile object;
- role of each color, not just the color names;
- fabric stitch direction, yarn thickness, relief, and camera distance.

If attached images are available in the conversation, send them to the image tool as visual inputs. Do not rely on a text-only paraphrase when the desired result depends on a specific layout. Use them for visual grammar only; do not reproduce their wording, logo, or brand identity.

## Visual identity

The image should feel like a photographed textile artifact: a soft knitted surface with raised yarn lettering and hand-made patch construction. The material is the design system, not a surface filter applied after a normal poster is made.

### Material

- Full-bleed knitted or crocheted fabric background.
- Visible stitch direction, loops, yarn twist, fiber fuzz, and small irregularities.
- Raised satin-stitch, chain-stitch, cord, or appliqué treatment for major lettering.
- Slight relief and soft cast shadow where thread sits above the fabric.
- Matte, tactile, warm, and touchable; avoid hard plastic, metal, glass, or glossy CGI.
- Use a close-up editorial product-photography feel with soft diffuse light and mild depth of field. Keep the type readable even when the edges are soft.

### Typography

- Main Chinese display type is thick, rounded, friendly, and slightly handmade.
- Strokes may bend, wobble, or vary subtly, but Chinese characters must remain legible.
- Secondary Latin text and numbers are smaller and cleaner, often acting as metadata or a brand-like signature.
- Make the primary title physically integrated into the textile: knitted, embroidered, corded, or cut as a cloth patch.
- Keep the readable title block restrained. Start with the textile badge, border letters, and fabric field as the dominant shapes; let the title occupy roughly one-fifth to one-third of the poster height, not most of the canvas.
- Do not enlarge the Chinese glyphs until they touch the patch edge. Preserve visible textile around the title and allow the material to carry visual weight.
- As a default, keep the main title around 15–22% of the canvas height and make the subtitle clearly smaller. The central badge and thematic perimeter lettering should remain the dominant shapes.
- If the background feels too heavy, use a finer-gauge knit with thinner yarn and smaller, tighter loops; keep the main lettering and border visibly thicker so the hierarchy survives.
- Use a short amount of copy. If the user supplies long copy, create clear title/subtitle hierarchy rather than shrinking everything.

### Color

Use a controlled 2–4 color system:

1. textile background;
2. central subject or patch;
3. high-contrast accent for border, punctuation, or metadata;
4. optional neutral thread such as cream or white.

Both soft pastel palettes and bold complementary palettes are valid. Saturation should feel like dyed yarn, not neon light. If the user gives no palette, infer one from the subject and keep the contrast intentional.

## Layout grammar

Default canvas is 4:5 portrait. Use a generous safe area and a centered visual anchor. The reference's layout skeleton has priority over mood adjectives.

When the user requests more whitespace, scale down the complete central group rather than merely adding blank bands. Keep the hero, title, and letter border at least 10% farther from all four canvas edges than the previous draft, and do not let the border crop into the frame.

### Shared editorial frame

- Small metadata or index may sit in the upper-left when supplied or explicitly free-filled.
- A small signature/mark may sit in the upper-right when supplied or explicitly requested; it is not mandatory.
- The central artwork occupies roughly the middle half to two-thirds of the canvas.
- A small descriptor or date may sit below the central artwork when supplied or explicitly free-filled.
- A three-part footer may run along the bottom edge when the user provides footer copy or asks for free editorial filling.

When the user does not request these zones, omit them or use quiet stitch marks/non-readable texture. Do not force a header, logo, or footer into every output. When free filling is explicitly allowed, use short contextual microcopy tied to the poster subject; never reproduce a recognizable reference brand or random slogan.

### Mode A: soft patch / stacked title

Use for descriptive Chinese titles, educational poster copy, or a warm playful mood.

- Treat the central patch as the hero object, not as a flat background behind text.
- Stack two or three title lines inside or across an irregular cream/white knitted patch.
- Give the patch a visible fabric edge, relief, and soft shadow so it reads as a sewn object.
- Keep the readable title smaller than the full patch and leave a visible field of textile around it.
- Add a small colored label near the lower-right of the central patch only when the user provides one or the reference clearly requires a reserved zone.
- Surround the title with a few sparse stitched marks or curved thread symbols.
- Keep the patch organic rather than geometric and avoid a perfectly clean sticker outline.

### Mode B: border badge / framed subject

Use for short slogans, a single subject, or image-first restyling.

- Create a contrasting central knitted patch or field that occupies most of the central hero area.
- When this mode is selected from a letter-border reference, make the perimeter out of oversized tubular yarn letterforms or a looping wordmark that visibly wraps around the patch. Do not substitute a plain cord, thin outline, or generic rounded frame.
- Derive the border wordmark from the user's subject, title, season, or mood. For a spring-walk subject, use a short thematic phrase such as “SPRING WALK” or “BREEZY WALK”; do not use an unrelated studio name or a copied brand.
- Put the main Chinese title or preserved subject inside the frame; the frame should support the subject rather than become random decoration.
- Keep the frame hand-drawn and asymmetrical; it should feel sewn around the patch, not typeset as a perfect badge.
- Keep the Chinese title smaller than the border system and use one small internal subtitle only when supplied.

Choose one mode for a poster. Do not combine every decorative device from both modes.

## Color-role mapping

Translate a requested palette into jobs in the composition. For example, a spring palette close to the supplied light-blue reference family can use:

- pale blue for the full-bleed knitted background;
- deep or medium blue for the central knitted hero field;
- coral or pink for the sewn border, punctuation, and small accents;
- cream white for the primary title or a small appliqué patch.

Do not distribute all colors evenly. A palette match depends on the same hierarchy of roles and contrast, not merely including the same swatches.

## Match priorities

When comparing a draft against the references, inspect in this order:

1. layout skeleton and central hero mass;
2. color-role relationship;
3. title hierarchy and stitched letter construction;
4. textile scale, stitch direction, and relief;
5. lighting softness and fine fibers.

If the first two are wrong, adding more yarn detail will not make the poster match.

## Image-first invariants

When a source image is supplied, preserve:

- the main subject's identity and recognizable silhouette;
- the important pose or orientation;
- the essential internal color relationships when they carry meaning;
- any user-specified text, reproduced verbatim.

You may change:

- the background fabric and stitch direction;
- the framing, patch shape, and border;
- the palette when harmonization is needed;
- the decorative metadata and footer when the user supplies new copy;
- the overall crop, as long as the subject remains the anchor.

If the source is a complete poster, extract its main visual subject and rebuild the poster around that subject. Do not preserve the original layout by default.

## Negative prompt language

Use only the negative constraints that help the current request. Useful defaults are:

```text
flat vector art, ordinary printed typography, smooth plastic, chrome, glass, glossy 3D render, generic corporate poster, sterile digital layout, excessive props, random invented wording, fake logos, watermark, illegible Chinese text, cluttered background, harsh specular lighting
```

When the user has complained about a previous draft, add only the relevant targeted negatives:

```text
giant text dominating the canvas, title filling the badge, generic plain yarn outline, cord-only border, mandatory header/footer, fake brand lockup
```

Avoid overloading the prompt with every negative term when a shorter list is sufficient.
