# Awesome Seedream API 🖼️ — Prompts, Variants & One-Call Image Generation

> The most complete open guide to **ByteDance Seedream — the state-of-the-art AI image model (Seedream 4 · 4.5 · 5.0)** — a community prompt library and a single API to run every variant.

<p align="center">
  <a href="https://wavespeed.ai/seedream-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><img src="https://img.shields.io/badge/▶_Run_Seedream_5-Get_API_Key-00E5FF?style=for-the-badge&labelColor=0B0B0F" alt="Run Seedream 5"></a>
  <a href="https://wavespeed.ai/seedream-4-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><img src="https://img.shields.io/badge/Seedream_4.5-Try_Now-7C3AED?style=for-the-badge&labelColor=0B0B0F" alt="Seedream 4.5"></a>
</p>

<p align="center">
  <b>🌊 Powered by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api">WaveSpeedAI</a> — serverless Seedream API, pay-as-you-go, zero cold starts.</b><br>
  <a href="https://wavespeed.ai/seedream-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><b>→ Get a Seedream 5 API key</b></a> &nbsp;·&nbsp; <a href="https://wavespeed.ai/seedream-4-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><b>→ Try Seedream 4.5</b></a>
</p>

<p align="center">
  🖥️ <b>No code?</b> Generate in your browser (no setup, free to start) → <a href="https://wavespeed.ai/image-generator?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><b>WaveSpeedAI Image Generator</b></a>
</p>

---

> **Generate right now**
> ```bash
> npm i -g @wavespeed/cli && wavespeed login
> wavespeed run bytedance/seedream-v5.0-pro -p "your prompt"
> ```
> No GPU, no cold start — the same endpoint powers every prompt below.

---

## 📖 Contents
1. [What is Seedream?](#what-is-seedream)
2. [Run it via API](#run-it-via-api)
3. [Model Variants](#model-variants)
4. [Prompt Library](#prompt-library) — 12 community prompts
5. [Related Model Guides](#related-model-guides)
6. [Contributing](#contributing)

---

## What is Seedream?

**Seedream** is ByteDance's frontier text-to-image and image-editing model, known for photoreal detail, accurate text rendering, and strong instruction-following edits. WaveSpeed serves **Seedream 5.0** (pro / lite), 4.5, and 4 — text-to-image, edit, sequential, and layer-decomposition.

---

## Run it via API

One endpoint, submit + poll. Swap the model path for any variant below.

```bash
curl -s -X POST "https://api.wavespeed.ai/api/v3/bytedance/seedream-v5.0-pro" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY" -H "Content-Type: application/json" \
  -d '{"prompt": "A photoreal portrait of an astronaut, dramatic rim light, ultra-detailed", "aspect_ratio": "1:1"}'
# → {"data": {"id": "<prediction_id>"}}

curl -s "https://api.wavespeed.ai/api/v3/predictions/<prediction_id>/result" \
  -H "Authorization: Bearer $WAVESPEED_API_KEY"
# → status: completed → outputs: ["<url>"]
```

**[→ Get your Seedream 5 API key](https://wavespeed.ai/seedream-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api)** · pay-as-you-go, live pricing on each model page.

---

## Model Variants

All variants open in-browser with a copy-paste API snippet.

### Seedream 5.0 — flagship &nbsp;[▶ API](https://wavespeed.ai/seedream-5-api)
[v5.0-pro](https://wavespeed.ai/models/bytedance/seedream-v5.0-pro) · [v5.0-pro edit](https://wavespeed.ai/models/bytedance/seedream-v5.0-pro/edit) · [v5.0-lite](https://wavespeed.ai/models/bytedance/seedream-v5.0-lite) · [layer-decomposition](https://wavespeed.ai/models/bytedance/seedream-v5.0-pro/layer-decomposition)

### Seedream 4 / 4.5 &nbsp;[▶ API](https://wavespeed.ai/seedream-4-5-api)
[v4.5](https://wavespeed.ai/models/bytedance/seedream-v4.5) · [v4.5 edit](https://wavespeed.ai/models/bytedance/seedream-v4.5/edit) · [v4](https://wavespeed.ai/models/bytedance/seedream-v4) · [v4 edit](https://wavespeed.ai/models/bytedance/seedream-v4/edit)

> Full catalog: **[wavespeed.ai/seedream-5-api](https://wavespeed.ai/seedream-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api)**

---

## Prompt Library

12 prompts curated from the Seedream creator community. Credit stays with the original author. Fill in `{...}` placeholders.

### 1. 票据风格 (ticket)封面
*community prompt*

```
帮我根据下面的设计风格要求和内容要求，生成一张中文的信息图片： 
设计风格要求： 
运用3-4种不同字号创造层次感，关键词使用最大字号 主标题字号需要比副标题和介绍大三倍以上，采用网格排版，类似高级杂志 文字与装饰元素间保持和谐的比例关系 确保视觉流向清晰，引导读者目光移动 
数字极简票券风设计风格 
**黑白对比主导：**高度对比的黑白配色方案，形成强烈视觉冲击 
**票券化布局：**类似登机牌、门票或电子凭证的结构设计 
**几何分区明确：**画面被精确划分为信息区块，井然有序 
**留白艺术运用：**大量有效留白提升整体通透感和优雅度 
**东西方美学融合：**结合中文传统排版与西方现代设计语言 
**工业设计感：**注册商标符号、条形码等商业元素的精致运用 
**数字界面映射：**模拟电子屏幕或应用界面的信息呈现方式 文字排版风格 
**中英混排对比：**中英文字体混合使用，创造文化融合感 
**尺寸层级分明：**主标题大号处理，副文本精致小巧 
**多向排列组合：**包含横排、竖排、斜排等多方向文字布局 
**间距精确控制：**字符间距和行距经过精心计算，保持呼吸感 
**符号化装饰：**括号、下划线、箭头融入文字设计 
**衬线与非衬线混搭：**不同字体家族交替使用，增强层次感 
**时间信息格式化：**日期标注采用统一格式，搭配方向指示符 视觉元素风格 
**功能性指示符：**各类箭头、星号作为视觉引导和强调 UI元素借鉴："CHECK IN"、"@"等数字界面元素的平面化应用 
**边框与分割线：**简洁线条用于区隔不同信息区域 
**简约图形符号：**最小化的设计符号传达核心信息 
**手写风点缀：**如"Romantic"的手写体为机械排版增添人文温度 
**方向性视觉流动：**通过元素排布创造从左到右、从上到下的阅读节奏 **负空间利用：**将空白区域视为积极设计元素的一部分 
文本信息：
```

### 2. 手写风格学习笔记封面
*community prompt*

```
在下面内容基础上制作逼真的手写风格学习笔记封面。使用学生手写字体，背景为带有纸张纹理的A4横线笔记本纸。关键术语用黄色荧光笔高亮标记，页面右上角写上日期 "2026年6月13日" 并用红色手绘圆圈圈出。在边缘添加手绘箭头、简笔画涂鸦来辅助解释概念。整体风格自然、略带随意的学习氛围。 
比例：16:9
内容为：
```

### 3. 矢量插画封面
*community prompt*

```
核心指令： 
生成一张横向全景式的扁平化矢量插画封面。画面中必须包含清晰的中文文字标题。 
插画风格： 
采用扁平化矢量插画（Flat Vector Illustration）。画面中所有元素（包括文字外框）必须包含清晰、统一粗细的黑色单线轮廓描边（Monoline/Uniform Stroke）。线条末端圆润，避免尖锐棱角，类似填色书线稿风格。色彩填涂需简洁，仅使用极少量扁平阴影，严禁使用任何渐变色或3D渲染效果。 构图与空间： 横向全景式构图（Panoramic），插画部分主要占据版面顶部 1/3 的空间。
采用平视或稍微俯视的 2.5D 视角。通过清晰的图层前后遮挡来表现纵深感，所有远近图层的清晰度一致，不要使用大气透视模糊。 
几何化内容： 将所有物体进行几何化简化，追求“玩具模型”般的可爱感。例如：树木简化为棒棒糖或三角形，建筑简化为简单的矩形块面组合，窗户简化为整齐的小方格网格。 
装饰与配色： 在空白处添加装饰性的几何元素平衡视觉密度，如放射状线条（代表阳光/能量）、药丸状云朵、小圆点和星星。背景使用米色/奶油色纸张纹理。
强调色采用复古柔和色调：珊瑚红、薄荷绿、芥末黄、赭石色和岩石蓝。 
字体排版与内容（关键修改）： 全局语言要求： 画面中显示的所有文本都必须是中文汉字。 
主标题： 位于画面显著位置，巨大的、加粗的中文复古衬线体风格（类似老报纸宋体），体现权威感与优雅感，带有黑色描边。 
副标题： 位于一个矩形色块容器内，使用清晰的中文黑体（无衬线风格）。 
请在下方填写需要生成的中文内容：
```

### 4. 强叙事自媒体封面
*community prompt*

```
围绕任意主题内容生成一张强叙事自媒体封面：画面必须由一个强烈而统一的主色场统摄，主色从主题自身的时代、材质、行业、地域和情绪里提取，占据绝大部分背景，像一层有厚度的旧纸、墙面、漆面或印刷底版；标题使用与主色形成高反差的旧白、灰白、浅金属色或主题派生的明亮浅色，带微微发黄、磨损、掉粉和纸浆颗粒感；最深的结构只用接近墨黑、焦褐或主题里的深暗色压住阴影、插画剪影和空间裂层。整体不要多彩，应该像同一种颜色系统里长出的三四个明暗角色：大底负责情绪，浅字负责冲击，深色负责重量，少量强调只在视线最该停留的地方出现。标题文字是画面的主结构，字体必须有碑刻、拓印、木刻、旧报刊大标题和民国招贴混合出的厚重感，笔画宽大、横竖有力，转折处带刀削般的硬边和不规则缺口，局部有宋体式骨架或雕版字的锋利收笔，但不能变成现代黑体、圆体、电脑综艺字或干净书法字。几个关键汉字要巨大到像占据空间的石块和墙体，字面有磨蚀、断墨、套印不齐、纤维刮痕和粗粝颗粒，次要文字围绕它们形成疏密节奏，而不是平均排满。插画配图跟随主题自然发生，不预设固定题材，只从主题自身的冲突、身份、时代、材质和精神里生出带叙事感的形象，让它们依附、潜入、遮蔽或浮现在巨字周围，像被同一张底版一起印出来，而不是后贴上去的说明图。信息不要说透，保留沉默、遮挡和未完全显影的部分；第一眼必须是巨大旧字和单一强色的压迫，第二眼才读到主题插画在文字内部和周围生长出的故事、压力和余味。

主题：
[替换为你的内容]

注意：文字逻辑重点，所有文字也要能快速读取，文字要大
比例16:9
```

### 5. 中式天庭+东方神话+巨型建筑
*community prompt*

```
东方超现实神殿美学，云海之上的东方神话世界。
画面主体为[场景主体]，空间中包含[建筑结构]，整体呈现巨构中式天宫/不可能建筑/神圣宫阙的感觉。
场景被[环境元素]包围，远处的[远景目标]被[遮挡方式]部分遮挡，只显露轮廓或局部，强化神秘感与想象空间。
画面中有[人物数量与身份]，他们[人物动作]，人物比例很小，用来强调建筑与世界尺度的巨大。天空或空间中出现[异象元素]，进一步强化东方神话与史诗感。
整体光线为[光线类型]，主色调为[色彩方案]。
构图强调[镜头构图]，气质应当[情绪关键词]。
cinematic oriental fantasy, celestial palace, monumental architecture, cloud sea, divine light, impossible architecture, epic scale, surreal sacred atmosphere, ultra detailed.
```

### 6. 手绘风格黑白插画
*community prompt*

```
手绘风格黑白插画，小红书封面设计，极简风，白色背景，黑色线稿人物，一个年轻男性坐在桌前认真写字，桌上有笔记本、马克杯、闹钟和书本，整体是线条感强的涂鸦风，类似手账插画风格
画面包含大标题排版：“{{标题}}”，字体为手写粗体，带有随意感 局部用黄色作为强调色（下划线、圈重点、星星点缀等）
画面左侧有便利贴，上面写文字：
{{便利贴文字，可以1、2、3分条}}
右侧有灯泡图标+“每天2小时认真尝试”
底部有一句黑底白字的文案条 整体风格： 知识博主风 、真实记录感、轻松但克制、不商业化
风格参考：手绘涂鸦、黑白线稿+少量高亮色 构图干净，信息分区清晰，适合内容封面传播
底部标签：{{底部标签，可用 | 分割}}
高分辨率
```

### 7. 黑神话悟空
*community prompt*

```
用 gpt-image-2 生成
根据{黑神话悟空}自动生成一张收藏版史诗叙事海报， 

巨大优雅的{悟空}人物侧脸剪影作为外轮廓，剪影内部自动生长出最契合该主题的完整世界观、标志性场景、角色关系、象征符号、关键建筑、生物、道具与氛围。

整体不是普通拼贴，而是高级的剪影轮廓填充式叙事合成，带有双重曝光式联想，但强化为电影级叙事表达与空间调度。

电影海报风格 + 东方现实主义美学融合，强调真实物理光影、镜头语言、空间纵深与叙事层级。

光影采用电影级侧逆光与局部暖光点缀，冷暖对比克制真实，加入体积光与轻雾增强空间感。

材质表现为真实质感（建筑、丝绸、肌肤、石材），避免纯绘画笔触感，

保留柔和空气透视，但优化为电影级景深与焦点控制。

轻微胶片颗粒，边缘飞白与刷痕改为电影式柔和融合过渡，

大面积留白，版式克制高级，安静、宏大、克制、宿命感强的东方电影叙事。

所有元素必须强绑定主题，一眼识别，不要杂乱，不要硬拼贴，不要模板化背景，不要廉价奇幻素材。
```

### 8. 清晰、准确、工程风格的爆炸图
*by [@beginnersblog1](https://x.com/beginnersblog1)*

```
Exploded isometric teardown diagram of [Put the name of the Object you are exploding]. Separate every component along a clear vertical axis with precise spacing. Render each part with accurate proportions and clean geometry. Include: outer casings, inner frame, mechanical parts, electrical modules, PCB, chips, connectors, buttons, switches, sensors, battery, screws. Use neutral lighting and a plain white background. Add thin uniform annotation lines pointing to each part with short, readable labels placed neatly around the image. No artistic style. No texture exaggeration. No distortion. Only a sharp, professional engineering breakdown similar to a hardware service manual.
```

### 9. 多视角主角图
*by [@LiEvanna85716](https://x.com/LiEvanna85716)*

```
分析输入图像的整个构图。识别所有存在的关键主体（无论是单人、群体/情侣、车辆还是特定物体）及其空间关系/互动。 生成一个连贯的 3x3 网格“电影印样（Contact Sheet）”，展示在同一环境中完全是这些主体的 9 个不同镜头。 你必须调整标准的电影镜头类型以适应内容（例如，如果是群体，保持群体在一起；如果是物体，构图包含整个物体）： 第 1 行（建立背景）： 大远景 (ELS)： 主体在广阔的环境中显得很小。 全景 (LS)： 完整的主体或群体从上到下可见（从头到脚 / 从车轮到车顶）。 中远景 (美式镜头/四分之三)： 构图从膝盖以上（针对人物）或 3/4 视角（针对物体）。 第 2 行（核心覆盖）： 4. 中景 (MS)： 构图从腰部以上（或物体的中心核心）。聚焦于互动/动作。 5. 中特写 (MCU)： 构图从胸部以上。主要主体的亲密构图。 6. 特写 (CU)： 紧凑构图于脸部或物体的“正面”。 第 3 行（细节与角度）： 7. 大特写 (ECU)： 强烈聚焦于关键特征（眼睛、手、标志、纹理）的微距细节。 8. 低角度镜头 (仰视/虫眼)： 从地面仰望主体（壮观/英雄感）。 9. 高角度镜头 (俯视/鸟瞰)： 从上方俯瞰主体。 确保严格的一致性：所有 9 个面板中是相同的人物/物体、相同的衣服和相同的光照。景深应逼真地变化（特写镜头中的背景虚化）。 一个包含 9 个面板的专业 3x3 电影故事板网格。 该网格以全面的焦距范围展示输入图像中的特定主体/场景。 顶行： 宽广环境镜头，全视图，3/4 剪辑（膝上景）。 中间行： 腰部以上视图，胸部以上视图，脸部/正面特写。 底行： 微距细节，低角度，高角度。 所有帧均具有照片般逼真的纹理，一致的电影级调色，以及针对所分析的主体或物体特定数量的正确构图。
```

### 10. Cute Halloween Coloring Pages
*community prompt*

```
a black and white coloring page of [insert Halloween scene], black pen outlines, white background, charming, lovable, minimalistic vector line drawing, flat output --no color --ar 49:64 --s 47 --v 5.2 --q 1
```

### 11. 日系朦胧感美女
*by [@MANISH1027512](https://x.com/MANISH1027512)*

```
a dreamy intimate portrait of a beautiful realistic asian woman lying under a blanket, soft natural light, cozy warm bedroom, cinematic film grain, 35mm film aesthetic, shallow depth of field, soft focus, delicate skin texture, natural makeup, slightly messy hair, Fujifilm Pro 400H look, pastel warm tones, realistic lighting, subtle haze, gentle atmosphere, by Petra Collins and Ren Hang --ar 3:4 --v7 --style raw
```

### 12. 梦幻般美女胶片照片
*by [@MANISH1027512](https://x.com/MANISH1027512)*

```
a dreamy top-down film photograph of a young beautiful East Asian woman lying on the floor surrounded by colorful anime magazines; relaxed gaze at camera, soft lips slightly parted; short fluffy dark hair with bangs; wearing a loose white short-sleeve blouse with lace trim and pale shorts, natural makeup with soft pink lips and subtle blush precise leg pose: pelvis slightly rotated toward camera; the near leg lifted and bent at the knee about 120 degrees, thigh pointing toward the camera with strong foreshortening, calf directed toward the bottom edge, ankle gently plantar-flexed, semi-transparent ankle sock visible; the far leg extended diagonally outward captured with a fisheye lens, producing ultra-wide barrel distortion, curved perspective lines, and central magnification; edges softly blurred with a dark circular vignette, creating a tunnel vision effect and nostalgic dreamy mood rainbow reflections from glossy magazines, warm ambient lighting, analog film grain texture, Japanese retro aesthetic
```

*Add yours via a PR — keep the original author's credit. See [Contributing](#contributing).*

---

## Related Model Guides
Part of the WaveSpeedAI **Awesome Model** series — one guide per frontier model, all runnable through one API:

- 🎬 [awesome-seedance-api](https://github.com/WaveSpeedAI/awesome-seedance-api) — ByteDance Seedance video
- 🌊 [awesome-wan-api](https://github.com/WaveSpeedAI/awesome-wan-api) — Alibaba Wan video
- ⚡ [awesome-minimax-h3-api](https://github.com/WaveSpeedAI/awesome-minimax-h3-api) — MiniMax Hailuo H3 video
- 🎞️ [awesome-kling-api](https://github.com/WaveSpeedAI/awesome-kling-api) — Kling video
- 🖼️ [awesome-seedream-api](https://github.com/WaveSpeedAI/awesome-seedream-api) — ByteDance Seedream image *(this repo)*
- 🎨 [awesome-gpt-image-api](https://github.com/WaveSpeedAI/awesome-gpt-image-api) — OpenAI GPT Image
- 🍌 [awesome-nano-banana-api](https://github.com/WaveSpeedAI/awesome-nano-banana-api) — Google Nano Banana image

---

## Contributing
PRs welcome:
1. Reusable prompts (`{placeholders}` for swappable parts).
2. **Credit the original author** with a link.
3. No output images unless you own and can license them.

## License
[CC0-1.0](LICENSE) — text & prompts are free to use. Model outputs follow the model provider's and [WaveSpeed](https://wavespeed.ai)'s terms.

---
<p align="center"><sub>Maintained by <a href="https://wavespeed.ai?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api">WaveSpeedAI</a> — the fastest way to run frontier image & video models via one API. <a href="https://wavespeed.ai/seedream-5-api?utm_source=github&utm_medium=readme&utm_campaign=awesome-seedream-api"><b>Run Seedream →</b></a></sub></p>
