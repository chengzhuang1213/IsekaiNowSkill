---
name: isekai-now
description: Create Chinese "isekai social feed / fantasy Moments" posts and image prompts. Use when the user asks for 异世界朋友圈, isekai-now, fantasy social posts, anime social-feed screenshots, character diary posts, fake Moments/Xiaohongshu-style feeds, or wants a scene turned into a modern social app post with fantasy characters, location, likes, comments, and image-generation prompts.
---

# Isekai Now

Turn a fantasy or anime scene into a believable modern social-feed post from inside the isekai. Preserve the joke: magical-world events are treated like casual daily posts.

## Workflow

1. Identify the post seed: poster, location, scene, mood, hidden incident, and whether the user wants text only, image prompt only, or a full screenshot prompt.
2. When generating Love Live-style characters, use `C:\Users\cheng\Desktop\异世界CG\asserts` as the default character reference folder if available. Treat these images as identity references for face, hair, color palette, and personality only.
3. For any image prompt or full UI composition, read `references/image-composition.md` to separate avatar identity, current-scene costume, props, and UI aspect ratio. For UI composition, read `references/avatar-library.md` and use fixed isekai avatars when available. Before writing likes and comments, read `references/comment-voice.md` and make the comment section feel like close friends reacting in real time.
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
- Make fantasy feel mundane: "first camp meal", "guild shift ended", "dragon taxi delay", "slime spilled in the bag".
- Prefer warm anime slice-of-life scenes over epic battle posters.
- Support two common post moods: cozy daily comedy (bakery, market, camp, inn, guild meal) and ceremonial adventure drama (castle gate, knight order departure, festival procession, public mission sendoff).
- Use Chinese nicknames and fantasy locations that read like map check-ins: `异世界·翡翠湖露营地`, `王都东门·晨市`, `银叶森林·临时营地`.
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
一张现代社交动态截图风格的竖版界面，白色卡片背景，圆形头像，蓝色昵称，灰色定位行，中文正文，一张大幅二次元异世界日常配图，下方有点赞和评论区，底部有评论输入框；内容为：...
```

## References

- Read `references/style-guide.md` when matching visual tone, layout, writing voice, or screenshot composition.
- Read `references/image-composition.md` before generating a main illustration or composing a full screenshot; it contains the role-vs-scene, prop, headwear, and aspect-ratio guardrails.
- Read `references/avatar-library.md` when using Muse characters, fixed avatars, symbols, or local UI composition.
- Read `references/comment-voice.md` before generating or revising comment sections.
- Read `references/example-pack.md` when the user wants examples, variants, or a quick reusable pattern.

