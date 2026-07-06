# Isekai Now Avatar Library

## Asset Paths

- Character reference folder: `assets/Avatars`
- Fixed isekai avatar folder: `assets/Avatars`

## Avatar Policy

Use fixed isekai character avatars whenever composing UI locally or when instructing image generation to reuse avatar assets. Use the bundled `assets/Avatars` files for poster avatars, comment avatars, and identity references.

For final social-feed images, do not rely on the image model to paint small comment avatars if local composition is possible. Generate or obtain the main illustration separately, then paste the exact avatar PNGs from `assets/Avatars` into the UI as circular crops. This is mandatory for comment avatars when the user cares about character identity stability.

When using a generated draft or a user-provided satisfied example as layout reference, replace every small UI头像 in that image with the matching bundled avatar crop. Keep the layout, theme, and typography direction if useful, but do not keep generated or mismatched small portrait faces.

Treat the isekai role below as the avatar-library default identity. Use it for profile flavor, captions, quick character lookup, and UI avatar selection. In the main illustration, preserve identity but adapt clothing, props, and job details to the user's current scene.

## Isekai Roles And Avatar Files

### Muse

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Honoka | 穗乃果 | 冒险家协会会长，热血开拓队长 | `Honoka_Avatar_Isekai.png` |
| Kotori | 南小鸟 | 治愈师导师，花园裁缝与结界修补师 | `Kotori_Avatar_Isekai.png` |
| Umi | 海未 | 冷库剑士，王都礼法与护卫训练官 | `Umi_Avatar_Isekai.png` |
| Eli | 绘里 | 骑士团团长，王宫仪仗与冰晶剑术教官 | `Eli_Avatar_Isekai.png` |
| Nozomi | 希 | 占星魔法师，命运牌与星象祭司 | `Nozomi_Avatar_Isekai.png` |
| Rin | 凛 | 快递员，猫步疾行的风信使 | `Rin_Avatar_Isekai.png` |
| Hanayo | 花阳 | 米饭店老板，圣米料理与粮仓守护者 | `Hanayo_Avatar_Isekai.png` |
| Nico | 妮可 | 盗贼偶像，暗巷情报商与舞台小恶魔 | `Nico_Avatar_Isekai.png` |
| Maki | 真姬 | 火法师，贵族炼金医师与炎术研究者 | `Maki_Avatar_Isekai.png` |

### Aqours

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Chika | 千歌 | 橘子旅店看板娘，阳光冒险发起人 | `Chika_Avatar_Isekai.png` |
| Riko | 梨子 | 宫廷乐师，水晶钢琴与结界旋律师 | `Riko_Avatar_Isekai.png` |
| Kanan | 果南 | 海渊巡护者，潜水向导与海兽调停人 | `Kanan_Avatar_Isekai.png` |
| Dia | 黛雅 | 黑蔷薇贵族骑士，礼仪监察官 | `Dia_Avatar_Isekai.png` |
| You | 曜 | 飞艇/船舶驾驶员，王都港口航路员 | `You_Avatar_Isekai.png` |
| Yoshiko | 善子 | 堕天使暗术师，禁书与诅咒道具收藏家 | `Yoshiko_Avatar_Isekai.png` |
| Hanamaru | 花丸 | 修道院图书管理员，古书面包店见习贤者 | `Hanamaru_Avatar_Isekai.png` |
| Mari | 鞠莉 | 宝石商会大小姐，闪耀赌场与宴会赞助人 | `Mari_Avatar_Isekai.png` |
| Ruby | 露比 | 甜点裁缝，红宝石玩偶与礼服工坊学徒 | `Ruby_Avatar_Isekai.png` |

### Nijigasaki

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Ayumu | 步梦 | 蔷薇守护者，温柔花园骑士与护符少女 | `Ayumu_Avatar_Isekai.png` |
| Ai | 爱 | 街头冒险家，庆典主持人与幸运传令员 | `Ai_Avatar_Isekai.png` |
| Kanata | 彼方 | 梦境旅馆老板，睡眠魔法与枕头结界师 | `Kanata_Avatar_Isekai.png` |
| Shizuku | 雫 | 剧场魔法演员，故事幻境与舞台召唤师 | `Shizuku_Avatar_Isekai.png` |
| Karin | 果林 | 夜会舞者，迷宫向导与魅惑侦察员 | `Karin_Avatar_Isekai.png` |
| Kasumi | 霞 | 可爱小恶作剧炼金商，魅力药水推销员 | `Kasumi_Avatar_Isekai.png` |
| Shioriko | 栞子 | 圣典审查官，神殿书记与适性判定员 | `Shioriko_Avatar_Isekai.png` |
| Setsuna | 雪菜 | 炎之勇者，正义圣剑与热血魔法战士 | `Setsuna_Avatar_Isekai.png` |
| Emma | 艾玛 | 高原牧歌治愈师，森林厨房与羊毛护符师 | `Emma_Avatar_Isekai.png` |
| Rina | 璃奈 | 魔导机关工程师，表情板与自动人偶调试员 | `Rina_Avatar_Isekai.png` |
| Mia | 米娅 | 天才吟游作曲家，魔音谱面与水晶录音师 | `Mia_Avatar_Isekai.png` |
| Lanzhu | 兰珠 | 异国歌姬公主，宝石舞台与华丽召唤师 | `Lanzhu_Avatar_Isekai.png` |

### Liella

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Kanon | 香音 | 旅店歌者，黄昏广场的吟游诗人 | `Kanon_Avatar_Isekai.png` |
| Keke | 可可 | 魔法偶像周边商，星杖宣传员 | `Keke_Avatar_Isekai.png` |
| Chisato | 千砂都 | 圆环武斗舞者，团子工坊护卫 | `Chisato_Avatar_Isekai.png` |
| Sumire | 堇 | 银河占卜艺人，贵族舞台魔女 | `Sumire_Avatar_Isekai.png` |
| Ren | 恋 | 魔法学院学生会长，古典礼法书记官 | `Ren_Avatar_Isekai.png` |
| Kinako | きな子 | 乡村药草见习，羊驼牧场采集员 | `Kinako_Avatar_Isekai.png` |
| Mei | 米女芽衣 | 兽耳暗卫见习，害羞偶像护卫 | `Mei_Avatar_Isekai.png` |
| Shiki | 四季 | 炼金术学生，魔法实验室研究员 | `Shiki_Avatar_Isekai.png` |
| Natsumi | 夏美 | 魔法影像博主，商会推广与流量炼金师 | `Natsumi_Avatar_Isekai.png` |
| Margarete | 薇恩 | 王立歌剧院竞争者，冰晶声乐贵族 | `Margarete_Avatar_Isekai.png` |
| Tomari | 冬毬 | 商会会计，冷静效率派契约管理员 | `Tomari_Avatar_Isekai.png` |

### Hasunosora

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Kaho | 花帆 | 新芽见习冒险者，阳光花田传令员 | `Kaho_Avatar_Isekai.png` |
| Kozue | 梢 | 白百合圣女，高阶礼仪与治愈导师 | `Kozue_Avatar_Isekai.png` |
| Sayaka | 沙耶香 | 冰湖剑舞者，纪律严明的护卫学徒 | `Sayaka_Avatar_Isekai.png` |
| Tsuzuri | 缀理 | 梦游诗画师，奇想魔法记录者 | `Tsuzuri_Avatar_Isekai.png` |
| Rurino | 瑠璃乃 | 水晶通讯员，魔法直播与情报传送手 | `Rurino_Avatar_Isekai.png` |
| Megumi | 慈 | 魅力前辈主播，舞台经营与人气策划师 | `Megumi_Avatar_Isekai.png` |
| Ginko | 吟子 | 神社剑巫，传统仪式与守护铃使 | `Ginko_Avatar_Isekai.png` |
| Kosuzu | 小铃 | 铃铛见习药师，活泼采集与补给员 | `Kosuzu_Avatar_Isekai.png` |
| Hime | 姬芽 | 流行甜心魔法师，心形饰品与潮流咒语师 | `Hime_Avatar_Isekai.png` |

### Extra

| Character | Chinese | Isekai role / identity | Avatar file |
|---|---|---|---|
| Izumi | 泉 | 冷静观察者，王都记录员与资料整理师 | `Izumi_Avatar_Isekai.png` |
| Ceras | Ceras | 异国秘术贵族，古代契约与星尘仪式师 | `Ceras_Avatar_Isekai.png` |

## Usage Rules

- Use the fixed avatar for the post author when available.
- Use fixed avatars for comment authors when generating or composing a full social-feed UI. Prefer direct local placement over prompt-only avatar descriptions.
- Use the role table to quickly infer avatar props, title flavor, and default isekai identity.
- Do not force the avatar-library role into the main image when it conflicts with the user's requested scene. Example: if `曜` is posting about an airship license, use airship pilot details even if another scene would use sailor details.
- If generating a new avatar, match the existing library: square portrait, bust-up framing, light novel anime style, fantasy outfit, no modern school uniform, circular-crop friendly.
- Do not overwrite fixed avatars unless the user explicitly asks for a new version.

