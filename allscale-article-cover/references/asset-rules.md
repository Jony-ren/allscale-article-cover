# Asset Rules

## Provided References

- `assets/examples/target-cover.png` is the primary target. Match its design language, not every exact object.
- `assets/brand/allscale-logo.png` is the required source asset for the AllScale logo.
- `assets/brand/dot-bg.jpg` is the required source asset for the dotted white background.
- `assets/examples/object-pack.png` is the required reference for the two object icons in the final cover. It contains: headphone statue, person with gold, paper plane, green sparkle orb, cash stack, globe/bolt, bank temple.
- `assets/examples/photo-pack.png` shows usable photo moods and crops: mountains, dreamy garden, bank temple in white card, phone users, green hills, globe card, flower shop, aerial texture.

## Using User Assets

If the user supplies images:

- Use them as visual reference or source material when calling `image_gen`.
- Prefer one primary rounded photo card, not a collage of all supplied images.
- When using a source board, screenshot, or photo pack, crop inside the chosen photo content before placing it in the lower-right rounded card.
- Do not include green source-board backgrounds, green edges, green corner mats, separators, or margins inside the lower-right photo card.
- Use object cutouts sparingly: one upper-right and one lower-left is usually enough.
- Convert finance/classical objects to grayscale unless the user asks otherwise.

## Required Object Selection

For every final cover, choose exactly two different object icons from `assets/examples/object-pack.png`:

- Place one selected object in the upper-right slot.
- Place the other selected object in the lower-left slot.
- Choose the two objects that best fit the article's topic and emotional angle.
- The selected objects replace the corresponding upper-right and lower-left objects in `target-cover.png`.
- Do not invent unrelated object icons if `object-pack.png` contains a suitable pair.
- Do not redesign, redraw, stylize, recolor, or replace the selected `object-pack.png` icons.
- This rule applies only to the object-pack icons. Other elements, including headline, border, dotted canvas, logo accents, handwritten note, and photo card, should continue to follow the existing cover style rules.

Selection guidance:

- Stablecoin, banking, treasury, trust: bank temple, cash stack, globe/bolt.
- Payroll, automation, programmable payments, AI operations: headphone statue, paper plane, globe/bolt.
- Global payments, settlement, cross-border movement: paper plane, globe/bolt, bank temple.
- Liquidity, money movement, cost efficiency: cash stack, globe/bolt, bank temple.
- Premium editorial or abstract optimism: green sparkle orb, headphone statue, paper plane.

## If Assets Are Missing

Generate analogous elements only if `object-pack.png` is unavailable or the user explicitly asks for new icons:

- Finance/trust topics: bank temple, cash, ledger, vault, stablecoin globe.
- Global payment topics: mountain/landscape photo card, globe, paper plane.
- AI/automation topics: statue with headphones, paper plane, orb, abstract signal.
- Compliance/risk topics: bank temple, stamped paper, guarded doorway, grayscale monument.

## Required Brand Assets

- Use `assets/brand/allscale-logo.png` for the AllScale logo in every final cover.
- Do not redesign, redraw, stylize, recolor, replace, or recreate the logo.
- Only scale and position the logo in the upper-left logo slot.
- Use `assets/brand/dot-bg.jpg` for the dotted white background in every final cover.
- Do not redraw, regenerate, recolor, restyle, or replace the dotted background.
- Only crop, scale, tile, or position the dotted background as needed to fill the cover canvas.

## Composition Discipline

Do not build a source-material moodboard as the final cover. The final cover is one editorial composition with typography, logo, border, dotted background, and a few curated assets.
