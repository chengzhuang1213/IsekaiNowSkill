# Isekai Now Style Guide

## Core Concept

Create a "social app post from inside another world": the UI is contemporary, while the content is fantasy slice-of-life. The humor comes from treating magical events as normal daily updates.

For finished images, the target is an **isekai Moments poster**, not a literal app screenshot. The whole `1206x2622` iPhone 16 Pro portrait image should be the status: themed paper/map/stone texture, UI frame, main illustration, likes, comments, and input field all belong to one coherent designed interface.

## Visual Layout

- Portrait finished image, fixed full-image size `1206x2622` px, ratio `19.5:9`, unless the user explicitly asks for another size. Keep every finished social-feed image at this same size for consistency across batches.
- Compose directly on the `1206x2622` production canvas. Do not build a shorter legacy layout first and scale it up with background padding; use the full vertical space with a larger main image, roomier comments, and a bottom input bar near the safe area.
- Choose a theme skin from the post location, mood, and caption instead of defaulting to a mostly white app frame.
- Use a readable rounded feed frame with subtle shadow or thin border. The frame may be ivory, parchment, mist-blue, blush, sage, midnight violet, dark stone, or another theme color; avoid large empty pure-white areas.
- The frame should not look like a big white card pasted onto a separate background. Let the background texture, border, post content, main image, comments, and input bar read as one integrated status design.
- Treat the theme as a restrained skin behind the post. Use subtle texture, watermarks, dividers, border accents, and corner ornaments; do not add foreground badges or decorative marks that look like app controls.
- Keep the top of the post compact. The author row and body text should not create a large blank area before the main image.
- Decorative labels and stamps must stay away from the three-dot menu and text. They should be lower contrast than UI text and should never look clickable.
- Top row: round anime avatar, blue display name, gray location with a pin icon, small three-dot menu.
- Body: short Chinese text with line breaks, casual tone, 0-3 emojis.
- Main image: large rectangular anime illustration, usually 4:3 or wide rectangle, centered under the text.
- Social area: pink/red heart icon, blue-gray likes line, then comments with tiny round avatars.
- Bottom: pale comment input field with placeholder like `评论...`.
- Some variants can omit the separate body text and let the image carry the moment, with the caption-like comments below.

## Satisfied Example Pattern

When matching the preferred examples, prioritize these qualities:

- Current approved finished-image samples:
  - `assets/Samples/sample-airship-port-native-1206x2622.png` for sky-port, travel, pilot-license, and pale map-paper layouts.
  - `assets/Samples/sample-rurino-guild-native-1206x2622.png` for adventurer guild, quest-board comedy, tired social-post humor, strict character identity lock, standalone main illustration generation, and local avatar composition.
  - `assets/Samples/sample-ayumu-palace-tea-native-1206x2622.png` for palace courtyard, princess afternoon tea, rose sweets, warm pink-gold UI, and compact four-comment layouts.
- The background is an in-world UI skin, such as airship map paper, magic academy parchment, dark ruin stone, or starry archive paper.
- The main illustration contains the social joke visually: a license, scoreboard, warning sign, certificate, treasure chest, magic accident, suspicious creature, or other readable story evidence.
- The UI text is crisp and typeset, not model-painted. Render captions, likes, comments, and input placeholders locally whenever possible.
- The main image is large but not the whole poster; comments and input remain clearly readable in the same vertical composition.
- The poster avatar and every comment avatar are exact circular crops from `assets/Avatars`, replacing any generated small portraits from examples or image outputs.
- The generated main illustration should visibly match the poster avatar identity. Use the Rurino guild sample as the reference for preserving hair color, hairstyle, eye color, signature accessories, and role cues across the avatar and main image.
- Use the Ayumu palace tea sample as the reference for translating avatar identity into current-scene costume: the main image can use a princess dress and tea props while preserving Ayumu's rose-pink hair, side bun, yellow-green eyes, gentle expression, and rose identity.
- The lower half should not be treated as leftover space. Use it for likes, roomy comment strips, and the bottom input bar.

## Theme Skin Selection

For finished social-feed images, choose the UI background and decorative skin from the post theme. The skin should color the background, dividers, comment blocks, and small ornaments while preserving the modern social-feed structure.

- Palace, princess, garden tea: ivory parchment, pale gold dividers, rose corner ornaments, soft blush comment blocks.
- Magic academy, library, spell research: warm parchment, ink-blue headers, faint magic-circle watermark, book-page dividers.
- Adventurer guild, quests, tavern: wooden notice-board background, parchment cards, wax seals, guild-stamp accents.
- Forest, camping, elves, healing: pale sage background, leaf texture, vine corner ornaments, soft green comment blocks.
- Ocean, port, ship, mermaid: pale aqua paper, compass icons, shell dividers, sea-map texture.
- Airship, sky port, pilot license: pale sky-blue map paper, compass/propeller ornaments, thin gold navigation lines, cloud-like comment strips.
- Night, astrology, gothic, fallen angel: deep violet or midnight gradient, moon-star ornaments, subtle glowing borders.
- Shrine, kimono, cherry blossom: washi paper texture, vermilion dividers, sakura corner ornaments.
- Dungeon, ruins, battle aftermath: dark stone or smoky parchment, torch-warm highlights, adventurer log styling.
- Ancient stardust ruins, star gates, lost civilization: midnight blue parchment or stone texture, faint star maps, pale blue rune dividers, small light-particle ornaments.
- Treasure, rare item discovery, mimic chest: dark violet or smoky parchment with gold trim, coin glints, chest-lock corner ornaments, warm comment blocks.
- Bakery, cafe, sweets: cream background, coffee stain texture, pastry sticker accents.

Avoid turning the post into a game menu, poster, or fantasy parchment letter. It should still read as a modern social app post from inside the isekai.

## Character References

- Default reference folder: `assets/Avatars`.
- Use the reference images to preserve each character's face shape, hairstyle, hair color, eye color, expression range, and recognizable vibe.
- Do not copy the modern school-uniform look into the final post unless explicitly requested. Translate the character into an isekai outfit: cloak, traveler tunic, mage robe, ranger cape, guild brooch, potion satchel, armor accents, fantasy hair ornament, or camp/adventurer accessories.
- The poster avatar and all comment avatars should also be isekai-style portraits. They may be small circular crops, but they should still show fantasy clothing or accessories rather than plain modern uniforms.
- When writing prompts, phrase this as: `based on the provided character reference for identity only, redesigned as an isekai adventurer portrait`.

## Local Fonts

- Prefer project fonts under `assets/Fonts` for local composition so outputs are portable across machines.
- If available, use Maple Mono CN from `assets/Fonts/MapleMono-CN-unhinted/`:
  - `MapleMono-CN-Regular.ttf` for body text, likes, comments, and input placeholders.
  - `MapleMono-CN-Bold.ttf` or `MapleMono-CN-ExtraBold.ttf` for poster names, comment names, and strong UI labels.
- Fall back to `NotoSansSC-VF.ttf` / `NotoSerifSC-VF.ttf` only when the project font is missing or a theme needs a serif parchment style.

## Image Style

- Detailed anime / light novel illustration.
- Warm cinematic lighting, expressive faces, cozy fantasy props.
- Prefer scenes like camping, guild dinner, market snacks, inn room, potion mishap, magic academy courtyard, lake travel, festival stall, caravan rest.
- Also support grand public scenes such as knight order departure, castle gate speeches, royal banners, guards, and dramatic sunlight when the post is about a mission, ceremony, or adventure sendoff.
- Include enough fantasy details: cloaks, lanterns, banners, runes, potions, familiar creatures, guild badges, medieval tents, enchanted cookware.
- Keep the scene readable as a candid social photo, not a poster or wallpaper.
- In-image text can be part of the joke: bakery chalkboards, motivational posters, speech bubbles, shop signs, royal banners, scoreboards, certificates, wanted notices, or cute warning labels. Keep it short and legible.

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

For finished social-feed images, prefer this two-stage pattern:

1. Generate the main illustration only, with no social UI, no comments, no app frame, and no watermark. In-world signs or documents are allowed only when they are part of the joke.
2. Compose the social-feed poster locally at `1206x2622`: themed background skin, exact circular avatars from `assets/Avatars`, crisp Chinese text, main image crop, likes line, comments, and bottom input field.

Only ask the image model for the whole UI when local composition is impossible. If doing so, still treat generated UI text as a draft and replace unreadable text locally afterward.
