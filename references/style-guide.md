# Isekai Now Style Guide

## Core Concept

Create a "social app post from inside another world": the UI is contemporary, while the content is fantasy slice-of-life. The humor comes from treating magical events as normal daily updates.

## Visual Layout

- Portrait screenshot, clean white or very light gray background.
- Rounded white feed card with subtle shadow or thin border.
- Top row: round anime avatar, blue display name, gray location with a pin icon, small three-dot menu.
- Body: short Chinese text with line breaks, casual tone, 0-3 emojis.
- Main image: large rectangular anime illustration, usually 4:3 or wide rectangle, centered under the text.
- Social area: pink/red heart icon, blue-gray likes line, then comments with tiny round avatars.
- Bottom: pale comment input field with placeholder like `评论...`.
- Some variants can omit the separate body text and let the image carry the moment, with the caption-like comments below.

## Character References

- Default bundled avatar folder: `assets/Avatars`.
- Default bundled symbol folder: `assets/Symbols`.
- On Cheng's local machine, the original character reference folder is `C:\Users\cheng\Desktop\异世界CG\asserts`.
- Use the reference images to preserve each character's face shape, hairstyle, hair color, eye color, expression range, and recognizable vibe.
- Do not copy the modern school-uniform look into the final post unless explicitly requested. Translate the character into an isekai outfit: cloak, traveler tunic, mage robe, ranger cape, guild brooch, potion satchel, armor accents, fantasy hair ornament, or camp/adventurer accessories.
- The poster avatar and all comment avatars should also be isekai-style portraits. They may be small circular crops, but they should still show fantasy clothing or accessories rather than plain modern uniforms.
- When writing prompts, phrase this as: `based on the provided character reference for identity only, redesigned as an isekai adventurer portrait`.

## Image Style

- Detailed anime / light novel illustration.
- Warm cinematic lighting, expressive faces, cozy fantasy props.
- Prefer scenes like camping, guild dinner, market snacks, inn room, potion mishap, magic academy courtyard, lake travel, festival stall, caravan rest.
- Also support grand public scenes such as knight order departure, castle gate speeches, royal banners, guards, and dramatic sunlight when the post is about a mission, ceremony, or adventure sendoff.
- Include enough fantasy details: cloaks, lanterns, banners, runes, potions, familiar creatures, guild badges, medieval tents, enchanted cookware.
- Keep the scene readable as a candid social photo, not a poster or wallpaper.
- In-image text can be part of the joke: bakery chalkboards, motivational posters, speech bubbles, shop signs, royal banners, or cute warning labels. Keep it short and legible.

## Writing Voice

- Use first-person daily-life phrasing.
- Keep the poster optimistic, excited, annoyed, sleepy, proud, or suspicious.
- The main text should sound like someone posting in the moment:
  - `今天第一次露营！`
  - `锅已经炖了一个小时了，大家都很期待🥺❤️`
  - `终于排到王都南门的限定烤肉串了！`
- Avoid encyclopedic fantasy lore and long explanations.

## Names and Location

Names can be Chinese, Japanese-idol-like, or light-novel style:

- 南小鸟
- 津岛善子
- 矢泽妮可
- 渡边曜
- 莉莉娅
- 艾露
- 米娅
- 诺亚

Locations should combine modern check-in format with fantasy place names:

- `异世界·翡翠湖露营地`
- `王都·银钟广场`
- `星屑森林·第七码头`
- `白塔学院·炼金教室`
- `月见丘·临时营地`

## Comment Hooks

Give comments a mini-drama:

- One practical or hungry comment.
- One ominous/suspicious comment.
- One teasing comment from a close friend.
- One comment that notices something in the image.
- For big ceremonial scenes, use a supportive comment pile: prayers, cheering, tactical support, teasing idol catchphrases, and one food-related promise for when the party returns.
- For comedy scenes, let the poster get caught in the act, then have friends tease them with affectionate nicknames and small visual evidence from the image.

Examples:

- `我怎么有种不祥的预感……`
- `快开锅！我饿死了！`
- `我刚刚好像看到有什么东西跳进去了🤔`
- `右下角那个不是史莱姆吗？`
- `你们是不是又没看任务说明书。`

## Image Prompt Pattern

Use this structure:

```text
anime light novel illustration, cozy isekai slice-of-life, [characters and expressions], [fantasy location], [main activity], warm lantern/firelight, detailed props, candid social media photo feeling, rich background, expressive faces, high detail, no UI text inside the illustration
```

If generating the whole screenshot, describe the UI separately from the illustration and ask for crisp Chinese UI text only if the image model can handle text reliably. Otherwise provide UI text as a layout guide and recommend adding text after generation.
