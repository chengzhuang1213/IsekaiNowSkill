# Isekai Now Image Composition Guardrails

## Core Distinction

Separate three layers before prompting or composing:

1. **Identity layer**: face, hair color, hairstyle, eye color, expression vibe, and recognizable personality. Preserve this from reference images or fixed avatars.
2. **Library avatar layer**: the fixed small头像 may have a default isekai job, such as rose shield guardian or fire mage. This is only a reusable profile identity.
3. **Current scene layer**: the main illustration must follow the user's current location, story, caption, and social joke. Scene clothing and props can change from the avatar job.
4. **Local UI layer**: the finished social-feed poster should be composed locally whenever possible. This layer owns the readable Chinese UI text, likes, comments, comment bubbles, input field, theme border, and exact circular avatar crops from `assets/Avatars`.

Never force avatar-job props into the main image when they do not serve the current post.

## Identity Lock Before Generation

Before generating any main illustration with a named Love Live-style character, inspect the bound avatar file from the avatar roster and write a strict identity lock. The lock must include:

- hair color and hairstyle, including twin tails, bob cuts, long hair, bangs, colored tips, ribbons, goggles, clips, or other signature accessories
- eye color and expression type
- face/personality vibe from the avatar
- fantasy role cues from the avatar-library table
- explicit negative cues for likely confusions, especially the character from the previous generated image

Do not rely on the character name alone. If the image model cannot receive the avatar file as a visual reference, the prompt still must spell out the exact visible anchors from the avatar. If the generated main character does not match those anchors, discard or regenerate the main illustration before local UI composition.

Example for Rurino:

```text
Osawa Rurino identity lock from Rurino_Avatar_Isekai.png: blonde high twin tails with pink-and-blue tinted ends, bright blue eyes, goggles on head, flower/ribbon hair accessories, lively crystal-communication adventurer vibe, energetic streamer personality now exhausted. Avoid brown bob hair, avoid Kasumi-like face, avoid moon hair clip, avoid previous character design.
```

## Prop And Costume Rules

- Include props only if they support the post's action, punchline, or visible story hook.
- Remove combat props from cozy scenes unless the joke is specifically about being overdressed or on guard.
- For tea, cafe, bakery, inn, palace, market, classroom, sleepover, or date-like posts, prioritize scene props: cups, plates, pastries, menus, flowers, bags, books, small familiars, or tableware.
- For ceremony, departure, battle, dungeon, rescue, or mission posts, allow weapons, shields, armor, banners, spell circles, and guild gear.
- For social-joke scenes, include visible evidence that comments can react to: license paper, exam board, lost-and-found notice, warning sign, suspicious menu, treasure chest, mimic, measurement marks, item tag, or guild stamp.
- If the caption creates a role for the moment, obey that role over the library job. Example: `公主的下午茶时间` means princess headpiece, elegant dress, tea table, and pastries. Do not add a shield unless the user asks for guardian/knight tension.
- Headwear should match the scene: tiara/circlet/ribbon for princess scenes; mage hat for magic scenes; hood/cape for travel; helmet only for knight or battle scenes.

## Character Prompt Pattern

Use this structure for main illustrations:

```text
[Character name] as an isekai version for this specific scene, preserving [identity lock from bound avatar file]. Current-scene role: [scene role from user/caption]. Outfit and props: [only props that support this scene]. Avoid: [library-job props that would be off-scene] and [likely wrong-character anchors].
```

Example:

```text
Ayumu Uehara as an isekai rose-themed princess at afternoon tea, preserving rose-pink side-bun hair, yellow-green eyes, and gentle sincere smile. Outfit and props: elegant princess dress, small tiara or rose circlet, coffee cup, pastries, palace courtyard tea table. Avoid shield, battle armor, weapons, school uniform, modern phone.
```

## Identity QA After Generation

Before composing the finished social-feed poster, compare the generated main illustration against the poster avatar. Reject the main image when any of these fail:

- wrong hair color or hairstyle
- missing signature accessory when it is important to identity
- wrong eye color when visible
- face/silhouette clearly resembles another roster character or previous generated character
- poster avatar and main image would read as different people to a viewer

Do not solve a wrong main character by pasting the correct circular avatar in the UI. Regenerate or revise the main illustration first.

## Main Image Aspect Ratio

- For finished social-feed poster generation, use a fixed iPhone 16 Pro portrait output size of `1206x2622` px, ratio `19.5:9`, unless the user explicitly requests another size. Keep all finished outputs the same size across a batch or series.
- Compose directly at `1206x2622`. Avoid rendering a shorter 1024-style layout and scaling it into the phone canvas; the native layout should use the extra height for a larger main illustration, expanded comment area, and bottom input controls.
- Use `assets/Samples/sample-airship-port-native-1206x2622.png` as the approved native-layout reference for finished posters. Follow its use of a large main image plus an actively used lower half instead of leaving dead space below the comments.
- For local UI composition, generate the main illustration as a wide rectangle whenever possible: prefer `1536x1024`, `1448x1086`, or another 3:2 to 4:3 image.
- In the final Moments-style card, crop or fit the main image to a stable rectangle around **1.33:1 to 1.5:1**.
- Do not let a square or vertical main image dominate the card unless the user specifically asks for a square post.
- Keep the main image width aligned with the text column and leave comfortable white margins; the image should not feel wider than the social card's rhythm.
- If the generated image has important content near the edges, use contain-with-padding or a gentler center crop instead of cutting faces, cups, hands, or story clues.
- Do not generate the main illustration with the social app frame included. The main illustration can contain in-world text and props, but the post header, caption, likes, comments, avatars, and input bar belong to the local UI layer.

## Theme Skin And White Space

- Select a theme skin from the post's location, activity, and caption instead of using a plain white social card by default.
- Avoid large empty pure-white areas. Prefer ivory parchment, warm cream, pale rose, pale gold, mist blue, sage, washi, wood, stone, or night-sky UI treatments when they fit the scene.
- The final image should feel like the whole canvas is the social status. Avoid a big white app card floating inside an unrelated fantasy background.
- Break up light backgrounds with subtle paper grain, faint ornamental dividers, pale colored comment strips, small badges, scene-matching corner ornaments, or soft fantasy accents.
- Make the main illustration carry enough visual weight; do not let blank card space dominate the screenshot.
- Match ornaments to the theme: rose corners for palace tea, guild stamps for quests, leaves for forest posts, compass/shell details for ocean posts, moon-star dividers for gothic or astrology posts, sakura corners for shrine posts.
- Treat all theme decoration as a low-priority background skin. It should sit behind content, usually at low opacity, and should never read as a foreground control.
- Do not place decorative stamps, seals, labels, or icons near the author avatar, display name, location, three-dot menu, body text, likes line, comment names, or input field. Keep decoration in corners, borders, dividers, or as a faint watermark.
- Avoid large blank header zones. The header and body text area should be compact; the main illustration should begin soon after the caption. If a generated or local decoration creates extra vertical space, remove or fade it instead of moving content down.
- If a themed label such as `SSR UP`, `Guild`, `Academy`, or a stamp is used, it must be clearly decorative: small or faint, lower contrast than normal UI text, and not aligned like a button/menu item.

## UI Composition Rules

- Fixed post width should read like a social feed card, not a poster frame.
- The finished artifact may be more polished than a literal phone screenshot: it can use themed paper texture, map lines, magical watermarks, border ornaments, and comment strips, as long as the content hierarchy still reads like a social feed.
- Main image should usually start below the caption with enough breathing room and be visually subordinate to the full post, not fill nearly the whole card height.
- Prioritize content hierarchy: header, caption, main image, likes, comments, and input field must be visually clearer than all background decoration.
- Keep author avatar 72-88 px, comment avatars 42-50 px, and preserve circular crops.
- For reliable finished images, compose UI avatars locally from fixed PNG files instead of asking image generation to draw small portraits. Crop each avatar square to a circle, paste the poster avatar at 72-88 px, and paste comment avatars at 42-50 px. The generated image may provide the main illustration and theme background, but small UI avatars must come from the avatar library whenever available.
- If a reference image or generated draft already has small avatars, replace those UI avatars with matching `assets/Avatars` circular crops. Do not keep generated small faces.
- Render UI text locally for readability: poster name, location, caption, likes, comments, reply labels, and input placeholder. Avoid emoji that the selected font cannot display; replace with simple readable punctuation or symbols when needed.
- Prefer 3-6 comments unless the user asks for many; comments should fit without crowding the input field.
- When the prompt includes 6-8 comments, use the native `1206x2622` height like the approved sample: keep each row readable, reduce blank footer space, and let comments occupy the lower half before the input bar.
- Validate the final image visually for: no text overlap, no clipped UI, no wrong avatar, no large blank white card, no unreadable generated UI text, no irrelevant main-image prop, and main image aspect ratio matching the feed.
