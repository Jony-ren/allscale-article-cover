# Prompt Template

Use this structure for one generated cover:

```text
Generate one polished wide horizontal AllScale-style article cover image.

Canvas:
White editorial canvas using assets/brand/dot-bg.jpg as the exact dotted background source asset, thin black outer border near the edge with 40px rounded corners and 60% corner smoothing, clean high-end blog cover layout, lots of whitespace. The border corners should be soft continuous corners, not stiff mechanical quarter-circles. Do not redraw, regenerate, recolor, restyle, or replace the dotted background; only crop, scale, tile, or position it to fill the canvas.

Brand:
Place assets/brand/allscale-logo.png in the upper-left as the exact logo source asset, close to the main headline like the target-cover reference. Scale the logo so its visible width is approximately the width of 2.5 headline letters at the chosen headline font size. Keep branding restrained and crisp. Do not redesign, redraw, stylize, recolor, replace, or recreate the logo; only scale and position it.

Typography:
Main headline text: "{HEADLINE}"
Make the headline huge, black, and set in Playfair Display SemiBold. Left-dominant layout, exactly 2 lines, readable and correctly spelled. Set headline line-height to exactly 1.0, so the line-height equals the headline font size. The headline is the primary visual. Do not create a third headline line and do not use loose leading.

Collage:
Use exactly two different object icons selected from assets/examples/object-pack.png because they best fit the article.
Place selected object 1 in the upper-right: {UPPER_RIGHT_OBJECT}.
Place selected object 2 in the lower-left: {LOWER_LEFT_OBJECT}.
These two objects selectively replace the upper-right and lower-left icons from the target-cover reference. Do not redesign, redraw, stylize, recolor, or replace the selected object-pack icons. Keep them premium, coherent with the editorial collage, and visually balanced with the headline.
Use one rounded rectangle photo card in the lower-right showing {PHOTO_CARD_SCENE}, with muted natural green tones. Position the photo card so its right margin to the outer border equals its bottom margin to the outer border. Crop inside the selected photo content before applying the rounded mask; the photo card must not show any green source-board edge, green corner, green matte, separator, or margin.
Optional handwritten note near lower-left: "{HANDWRITTEN_NOTE}", set in Figma Hand, black marker style with underline.

Style:
Editorial collage, premium fintech blog cover, minimal, crisp, spacious, black and white with small green accents. The visual should resemble a designed article header, not a generic poster. Preserve the target-cover reference's clear breaking space between every major element: logo/headline, headline/upper-right object, headline/lower-left object, lower-left object/handwritten note, photo card/surrounding content, and all elements/outer border.

Constraints:
No dark background. No gradient SaaS hero. No cartoon. No infographic. No dashboard UI. No crowded moodboard. Do not use many cards. Do not make the text small. Do not misspell or distort the headline. Do not use 1-line or 3-line headline layouts; the headline must be exactly 2 lines. Use Playfair Display SemiBold for the headline and Figma Hand for the handwritten note. Headline line-height must equal headline font size. Logo visible width must be approximately 2.5 headline letters. The lower-right photo card's right margin must equal its bottom margin. The outer border must be thin, black, and rounded with a 40px corner radius plus 60% corner smoothing, not sharp rectangular corners and not stiff mechanical circular corners. Preserve clean margins, white space, and breaking space between all major elements. The lower-right photo card must not show green source-board edges or green corner mats. Do not redesign, redraw, stylize, recolor, or replace the selected object-pack icons. Do not redesign, redraw, stylize, recolor, replace, or recreate the AllScale logo. Do not redraw, regenerate, recolor, restyle, or replace the dotted background.
```

## Title Handling

- Use the user's article title if it is already strong.
- Shorten titles that are too long for a cover.
- Prefer 4-8 large words when possible.
- The final cover headline must be exactly two lines. Rewrite or shorten until it naturally breaks into two balanced lines.
- If the article is technical, make the cover headline more editorial and direct.

## Example Headline Transformations

- "Comprehensive financial infrastructure for Web3 teams..." -> "Web3 Teams / Need Payment Rails"
- "Stablecoin payroll and treasury management..." -> "Stablecoin Payroll / Matters"
- "Automated invoicing for global vendors..." -> "Invoices Should / Move Faster"
