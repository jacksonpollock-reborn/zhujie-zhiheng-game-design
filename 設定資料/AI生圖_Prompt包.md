# AI 生圖 Prompt 包 — 諸界之衡

> 給 ChatGPT (GPT-4o image)、Gemini (Imagen 3)、Midjourney 使用的可直接複製貼上的 prompt 集。
> 包含：整體美術指南 + 11 名角色立繪 + 9 個場景背景 + 7 個證物圖 + UI 元素。

---

## 0. 整體美術風格指南（必讀）

### 0.1 風格定位
- **主風格**：日式視覺小說 anime art style + 中華奇幻服飾元素
- **參考作品 mood board**：
  - 逆轉裁判（角色構圖、表情誇張化）
  - 鬼滅之刃（強光影對比）
  - 原神璃月（中華奇幻服裝）
  - 千與千尋（妖異半透明氛圍）
  - 罪惡裝備 Strive（鋒利線條）

### 0.2 主色調
| 陣營 | 主色 | 輔色 | 用途 |
|------|------|------|------|
| 律師（言衡陣營） | 深藍 #1a2855 | 銀 #c0c0c0 | 律師袍、辯方道具 |
| 神諭院 | 神諭金 #c9a227 | 紫 #4a1a6b | 神諭官袍、神諭法器 |
| 靈族 | 銀白 #e8eef4 | 淡青 #a3d9d9 | 靈族服飾、招魂法器 |
| 影族 | 暗紅 #5c0a18 | 黑紫 #1a0a2a | 影族暗市、刺客 |
| 矮人 | 銅褐 #8b4513 | 鐵灰 #4f4f4f | 鑄造、魔器 |
| 獸人 | 土黃 #a0805a | 暗綠 #3c5a3c | 警備隊、傭兵 |
| 龍裔 | 古金 #d4af37 | 翡翠綠 #138a3f | 貴族、神諭官 |
| 精靈 | 藤綠 #6b8e23 | 月白 #f0f8ff | 法官、學者 |

### 0.3 通用 keyword 模板（每個 prompt 都該有）

**通用前綴**（角色用）：
```
anime style, visual novel character portrait, cel-shaded with detailed shading, 
sharp clean lines, professional Japanese illustration, 
chest-up shot, 2:3 aspect ratio
```

**通用前綴**（場景用）：
```
anime visual novel background art, detailed environment illustration, 
cinematic composition, 16:9 aspect ratio, 
dramatic lighting, atmospheric perspective
```

**通用前綴**（證物用）：
```
anime style game item icon, detailed object illustration on neutral background, 
1:1 aspect ratio, soft drop shadow, 
slight metallic sheen for realism
```

### 0.4 一致性技巧（最關鍵！）

1. **單角色多表情**：用 GPT-4o image input 功能。先生成「平」表情成功後，把那張圖作為 reference 餵回去並要求「same character, same outfit, but [表情]」。
2. **跨角色風格一致**：所有角色的第一張圖完成後，挑一張最滿意的當「style reference」，後續所有 prompt 末尾加：`in the exact same art style and color palette as the reference image attached`。
3. **場景一致**：同一案的所有場景用同一個 lighting keyword（如「late afternoon golden hour」），維持時段感一致。
4. **AI 工具選擇建議**：
   - **GPT-4o**：人物表情最準（會聽你細節指示），多輪迭代強
   - **Gemini Imagen 3**：場景與光影最強，文字 prompt 理解力高
   - **Midjourney v6**：藝術感最強，適合 hero key art、宣傳圖
   - **建議組合**：人物用 GPT-4o，場景用 Gemini，宣傳圖用 Midjourney

---

## 1. 角色立繪 Prompts（11 名）

### 1.1 言衡（主角・人族律師・22 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, young Asian male in his early 20s, 
named Yan Heng, hero protagonist of fantasy courtroom drama,
neat black short hair with side-swept bangs, sharp dark brown eyes, 
clean-shaven, slim athletic build, average height,
wearing a deep navy blue Chinese-style lawyer robe with silver embroidery 
and a small silver Chinese character "衡" (meaning balance) emblem on the chest, 
white inner collar, wide sleeves, 
standing chest-up pose, slight 3/4 angle, looking forward,
gradient background from soft navy to white,
cel-shaded anime art style, detailed shading, sharp clean lines, 
professional Japanese visual novel illustration,
mood: idealistic young lawyer, serious but kind,
2:3 aspect ratio, high detail
```

**5 種表情變體**（在基礎 prompt 後追加）：
- **平 (calm)**：`+ calm neutral expression, slight forward lean, professional demeanor`
- **驚 (shocked)**：`+ shocked expression, wide eyes, slightly open mouth, eyebrows raised, leaning back, sweat drop on temple`
- **思考 (thinking)**：`+ thoughtful expression, right hand on chin, looking up and to the side, soft contemplative eyes`
- **充滿信心 (confident)**：`+ extremely confident expression, finger pointing forward, eyes blazing with determination, mouth open as if shouting "objection!", dramatic uplighting, cape-like robe billowing slightly`
- **崩潰 (broken)**：`+ broken despair expression, sweat dripping, eyes wide and trembling, mouth in shocked O shape, hands raised defensively, dark shadow over upper face`

**緣命絲使用版**（特殊立繪）：
```
[base prompt] + golden glowing eyes with subtle thread-like patterns visible, 
faint golden mystical aura around head, 
very slight wisps of golden light coming from his eyes
```

---

### 1.2 靈墟（助手・靈族・16 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, young teenage Asian girl, age 16,
named Ling Xu, spirit medium apprentice from a mystical mountain sect,
long silver-white hair flowing past waist with two small braids on the sides,
large pale silver-blue eyes (almost luminescent), pale ethereal complexion,
wearing white and pale blue traditional Chinese-style robe with cloud patterns,
silver bell tassels on the sleeves, blue silk sash, white socks with cloth shoes,
small silver hair ornaments shaped like crescent moons,
standing chest-up pose, gentle 3/4 angle,
soft pale blue gradient background with faint floating petals,
cel-shaded anime art style, ethereal and otherworldly mood,
2:3 aspect ratio, high detail, 
inspired by Genshin Impact's Liyue style and traditional Chinese spirit medium aesthetic
```

**5 種表情變體**：
- **天真 (innocent)**：`+ wide curious eyes, slightly tilted head, small open mouth`
- **吃貨 (foodie)**：`+ eyes sparkling at imaginary food, mouth slightly open with drool, hands held up in excitement`
- **嚴肅招魂 (serious channeling)**：`+ closed eyes, hands held in mudra position, faint silver aura, ethereal calm`
- **傷心 (sad)**：`+ tearful eyes, looking down, lower lip trembling`
- **生氣 (angry)**：`+ pouting cheeks, eyes narrowed, fists clenched, comically angry`

**招魂啟動版**：
```
[base prompt] + eyes glowing pure silver, surrounded by translucent ghostly silver flames, 
hair floating upward as if in zero gravity, 
faint figure of a ghost forming behind her, ethereal mystical atmosphere
```

---

### 1.3 霜訣明（對手檢察官・半精靈・26 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, handsome young man in his mid-20s, 
named Shuang Jue-ming, half-elf prosecutor (half human, half elf),
silver-blonde hair styled back elegantly, slightly pointed elven ears,
piercing ice-blue eyes, sharp aristocratic features, pale complexion,
wearing a high-collared deep crimson and black prosecutor's coat 
with silver chain accents and gold embroidery on the cuffs,
white cravat, black gloves, fitted slim cut,
standing chest-up pose, arrogant 3/4 angle, slight smirk,
cool blue-gray gradient background with subtle ice crystal patterns,
cel-shaded anime art style, dramatic chiaroscuro lighting,
mood: cold genius prodigy, looks down on opponents,
2:3 aspect ratio, inspired by Edgeworth from Ace Attorney crossed with Genshin's Diluc
```

**5 種表情變體**：
- **冷峻 (cold)**：`+ cold neutral expression, slight smirk, looking down at viewer`
- **嗤笑 (smirking)**：`+ confident smirk, raised eyebrow, head tilted with arrogance`
- **驚訝 (surprised)**：`+ shocked expression, eyes wide, smirk dropped, mouth slightly open`
- **憤怒 (angry)**：`+ angry intense expression, eyebrows knitted, teeth gritted, eyes blazing`
- **思考 (thinking)**：`+ contemplative expression, fingers steepled, looking aside`

**冰鏡使用版**：
```
[base prompt] + raised hand projecting a translucent blue ice mirror in front of him, 
faint blue magical runes around the mirror, 
cold mist swirling at his feet
```

---

### 1.4 雷狼（偵探・獸人狼裔・30 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, muscular wolf-beastman in his early 30s,
named Lei Lang, gruff police detective,
gray and white wolf features: pointed wolf ears on top of head, 
thick gray hair, bushy gray sideburns, sharp canines visible when smiling,
golden-yellow eyes with vertical pupils, weathered face with small scars,
strong build, broad shoulders,
wearing earthy brown and dark green police detective uniform: 
open trench coat over white shirt, leather belt with badge, 
fingerless leather gloves, claws on fingertips visible,
standing chest-up pose, hands on hips,
warm brown and tan gradient background with subtle wood grain texture,
cel-shaded anime art style, rough sketchy lines for ruggedness,
mood: gruff but loyal beastman detective, intimidating exterior,
2:3 aspect ratio, inspired by werewolves and Final Fantasy beastfolk
```

**3 種表情變體**：
- **兇 (intimidating)**：`+ snarling expression, teeth bared, ears flat, eyes narrowed`
- **笑 (laughing)**：`+ hearty grin, mouth wide showing teeth, eyes squinted with joy, ears perked up`
- **思考 (thinking)**：`+ scratching chin with claws, brow furrowed, ears slightly tilted`

---

### 1.5 沉律（法官・精靈族・近 200 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, ancient elder elf judge appearing wise and dignified,
named Chen Lü, judge of the Imperial Court, age nearly 200,
long silver-white hair past shoulders neatly tied back, long white beard reaching chest,
deeply pointed elven ears, piercing emerald green eyes with crow's feet,
weathered yet noble face, calm authoritative aura,
wearing deep purple judge's robe with gold and green embroidery, 
high formal collar, wide ceremonial sleeves, 
holding a wooden gavel in right hand,
standing chest-up pose, slight downward angle (looking down from bench),
muted purple and gold gradient background with subtle court motifs,
cel-shaded anime art style, traditional Asian court aesthetic,
mood: wise but easily flustered elder, dignified,
2:3 aspect ratio
```

**3 種表情**：
- **平 (calm)**：`+ calm composed expression, eyes half-closed in contemplation`
- **生氣拍桌 (angry banging)**：`+ furious expression, gavel raised mid-strike, eyes wide with anger, beard bristling`
- **滿意 (pleased)**：`+ slight pleased smile, beard slightly raised, eyes warm with approval`

---

### 1.6 雲息（師父・人族・50 歲・第一部結尾消失）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, distinguished middle-aged Asian man in his 50s,
named Yun Xi, master lawyer and mentor figure with hidden secrets,
salt-and-pepper hair neatly combed back, well-trimmed gray goatee,
deep wise dark eyes with subtle sadness, slight crow's feet,
calm composed face,
wearing an elegant dark gray and silver Chinese-style senior lawyer robe 
with intricate silver phoenix embroidery on the shoulders, 
high collar, holding a folded fan in one hand,
standing chest-up pose, calm and composed posture,
muted gray-blue gradient background with subtle ink-painting style mountains,
cel-shaded anime art style, ink-painting aesthetic accents,
mood: wise mentor with hidden burdens, calm but melancholic,
2:3 aspect ratio
```

**4 種表情**：
- **平 (calm)**：`+ calm wise expression, slight knowing smile`
- **嚴肅 (serious)**：`+ serious focused expression, brow slightly furrowed`
- **悲傷 (sad)**：`+ sad melancholic expression, eyes downcast, slight frown`
- **消失 (disappearing)**：`+ body becoming translucent, golden disintegration particles rising from his form, calm acceptance expression`

---

### 1.7 歿言子（主反派・前龍裔神諭官）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, sinister middle-aged man with dragon heritage,
named Mo Yan-zi, head of the secret cult "Return-to-Origin Faction",
long jet-black hair with crimson streaks, partially tied up with a gold dragon hairpin,
dragon-like vertical pupils, deep crimson irises, pale grayish skin,
small subtle dragon scale patterns on temples and neck,
sharp gaunt features, malevolent confident smirk,
wearing a black and gold high-priest robe with intricate dragon embroidery,
torn neck cloth showing scarred neck, 
golden ceremonial pendant shaped like a broken seal,
standing chest-up pose, dramatic 3/4 angle,
ominous deep red and gold gradient background with subtle dragon motifs,
cel-shaded anime art style, dark dramatic lighting,
mood: charismatic dangerous heretic, calmly menacing,
2:3 aspect ratio, inspired by Sephiroth and Ace Attorney's Manfred von Karma
```

**5 種表情**：
- **冷笑 (cold smile)**：`+ cold mocking smile, head slightly tilted`
- **狂笑 (manic laugh)**：`+ mad grin, head thrown back, eyes wide and crazed`
- **憤怒 (rage)**：`+ enraged expression, dragon eyes glowing crimson, mouth twisted in snarl`
- **平 (composed)**：`+ calm composed expression, slight knowing smile`
- **神諭附體 (oracle possession)**：`+ eyes glowing pure gold, mouth open speaking in tongues, golden runes floating around face, hair flowing upward`

---

### 1.8 赤絹（影族刺客・歸源派執行者）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, mysterious shadow-race young woman, age 24,
named Chi Juan ("crimson silk"), assassin of the Return-to-Origin Faction,
straight long black hair with crimson red highlights, hair partially covering left eye,
dark violet eyes (right eye visible), pale almost gray skin, sharp angular features,
intricate crimson lotus tattoo on the visible side of her neck extending up to cheek,
wearing tight-fitting black and dark crimson assassin's outfit: 
sleeveless qipao-style top with high collar, fingerless black gloves with red accent,
multiple short knives visible on belt, dark red silk scarf wrapped around lower face (can be worn or down),
standing chest-up pose, sultry 3/4 angle,
deep crimson and black gradient background with shadowy smoke,
cel-shaded anime art style, sharp dramatic lines,
mood: alluring deadly assassin, conflicted soul beneath cold exterior,
2:3 aspect ratio
```

**4 種表情**：
- **冷漠 (cold)**：`+ emotionless cold expression, half-lidded eyes`
- **嗤笑 (smirking)**：`+ playful dangerous smirk, head tilted, scarf pulled down`
- **痛苦 (in pain)**：`+ pained expression, scar/tattoo glowing red, gripping side, sweat on forehead`
- **倒戈 (defection)**：`+ tearful regretful expression, scarf removed, looking up with hope`

---

### 1.9 言瑤（主角母親・前守護者）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, gentle but strong woman in her early 40s,
named Yan Yao, Yan Heng's long-lost mother,
black long hair with subtle white streaks at temples (from prison stress),
warm dark brown eyes (same as Yan Heng), gentle yet sharp features,
slight resemblance to Yan Heng visible,
wearing a flowing white and pale gold elegant robe with silver thread embroidery 
representing the "Cross-Realm Codex" symbols,
delicate gold pendant around neck (heirloom),
standing chest-up pose, motherly warm presence,
soft warm gold gradient background with subtle thread-like light patterns,
cel-shaded anime art style,
mood: loving mother and former guardian, wise and resilient,
2:3 aspect ratio
```

**3 種表情**：
- **慈愛 (loving)**：`+ warm gentle smile, eyes soft with affection`
- **堅毅 (resolute)**：`+ determined expression, eyes blazing with conviction`
- **悲傷 (sad)**：`+ tearful smile, looking at viewer with longing`

**囚禁版（神諭院靈魂室內）**：
```
[base prompt] + thinner pale figure, faint translucent chains of golden light around wrists, 
eyes closed in meditation, faint golden aura sustaining her form
```

---

### 1.10 漆夜（靈族封印師青年・案 2-3 後加入）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, mysterious young man, age 23,
named Qi Ye, spirit-race seal master,
long dark blue-black hair tied in a low ponytail, side bangs falling over one eye,
deep purple eyes, pale complexion, slender androgynous features,
intricate sealing tattoos on arms (visible through sleeves),
wearing a dark blue and purple robe with traditional Chinese seal patterns,
ornate seal scroll tied to belt, prayer beads on wrist,
standing chest-up pose, calm mysterious aura,
deep purple gradient background with floating seal characters,
cel-shaded anime art style, mystical aesthetic,
mood: quiet but loyal seal master, scholar of forbidden arts,
2:3 aspect ratio
```

**3 種表情**：
- **平 (calm)**：`+ calm contemplative expression`
- **施術 (casting)**：`+ focused expression, eyes glowing purple, hands forming mudra, paper seals floating around`
- **驚訝 (surprised)**：`+ wide-eyed surprised look, slight gasp`

---

### 1.11 林晨（案 1-1 客戶・人族・25 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, ordinary young Asian man in his mid-20s,
named Lin Chen, magic shop apprentice and Yan Heng's childhood friend,
short messy brown hair, kind hazel eyes, average plain features,
slightly tired worn appearance, sweet honest demeanor,
wearing a simple dark green and brown apprentice apron over white shirt,
sleeves rolled up, leather wrist guards,
standing chest-up pose, slightly slumped from stress,
neutral warm beige gradient background,
cel-shaded anime art style, simple clean design,
mood: innocent victim of false accusation, kind everyman,
2:3 aspect ratio
```

**3 種表情**：
- **沮喪 (dejected)**：`+ slumped posture, sad eyes downcast, hands clasped`
- **感激 (grateful)**：`+ tearful grateful smile, eyes shining`
- **驚訝 (surprised)**：`+ wide eyes, mouth open, hands raised slightly`

---

### 1.12 阿諾（案 1-1 真兇・人族・24 歲）

**基礎立繪 prompt**：
```
Anime visual novel character portrait, deceptively friendly young man, age 24,
named A Nuo, secretly an unlicensed transformation magic user,
neat blond medium-length hair, bright blue eyes (initially friendly),
average slim build, ordinary handsome face that hides darker emotions,
wearing same dark green and brown apprentice apron as Lin Chen but neater,
clean white shirt, polished demeanor,
standing chest-up pose, fake friendly stance,
neutral warm gradient background that becomes darker red in later expressions,
cel-shaded anime art style,
mood: jealousy hidden beneath friendly mask,
2:3 aspect ratio
```

**5 種表情（最重要 — 真兇變化曲線）**：
- **友善 (friendly)**：`+ wide warm smile, friendly eyes, hand raised in greeting`
- **緊張 (nervous)**：`+ forced smile, sweat drop, eyes shifting nervously`
- **崩潰 (breaking)**：`+ smile cracking, eyes wide with panic, sweat heavy, voice cracking`
- **猙獰 (sinister)**:` + twisted angry expression, mouth in snarl, eyes wide and crazed, dark shadow over face, background turns dark red`
- **絕望認罪 (despair confession)**：`+ tears running down, hands clutching head, mouth open in anguished cry`

**變形術中版**：
```
[base prompt] + body shimmering with crimson magical light, 
features morphing/blurring, transformation in progress, 
red runes floating around him
```

---

## 2. 場景背景 Prompts（案 1-1 的 9 個場景）

### 2.1 雲息律所大廳

```
Anime visual novel background art, interior of a traditional Chinese-style lawyer's office,
named "Yun Xi Law Firm", warm afternoon sunlight streaming through paper screen windows,
wooden floor with subtle Chinese pattern, dark wooden bookshelves filled with magical scrolls and law books,
central low table with tea set, two empty cushions, 
calligraphy scrolls on walls including one large scroll reading "衡律" (balance law),
single empty large chair at the back (representing absent master),
warm earth-tone color palette: brown, beige, soft gold,
detailed environment illustration, cinematic composition,
no characters in scene, 16:9 aspect ratio,
mood: traditional, warm, slightly empty,
inspired by Genshin Impact Liyue interiors
```

### 2.2 拘留所會見室

```
Anime visual novel background art, prison meeting room interior,
cold gray stone walls with iron bars dividing the room in half,
single wooden table and two chairs (one on each side of bars),
small high window with iron grate, single dim lantern hanging from ceiling,
shadows cast across floor in stark patterns,
muted gray and pale yellow color palette,
detailed environment illustration, dramatic chiaroscuro lighting,
no characters in scene, 16:9 aspect ratio,
mood: oppressive, cold, hopeless,
cel-shaded anime art style
```

### 2.3 鏗鳴齋外觀（魔器舖）

```
Anime visual novel background art, fantasy magic-item shop exterior,
named "Keng Ming Zhai", traditional Chinese street in the capital city,
two-story wooden building with brass gear decorations and dwarven craftsman aesthetics,
ornate signboard with brass letters reading "鏗鳴齋" (Keng Ming Zhai),
glowing magical orbs hanging by entrance, 
display window showing magical timepieces and trinkets,
cobblestone street, neighboring shops in soft focus,
late afternoon golden hour lighting,
warm brown, brass, and amber color palette,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: mysterious magical commerce,
inspired by Spirited Away streets and Genshin Liyue
```

### 2.4 鏗鳴齋內倉（含保險櫃）

```
Anime visual novel background art, interior storage room of magic-item shop,
walls lined with wooden shelves displaying magical items: glowing orbs, ornate clocks, 
magical weapons, scrolls in tubes,
center of room: large ornate brass safe with intricate dwarven engravings 
and a magical lock (faint golden runes around the keyhole when active),
soft warm lantern light, cluttered but organized,
brown, brass, and faint gold color palette,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: treasure room atmosphere,
cel-shaded anime art style
```

### 2.5 鏗鳴齋後巷

```
Anime visual novel background art, narrow back alley behind a magic shop,
cobblestone path between two stone walls, slightly darker lighting,
overturned trash bin with debris scattered, 
back door of the shop visible at far end, 
single oil lamp on wall providing dim lighting,
moss growing on stone, slight mist in the air,
muted gray-brown color palette with golden lantern accent,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: secretive, slightly ominous,
cel-shaded anime art style
```

### 2.6 警備隊辦公室

```
Anime visual novel background art, fantasy police department office interior,
cluttered wooden desk piled with case files and scrolls, 
tin cup of cold tea, half-eaten meat bun on desk,
wall behind covered with wanted posters and city map with pins,
weapon rack with police staffs in corner, large window showing city outside,
warm afternoon light through window, slightly dusty atmosphere,
warm brown, beige, and dark green color palette,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: hardworking detective's lair,
cel-shaded anime art style
```

### 2.7 阿諾住處（外觀）

```
Anime visual novel background art, modest three-story wooden apartment building exterior,
in a working-class district of a fantasy capital city,
narrow stairs leading up the side, lanterns at each floor entrance,
laundry hanging on poles, neighboring buildings visible,
late afternoon soft light, slightly shabby but lived-in atmosphere,
warm brown and weathered wood color palette,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: ordinary commoner residence,
cel-shaded anime art style
```

### 2.8 律廷主庭（court room）

```
Anime visual novel background art, grand fantasy courtroom interior,
high vaulted ceiling with elven architectural style: pointed arches, intricate filigree,
elevated central judge's bench (carved dark wood with gold inlay),
podium for defense (left, navy blue) and prosecution (right, crimson),
witness stand in front of judge's bench, 
stained glass windows depicting scales of justice and dragons, 
massive doors at the back, audience benches on both sides,
warm dramatic spotlighting from above, hushed atmosphere,
dark wood, gold accents, deep navy and crimson color palette,
detailed environment illustration, 16:9 aspect ratio,
cinematic perspective from defense podium angle,
no characters, mood: solemn, dramatic, where truths emerge,
inspired by Ace Attorney courtroom + cathedral architecture
```

### 2.9 律廷外景（臺階上）

```
Anime visual novel background art, exterior of grand fantasy court building,
white marble facade with grand columns, wide stone staircase leading up,
massive bronze cauldron at the entrance with character "律" (law) embossed,
two dragon statues flanking the entrance,
late afternoon golden hour, soft city skyline visible in background,
warm white, gold, and bronze color palette,
detailed environment illustration, 16:9 aspect ratio,
no characters, mood: imposing yet hopeful, justice prevails,
cel-shaded anime art style with cinematic atmosphere
```

---

## 3. 證物圖 Prompts（案 1-1 的 7 個證物）

### 3.1 司辰魔懷錶

```
Anime style game item icon, ornate dwarven-crafted magical pocket watch,
silver casing with gold trim and intricate gear engravings,
clock face has glowing magical crystal at center, golden hour and minute hands,
small Chinese character "鏗" (forge) engraved on back,
silver chain attached, slightly worn antique appearance,
floating on neutral cream background with subtle magical aura,
soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style,
mood: precious heirloom-quality artifact
```

### 3.2 警方鑑識報告（紙本）

```
Anime style game item icon, official police forensic report document,
parchment-style paper with fantasy-ornate header reading "警備隊鑑識報告",
red ink stamp at top, handwritten notes describing "紅色魔紋" (red magical pattern),
small detailed sketch of magical residue pattern on side,
slightly aged paper texture, official seal at bottom,
floating on neutral background, soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style
```

### 3.3 保險櫃照片（含金色魔紋）

```
Anime style game item icon, photograph-style image of an ornate magical safe lock,
detailed brass keyhole with faint golden magical runes glowing around it,
photograph has soft white border and slight aged tint,
focus on the golden runes around the lock,
floating on neutral background, soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style,
mood: forensic evidence photo
```

### 3.4 阿諾的證詞紀錄

```
Anime style game item icon, official testimony transcript document,
parchment paper with fantasy-style header, neatly handwritten testimony,
witness signature at bottom reading "阿諾",
red wax seal at corner, official court formatting,
floating on neutral background, soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style
```

### 3.5 鏗匠的工坊地圖

```
Anime style game item icon, hand-drawn map of a magic shop layout,
parchment with ink-drawn floor plan showing: front door, main hall, 
inner storage room (內倉), back alley exit, and safe location,
labels in Chinese characters, small compass rose in corner,
slightly rolled at edges, hand-drawn organic style,
floating on neutral background, soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style
```

### 3.6 變形術籙殘片

```
Anime style game item icon, half-burned magical paper talisman fragment,
crimson-red ink writing on yellow ritual paper, 
visible Chinese characters "變" and "形" (transformation),
edges singed and burnt black, faint red magical glow still emanating,
small ash particles around it,
floating on neutral background, soft drop shadow, 1:1 aspect ratio,
detailed object illustration, cel-shaded anime style,
mood: forbidden magic evidence
```

### 3.7 緣命絲讀數視覺化（UI 圖）

```
Anime style game UI element, visualization of "Fate Threads" ability reading,
two stylized human silhouettes facing each other, 
thick crimson red glowing thread connecting their chests,
the thread pulses and emits faint red sparks,
abstract dark background with faint golden particles,
soft drop shadow, 1:1 aspect ratio,
detailed UI illustration, cel-shaded anime style,
mood: mystical ability revelation
```

---

## 4. UI 元素 Prompts

### 4.1 遊戲標題 logo

```
Fantasy game title logo design, Chinese characters "諸界之衡" 
in elegant brush-stroke calligraphy style with metallic silver and gold gradient,
each character with subtle magical effects (faint glowing edges),
small subtitle in elegant English: "Balance of Realms",
deep navy and gold color scheme,
ornate decorative border with seven small symbols representing the seven races,
transparent background, professional game logo design,
inspired by Genshin Impact and Ace Attorney logo aesthetics
```

### 4.2 「異議！」效果圖

```
Anime style game effect illustration, dynamic action text "異議！" (Objection!),
large bold Chinese calligraphy with explosive energy, 
electric blue and white color scheme, lightning bolts radiating outward,
slight 3D perspective tilted dramatically, 
transparent background for overlay use,
manga-style impact effect, cel-shaded with sharp edges,
inspired by Ace Attorney's iconic objection screen
```

### 4.3 「揭穿！」效果圖

```
Anime style game effect illustration, dynamic action text "揭穿！" (Expose!),
large bold Chinese calligraphy with golden magical aura, 
threads of golden light radiating outward (representing 緣命絲),
slight 3D perspective, electric crackling at edges,
transparent background,
mystical impact effect, cel-shaded
```

### 4.4 緣命絲動畫（粒子效果參考圖）

```
Game VFX reference illustration, magical "Fate Threads" effect,
multiple glowing colored threads (gold for love, red for hate, black for blood debt, 
silver for master-disciple) floating in air,
threads have subtle particle effects and pulsing glow,
swirling around an unseen central character,
dark background to highlight thread colors,
high detail VFX reference art, 16:9 aspect ratio
```

### 4.5 對話框 UI

```
Game UI design element, fantasy visual novel dialogue box,
elegant Chinese-style frame with brass corners and dark navy interior,
subtle silver phoenix decorative pattern on border,
character name plate on top-left in elegant calligraphy style,
small triangular continue indicator in bottom-right,
semi-transparent dark navy background for text,
clean modern game UI design with traditional Asian aesthetics,
transparent background showing only the UI element
```

---

## 5. 後續案件的場景需求清單（待你完成 1-1 的圖後再生）

### 案 1-2 歌劇院的影子
- 律都歌劇院外觀（壯麗）
- 後台化妝間（兇案現場）
- 歌姬寓所（雅緻）
- 靈族山門（仙境）
- 歌劇院主舞台

### 案 1-3 龍裔的證詞
- 神諭院古井（兇案現場）
- 神諭院主殿
- 龍裔燁府（豪華）
- 影族貧民窟

### 案 1-4 夏祭夜的煙火
- 煙火工坊頂樓（兇案現場）
- 律都夏祭夜會場（華麗）
- 煙火工坊內部

### 案 1-5 神諭官之死
- 翊辰私邸書房
- 神諭院禁區
- 律都古籍館

---

## 6. 角色一致性檢查清單

每個角色生成完一組圖後，自查：
- [ ] 髮色／髮型是否一致
- [ ] 眼睛顏色是否一致
- [ ] 服裝紋路與配色是否一致
- [ ] 角色比例是否一致（同框時不會大小錯亂）
- [ ] 表情變化看起來是同一個人

若不一致，使用 GPT-4o image input 把已通過的圖當參考重新生成。

---

## 7. 推薦的生圖工作流（最節省時間）

1. **第一輪**：用 Midjourney 為每個主要角色（言衡、靈墟、霜訣明）各生 1 張 hero shot，確定整體美術風格
2. **第二輪**：用 GPT-4o image，把 Midjourney 的 hero shot 當 reference，生角色的 5 種表情變體
3. **第三輪**：用 Gemini Imagen 3 生所有場景（描述場景 + 加「same art style as the character references」）
4. **第四輪**：用 GPT-4o 生證物圖（一致性要求較低，可獨立生）
5. **第五輪**：UI 元素 — 可手繪或用 Photoshop 加工 AI 圖

預估：完整案 1-1 的全部圖像生成（11 角色 × 表情 + 9 場景 + 7 證物 + UI），含調整時間約 8–15 小時。

---

## 8. 法律與授權提醒

- ChatGPT/Gemini/Midjourney 生成的圖像版權歸屬請查最新平台 ToS
- 商業遊戲使用建議：Midjourney Pro 訂閱有商業使用授權；GPT-4o image 商業使用須查 OpenAI 最新政策
- 為避免風險，可考慮以 AI 生圖為「概念稿」，再請專業繪師依此重繪正式版

---

> Prompt 包完成。開始生圖時建議先做言衡基礎立繪 + 律廷主庭場景 — 這兩張是最常出現、影響最大的素材。
