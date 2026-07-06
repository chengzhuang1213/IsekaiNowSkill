# Isekai Now Avatar Library

## Asset Paths

- Bundled fixed isekai avatar folder: `assets/Avatars` inside this skill.
- Bundled symbol folder: `assets/Symbols` inside this skill.
- Local character reference folder, when available on Cheng's machine: `C:\Users\cheng\Desktop\异世界CG\asserts`
- Local fixed isekai avatar folder, when available: `C:\Users\cheng\Desktop\异世界CG\asserts\Avatars`
- Local symbol folder, when available: `C:\Users\cheng\Desktop\异世界CG\asserts\Symbols`

## Avatar Policy

Use fixed isekai character avatars whenever composing UI locally or when instructing image generation to reuse avatar assets. Prefer real character avatars over symbols for comment avatars when the goal is intimacy, friend-group feeling, and character recognition.

Use symbols only as a fallback for tiny UI, decorative badges, or when the image model cannot keep small faces stable.

When this skill is installed from GitHub, prefer bundled relative asset paths (`assets/Avatars`, `assets/Symbols`). Use Cheng's desktop asset paths only when running in the original local environment and those folders exist.

## Muse Isekai Roles

| Character | Chinese | Role | Avatar file |
|---|---|---|---|
| Honoka | 穗乃果 | 冒险家协会会长 | `Honoka_Avatar_Isekai.png` |
| Kotori | 南小鸟 | 治愈师导师 | `Kotori_Avatar_Isekai.png` |
| Umi | 海未 | 冷库剑士 | `Umi_Avatar_Isekai.png` |
| Eli | 绘里 | 骑士团团长 | `Eli_Avatar_Isekai.png` |
| Nozomi | 希 | 占星魔法师 | `Nozomi_Avatar_Isekai.png` |
| Rin | 凛 | 快递员 | `Rin_Avatar_Isekai.png` |
| Hanayo | 花阳 | 米饭店老板 | `Hanayo_Avatar_Isekai.png` |
| Nico | 妮可 | 盗贼偶像 | `Nico_Avatar_Isekai.png` |
| Maki | 真姬 | 火法师 | `Maki_Avatar_Isekai.png` |

## Usage Rules

- Use the fixed avatar for the post author when available.
- Use fixed avatars for comment authors when generating or composing a full social-feed UI.
- Treat role assignments as avatar-library defaults and relationship context, not mandatory props for every main illustration. In main images, preserve identity but adapt clothing, props, and accessories to the current scene and caption.
- If generating a new avatar, match the existing library: square portrait, bust-up framing, light novel anime style, fantasy outfit, no modern school uniform, circular-crop friendly.
- Do not overwrite fixed avatars unless the user explicitly asks for a new version.

