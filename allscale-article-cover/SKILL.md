---
name: allscale-article-cover
description: "Generate AllScale-style article cover images from articles, blog drafts, titles, URLs, or marketing topics. Use when the user asks for an article cover, blog cover, hero image, social preview, thumbnail, or header image in the AllScale visual style: dotted white editorial canvas, large black serif headline, AllScale logo mark, green accent corners, grayscale finance/classical objects, rounded photo blocks, and clean collage composition."
---

# AllScale Article Cover

## Core Output

Create one polished article cover image that looks like an AllScale editorial/blog cover, not a generic AI illustration. The default target is a wide horizontal cover, preferably 16:9 or close to the supplied reference aspect. The main headline must be exactly two lines.

The cover should feel like a designed editorial layout: large typography first, curated object collage second, restrained brand accents, and lots of breathing room.

## Read References

Load only what is needed:

- `references/style-dna.md`: visual rules, layout, typography, color, and prohibitions.
- `references/asset-rules.md`: how to use supplied screenshots, object packs, photo packs, logos, and generated assets.
- `references/prompt-template.md`: default `image_gen` prompt structure.
- `references/qa-checklist.md`: post-generation checks and iteration rules.
- `assets/examples/target-cover.png`: primary target style reference.
- `assets/brand/allscale-logo.png`: required AllScale logo source asset.
- `assets/brand/dot-bg.jpg`: required dotted background source asset.
- `assets/examples/object-pack.png`: usable object/source-material reference.
- `assets/examples/photo-pack.png`: usable photo/source-material reference.

## Workflow

### 1. Understand the Article

Read the user's article, URL, title, draft, or topic first. Extract:

- the final cover headline
- the emotional angle of the article
- 2-4 visual metaphors or objects
- whether the topic is finance, stablecoin, payroll, treasury, compliance, global business, AI agents, or another category
- whether the user supplied required assets

Do not generate a cover from a title alone if the article text or URL is available.

### 2. Decide the Layout

Use the target-cover composition unless the user asks otherwise:

- AllScale logo in the upper-left area, using `assets/brand/allscale-logo.png` directly, placed close to the main headline like the target-cover reference.
- Huge black Playfair Display SemiBold headline on the left, strictly 2 lines, with line-height equal to the headline font size.
- Dotted white background across the whole canvas, using `assets/brand/dot-bg.jpg` directly.
- Thin black outer border with 40px rounded corners and 60% corner smoothing.
- One object from `assets/examples/object-pack.png` on the upper-right, chosen because it fits the article.
- One different object from `assets/examples/object-pack.png` on the lower-left, chosen because it fits the article.
- One rounded rectangular photo block on the lower-right.
- Optional handwritten subtitle near the lower-left, short, underlined, and set in Figma Hand.
- Small green corner marks near the logo or as restrained brand accents.

Keep the headline as the hero. Assets should support the idea, not compete with the words. Do not reuse the default target-cover upper-right and lower-left objects unless those exact objects are the best two choices from `object-pack.png` for the article.

Maintain clear breaking space between every major element, following `assets/examples/target-cover.png`: logo to headline, headline to upper-right object, headline to lower-left object, lower-left object to handwritten note, headline/object area to lower-right photo card, and all elements to the outer border. Elements must feel intentionally separated, never touching, colliding, or visually crowding each other.

Set the headline line-height to exactly 1.0, meaning the line-height equals the headline font size. Do not use loose leading between the two headline lines.

Scale the AllScale logo so its visible width is approximately the width of 2.5 headline letters at the chosen headline font size. The logo should feel deliberately smaller than the headline, like the reference, while remaining readable.

Position the lower-right photo card so its distance to the right outer border equals its distance to the bottom outer border. These two margins must visually match.

The lower-right photo card must not show any green edge, green corner, green matte, or source-pack background around the photo. Crop inside the selected photo/image content before applying the rounded photo mask; do not include the green background from a source board or screenshot.

Always use `assets/brand/allscale-logo.png` as the logo source asset. Do not redesign, redraw, stylize, recolor, replace, or recreate the AllScale logo. Only scale and position it in the upper-left logo slot.

Always use `assets/brand/dot-bg.jpg` as the dotted canvas source asset. Do not redraw, regenerate, recolor, restyle, or replace the background dots. Only crop, scale, tile, or position it as needed to fill the cover canvas.

When choosing the upper-right and lower-left object icons, selectively replace the corresponding target-cover icons with the two `object-pack.png` icons that best match the article. Do not redesign, redraw, stylize, recolor, or replace the selected `object-pack.png` icons. This restriction applies only to the object-pack icons; keep all other cover elements governed by the existing style, layout, typography, and QA rules.

### 3. Generate

When the user asks to generate, output, create, or make the cover, call `image_gen` directly. Do not stop for confirmation unless the title or article is missing and cannot be inferred.

If the user supplies usable assets, mention them explicitly in the prompt as reference material. If assets are not available, ask `image_gen` to create analogous collage elements.

Generate one cover at a time unless the user asks for variants.

### 4. Check and Iterate

After generation, check `references/qa-checklist.md`. Regenerate or edit if:

- the headline is small or not the main visual signal
- the background is not white dotted
- the output looks like a generic poster, ad, infographic, or SaaS hero
- the logo area is missing or messy
- the composition lacks the reference's editorial collage structure
- the title text is misspelled, garbled, or unreadable
- the layout is too crowded
- green overwhelms the white editorial canvas

### 5. Save

If working in a workspace, copy final covers to:

```text
assets/<article-slug>-cover/
```

Use filenames:

```text
01-cover.png
02-cover-variant.png
```

Keep original generated files. Do not overwrite existing assets unless the user explicitly asks.

## Delivery

After generation, report:

- how many covers were generated
- recommended usage, such as blog header, social preview, or hero image
- saved path
- whether the result is final or needs another typography/layout pass

Keep the explanation short. The cover should carry the work.
