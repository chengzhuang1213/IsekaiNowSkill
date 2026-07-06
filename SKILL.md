---
name: isekai-now
description: Create Chinese "isekai social feed / fantasy Moments" posts and image prompts. Use when the user asks for 异世界朋友圈, isekai-now, fantasy social posts, anime social-feed screenshots, character diary posts, fake Moments/Xiaohongshu-style feeds, or wants a scene turned into a modern social app post with fantasy characters, location, likes, comments, and image-generation prompts.
---

# Isekai Now

Turn a fantasy or anime scene into a believable modern social-feed post from inside the isekai. Preserve the joke: magical-world events are treated like casual daily posts.

## Workflow

1. Identify the post seed: poster, location, scene, mood, hidden incident, and whether the user wants text only, image prompt only, or a full screenshot prompt.
2. When generating Love Live-style characters, use `C:\Users\cheng\Desktop\异世界CG\asserts` as the default character reference folder if available. For social-feed UI avatars, prefer the fixed isekai avatar library at `C:\Users\cheng\Desktop\异世界CG\asserts\Avatars`. Treat these images as identity references for face, hair, color palette, fantasy role cues, and personality only.
3. For any image prompt or full UI composition, read `references/image-composition.md` to separate avatar identity, current-scene costume, props, and UI aspect ratio. For UI composition, read `references/avatar-library.md` and use fixed isekai avatars when available. For reliable full screenshots, prefer a hybrid workflow: generate the main illustration and theme texture, then compose the social UI locally and paste circular crops from the fixed avatar PNGs; do not ask the image model to redraw tiny comment avatars when local composition is possible. Before writing likes and comments, read `references/comment-voice.md` and `references/character-voice.md`; if the user does not specify a custom tone, use each character's default official-style personality and voice from `character-voice.md`.
4. If the user provides an example image or asks to match the style closely, read `references/style-guide.md`.
5. Output a complete post package in Chinese unless the user asks for another language:
   - poster name
   - location line
   - post text
   - image prompt
   - likes line
   - 3-8 comments
   - optional full screenshot prompt
6. Keep the post short, social, and character-voiced. Avoid lore dumps.
7. Add a tiny story hook in the comments: ominous detail, comic misunderstanding, unseen creature, suspicious ingredient, magical accident, or rival teasing.

## Style Rules

- Use a modern social app frame, but do not claim it is an exact real app screenshot.
- Full screenshot images must use a fixed `1024x1536` vertical size unless the user explicitly asks for another size.
- Choose the UI background and decorative skin from the post theme instead of defaulting to a mostly white card; avoid large empty pure-white areas.
- Theme background is a skin layer, not a content layer. It must stay behind the social post content as low-opacity texture, watermark, border, or corner ornament; it must not create empty header space, look like an unfinished UI control, or compete with the avatar, display name, location, menu, text, main image, likes, or comments.
- Keep the top area compact. Header plus post text should not push the main image far down; after the final post-text line, the main image should start promptly with only normal feed spacing.
- Decorative text badges such as `SSR UP`, guild stamps, academy seals, or compass labels must be subtle background marks only. Place them away from the three-dot menu and readable UI text, use low contrast/opacity, and never make them look clickable or primary.
- Make fantasy feel mundane: "first camp meal", "guild shift ended", "dragon taxi delay", "slime spilled in the bag".
- Prefer warm anime slice-of-life scenes over epic battle posters.
- Support two common post moods: cozy daily comedy (bakery, market, camp, inn, guild meal) and ceremonial adventure drama (castle gate, knight order departure, festival procession, public mission sendoff).
- Use Chinese nicknames and fantasy locations that read like map check-ins: `异世界·翡翠湖露营地`, `王都东门·晨市`, `银叶森林·临时营地`.
- In the post header, keep the poster's full official display name. In the likes and comment area, show character names as short given names only, not full names. Example: poster `上原步梦`; comments `步梦：...`, `善子：...`, `花帆：...`, `堇：...`, `真姬：...`.
- Likes overlap rule: each post may have exactly one character who both liked and commented. Choose one commenter to also appear in the likes line; all other liked characters must be randomly chosen from characters who do not comment on that post. If the user provides a likes line that overlaps with multiple commenters, rewrite it to keep only one overlapping name.
- For full social-feed screenshots, use fixed local avatar files for the poster and comment avatars whenever possible. Paste them into the UI as circular crops from `C:\Users\cheng\Desktop\异世界CG\asserts\Avatars` instead of relying on the image model to generate small faces.
- Convert all character appearances into isekai versions. The main image and every avatar should have fantasy clothing, accessories, or setting cues; do not keep modern school uniforms unless the user explicitly asks for a crossover.
- The main illustration may include in-world Chinese signs, chalkboards, posters, banners, and speech bubbles when they make the scene funnier or clearer.
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

For a full screenshot prompt, include:

```markdown
**整图生成提示词**：
一张现代社交动态截图风格的竖版界面，固定尺寸 1024x1536；根据地点和正文选择异世界主题皮肤，避免大面积纯白；圆形头像，蓝色昵称，灰色定位行，中文正文，一张大幅二次元异世界日常配图，下方有点赞和评论区，底部有评论输入框；内容为：...
```

## References

- Read `references/style-guide.md` when matching visual tone, layout, writing voice, or screenshot composition.
- Read `references/image-composition.md` before generating a main illustration or composing a full screenshot; it contains the role-vs-scene, prop, headwear, and aspect-ratio guardrails.
- Read `references/avatar-library.md` when using Muse characters, fixed avatars, symbols, or local UI composition.
- Read `references/character-voice.md` when writing character posts, captions, or comments. Use it as the default voice guide unless the user overrides a character's mood or role.
- Read `references/comment-voice.md` before generating or revising comment sections.
- Read `references/example-pack.md` when the user wants examples, variants, or a quick reusable pattern.


