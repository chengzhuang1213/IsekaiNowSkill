# Isekai Now Style Guide

## Core Concept

Create a "social app post from inside another world": the UI is contemporary, while the content is fantasy slice-of-life. The humor comes from treating magical events as normal daily updates.

## Visual Layout

- Portrait screenshot, fixed full-image size `1024x1536` unless the user explicitly asks for another size. Keep every generated full social-feed screenshot at this same size for consistency across batches.
- Choose a theme skin from the post location, mood, and caption instead of defaulting to a mostly white app frame.
- Use a readable rounded feed card with subtle shadow or thin border. The card may be ivory, parchment, mist-blue, blush, sage, or another pale theme color; avoid large empty pure-white areas.
- Treat the theme as a restrained skin behind the post. Use subtle texture, watermarks, dividers, border accents, and corner ornaments; do not add foreground badges or decorative marks that look like app controls.
- Keep the top of the post compact. The author row and body text should not create a large blank area before the main image.
- Decorative labels and stamps must stay away from the three-dot menu and text. They should be lower contrast than UI text and should never look clickable.
- Top row: round anime avatar, blue display name, gray location with a pin icon, small three-dot menu.
- Body: short Chinese text with line breaks, casual tone, 0-3 emojis.
- Main image: large rectangular anime illustration, usually 4:3 or wide rectangle, centered under the text.
- Social area: pink/red heart icon, blue-gray likes line, then comments with tiny round avatars.
- Bottom: pale comment input field with placeholder like `评论...`.
- Some variants can omit the separate body text and let the image carry the moment, with the caption-like comments below.

## Theme Skin Selection

For full screenshot prompts, choose the UI background and decorative skin from the post theme. The skin should color the background, dividers, comment blocks, and small ornaments while preserving the modern social-feed structure.

- Palace, princess, garden tea: ivory parchment, pale gold dividers, rose corner ornaments, soft blush comment blocks.
- Magic academy, library, spell research: warm parchment, ink-blue headers, faint magic-circle watermark, book-page dividers.
- Adventurer guild, quests, tavern: wooden notice-board background, parchment cards, wax seals, guild-stamp accents.
- Forest, camping, elves, healing: pale sage background, leaf texture, vine corner ornaments, soft green comment blocks.
- Ocean, port, ship, mermaid: pale aqua paper, compass icons, shell dividers, sea-map texture.
- Night, astrology, gothic, fallen angel: deep violet or midnight gradient, moon-star ornaments, subtle glowing borders.
- Shrine, kimono, cherry blossom: washi paper texture, vermilion dividers, sakura corner ornaments.
- Dungeon, ruins, battle aftermath: dark stone or smoky parchment, torch-warm highlights, adventurer log styling.
- Bakery, cafe, sweets: cream background, coffee stain texture, pastry sticker accents.

Avoid turning the post into a game menu, poster, or fantasy parchment letter. It should still read as a modern social app post from inside the isekai.

## Character References

- Default reference folder: `assets/Avatars`.
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
