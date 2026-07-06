# Isekai Now Image Composition Guardrails

## Core Distinction

Separate three layers before prompting or composing:

1. **Identity layer**: face, hair color, hairstyle, eye color, expression vibe, and recognizable personality. Preserve this from reference images or fixed avatars.
2. **Library avatar layer**: the fixed small头像 may have a default isekai job, such as rose shield guardian or fire mage. This is only a reusable profile identity.
3. **Current scene layer**: the main illustration must follow the user's current location, story, caption, and social joke. Scene clothing and props can change from the avatar job.

Never force avatar-job props into the main image when they do not serve the current post.

## Prop And Costume Rules

- Include props only if they support the post's action, punchline, or visible story hook.
- Remove combat props from cozy scenes unless the joke is specifically about being overdressed or on guard.
- For tea, cafe, bakery, inn, palace, market, classroom, sleepover, or date-like posts, prioritize scene props: cups, plates, pastries, menus, flowers, bags, books, small familiars, or tableware.
- For ceremony, departure, battle, dungeon, rescue, or mission posts, allow weapons, shields, armor, banners, spell circles, and guild gear.
- If the caption creates a role for the moment, obey that role over the library job. Example: `公主的下午茶时间` means princess headpiece, elegant dress, tea table, and pastries. Do not add a shield unless the user asks for guardian/knight tension.
- Headwear should match the scene: tiara/circlet/ribbon for princess scenes; mage hat for magic scenes; hood/cape for travel; helmet only for knight or battle scenes.

## Character Prompt Pattern

Use this structure for main illustrations:

```text
[Character name] as an isekai version for this specific scene, preserving [identity anchors]. Current-scene role: [scene role from user/caption]. Outfit and props: [only props that support this scene]. Avoid: [library-job props that would be off-scene].
```

Example:

```text
Ayumu Uehara as an isekai rose-themed princess at afternoon tea, preserving rose-pink side-bun hair, yellow-green eyes, and gentle sincere smile. Outfit and props: elegant princess dress, small tiara or rose circlet, coffee cup, pastries, palace courtyard tea table. Avoid shield, battle armor, weapons, school uniform, modern phone.
```

## Main Image Aspect Ratio

- For local UI composition, generate the main illustration as a wide rectangle whenever possible: prefer `1536x1024`, `1448x1086`, or another 3:2 to 4:3 image.
- In the final Moments-style card, crop or fit the main image to a stable rectangle around **1.33:1 to 1.5:1**.
- Do not let a square or vertical main image dominate the card unless the user specifically asks for a square post.
- Keep the main image width aligned with the text column and leave comfortable white margins; the image should not feel wider than the social card's rhythm.
- If the generated image has important content near the edges, use contain-with-padding or a gentler center crop instead of cutting faces, cups, hands, or story clues.

## UI Composition Rules

- Fixed post width should read like a social feed card, not a poster frame.
- Main image should usually start below the caption with enough breathing room and be visually subordinate to the full post, not fill nearly the whole card height.
- Keep author avatar 72-88 px, comment avatars 42-50 px, and preserve circular crops.
- Prefer 3-6 comments unless the user asks for many; comments should fit without crowding the input field.
- Validate the final image visually for: no text overlap, no clipped UI, no wrong avatar, no irrelevant main-image prop, and main image aspect ratio matching the feed.
