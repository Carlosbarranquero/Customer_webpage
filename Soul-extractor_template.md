
### A prompt for transforming raw business research into structured brand documents

---

## What this does

Takes messy raw research AI-generated reports, Google Maps data, customer reviews, photo descriptions, brand notes  and transforms it into four clean, structured documents with zero duplication between them.

**Input:** Any combination of raw research files about a business. **Output:** Four `.md` files, one per concept.

| File                       | Contains                                                                      |
| -------------------------- | ----------------------------------------------------------------------------- |
| `[business]_soul.md`       | Identity, essence, tagline, personality, tone of voice, positioning           |
| `[business]_visual.md`     | Color palette, typography, photography direction, materials & textures        |
| `[business]_operations.md` | Address, hours, phone, menu/services, price range, amenities                  |
| `[business]_experience.md` | Real customer quotes, key attributes, reasons people return, honest criticism |

---

## How to use it

1. Gather your raw research files in one folder. They can be `.md`, `.txt`, or `.pdf` files from any source: Perplexity, Grok, Google Maps scrapes, TripAdvisor exports, review compilations, your own notes, etc.
2. If you have photos, reference the folder path.
3. Paste this prompt into Claude (or any capable LLM) and include or reference your files.
4. The model will read everything, synthesize it, and produce the four output files.

---

## The Prompt

Copy everything below this line and paste it as your instruction to the AI.

---

You are a brand strategist and researcher. Your task is to read all the raw research files I provide and transform them into four structured brand documents. These documents will be used as the foundation for a website, a deck, or a communication project.

**Before writing anything, read every single source file completely.** Do not start producing output until you have processed all available inputs.

---

### Rules that apply to all four documents

1. **No duplication.** Each piece of information appears in exactly one document. If the address fits in Operations, it does not appear in Soul or Experience.
2. **Synthesize, do not transcribe.** Extract patterns and insights. Do not copy-paste blocks from the source files.
3. **Resolve contradictions.** If two sources disagree (e.g., one says 7:00 AM, another says 7:30 AM), note both versions and flag the discrepancy.
4. **Preserve customer quotes verbatim.** Reviews and testimonials must be reproduced exactly — never paraphrased.
5. **Write the honest criticism.** Do not omit weaknesses. The most consistently mentioned negative is a required section in Experience.
6. **If data is missing,** write `[Not available in source material]` — never invent or assume.
7. **Tone:** analytical and precise. Not promotional. Not poetic (unless quoting a real source). Think brand strategy report, not marketing copy.

---

### Document 1 — `[slug]_soul.md`

Use `[slug]` as a lowercase, hyphenated version of the business name (e.g., `wind-garden`).

Write these sections:

**Who they are** Two or three paragraphs describing what this business fundamentally is not what it sells, but what it means. Written as a thoughtful observer who has spent time there.

**Tagline** The official tagline or most evocative phrase associated with the brand. Followed by one paragraph explaining what it means and where/how it is used physically or visually.

**Brand promise** One paragraph. The core emotional promise to the customer. What they will _feel_, not what they will _get_.

**Personality** A table with four to six rows:

|Attribute|How it shows up|
|---|---|
|[Trait]|[Concrete manifestation in the business]|

**Tone of voice** One paragraph. How does this brand communicate? Include: pace, vocabulary register, what to avoid. Include one "right way / wrong way" example if possible.

**Positioning** Three to five bullet points. Where does this business sit relative to alternatives? What does it _not_ compete on?

**Who it's for** One paragraph describing the real customer — not a demographic, but a portrait of the person who instinctively "gets" this place.

**What it is not** One short paragraph. A business is often best defined by what it refuses to be.

---

### Document 2 — `[slug]_visual.md`

**Color palette**

Two sub-sections:

_Accent colors (high impact, used sparingly):_

|Name|Hex|Usage|
|---|---|---|
|[Name]|`#XXXXXX`|[Where and how]|

_Base colors (dominate the composition):_

|Name|Hex|Usage|
|---|---|---|
|[Name]|`#XXXXXX`|[Where and how]|

_Golden rule:_ One sentence stating which colors dominate and which are reserved as accents.

**Typography** If brand guidelines exist in the source material, extract directly. If only photos or descriptions are available, derive recommendations from what is visible or described.

- Display / headlines: [font name or style + where used]
- Body text: [font name or style + where used]
- Recommended pairing: [display] + [body]

**Visual language and photography**

_Key visual motifs:_ Five to eight recurring motifs extracted from photos or descriptions. Each: motif name + brief description of how it appears.

_Photography direction:_ Five to seven guidelines — lighting, color treatment, composition style, what to avoid. Written as clear directives.

**Materials and textures**

|Material|Where it appears|
|---|---|
|[Material]|[Location in the space + how it feels]|

**Multisensory reference** One paragraph. Beyond visual: sound, texture, smell, atmosphere. How does the space feel to the body, not just the eye? This is reference material for anyone designing a visual piece — it should evoke the full experience.

---

### Document 3 — `[slug]_operations.md`

**Business file**

|Field|Value|
|---|---|
|Commercial name||
|Address||
|Hours||
|Phone||
|Website||
|Facebook||
|Instagram||
|Capacity||
|Price range||
|Google rating|[stars + number of reviews]|

**Available services** Bulleted list of confirmed amenities: Wi-Fi, parking, payment methods, outdoor seating, reservations, delivery, takeaway, private rooms, etc.

**Menu / Main services**

Organize by category. For each item:

|Item|Notes|
|---|---|
|**[Name]**|[What makes it notable — not marketing copy]|

**Location and surroundings** One paragraph: neighborhood context, nearby landmarks, accessibility, what else is in the area. Useful for writing "Find Us" copy.

**Best times to visit**

|Time window|Why|
|---|---|
|[Range]|[Reason based on source data]|

**Service notes** Any consistent patterns about service quality, pace, wait times, or tips for getting the best experience. Include weaknesses if they appear consistently in reviews.

---

### Document 4 — `[slug]_experience.md`

**What customers feel (synthesis)** One paragraph. Not a list of review excerpts — a narrative synthesis of the emotional experience customers describe. What do they feel while they're there? What do they feel when they leave?

**Phrases that define the place (real voices)** Five to eight direct quotes from real reviews. Select for: emotional resonance, specificity, diversity of perspective.

Format each as:

> _"[Exact quote]"_ — [Author name]

**Most cited attributes in reviews**

|Attribute|Frequency|Notes|
|---|---|---|
|[Attribute]|★★★★★|[What people specifically say about this]|

Use the star scale: ★★★★★ = consistently mentioned, ★★★★☆ = frequently, ★★★☆☆ = occasionally.

**Why people come back** Numbered list, four to six items. The actual motivators for repeat visits, extracted from patterns in the reviews — not what the business claims.

**Real use cases** How people actually use this space or service, based on review data and descriptions. Not how the business wants them to use it.

**The honest criticism** One paragraph. The most consistently mentioned complaint or weakness. Do not soften or omit. This is the most operationally useful part of the document.

**The human detail** One specific, surprising, or emotionally resonant detail that does not fit neatly into other categories — a stray cat the staff feeds, a ritual, an unexpected service touch. If none exists in the source material, omit this section. Do not invent.

**Writing guidelines for this business** Five to seven directives for anyone who will write copy, captions, or scripts for this brand. Derived from the reviews, the atmosphere, and the personality. Written as concrete creative instructions.

---

### Delivery

Save the four files in the project folder using the naming convention above. Then confirm briefly:

- What business was processed
- Total source files read
- Any data gaps or contradictions found

Do not explain what each file contains — the user can read them.

---

_Soul Extractor — created for reuse across business projects_