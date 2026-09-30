# Continuity and UI lock

## Continuity ledger

Record the following before motion generation and update it after every approved shot:

- character ID, body proportions, face, hair, costume layers, materials, dirt, injuries, and handedness;
- equipped weapon, carried items, ammo, ability state, and damage state;
- enemy type, count, position, damage, and awareness;
- location, time, weather, key light direction, palette, and persistent destruction;
- camera height, lens character, screen direction, player position, and next-shot exit;
- HUD state, objective text, health, stamina, ammo, minimap, abilities, cooldowns, and selection focus.

The end state of one shot is the start state of the next unless the edit explicitly communicates a time or location jump.

## UI master

Create UI once as a master overlay. Define:

- a reference canvas and safe-area margins;
- pixel coordinates or normalized anchors for every element;
- width, height, spacing, corner radius, stroke, and icon bounds;
- typeface, size, weight, line height, alignment, and language fallback;
- color tokens, opacity, blend behavior, and accessibility contrast;
- explicit variants for idle, selected, disabled, cooldown, damage, warning, and results states.

Prefer vector or lossless sources outside the Lumina skill package. Reference them by stable asset ID or URL in the manifest.

## Compositing order

Use this default stack from back to front:

1. generated or captured gameplay plate;
2. world-space markers that need occlusion;
3. screen-space HUD master;
4. subtitles and accessibility text;
5. edit-only title cards, ratings, and legal copy.

Do not bake persistent HUD into a generative plate when post-compositing is available.

## Validation

Compare representative frames against the UI master at shot start, midpoint, and end. Reject or repair when:

- an anchor moves unexpectedly;
- a control changes shape or scale;
- text becomes illegible or changes wording;
- health, ammo, cooldown, or objective state contradicts the action;
- a HUD element crosses the safe area or hides the focal action.
