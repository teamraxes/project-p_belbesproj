# Belbes Studio — Site Generation Prompt

**Project:** `p_belbesproj`
**Tariff:** premium
**Niche:** AI-driven digital studio

This prompt drives Claude Design's Pages generation, **after** the Design System is published. Attached files (paperclip): `composition.json`, `brief.json`, `creative_direction.json`. The DS already encodes typography/colors/components — this prompt focuses on layout grid, sitemap, и per-page content briefs.


---

## Grid Logic

*Component:* `cmp_full_bleed_editorial_pacing@1.0.0`

# Magazine-spread full-bleed hero rhythm

**Axis:** `grid_logic`
**Component ID:** `cmp_full_bleed_editorial_pacing`

## When this component is selected

См. `vector_centroid` (density=0.32 → sparse band) + `niche_affinity`.

## Pattern signals

- `full-bleed-hero` (3×)
- `low-density-editorial` (2×)
- `vertical-sidebar-nav` (1×)
- `asymmetric-vertical-nav` (1×)
- `magazine-pacing-rhythm` (1×)
- `full-bleed-aerial-hero` (1×)
- `3-col-sub-brand-section` (1×)
- `manifest-footer-display` (1×)
- `5-section-low-density` (1×)
- `full-bleed-interior-hero` (1×)

## Grid directives 

**Column structure:**
- Columns: **2**
- Breakpoints: [320, 768, 1024, 1440] (mobile / tablet / laptop / desktop)
- Hero layout: **full-bleed**

**Density profile (`sparse`):**
- Row rhythm: 24px baseline grid
- Gutter: 48px between columns
- Margin: 96px page padding
- Section count target: ~6 sections
- Rhythm: **accelerating**

**Section pacing details:**
- Accelerating — sections shorter as user scrolls deeper (editorial)

## Anti-patterns

- вертикальный sidebar nav требует серьёзного UX-investment; без продуманной реализации сбивает пользователей, ожидающих стандартную топ-навигацию
- tracklist layout works только для venue с реальной music programming; для cafe/restaurant без концепции = неуместно

---

## Sitemap


**Page strategy:** multi_page_separate  |  **Responsiveness:** single_responsive


**Rationale:** Premium tariff (7+ pages): editorial long-form home as a self-contained narrative + dedicated /how-it-works (5 phases deep dive), /pricing (honest spec-sheet), /case-studies (list) + /case-study/[slug] (detail template), /about (team + AI-pipeline-as-member), /contacts, /404. Multi-page separate (not single-responsive long-scroll) preserves editorial pacing and matches the explicit brief request for separate mobile-flow on premium.


- **/home** [landing, responsive]

    - `hero` — Open with the core promise — site in 24 hours on our AI-pipeline, not a template — and the primary CTA (request demo).

    - `proposition` — Three tariffs explained in plain language (Landing / Multipage / Premium) with timeline and price upfront.

    - `process_overview` — Five phases (Brief → Research → Synthesizer → Stagehand → Downstream) shown as a typographic narrative, not abstract icons; link to /how-it-works for deep dive.

    - `case_studies_preview` — Three to four delivery examples with hard metrics (hours to deploy, sections shipped) — anti-generic-testimonial.

    - `offers` — Pricing summary with what is included and timeline per tier; link to /pricing for full spec-sheet.

    - `team_preview` — Brief introduction: Tim + Victor + AI-pipeline as a named third member; link to /about.

    - `cta` — Final ask — brief / order form / direct Telegram contact.

    - `contacts` — Telegram, email, working hours, geographic scope.

- **/how-it-works** [process, responsive]

    - `hero` — Honest framing — show the actual five phases instead of hiding behind 'magic AI' language.

    - `process_step` — How a 30-minute Telegram intake produces structured brief.json; what we ask, what we never ask.

    - `process_step` — Niche-intelligence harvest: competitive landscape, visual tropes to avoid, underused directions.

    - `process_step` — Style-dimensions vector, color invariant, typography pair, sitemap, image and video briefs.

    - `process_step` — Production-grade code: semantic HTML, accessibility, responsive on three viewports, deploy targets.

    - `process_step` — Image and video generation, copy polish, QA gates, deploy to Timeweb.

    - `cta` — Convert from process trust into a concrete intake.

- **/pricing** [offering, responsive]

    - `hero` — Frame pricing as an honest spec-sheet, not 'starting from' marketing.

    - `pricing_tier` — One page, mobile adaptation, deploy. What is included and what is not.

    - `pricing_tier` — Three to five pages, forms, analytics. Full inclusions list.

    - `pricing_tier` — Five-plus pages, separate mobile flow, custom animations, deeper copywriting.

    - `exclusions` — Honest list of out-of-scope items — anti-hidden-fees signal.

    - `faq` — Common questions on timeline, ownership, hosting, revisions.

    - `cta` — Tier-aware CTA into intake form.

- **/case-studies** [case_study, responsive]

    - `hero` — Frame: hours-to-deploy and concrete outcomes, not years-of-experience.

    - `case_grid` — Three to four cards with niche, tariff, hours-to-deploy, headline result.

    - `cta` — From observed proof into intake.

- **/case-study** [case_study_detail, responsive] (template) — instantiated for `case_studies[]`

    - `hero` — Project name, niche, tariff, hours-to-deploy, headline metric.

    - `summary` — Three to five bullet outcomes — measurable, not adjectival.

    - `problem` — What the client came with; constraints; what they had tried before.

    - `approach` — Which pipeline phases mattered most; design choices and why.

    - `result` — Concrete metrics, screenshots, link to live site.

    - `cta` — Niche-similar CTA into intake.

- **/about** [about, responsive]

    - `hero` — Studio one-liner — two humans plus a named AI-pipeline, not a 'team of experts'.

    - `team` — Two founders, decomposed responsibility — who owns brief intake, who owns code, no anonymised 'we'.

    - `ai_pipeline_as_member` — Name the pipeline, list what it owns, show that it is supervised — anti-magical framing.

    - `values` — Editorial restraint, no hype vocabulary, fixed timeline, transparent process.

    - `cta` — Light CTA into Telegram intake.

- **/contacts** [contact, responsive]

    - `hero` — Direct ask — pick a channel, expected response time per channel.

    - `form` — Structured intake — niche, tariff intent, deadline, link to current site if any.

    - `direct` — Telegram @door2key, hello@belbes.ru, working hours GMT+3.

    - `contacts` — Studio details and geographic scope (RU market).

- **/404** [error, responsive]

    - `hero` — Restrained error state — no jokes, single back-home CTA, link to sitemap.


---

## Brief Highlights


**Main message:** Сайт под ключ за 24 часа на собственном AI-конвейере. Не шаблон. Конкретный сайт под ваш бизнес — с реальной копией, дизайном под нишу, и production-grade кодом.


**CTA goal:** request_demo


**Target audience:** Основатели стартапов и SMB-команды в РФ/СНГ, которым нужен сайт под ключ за 24-48 часов без compromise на качество. Внутренний целевой образ: тех-грамотный фаундер, который ценит прозрачность процесса и быструю доставку.


**Key offers:**
- Landing 30 000 RUB / 24 часа — одна страница, мобильная адаптация, deploy
- Multipage 60 000 RUB / 36 часов — 3-5 страниц, формы, аналитика
- Premium 100 000 RUB / 48 часов — 5+ страниц, отдельный мобайл-флоу, кастомные анимации, копирайт с глубиной


**Required sections:**
- hero
- что мы делаем (3 тарифа объяснены простыми словами)
- как работает AI-конвейер (5 фаз — Brief → Research → Synthesizer → Stagehand → Downstream)
- case studies (3-4 примера деливери, метрики и timeline)
- тарифы (детальный pricing + что входит + сроки)
- команда (TB + Виктор + AI-конвейер как третий сотрудник)
- контакты (TG, email, форма заказа)



## Image Briefs


### 1. role=hero_main

```json
{
  "role": "hero_main",
  "type": "photo",
  "default_dimensions": "1920x1080",
  "model": "openai/gpt-image-1",
  "prompt_seed": "Editorial-restrained studio workspace shot: warm cream off-white surfaces (#F7F4EE), a single saturated red object (SBB Red #EB0000) as the only chromatic anchor — e.g. an open hardcover notebook with a crimson bookmark on a beech-wood desk, or a red ceramic cup beside a closed laptop. Diffused morning light from the left, soft long shadows. Subject centered, photographed straight-on at desk height. Generous negative space top-right for headline overlay. Mood: calm, technically-confident, anti-hype — no people in frame, no glowing AI orbs, no gradient backdrops. Photographic, magazine-editorial register, warm-neutral color grading.",
  "negative_prompt": "no neon gradients, no glowing orbs, no people, no AI/tech clichés, no centered text overlay in scene, no holograms, no abstract data visualizations",
  "viewport_variants": [
    {
      "viewport": "desktop",
      "aspect_ratio": "16:9",
      "exact_dimensions": "1920x1080",
      "crop_intent": "subject_centered"
    },
    {
      "viewport": "tablet",
      "aspect_ratio": "4:3",
      "exact_dimensions": "1024x768",
      "crop_intent": "subject_centered"
    },
    {
      "viewport": "mobile",
      "aspect_ratio": "9:16",
      "exact_dimensions": "1080x1920",
      "crop_intent": "subject_centered"
    }
  ],
  "used_in_pages": [
    "home",
    "how-it-works",
    "about",
    "case-study"
  ]
}
```


### 2. role=founders_portrait

```json
{
  "role": "founders_portrait",
  "type": "photo",
  "default_dimensions": "1920x1080",
  "model": "openai/gpt-image-1",
  "prompt_seed": "Editorial duo portrait of two software-studio founders (one named Tim, the other Victor), both in their early-to-mid 30s, in a warm off-white studio interior (#F7F4EE walls). Casual smart attire — fine-knit sweaters or unstructured shirts, no suits, no hoodies. Relaxed but engaged expressions, half-smiles, eyes on camera. Natural diffused window light from the left, soft shadows. Medium shot, subjects offset slightly left in frame, generous negative space right for caption block. A single subtle red accent (SBB Red #EB0000) somewhere in scene — e.g. a red book spine on a low shelf behind them. Mood: trustworthy, technically-grounded, anti-corporate. Photographic, magazine-editorial register, warm-neutral color grading.",
  "negative_prompt": "no corporate suits, no stiff handshake poses, no fake bright laughter, no whiteboard with code behind them, no neon office, no AI-generated facial distortion artifacts",
  "viewport_variants": [
    {
      "viewport": "desktop",
      "aspect_ratio": "16:9",
      "exact_dimensions": "1920x1080",
      "crop_intent": "subject_centered"
    },
    {
      "viewport": "tablet",
      "aspect_ratio": "4:3",
      "exact_dimensions": "1024x768",
      "crop_intent": "subject_centered"
    },
    {
      "viewport": "mobile",
      "aspect_ratio": "4:5",
      "exact_dimensions": "1024x1280",
      "crop_intent": "subject_centered"
    }
  ],
  "used_in_pages": [
    "about",
    "home"
  ]
}
```


### 3. role=case_thumb

```json
{
  "role": "case_thumb",
  "type": "photo",
  "default_dimensions": "1920x1080",
  "model": "openai/gpt-image-1",
  "prompt_seed": "Editorial product-style shot of a laptop or large monitor showing a finished website, photographed from a low three-quarter angle on a warm off-white surface (#F7F4EE). Screen content readable but not the focus. Single red object (#EB0000) in frame as chromatic anchor — pen, sticky note, book corner. Diffused side light, soft shadow. Magazine-editorial register. Composition leaves rule-of-thirds focal weight on the device. No people, no hands.",
  "negative_prompt": "no glowing screens, no neon RGB lighting, no busy desk clutter, no people, no centered logo overlay",
  "viewport_variants": [
    {
      "viewport": "desktop",
      "aspect_ratio": "16:9",
      "exact_dimensions": "1920x1080",
      "crop_intent": "rule_of_thirds_focal"
    },
    {
      "viewport": "tablet",
      "aspect_ratio": "4:3",
      "exact_dimensions": "1024x768",
      "crop_intent": "rule_of_thirds_focal"
    },
    {
      "viewport": "mobile",
      "aspect_ratio": "4:5",
      "exact_dimensions": "1024x1280",
      "crop_intent": "rule_of_thirds_focal"
    }
  ],
  "used_in_pages": [
    "case-studies",
    "case-study",
    "home"
  ]
}
```



---

## Output Format

Generate a complete static multi-page website implementing the Design System и this site brief.

**Required pages:** /home, /how-it-works, /pricing, /case-studies, /about, /contacts, /404.
**Required asset:** `assets/styles.css` (shared CSS with semantic tokens matching the published Design System).

Constraints:
- All HTML must be valid HTML5 with semantic landmarks (`<header>`, `<main>`, `<footer>`, `<nav>`).
- All inter-page links must be relative.
- Do NOT use Tailwind utility classes — write plain CSS only.
- Do NOT use Lorem ipsum — use real content driven by the brief.
- Hero must surface main_message in <30s scan.
