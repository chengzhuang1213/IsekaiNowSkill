# Isekai Now Sample Reference

## Approved Production Samples

Use this file when producing or revising a finished social-feed poster:

- Sample image: `assets/Samples/sample-airship-port-native-1206x2622.png`
- Scenario: You Watanabe at the isekai royal airship port
- Canvas: native `1206x2622` px, portrait, ratio `19.5:9`

- Sample image: `assets/Samples/sample-rurino-guild-native-1206x2622.png`
- Scenario: Rurino Osawa at the isekai adventurer guild after missing A-rank commissions
- Canvas: native `1206x2622` px, portrait, ratio `19.5:9`

- Sample image: `assets/Samples/sample-ayumu-palace-tea-native-1206x2622.png`
- Scenario: Ayumu Uehara at a royal palace courtyard afternoon tea
- Canvas: native `1206x2622` px, portrait, ratio `19.5:9`

These samples are the current baselines for the full-poster format. Use the airship sample for sky-port, travel, pilot-license, and pale map-paper layouts. Use the Rurino guild sample for adventurer guild, quest-board, tired comedy, strict character identity lock, standalone main illustration generation, and locally rendered UI avatars. Use the Ayumu palace tea sample for palace courtyard, princess, rose, cafe, sweets, warm pink-gold UI, and compact four-comment layouts.

## What To Preserve

- The whole image is the social-feed status. There is no separate white screenshot card floating inside another poster.
- The canvas is composed directly at `1206x2622`. Do not create a shorter layout and pad or scale it into the phone size.
- The theme skin fills the full image: pale sky-blue map paper, fine border, subtle route arcs, compass/propeller ornaments, and low-contrast texture.
- Header, caption, main image, likes, comments, and input bar live inside one coherent interface frame.
- The top header stays compact enough that the main image begins early.
- The main illustration is large, colorful, and story-rich, but it leaves enough lower-screen space for readable likes, comments, and input controls.
- The lower half is actively used. Comment rows are roomy and readable instead of squeezed above a large blank footer.
- The bottom input bar sits near the safe area and feels like part of the same themed UI.
- Poster avatar and comment avatars are exact circular crops from `assets/Avatars`.
- UI text is crisp local text, not image-model-painted text.
- When character identity matters, the main illustration must visibly match the poster avatar before UI composition. The Rurino guild sample demonstrates rejecting a wrong main character and regenerating with a stricter identity lock.

## Main Illustration Expectations

The main illustration should carry the joke visually. In the airship sample, the license paper, airship, warning sign, port banner, and cheerful victory pose all support the caption and comments. In the Rurino guild sample, `今日任务已满`, the `301` ticket, the `凌晨5:00` note, the long queue, and unused equipment support the caption and comments. In the Ayumu palace tea sample, the coffee, rose pastries, palace courtyard, and `9999金币` price card support the princess tea caption plus green-tea and teasing comments.

For future posts, include similarly visible story evidence when the user prompt allows it:

- license, certificate, exam board, treasure chest, lost-and-found notice, warning sign
- scoreboard, map, magical contract, guild stamp, suspicious creature, item tag
- short in-world labels that are funny or useful, while keeping real UI text local

## Native Layout Ratios

Use these as flexible composition targets, not hard pixel locks:

- Outer safe margin: generous enough for border ornaments without crowding the content.
- Header height: compact, usually under one sixth of the canvas.
- Main illustration: aligned to the text column, large enough to be the visual center, usually about one third of the canvas height.
- Social area: likes plus comments should comfortably occupy much of the lower half.
- Comment avatars: small, consistent, and vertically centered with comment bubbles.
- Input area: present at the bottom, not hidden, clipped, or overlapping comments.

## Things To Avoid

- Large pure-white card or blank white center panel.
- Upscaled 1024-style output with extra padding.
- Tiny or unreadable comments.
- Generated small avatars left in the UI.
- Image-model captions, comments, or likes text.
- Decorations that look like buttons, compete with the three-dot menu, or create empty header space.
- Emoji fallback glyphs that render as boxes or unrelated symbols; replace them with readable simple symbols or omit them.
