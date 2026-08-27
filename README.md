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

### 1. Ticket-style infographic cover
*community prompt*

```
Generate an infographic image following the design-style and content requirements below.

Design style:
Use 3–4 different font sizes to create hierarchy, with the keyword in the largest size. The main title must be at least 3× larger than subtitles and body text. Use a grid layout, like a premium magazine. Keep harmonious proportions between text and decorative elements, with a clear visual flow guiding the reader's eye.

Digital minimalist ticket-stub design language:
**Black-and-white dominance:** a high-contrast monochrome palette for strong visual impact
**Ticket layout:** structured like a boarding pass, admission ticket, or e-voucher
**Clear geometric zoning:** the canvas is precisely divided into orderly information blocks
**Negative space:** generous, deliberate whitespace for openness and elegance
**East-meets-West aesthetics:** traditional typographic conventions blended with modern Western design language
**Industrial-design touches:** refined use of commercial elements like ® marks and barcodes
**Digital-interface mapping:** information presented like a screen or app UI

Typography:
**Mixed-script contrast:** mixing typefaces for a cross-cultural feel
**Distinct size hierarchy:** oversized main title, delicate small supporting text
**Multi-directional layout:** horizontal, vertical, and diagonal text arrangements
**Precise spacing:** carefully tuned letter-spacing and leading for breathing room
**Symbolic ornament:** brackets, underlines, and arrows woven into the type design
**Serif/sans mix:** alternating font families for depth
**Formatted time info:** dates in a consistent format with directional markers

Visual elements:
**Functional indicators:** arrows and asterisks for guidance and emphasis; flat UI elements like "CHECK IN" and "@"
**Borders and dividers:** clean lines separating information zones
**Minimal glyphs:** pared-down symbols conveying core information
**Handwritten accents:** e.g. a script "Romantic" to warm up the mechanical layout
**Directional flow:** element placement creating a left-to-right, top-to-bottom reading rhythm
**Negative space as a design element**

Text content:
```

### 2. Handwritten study-notes cover
*community prompt*

```
Based on the content below, create a realistic handwritten-style study-notes cover. Use a student's handwriting font on A4 ruled-notebook paper with visible paper texture. Highlight key terms with a yellow highlighter. Write the date "June 13, 2026" in the top-right corner, circled in red by hand. Add hand-drawn arrows and doodles in the margins to help explain concepts. Overall feel: natural, slightly casual study vibes.
Aspect ratio: 16:9
Content:
```

### 3. Flat vector illustration cover
*community prompt*

```
Core instruction:
Generate a horizontal, panoramic flat-vector illustration cover. The image must include a clear text title.

Illustration style:
Flat Vector Illustration. Every element (including the title's outline box) must have clean, uniform-weight black monoline stroke outlines. Line ends are rounded, no sharp corners — like coloring-book linework. Color fills stay simple with minimal flat shadows; strictly no gradients or 3D rendering.

Composition & space:
Panoramic composition, with the illustration occupying the top 1/3 of the layout. Eye-level or slightly top-down 2.5D perspective. Convey depth through clear layer overlap; all layers equally sharp — no atmospheric blur.

Geometric simplification:
Simplify all objects into geometric shapes for a "toy model" cuteness — trees become lollipops or triangles, buildings become simple rectangular blocks, windows become neat little grids.

Decoration & palette:
Fill empty areas with decorative geometry to balance density: radiating lines (sun/energy), pill-shaped clouds, dots and stars. Background: beige/cream paper texture. Accent colors in retro-soft tones: coral red, mint green, mustard yellow, ochre, and slate blue.

Typography:
Main title: prominent, huge, bold retro serif style (old-newspaper feel) conveying authority and elegance, with a black outline.
Subtitle: inside a rectangular color block, in a clean sans-serif.

Fill in the content to generate below:
```

### 4. Narrative-heavy content cover
*community prompt*

```
Generate a strongly narrative cover for any topic. The frame must be governed by one intense, unified dominant color field, extracted from the subject's own era, material, industry, region, and mood. It fills most of the background like a layer of aged paper, wall plaster, lacquer, or a printing plate with real thickness. The title uses a high-contrast aged white, off-white, pale metallic, or a bright light tone derived from the subject, with a slight yellowing, wear, chalking, and paper-pulp grain. The deepest structures — shadows, illustration silhouettes, spatial cracks — use only near-ink-black, scorched brown, or the subject's own darkest tone. The whole must NOT be colorful: it should feel like three or four light-dark roles grown from a single color system — the big field carries emotion, the pale letters carry impact, the dark tone carries weight, and sparing accents appear only where the eye must rest.

The title type is the frame's main structure. The lettering must carry the weight of stone inscriptions, rubbings, woodblock prints, old newspaper mastheads, and Republican-era posters blended together: wide, forceful strokes, knife-cut hard edges and irregular notches at the turns, with hints of engraved-type sharpness — but never a modern sans, rounded font, computer display face, or clean calligraphy. A few key characters should be huge, like stone blocks and walls occupying space, their surfaces eroded, ink-broken, misregistered, scratched, and coarsely grained; secondary text forms a sparse-dense rhythm around them rather than filling evenly.

The illustration grows naturally from the topic — no preset subject matter. Narrative imagery emerges from the topic's own conflicts, identities, era, materials, and spirit, attaching to, slipping into, veiling, or surfacing around the giant letters — as if printed from the same plate rather than pasted on. Don't spell everything out; keep silence, occlusion, and half-developed passages. The first glance must be the pressure of huge aged letters and a single strong color; only the second glance reveals the story, tension, and aftertaste growing inside and around the type.

Topic:
[replace with your content]

Note: text is the logical focus — all text must read fast and large.
Aspect ratio 16:9
```

### 5. Celestial Chinese palace — Eastern mythology megastructure
*community prompt*

```
Eastern surrealist temple aesthetics — a mythological Chinese world above a sea of clouds.
The main subject is [scene subject]; the space contains [architectural structure], reading as a megastructure celestial palace / impossible architecture / sacred halls.
The scene is surrounded by [environment elements]; a distant [far target] is partially hidden by [occlusion method], showing only silhouette or fragments to heighten mystery and imagination.
There are [number and identity of figures], who are [figure action]; the figures are tiny, emphasizing the colossal scale of the architecture and world. [Anomalous element] appears in the sky or space, deepening the sense of Eastern myth and epic.
Overall lighting: [light type]; dominant palette: [color scheme].
Composition emphasizes [camera composition]; the mood should be [emotion keywords].
cinematic oriental fantasy, celestial palace, monumental architecture, cloud sea, divine light, impossible architecture, epic scale, surreal sacred atmosphere, ultra detailed.
```

### 6. Hand-drawn black-and-white doodle cover
*community prompt*

```
Hand-drawn black-and-white illustration, social-media cover design, minimalist, white background, black line-art figure: a young man sitting at a desk writing intently. On the desk: a notebook, a mug, an alarm clock, and books. Strong linework doodle style, like journal illustrations.
Include a large title: "{{title}}" in bold handwritten type with a casual feel. Use yellow as the single accent color (underlines, circled highlights, star doodles).
On the left, a sticky note reading:
{{sticky-note text, can be numbered 1/2/3}}
On the right, a lightbulb icon + "2 focused hours every day"
At the bottom, a white-on-black caption bar.
Overall style: knowledge-creator vibe, authentic documentation feel, relaxed but restrained, non-commercial.
Style reference: hand-drawn doodles, black-and-white line art + a small amount of highlight color. Clean composition, clearly zoned information, made for content covers.
Bottom tags: {{bottom tags, separated by |}}
High resolution
```

### 7. Epic silhouette narrative poster (Black Myth: Wukong)
*community prompt*

```
From {Black Myth: Wukong}, auto-generate a collectible epic narrative poster.

A huge, elegant profile silhouette of {Wukong} forms the outer contour; inside the silhouette, the theme's complete worldview grows organically — iconic scenes, character relationships, symbols, key architecture, creatures, props, and atmosphere.

Not an ordinary collage but a refined silhouette-fill narrative composite, double-exposure-like association elevated to cinematic storytelling and spatial blocking.

Movie-poster style fused with Eastern realism — real physical light and shadow, cinematic lens language, spatial depth, and narrative hierarchy.

Lighting: cinematic rim/backlight with restrained warm accents, believable warm-cool contrast, volumetric light and light haze for depth.

Materials rendered with true physical texture (architecture, silk, skin, stone) — avoid painterly brush-stroke feel.

Keep soft aerial perspective, refined into cinematic depth-of-field and focus control.

Subtle film grain; edge fly-white and brush marks resolved into soft cinematic transitions.

Generous negative space, restrained premium layout — quiet, monumental, restrained, fate-laden Eastern cinematic storytelling.

Every element must bind tightly to the theme and read at a glance. No clutter, no hard collage, no template backgrounds, no cheap fantasy stock.
```

### 8. Clean engineering-style exploded diagram
*by [@beginnersblog1](https://x.com/beginnersblog1)*

```
Exploded isometric teardown diagram of [Put the name of the Object you are exploding]. Separate every component along a clear vertical axis with precise spacing. Render each part with accurate proportions and clean geometry. Include: outer casings, inner frame, mechanical parts, electrical modules, PCB, chips, connectors, buttons, switches, sensors, battery, screws. Use neutral lighting and a plain white background. Add thin uniform annotation lines pointing to each part with short, readable labels placed neatly around the image. No artistic style. No texture exaggeration. No distortion. Only a sharp, professional engineering breakdown similar to a hardware service manual.
```

### 9. 3x3 cinematic contact sheet from one image
*by [@LiEvanna85716](https://x.com/LiEvanna85716)*

```
Analyze the full composition of the input image. Identify all key subjects present (a single person, a group/couple, a vehicle, or a specific object) and their spatial relationships/interactions. Generate a coherent 3x3 grid "cinematic contact sheet" showing 9 different shots of exactly these subjects in the same environment. Adapt standard cinematic shot types to the content (keep groups together; frame whole objects). Row 1 (establishing context): 1. Extreme Long Shot (ELS): subject small in a vast environment. 2. Long Shot (LS): full subject or group visible head-to-toe / wheels-to-roof. 3. Medium Long Shot (American / three-quarter): framed from the knees up (people) or a 3/4 view (objects). Row 2 (core coverage): 4. Medium Shot (MS): waist-up (or the object's central core), focused on interaction/action. 5. Medium Close-Up (MCU): chest-up, intimate framing of the main subject. 6. Close-Up (CU): tight on the face or the object's "front". Row 3 (details & angles): 7. Extreme Close-Up (ECU): macro detail on a key feature (eyes, hands, logo, texture). 8. Low-angle shot (worm's-eye): looking up at the subject (epic/heroic). 9. High-angle shot (bird's-eye): looking down from above. Enforce strict consistency: same person/object, same clothes, same lighting in all 9 panels. Depth of field varies realistically (background bokeh in close-ups). A professional 3x3 cinematic storyboard grid of 9 panels covering the full focal range of the specific subject/scene from the input image. Photo-real textures, consistent cinematic color grade, correct framing per panel.
```

### 10. Cute Halloween Coloring Pages
*community prompt*

```
a black and white coloring page of [insert Halloween scene], black pen outlines, white background, charming, lovable, minimalistic vector line drawing, flat output --no color --ar 49:64 --s 47 --v 5.2 --q 1
```

### 11. Dreamy Japanese-style film portrait
*by [@MANISH1027512](https://x.com/MANISH1027512)*

```
a dreamy intimate portrait of a beautiful realistic asian woman lying under a blanket, soft natural light, cozy warm bedroom, cinematic film grain, 35mm film aesthetic, shallow depth of field, soft focus, delicate skin texture, natural makeup, slightly messy hair, Fujifilm Pro 400H look, pastel warm tones, realistic lighting, subtle haze, gentle atmosphere, by Petra Collins and Ren Hang --ar 3:4 --v7 --style raw
```

### 12. Dreamy top-down film photograph
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
