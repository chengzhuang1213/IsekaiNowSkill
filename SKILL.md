---
name: isekai-now
description: Create Chinese "isekai social feed / fantasy Moments" posts and image prompts. Use when the user asks for 异世界朋友圈, isekai-now, fantasy social posts, anime social-feed screenshots, character diary posts, fake Moments/Xiaohongshu-style feeds, or wants a scene turned into a modern social app post with fantasy characters, location, likes, comments, and image-generation prompts.
---

# Isekai Now

Turn a fantasy or anime scene into a complete isekai social-feed poster. Preserve the joke: magical-world events are treated like casual daily posts, while the full image feels like a designed Moments-style status from inside that world.

## Workflow

1. Identify the post seed: poster, location, scene, mood, hidden incident, and whether the user wants text only, image prompt only, or a full finished social-feed image.
2. Before writing or generating images, extract every named character from the user's request: poster, visible characters in the image, likes, comment authors, and characters mentioned inside comments. Read `references/avatar-library.md`, map each extracted character to its exact bundled avatar file in `assets/Avatars`, and keep this avatar roster as the identity source for the whole task. If a named Love Live-style character has no matching bundled avatar, state the missing mapping instead of silently substituting another character.
3. Before generating a main illustration, visually inspect the poster's bound avatar file and write an identity lock from that image: hair color, hairstyle, eye color, signature accessories, expression/personality, and fantasy role cues. If the previous generated image or prior turn used a different character, add an explicit negative lock such as `not Kasumi, not brown bob hair, not previous character design`. A main image that does not visibly match the bound avatar identity is a failed generation and must not be used for final composition.
4. When generating Love Live-style characters, use the extracted avatar roster and this skill's bundled avatar library at `assets/Avatars` as the default character reference source. Treat these images as identity references for face, hair, color palette, fantasy role cues, and personality only.
5. For any image prompt or full UI composition, read `references/image-composition.md` to separate avatar identity, current-scene costume, props, and UI aspect ratio. For UI composition, use the extracted avatar roster and fixed isekai avatars when available. For reliable finished images, use a hybrid workflow: generate the main illustration without UI, then compose the whole social-feed poster locally with themed background skin, real rendered text, and circular avatar crops from `assets/Avatars`. Do not ask the image model to redraw tiny poster/comment avatars when local composition is possible. Before writing likes and comments, read `references/comment-voice.md` and `references/character-voice.md`; if the user does not specify a custom tone, use each character's default official-style personality and voice from `character-voice.md`.
6. After generating a main illustration, compare the visible main character against the poster avatar roster entry before composing the UI. Check hair color, hairstyle, eye color, accessories, and overall silhouette. If any major identity anchor is wrong, discard or regenerate the main illustration instead of hiding the mismatch with correct UI avatars.
7. If the user provides an example image or asks to match the style closely, read `references/style-guide.md`. For the current approved production target, also read `references/sample-reference.md` and use `assets/Samples/sample-airship-port-native-1206x2622.png` as the sample for native long-screen spacing.
8. Output a complete post package in Chinese unless the user asks for another language:
   - avatar roster when preparing image generation or local composition
   - identity lock for the poster/main visible characters when preparing image generation
   - poster name
   - location line
   - post text
   - image prompt
   - likes line
   - 3-8 comments
   - optional full finished-image plan
9. Keep the post short, social, and character-voiced. Avoid lore dumps.
10. Add a tiny story hook in the comments: ominous detail, comic misunderstanding, unseen creature, suspicious ingredient, magical accident, or rival teasing.

## Style Rules

- Use a modern social app structure, but make the final artifact read as a full isekai Moments-style poster, not a plain screenshot pasted on a blank page.
- Full finished social-feed images must use a fixed iPhone 16 Pro portrait canvas: `1206x2622` px, ratio `19.5:9`, unless the user explicitly asks for another size.
- Treat `assets/Samples/sample-airship-port-native-1206x2622.png` as the approved baseline sample for finished-image layout: native long screen, no legacy upscale padding, large main illustration, expanded lower comment area, and bottom input controls near the phone safe area.
- Choose the entire UI background and decorative skin from the post theme instead of defaulting to a mostly white card; avoid large empty pure-white areas.
- The whole image should be the status. Do not place a large white social card inside an unrelated poster background. The feed frame, paper/stone/map texture, ornaments, text, main illustration, comments, and input bar must feel like one designed interface.
- Theme background is a skin layer, not a content layer. It must stay behind the social post content as low-opacity texture, watermark, border, or corner ornament; it must not create empty header space, look like an unfinished UI control, or compete with the avatar, display name, location, menu, text, main image, likes, or comments.
- Keep the top area compact. Header plus post text should not push the main image far down; after the final post-text line, the main image should start promptly with only normal feed spacing.
- Decorative text badges such as `SSR UP`, guild stamps, academy seals, or compass labels must be subtle background marks only. Place them away from the three-dot menu and readable UI text, use low contrast/opacity, and never make them look clickable or primary.
- Make fantasy feel mundane: "first camp meal", "guild shift ended", "dragon taxi delay", "slime spilled in the bag".
- Prefer warm anime slice-of-life scenes over epic battle posters.
- Support two common post moods: cozy daily comedy (bakery, market, camp, inn, guild meal) and ceremonial adventure drama (castle gate, knight order departure, festival procession, public mission sendoff).
- Use Chinese nicknames and fantasy locations that read like map check-ins: `异世界·翡翠湖露营地`, `王都东门·晨市`, `银叶森林·临时营地`.
- In the post header, keep the poster's full official display name. In the likes and comment area, show character names as short given names only, not full names. Example: poster `上原步梦`; comments `步梦：...`, `善子：...`, `花帆：...`, `堇：...`, `真姬：...`.
- Likes overlap rule: each post may have exactly one character who both liked and commented. Choose one commenter to also appear in the likes line; all other liked characters must be randomly chosen from characters who do not comment on that post. If the user provides a likes line that overlaps with multiple commenters, rewrite it to keep only one overlapping name.
- For full social-feed images, always use fixed local avatar files for the poster and comment avatars whenever possible. Paste them into the UI as circular crops from `assets/Avatars` instead of relying on the image model to generate small faces. If adapting a generated or example UI, replace every small UI头像 with the matching bundled avatar.
- Before any full social-feed image or image prompt, explicitly resolve the character identity roster from the request and bind each character to a concrete local avatar filename. Use those bound files for poster and comment avatars, and use the same roster to describe identity anchors in the main illustration prompt.
- Main illustration identity must match the poster's bound avatar. Do not accept a main image whose visible character looks like a different avatar-library character, even if the caption, setting, or UI avatars are correct.
- Convert all character appearances into isekai versions. The main image and every avatar should have fantasy clothing, accessories, or setting cues; do not keep modern school uniforms unless the user explicitly asks for a crossover.
- The main illustration may include in-world Chinese signs, chalkboards, posters, banners, scoreboards, certificates, warning labels, and speech bubbles when they make the scene funnier or clearer.
- Real UI text must be rendered locally whenever possible. Do not depend on image generation for readable captions, likes, comments, or input placeholders. Keep in-image generated text short and story-relevant only.
- When composing UI locally, prefer project-bundled fonts under `assets/Fonts` before falling back to system fonts. If Maple Mono CN is available, use `assets/Fonts/MapleMono-CN-unhinted/MapleMono-CN-Regular.ttf` for normal UI text and `MapleMono-CN-Bold.ttf` or `MapleMono-CN-ExtraBold.ttf` for names and emphasis.
- Use 1-3 emojis at most in the post text.
- Let comments reveal character relationships and small plot tension. Prefer image-specific teasing over exposition.
- Do not over-explain UI. Generate the artifact directly.

## Output Templates

For a compact text post:

```markdown
**昵称**：...
**定位**：...
**正文**：...
**配图提示词**：...
**点赞**：...
**评论**：
...
```

For a full finished image plan, include:

```markdown
**主图生成提示词**：
一张无 UI 的二次元异世界主图，宽图比例；内容为：...

**本地合成要求**：
固定尺寸 1206x2622，竖屏，比例 19.5:9；根据地点和正文选择异世界主题皮肤；整张图就是朋友圈状态而不是白框套图；头像全部从 `assets/Avatars` 圆裁；正文、点赞、评论和输入框用本地字体渲染；主图、评论区、底部输入框都不能互相遮挡。
```

## References

- Read `references/style-guide.md` when matching visual tone, layout, writing voice, or screenshot composition.
- Read `references/sample-reference.md` when producing or revising a full finished social-feed image; it describes the approved sample image and the layout traits to preserve.
- Read `references/image-composition.md` before generating a main illustration or composing a finished social-feed poster; it contains the role-vs-scene, prop, headwear, and aspect-ratio guardrails.
- Read `references/avatar-library.md` when using Love Live-style characters, fixed avatars, or local UI composition.
- Read `references/character-voice.md` when writing character posts, captions, or comments. Use it as the default voice guide unless the user overrides a character's mood or role.
- Read `references/comment-voice.md` before generating or revising comment sections.
- Read `references/example-pack.md` when the user wants examples, variants, or a quick reusable pattern.


