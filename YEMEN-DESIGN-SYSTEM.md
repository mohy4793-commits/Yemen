# YEMEN: BEYOND THE HEADLINES — Design System v1.0

Companion to `YEMEN-BEYOND-THE-HEADLINES.md`. Written for hand-off to Claude InDesign.
Language of this file: English (the book's market language). Status: **Phase 1 — book + identity**. Video is a later phase (see §13).

**Contents**
1. Strategic brief — what the analysis found, and what the redesign does about it
2. Identity concept — "Lit From Within"
3. Color tokens
4. Typography
5. Cover system
6. Page architecture (ebook + paperback)
7. Markup → style map (how the book file maps to InDesign styles)
8. Component specifications
9. Imagery rules and audit of the current images
10. Visual prompt library (identity, cover, part openers, scenes)
11. EPUB / Kindle technical notes
12. Hand-off checklist, open items to verify, editorial change log
13. Forward compatibility with the video phase

---

## 1. Strategic brief

### 1.1 What was reviewed

| Input | Notes |
|---|---|
| Book text (`BEFORE YOU GO TO YEMEN.md`) | All 12 chapters, opening, closing, sources, notes — re-read in full |
| Screenshot (`لقطة شاشة 2026-10-10 190254.png`) | This is the **KDP Bookshelf dashboard**, not the public Amazon product page. It shows title, author, price, status, ASIN, formats. It does **not** show rating, review count, BSR, description, categories, or Look Inside. The public Amazon page was not reachable from this environment, so those items are **not analyzed**. |
| Cover (`cover.png`) and 6 interior images | Reviewed visually |
| Video guide PDF + `video-production.skill` | Read only to understand the next phase; nothing executed |

### 1.2 Why the book is likely under-performing (evidence-based, ranked)

| # | Finding | Evidence | Why it hurts | What this redesign does |
|---|---|---|---|---|
| 1 | **Title promises a travel guide; the book is not one** | Title "Before You Go to Yemen"; text says "This is not a travel guide" and every government advises against travel | Attracts the wrong click (travel intent), disappoints, invites bad reviews; readers who want an introduction to Yemen's history/culture don't recognize themselves in the title | New title built on what the book actually delivers (§1.4). Travel content kept, but demoted to one honest chapter. |
| 2 | **Cover is weak at thumbnail size** | In the dashboard thumbnail the cover reads as beige-on-beige; the "GO" paper-plane gimmick splits the title; subtitle is illegible; the collage has 5+ competing focal points | Cover is the strongest click factor. At ~100–160 px wide nothing is instantly legible or emotionally clear. | New cover system: one dominant image (a glowing window), one dominant word (YEMEN), dark ground with high contrast (§5). |
| 3 | **Price vs length vs royalty band** | $12.00 USD shown; the book calls itself "twenty-five pages"; Kindle-only | A ~25-page short read at $12 is far above what short non-fiction typically sells for; and $12.00 sits above the long-standing 70%-royalty ceiling of $9.99 | See §1.5. Recommend testing $3.99–$4.99. |
| 4 | **Metadata/search positioning is thin** | Title carries only one searchable noun ("Yemen"); subtitle "…Oldest Corner of Arabia" has no buyer-intent terms | Little keyword coverage; the sub-title is poetic, not searchable | New title + subtitle contain: Yemen, Short Introduction, History, People, Culture. |
| 5 | **Author-name inconsistency** | KDP shows "MOOHIALDIN ALQUDAIMI"; the cover shows "AL-QUDAIMI" | Splits the author's name into two spellings; hurts author-page and search matching | One form everywhere (the book file uses "Moohialdin Al-Qudaimi" — the author must confirm and match KDP exactly). |
| 6 | **No back-of-book conversion path** | Original ends at "Sources" and a disclaimer | No review request, no next-book link, no email capture — the cheapest marketing is missing | Back matter CTA block added (placeholders for links). |
| 7 | **One format only** | Dashboard shows "Create paperback / hardcover" unused | No print edition: no price anchor, no "Paperback" tab, lower credibility for a reference-style book | Print-ready spec included (§6). |
| 8 | **Cover file is not Kindle-shaped** | `cover.png` is 1240×1754 px (A4 ratio 1:1.41) with large white margins; Kindle's ideal is 1600×2560 px (1:1.6) | Low resolution; cropping/margins risk | New cover spec at 1600×2560 (§5). |
| 9 | **Interior images are low-resolution and some captions overclaim** | 848–1376 px wide; several look AI-generated; captions present them as specific real places | Weak in print; credibility risk; KDP asks publishers to disclose AI-generated content | See §9. |

> **Not known and therefore not claimed:** sales figures, BSR, rating, review count, description, categories, keywords in use. If you share the live page text, rating/review count and BSR, the diagnosis can be sharpened.

### 1.3 Positioning

- **Category promise:** *the 30-minute primer on Yemen that replaces the headline image with the real country.*
- **Reader:** curious general readers; students and teachers; aid, policy and journalism newcomers; travelers who want context first; people of the Yemeni diaspora and their friends.
- **Unique mechanism:** a country introduced through six landscapes, five myths corrected, and one honest chapter on why not to travel — in one sitting.
- **Tone:** warm, authoritative, plain. Never exoticizing, never alarmist. Respect both the heritage and the suffering.

### 1.4 Title decision

**Recommended — Title:** `Yemen: Beyond the Headlines`
**Recommended — Subtitle:** `A Short Introduction to Its History, People, and Culture`
(*Cover tagline, not part of metadata:* "The ancient country the world only knows from the news.")

| Candidate | Search match ("Yemen" + intent) | Honest to the content | Emotion / curiosity | Thumbnail legibility | Series potential | Verdict |
|---|---|---|---|---|---|---|
| Before You Go to Yemen *(current)* | Weak — reads as travel | **No** — not a guide | Medium | Long, 5 words | Low | Replace |
| **Yemen: Beyond the Headlines** | **Strong** — "Yemen" leads | **Yes** — the book's own closing theme | **High** — implies a hidden, truer story | **Excellent** — "YEMEN" can fill the cover | **High** — "Beyond the Headlines" works as a series line | **Recommended** |
| Understanding Yemenis | Medium — "Yemenis" is narrower than "Yemen" (assumption: lower search demand than "Yemen"; verify with Amazon autocomplete) | Partial — covers people only; the book also covers landscape, history, architecture, coffee, diaspora, the war | Medium, a little academic | Good | Medium ("Understanding …" is crowded with textbooks) | Do not use as the main title. **Use it as a chapter title or a backend keyword phrase** ("understanding Yemeni culture"). |
| What the World Gets Wrong About Yemen | Medium | Yes | **High** but confrontational | Long | Medium | Strong **alternate**; consider as subtitle or ad headline |
| The Country Behind the Headlines | Weak ("Yemen" missing from title) | Yes | High | Medium | High | Good **alternate** *if* the subtitle names Yemen |
| Yemen Is Not What You Think | Medium | Yes | High, but "not what you think" is a worn formula | Medium | Medium | Alternate |

Rules applied: keep the key search word first; subtitle holds buyer-intent terms; no superlatives ("oldest", "most") in metadata that the author cannot defend; cover title must exactly match the KDP title field.

### 1.5 Pricing and format recommendations (to verify in KDP before acting)

- Royalty bands: most sources still give **$2.99–$9.99 → 70%**, otherwise **35%**. One source claims the ceiling moved to $12.99 on 7 July 2026; this could not be confirmed against KDP's own help pages. **Check KDP's current pricing page.** Either way, $12 is high for a short read.
- Recommended test: **$3.99 or $4.99** for the first 30–60 days (price to be confirmed against current KDP bands).
- 70% royalty is paid **after a file-delivery fee** that scales with file size (one source cites about $0.15 per MB for the US store — verify). Therefore **keep the EPUB lean: aim for ≤ 3 MB total**, compress images (see §9.4). *Illustrative estimate:* at $4.99 and a 2 MB file ≈ 0.70 × 4.99 − (2 × 0.15) ≈ **$3.19 per sale**. This is an estimate, not a promise.
- KDP Select: stay enrolled for the launch window (no other store is currently in use); revisit after 90 days.
- Create the **paperback** (spec in §6). Per KDP, the ebook price generally needs to sit below the paperback price for the 70% band.

### 1.6 Do this next (priority order)

1. Replace the cover (§5, prompts CV-1…CV-3) and the title/subtitle in KDP.
2. Re-upload the interior from this book file; fix the author-name spelling to match the cover.
3. Reprice to a tested short-read price; compress the EPUB.
4. Paste the new description and 7 keyword slots (not yet produced — ask for the "listing pack" next).
5. Add the paperback.

---

## 2. Identity concept — "Lit From Within"

**Idea.** The book's most beautiful image is also its truest metaphor: in Sana'a's tower houses, stained-glass *qamariyyat* ("little moons") glow from the upper floors at dusk — "a city illuminated from within." The brand says the same thing about the country: **beneath the dark headlines, a warm light that was always on.**

**Rules of the system**
1. **One warm light in a cool field.** Every cover, opener and scene has a single amber source (a window, a lamp, dawn) against deep indigo or sand. That *is* the brand.
2. **Stone, brick, mud, gypsum.** Surfaces are tactile and mineral. Ornament comes from gypsum tracery geometry, never from clichéd "Arabian" decoration.
3. **Vertical.** Yemen is "a vertical country." Prefer tall compositions, stacked sections, upward motion. The cover is a portrait; the page grid emphasizes the vertical axis.
4. **Human, not heroic.** People appear as hands, silhouettes, backs — dignified, never posed as victims or warriors.
5. **No war imagery.** No weapons, soldiers, rubble, smoke or flags anywhere in the identity. The conflict is told in words (Chapter 10), not pictures.

**Voice in captions and UI text:** concrete nouns, short sentences, one idea per caption.

---

## 3. Color tokens

### 3.1 Palette

| Token | Hex | Role | Origin in the book |
|---|---|---|---|
| `--night` | `#0B1426` | Cover ground, dark sections, ebook night mode | The blue hour over Sana'a |
| `--indigo` | `#1B2B4D` | Headings on light pages; secondary dark ground | Dusk sky |
| `--lamp` | `#F2A83B` | **Signature accent — only on dark grounds** | The glowing *qamariyyah* |
| `--lamp-soft` | `#FFD58A` | Highlights, large display on dark | Light spill on brick |
| `--gypsum` | `#F6EFE2` | **Page background (print and ebook light)** | White gypsum tracery |
| `--sand` | `#EADFC8` | Boxes, callouts, tinted panels | Mud brick in sun |
| `--mudbrick` | `#A4502B` | Rules, kickers, links on light | Fired brick |
| `--crimson` | `#9E2A2B` | Rare emphasis; "Myth" label | Dragon's blood resin |
| `--terrace` | `#3E6B4A` | Rare emphasis; "Fact" label | Coffee terraces |
| `--ink` | `#1E1A16` | Body text | — |
| `--stone` | `#5E564C` | Captions, metadata | — |

### 3.2 Verified contrast (WCAG 2.x ratios, computed)

| Pair (text on ground) | Ratio | Use |
|---|---|---|
| `ink` on `gypsum` | 15.1 | Body text |
| `indigo` on `gypsum` | 12.3 | Headings |
| `stone` on `gypsum` | 6.3 | Captions |
| `mudbrick` on `gypsum` | 4.9 | Kickers, links (≥ 9 pt caps or bold) |
| `crimson` on `gypsum` | 6.5 | "Myth" label |
| `terrace` on `gypsum` | 5.4 | "Fact" label |
| `ink` on `sand` | 13.1 | Text in callouts |
| `stone` on `sand` | 5.5 | Captions in callouts |
| `crimson` on `sand` | 5.6 | Labels in callouts |
| `terrace` on `sand` | 4.7 | Labels in callouts (bold only) |
| `gypsum` on `night` | 16.1 | Text on dark |
| `lamp-soft` on `night` | 13.3 | Display on dark |
| `lamp` on `night` | 9.1 | Accent on dark |
| `lamp` on `indigo` | 7.0 | Accent on dark |
| `gypsum` on `mudbrick` | 4.9 | Reversed labels (bold ≥ 10 pt) |

**Forbidden pairs (fail contrast):** `lamp` on `gypsum` (1.8) · `mudbrick` on `sand` (4.2, use `indigo` or `ink` instead) · `mudbrick` on `night` (3.3).

### 3.3 Machine-readable tokens

```json
{
  "color": {
    "night": "#0B1426", "indigo": "#1B2B4D",
    "lamp": "#F2A83B", "lamp-soft": "#FFD58A",
    "gypsum": "#F6EFE2", "sand": "#EADFC8",
    "mudbrick": "#A4502B", "crimson": "#9E2A2B", "terrace": "#3E6B4A",
    "ink": "#1E1A16", "stone": "#5E564C"
  }
}
```

```css
:root{
  --night:#0B1426; --indigo:#1B2B4D; --lamp:#F2A83B; --lamp-soft:#FFD58A;
  --gypsum:#F6EFE2; --sand:#EADFC8; --mudbrick:#A4502B; --crimson:#9E2A2B;
  --terrace:#3E6B4A; --ink:#1E1A16; --stone:#5E564C;
}
```

**Print color:** build in sRGB for ebook; for the paperback convert with the printer profile KDP specifies and re-check `lamp` and `night` after conversion (deep blues and saturated ambers shift most). Keep rich black for large dark areas; use plain K 100 for body text only.

---

## 4. Typography

All families are open-licence (SIL OFL) and available on Google Fonts. Embed them; do not rely on system fonts.

| Role | Family | Weights | Notes |
|---|---|---|---|
| Display (title, part, chapter, pull quote) | **DM Serif Display** | Regular, Italic | High-contrast serif; holds up at thumbnail size |
| Text | **Source Serif 4** | Regular, Italic, Semibold, Bold | Book text, captions, decks |
| Labels (kicker, takeaways label, folios) | **Source Sans 3** | Semibold, Bold | Always uppercase with tracking |
| Arabic accent only | **Reem Kufi** (wordmark) · **Amiri** (inline Arabic) | Regular | The word **اليمن** as an optional cover/part-opener ornament; do not set long Arabic text |

**Diacritics and apostrophes.** The text uses ʿ/' transliteration marks (Sana'a, Rub' al-Khali, *'urf*). Use typographic apostrophes (’) consistently, and confirm the chosen fonts render *ʿ ʾ ā ī ū* if they are ever added.

### 4.1 Type scale — paperback (6 × 9 in)

| Style | Font | Size / leading | Spacing | Color |
|---|---|---|---|---|
| Book title (title page) | DM Serif Display | 40 / 42 pt | caps, +10 tracking | `indigo` |
| Part title | DM Serif Display | 34 / 38 pt | — | `indigo` |
| Part label ("PART ONE") | Source Sans 3 Bold | 9 pt | caps, +220 | `mudbrick` |
| Chapter number+title (H2) | DM Serif Display | 28 / 32 pt | — | `indigo` |
| Kicker | Source Sans 3 Semibold | 8.5 / 12 pt | caps, +160 | `mudbrick` |
| Deck | Source Serif 4 Italic | 13 / 19 pt | — | `stone` |
| Section heading (H3) | Source Serif 4 Semibold | 13 / 17 pt | space before 18 pt, after 4 pt | `indigo` |
| Body | Source Serif 4 Regular | 10.5 / 15.5 pt | justified, hyphenation on, 2-line widow/orphan control | `ink` |
| Body — first paragraph after heading | Source Serif 4 | 10.5 / 15.5 pt | no indent | `ink` |
| Body — following paragraphs | Source Serif 4 | 10.5 / 15.5 pt | first-line indent 1.2 em, no extra space | `ink` |
| Pull quote | DM Serif Display Italic | 17 / 23 pt | centered or hung; lamp rule | `indigo` |
| Caption | Source Sans 3 Regular | 8.5 / 12 pt | — | `stone` |
| List item | Source Serif 4 | 10.5 / 15 pt | hanging indent 14 pt, bullet in `mudbrick` | `ink` |
| Box label ("IN BRIEF") | Source Sans 3 Bold | 8.5 pt | caps, +180 | `mudbrick` |
| Running head / folio | Source Sans 3 Semibold | 8 pt | caps, +120 | `stone` |

### 4.2 Type scale — ebook (reflowable)

Do not force font sizes. Use relative units and let the reader's device choose the face: body `1em`; H2 `1.85em`; H3 `1.2em`; kicker `0.72em` caps; deck `1.05em` italic; caption `0.8em`; pull quote `1.3em` italic. Embed **DM Serif Display** for headings only; leave body to the reader's default face (embedding body fonts is optional and adds to file size).

---

## 5. Cover system

### 5.1 Specs

| Item | Ebook | Paperback (later) |
|---|---|---|
| Size | **1600 × 2560 px** (ratio 1:1.6), sRGB, JPEG or TIFF | 6 × 9 in trim + 0.125 in bleed all sides; spine width from KDP's cover calculator once the final page count is known |
| Resolution | ≥ 300 dpi at that size where applicable | 300 dpi, PDF/X-1a or print-ready PDF per KDP |
| Safe zone | 6 % margin each side (96 px) | 0.25 in inside trim |
| Title text must match | KDP title field exactly | same |

### 5.2 Wireframe (portrait, % of cover height from top)

```
0–6 %      margin (optional Arabic ornament اليمن, small, --lamp-soft)
6–30 %     "YEMEN"  — DM Serif Display, caps, color --gypsum; sized so the word
           spans 78–88 % of cover width (≈ 10–11 % of cover height in cap-height;
           let the width rule decide)
30–37 %    "Beyond the Headlines" — DM Serif Display Italic, color --lamp-soft,
           x-height ≥ 3 % of cover height
37–82 %    HERO IMAGE zone (CV-1): glowing qamariyyah in a tower-house facade.
           The glow is the focal point at ≈ 58 % height, optical center.
82–89 %    Subtitle — Source Sans 3 Semibold caps +160, --gypsum, ≥ 1.7 % of height
           "A SHORT INTRODUCTION TO ITS HISTORY, PEOPLE, AND CULTURE"
89–95 %    Author — Source Sans 3 Bold caps +220, --lamp-soft, ≥ 2.2 % of height
           "MOOHIALDIN AL-QUDAIMI"
Ground: --night, with the image blending into it by a vertical gradient (top 35 % = near-solid night for type contrast).
```

**Thumbnail test (mandatory before approval):** export at 160 × 256 px and at 100 × 160 px. Pass only if (a) "YEMEN" is instantly legible, (b) the glow is clearly the focal point, (c) the author name is still readable at 160 px, (d) the cover still looks distinct beside a row of beige and white covers. No element may be removed by the thumbnail that is essential to the message.

**What to retire from the old cover:** the "GO" paper-plane (it implies a travel guide), the beige scrapbook collage, the multi-image tape-and-torn-paper layering, the year "2026" as a cover element, and the tiny subtitle.

### 5.3 Cover copy

- **Front tagline (optional, ≤ 9 words, not part of metadata):** *The ancient country the world only knows from the news.*
- **Back cover (≈ 95 words):**

> You already know a Yemeni word: *mocha*.
>
> Yet most of what the world knows about Yemen comes from headlines. Behind them is one of the oldest continuously inhabited places on Earth — a country of mountain terraces, mud-brick skyscrapers, glowing stained-glass windows, a canyon civilization, a volcanic port, and an island where dragon's blood trees grow.
>
> In one sitting, this short book shows you the Yemen that headlines miss: its ancient kingdoms, its people and customs, the tribe as it really is, the coffee that began here, and the diaspora that reshaped the Indian Ocean.
>
> **Not a travel guide. An introduction to the country behind the headlines.**

### 5.4 Alternates (A/B test candidates)

- **CV-2** — *Vertical Country* illustrated poster (more editorial, warmer).
- **CV-3** — *Single Light* minimal cover (most striking at thumbnail; hero is built from the glow and a real vector map assembled in InDesign).

---

## 6. Page architecture

### 6.1 Formats

| Format | Spec |
|---|---|
| Ebook | Reflowable EPUB (KDP converts); cover separate (§5.1) |
| Paperback | 6 × 9 in trim; interior in `--gypsum`-tinted paper only if the printer allows; otherwise white paper and no full-page tint |

### 6.2 Paperback grid

| Item | Value |
|---|---|
| Trim | 6 × 9 in (152.4 × 228.6 mm) |
| Margins | Top 0.80 in · Bottom 0.90 in · Inside **0.85 in** · Outside 0.65 in (KDP's minimum inside margin depends on page count — confirm on KDP) |
| Bleed | 0.125 in (images that touch the edge only) |
| Columns | 1 column; baseline grid 15.5 pt; text box height snaps to the grid |
| Estimated length | ~64–80 pages once openers and images are set (final count decides spine) |
| Running head | Left page: book title · right page: current chapter title. None on part/chapter openers, blank pages, or full-page images |
| Folio | Bottom outside; none on openers |
| Page order | Half-title → Title page → Rights → Note → Contents → Start Here → At a Glance → Ten Things → Parts/Chapters → Closing → Quick Reference (Timeline, Glossary, Sources) → Author → CTA |

### 6.3 Openers

- **Part opener:** full right-hand page (recto). Art slot in the upper 55 % (`OP-1…OP-5`); "PART ONE" label; part title; thin `--lamp` rule on dark parts or `--mudbrick` rule on light pages. Consider tinting the part-opener page in `--night` with `--gypsum` text (print: confirm the printer can hold the ink coverage; otherwise use the art on white paper).
- **Chapter opener:** starts on a new recto page or after a column of white space (≥ 1/3 page). Order: kicker → chapter number (small caps) + title → deck → hairline rule → body with a 3-line drop cap on the first paragraph (print only).

---

## 7. Markup → style map

The book file is Markdown with Pandoc-style fenced divs (`::: name … :::`). Map each construct to an InDesign paragraph/character/object style:

| Markup in the book file | InDesign style | Notes |
|---|---|---|
| YAML header | Document metadata | `title`, `subtitle`, `author`, `lang: en` |
| `::: titlepage` | **Title Page** (master page) | `# …` → *Book Title* |
| `::: subtitle` / `::: author` | *Subtitle*, *Author* | |
| `::: rights` | *Rights* | Small, centered, `stone` |
| `::: part` containing `# PART …` and `## …` | **Part Opener** (master page + *Part Label*, *Part Title*) | Recto, starts new spread |
| `## Chapter N · Title` | *Chapter Title* (H2) | Split at `·` into *Chapter Number* + *Chapter Title* |
| `## Start Here`, `## Contents`, `## A Note Before You Begin`, etc. | *Front Heading* | Same as Chapter Title, no number |
| `::: kicker` | *Kicker* | Appears **above** the chapter title in layout even though it follows it in the file (the file keeps it directly after the heading for reading clarity) |
| `::: deck` | *Deck* | |
| `### Heading` | *Section Heading* (H3) | |
| Body paragraphs | *Body* (first after a heading: *Body First*) | |
| `*italic*`, `**bold**`, `***bold italic***` | *Emphasis*, *Strong*, *Term* (bold italic = first use of a transliterated term) | |
| `::: pullquote` | *Pull Quote* (anchored object) | At most one per two-page spread |
| `::: takeaways` (with `### In Brief` or `### By the last page, you will be able to`) | **Takeaways Box**: fill `sand`, top rule `mudbrick` 2 pt, label *Box Label* | Keep together; never split across pages |
| `::: glance` | **Glance Panel**: two-column or bold-label list on `sand` | Used in "Yemen at a Glance" and for statistics in Chapter 10 (large numerals in DM Serif Display, `indigo`) |
| `::: myth` | **Myth Card**: `Myth:` label in `crimson`, `Fact:` label in `terrace`, pointer line in *Caption*; hairline between cards | Cards may flow two to a page; never split a card |
| `::: note` | **Note Box**: left rule `lamp` 3 pt (on dark) or `mudbrick` 3 pt (on light), fill `sand` | Used for time-sensitive and disclaimer text |
| `::: figure` containing `![…](…)` + italic caption | **Figure**: image + *Caption* | Alt text = the text inside `[...]`; caption = the italic line |
| `::: art-slot` | **Art Slot** (placeholder frame) | Fill with the image named in §10 (`OP-n`); remove the placeholder text before export |
| `::: toc` | *TOC* | Rebuild from real page numbers in print; link entries in EPUB |
| `::: timeline` | **Timeline**: bold date in `mudbrick`, event in body; vertical rule down the left | |
| `::: glossary` | **Glossary**: term in bold italic, definition in body; two-level hanging indent | |
| `::: author-bio` | *Author Bio* | |
| `::: cta` | **CTA Panel**: `night` fill with `gypsum` text and `lamp` links (print: boxed in `sand`) | |
| `- ` lists | *List* | |
| `---` between sections | *Section Break* ornament (a single centered qamariyyah glyph, BR-2) | |
| `> ` quotes | (not used) | |

---

## 8. Component specifications

1. **Chapter opener.** Kicker above the title; 3-line drop cap (print) in DM Serif Display, `indigo`; first line in small caps for the first 4–6 words.
2. **Pull quote.** One lamp-colored hairline (`--mudbrick` on light pages) above; no quotation marks; centered; max 3 lines at print width.
3. **Takeaways box ("In Brief").** 3 bullets max, each ≤ 20 words. Label *IN BRIEF*. Closes every chapter in Parts One–Five.
4. **Myth card.** Fixed anatomy: label *Myth:* + quoted claim → label *Fact:* + one paragraph → pointer *(→ Chapters …)*. Ten cards, same height class; they are the book's most shareable content.
5. **Glance panel.** Facts are a two-column grid in print (label left in `mudbrick` caps, value right). In ebook, a simple definition list.
6. **Note box.** Used for the opening disclaimer, "time-sensitive" markers, and the end-of-book information note.
7. **Figure.** Full measure; caption below; alt text always present. Maps carry no baked-in title (see §9.2).
8. **Timeline.** Entries in order; date column fixed width (1 in); no more than 15 rows.
9. **Glossary.** Alphabetical; term first; Arabic transliterations in italic.
10. **CTA panel.** Review request is a genuine request, never incentivized. Link placeholders must be replaced before upload.

**Accessibility:** alt text on every image; a logical heading order (one H1 per document, H2 chapters, H3 sections); no information conveyed by color alone (labels *Myth*/*Fact* are words, not just colors); minimum body size 10 pt print.

---

## 9. Imagery rules and audit

### 9.1 Rules

1. One warm light source per image; cool shadows (§2).
2. No text or fake Arabic inside generated images — type is set in InDesign.
3. People: backs, hands, silhouettes, or far figures; no identifiable faces; never in combat or distress.
4. No weapons, flags, soldiers, rubble or smoke. The *jambiya* appears only as a sheathed heritage object (Chapter 6).
5. Architecture accuracy matters: do not mix Sana'a (dark stone base, brick above, white gypsum tracery), Shibam (earthen mud-brick, uniform tan), Tarim (whitewashed palaces), Zabid (geometric brick decoration) or the Tihama (round reed huts).
6. Captions say what the image **is**. If an image is an illustration, say so ("Illustration:"). Do not caption AI imagery as a documentary photo of a named place.

### 9.2 Audit of the six interior images and the old cover

| File | Size (px) | Issues | Recommendation |
|---|---|---|---|
| `images/cover.png` | 1240 × 1754 | A4 ratio with white page margins; below Kindle's ideal; weak thumbnail | **Replace** (CV-1) |
| `images/geographic-regions.png` | 1376 × 768 | Useful content; Aden's blue shape reads as sea, not a port; labels in a different typeface; no scale or north arrow; Socotra is not marked as an inset | Redraw as a clean vector map from open geodata in InDesign/Illustrator using the palette; keep the same six regions |
| `images/qamariyyah-window.png` | 848 × 698 | Strongest image in the book; low resolution for print (≈ 141 dpi at 6 in) | Keep for the ebook; for print, upscale carefully or replace with a higher-resolution image in the same style |
| `images/mud-brick-towers-hadramawt.png` | 1200 × 896 | Good subject; low print resolution | Keep for ebook; upgrade for print |
| `images/stone-terraces-coffee.png` | 1264 × 848 | Good; low print resolution | Same |
| `images/dragons-blood-trees-socotra.png` | 1376 × 768 | Good; low print resolution; flat gray sky | Same |
| `images/hadrami-diaspora-trade-routes.png` | 1376 × 768 | Title baked into the image duplicates the caption; schematic, imprecise outlines for Yemen and the surrounding coasts | Redraw as vector; remove baked-in title; keep the six destinations (Gulf, East Africa & Zanzibar, Hyderabad, Singapore, Java) |

> **Disclosure.** Several of these images look AI-generated or composited. If so, Amazon KDP asks publishers to **disclose AI-generated content** when submitting the book — check the current KDP content-guidelines page before upload and answer truthfully. Captions currently read as documentary photographs of specific places; prefer "Illustration:" or replace with licensed photography.

### 9.3 Image register (every image slot in the book)

| Slot | Position | Source | Format | Alt text |
|---|---|---|---|---|
| Cover | Front cover | CV-1 (+ typography in InDesign) | 1600 × 2560 | "Cover of *Yemen: Beyond the Headlines*: a glowing stained-glass window in a tower house at dusk." |
| `OP-1` | Part One opener | OP-1 | 3:2, ≥ 3000 px wide | "Misty terraced highlands descending toward a coastal plain." |
| Fig. 1 | Ch. 1 | Redrawn map | vector | existing alt |
| `SC-01` *(optional)* | Ch. 1, Tihama | SC-01 | 3:2 | "Round reed huts with painted doors on Yemen's Red Sea coastal plain." |
| Fig. 2 | Ch. 2 | existing / SC-02 | 3:2 | existing alt |
| `OP-2` | Part Two opener | OP-2 | 3:2 | "Ancient South Arabian stone ruins at sunset." |
| `SC-03` *(optional)* | Ch. 3 | SC-03 | 3:2 | "Frankincense resin and a brazier." |
| Fig. 3, 4 | Ch. 4 | existing | as is | existing alt |
| `SC-04`, `SC-05` *(optional)* | Ch. 4 | SC-04/05 | 3:2 | per prompt |
| `OP-3` | Part Three opener | OP-3 | 3:2 | "Hands pouring coffee in a tower-house reception room." |
| `SC-09` *(optional)* | Ch. 6 | SC-09 | 3:2 | "A sheathed curved dagger on an embroidered belt." |
| `OP-4` | Part Four opener | OP-4 | 3:2 | "Aden's harbor wrapped around an extinct volcanic crater." |
| Fig. 5 | Ch. 7 | existing | as is | existing alt |
| `SC-06`, `SC-07` *(optional)* | Ch. 7 | SC-06/07 | 3:2 | per prompt |
| Fig. 6 | Ch. 8 | Redrawn map | vector | existing alt |
| `OP-5` | Part Five opener | OP-5 | 3:2 | "A quiet market street at dawn." |
| `SC-13` | Closing | SC-13 | 3:2 | "Sana'a rooftops at dawn." |

### 9.4 Export for ebook (to control delivery cost)

JPEG, sRGB, long edge ≤ 1600 px for interior images, quality 70–80, progressive; target ≤ 250 KB per image and ≤ 3 MB total. Vector maps export as PNG at 1600 px wide with a transparent or `gypsum` background. Cover is separate (≤ 50 MB per KDP; aim far smaller).

---

## 10. Visual prompt library

Built from the book's own passages. Each prompt quotes the line or fact it comes from, so the images stay faithful. Prompts are tool-agnostic (Midjourney, Flux, Imagen, Higgsfield, etc.). **Generate scenes without any text; set all type in InDesign.**

### 10.1 How to assemble a prompt

`[MASTER STYLE] + [SCENE] + [LIGHT] + [COMPOSITION] + [ANCHORS]` and always apply the **Global Negative**.

**MASTER STYLE**
> Documentary-cinematic photography with painterly restraint. The "lit from within" principle: one warm amber light source (a window, a lamp, sunrise) against deep indigo blue-hour shadows. Natural, slightly desaturated earth tones — dark basalt, fired brick, sun-baked mud, white gypsum, sand. Fine film grain, full-frame 35 mm look, shallow to medium depth of field, dignified, human, unromanticized. Generous calm negative space in the sky or on a wall for typography. No text.

**ANCHORS (repeat for continuity)** — palette: deep night indigo `#0B1426`, indigo `#1B2B4D`, amber lamp `#F2A83B`, soft gold `#FFD58A`, gypsum cream `#F6EFE2`, mud-brick terracotta `#A4502B`, dragon's-blood crimson `#9E2A2B`.

**GLOBAL NEGATIVE**
> text, letters, fake Arabic calligraphy, watermark, signage, logos, flags, soldiers, weapons, guns, rubble, explosions, smoke, camels in dunes, orientalist fantasy, genie lamps, cartoon, 3D render look, oversaturated colors, HDR halos, plastic skin, extra fingers, warped architecture, identifiable faces.

**Format rule (all scenes):** compose at **3:2 landscape** with the key subject inside the central 60 % so the image reframes cleanly to 1:1 and to 9:16 later. Cover prompts are portrait **1:1.6** (e.g., 1600 × 2560).

### 10.2 Brand elements

**BR-1 · Gypsum tracery tile (seamless)** — *Source: "decorated with white gypsum tracery around every window."*
> A seamless repeating pattern of white gypsum window-tracery geometry: interlocking arches, stepped crenellations, and eight-pointed stars, carved in low relief on dark fired-brick, lit from the upper left with soft shadows. Monochrome cream `#F6EFE2` on night indigo `#0B1426`, very low contrast so it can sit behind text at 8–12 % opacity. Flat, square tile, no text.

**BR-2 · Qamariyyah glyph (section ornament)** — *Source: "stained-glass fanlights — qamariyyat, literally 'little moons'."*
> A minimal emblem of a semicircular fanlight window with radiating glass segments like a rising sun, single-weight line style, symmetrical, in amber `#F2A83B` on transparent or night background, crisp geometric edges, 1:1, vector look. No text. (Redraw as a vector in InDesign/Illustrator for final use.)

**BR-3 · Paper and plaster texture** — *Source: sand, mud, gypsum surfaces.*
> A subtle plaster-and-paper texture: warm gypsum cream `#F6EFE2` with faint fibers and hand-troweled mineral variation, no marks, no stains, extremely low contrast, flat lighting, seamless, 1:1.

### 10.3 Cover candidates

**CV-1 · "The City Lit from Within" (recommended)** — *Source: "At night, stained-glass fanlights … glow from the upper floors. The effect is of a city illuminated from within."*
> [MASTER STYLE] A tall portrait view of the facade of a multi-storey Sana'a tower house at blue hour: dark basalt stone in the lower courses, lighter fired brick above, white gypsum tracery bordering every window. On an upper floor a single arched stained-glass fanlight (qamariyyah) glows intensely in amber, crimson and gold, with a fan of radiating segments, casting warm light onto the brickwork around it; a lower rectangular window glows softly behind simple curtains. Neighboring tower houses recede into deep indigo dusk with faint warm points of light. The upper third of the frame is a calm, clean deep-indigo twilight sky fading to near-black at the very top. Slight upward camera angle, the glowing window placed at the optical center, strong silhouette. Aspect 1:1.6, ultra-detailed, tactile brick texture, no text.

**CV-2 · "A Vertical Country" (editorial illustration alternate)** — *Source: "It is a vertical country of mountains, a tropical coast, an interior desert, a canyon civilization, a volcanic port, and an island that evolution forgot."*
> A tall, stylized gouache-and-ink poster illustration, six horizontal bands stacked vertically like geological strata, each a different landscape connected by a single glowing window-light that moves from band to band: misty coffee terraces; a hot coastal plain with round reed huts; a pale gravel plateau; a canyon of earthen tower houses; a crescent harbor around an extinct volcano with a lateen-sail dhow; and, at the very bottom, an umbrella-shaped dragon's blood tree on a rocky island. Palette strictly night indigo, amber, gypsum cream, terracotta and one note of crimson; flat shapes, subtle paper grain, a sky area at the top left empty for the title. Aspect 1:1.6, no text.

**CV-3 · "Single Light" (minimal alternate)** — *Source: "Both facts are true. Neither is the whole story."*
> Minimalist cover background: a deep night-indigo field with an ultra-fine gypsum-tracery pattern barely visible, and one luminous amber fan-shaped stained-glass window floating slightly above center, radiating a soft warm glow that fades into the dark; gentle film grain; large clean negative space above and below for a typographic title and for a silhouette of Yemen's coastline to be added later as a vector in InDesign. Aspect 1:1.6, no text.

### 10.4 Part openers (3:2)

**OP-1 · The Land** — *Source Ch. 1: "terraced hillsides dense with agriculture … the air is cool, the light sharp, the sky enormous."*
> [MASTER STYLE] Dawn over Yemen's western highlands: steep stone-walled agricultural terraces stepping down mist-filled valleys, sharp ridgelines catching the first amber light, a thread of path winding between terraces, and far below a hint of hot coastal plain. Cool indigo shadows, one band of warm gold on the highest ridge, expansive sky with soft cloud. 3:2, subject in the central 60 %, sky empty at top.

**OP-2 · The Deep Past and the Built World** — *Source Ch. 3: "The Marib Dam … an enormous dam held back seasonal floodwaters."*
> [MASTER STYLE] The weathered stone sluices and massive masonry walls of an ancient South Arabian dam in a dry wadi at sunset, huge carefully fitted blocks, a long shadow across the valley floor, distant low mountains in indigo haze, a single warm band of sun on the stone. Epic but quiet; no tourists, no modern structures. 3:2.

**OP-3 · The People** — *Source Ch. 5: "Offering food, coffee, and shelter to a guest is not a formality… it is a deeply internalized social obligation."*
> [MASTER STYLE] Interior of a top-floor mafraj reception room in a Sana'a tower house, late afternoon: low cushions along the walls, patterned carpet, a row of small windows topped with stained-glass fanlights throwing colored light across the floor. In the foreground the hands of a host pouring coffee into a small cup for an unseen guest; only hands and sleeves visible. Warm amber and rose reflections, deep indigo corners. 3:2, no faces.

**OP-4 · Yemen and the World** — *Source Ch. 9: "Aden is a port city, wrapped around the craters of extinct volcanoes … shaped by who arrived by sea."*
> [MASTER STYLE] Aden's harbor from the water at dawn: jagged volcanic crater rims in violet-brown, a crescent bay, Ottoman-era and British-era stone buildings along the waterfront, a wooden dhow with a triangular sail in the foreground with a modern cargo vessel small in the distance, warm gold light on the water. Layered, calm, peaceful; no military vessels, no damage. 3:2.

**OP-5 · Today** — *Source Ch. 10: "What gets lost in these headlines is ordinary life … Markets still open."*
> [MASTER STYLE] A narrow stone market lane in an old Yemeni city at first light: shopkeepers raising shutters, baskets of produce, a few figures seen from behind or as soft silhouettes, warm string-lights and lamplight against cool blue morning shadows, steam from a tea vendor. Quiet, hopeful, ordinary; intact buildings only. 3:2, no faces, no damage.

### 10.5 Scene prompts (chapter-level)

**SC-01 · Tihama** — *Ch. 1: "round reed huts and brightly painted buildings."*
> [MASTER STYLE] Round conical thatched reed huts with painted wooden doors and low woven-reed fences on a flat hot coastal plain, warm early-morning light, hazy sea-air sky, a woman's silhouette in the far distance carrying a basket, African-influenced village layout, palm trees. 3:2.

**SC-02 · Dragon's blood tree** — *Ch. 2: "dense, umbrella-shaped canopy and crimson-red resin."*
> [MASTER STYLE] A single dragon's blood tree (*Dracaena cinnabari*) in close-medium view on a limestone plateau, dense umbrella canopy of stiff green leaves against low mist, a thick pale trunk with beads of dark crimson resin, a few younger trees behind and a cliff edge dissolving into cloud; late golden hour, long shadows. 3:2.

**SC-03 · Frankincense road** — *Ch. 3: "exporting frankincense and myrrh along caravan routes that stretched to the Mediterranean."*
> [MASTER STYLE] Macro still life: tears of pale-gold frankincense resin and dark myrrh on a worn stone slab beside a small clay brazier releasing a thin curl of fragrant smoke; in the soft-focus background a line of laden pack animals and drivers in silhouette crossing a ridge at dusk. Warm light, indigo shadows. 3:2.

**SC-04 · Tarim** — *Ch. 4: "whitewashed palaces and mansions in a style that mixes Yemeni traditions with influences brought home by merchants … Southeast Asia."*
> [MASTER STYLE] A grand whitewashed multi-storey mansion in a Hadramawt oasis town, cream lime-washed walls with elaborate carved wooden shutters and decorative cornices, a tall square minaret behind it, palms in the foreground, warm late sun, sky deep blue. Subtle Southeast-Asian-inspired detailing in the woodwork. 3:2.

**SC-05 · Zabid** — *Ch. 4: "geometric brick decoration reaches a level of refinement that reflects centuries of scholarly prestige."*
> [MASTER STYLE] A close, frontal study of a historic facade in Zabid: red fired-brick wall with intricate geometric patterns picked out in white lime-wash — interlocking diamonds and stepped motifs around a carved wooden door, soft raking afternoon light revealing the relief. Architectural detail photography. 3:2.

**SC-06 · Coffee harvest** — *Ch. 7: "smallholder farmers who often irrigate by hand."*
> [MASTER STYLE] Close view of a farmer's hands harvesting ripe red coffee cherries from a branch on a stone-walled highland terrace, glossy green leaves, drops of mist on the leaves, the terraced slope receding in soft focus behind, early morning gold light. Hands and forearms only, no face. 3:2.

**SC-07 · Saltah** — *Ch. 7: "a meat-and-vegetable stew topped with a frothy fenugreek sauce called hulbah."*
> [MASTER STYLE] A communal Yemeni table seen from slightly above: a heavy stone bowl of bubbling saltah topped with pale frothy hulbah, torn flatbread around it, small dishes, a comb of dark Wadi Do'an honey on a plate, hands reaching in from the edges; warm lamplight, indigo shadows, rich textures. 3:2.

**SC-08 · Afternoon salon** — *Ch. 7: "the afternoon qat session functions as a salon — a space for conversation, negotiation, poetry, gossip, and community bonding."*
> [MASTER STYLE] A wide, quiet view of a mafraj at golden hour: men seated on cushions in a circle in conversation, seen mostly from behind or in soft silhouette; sunlit stained-glass fanlights above, a tray of small cups in the center, a bundle of green leaves on a cloth. Warm dust-lit atmosphere, a sense of talk and listening. 3:2, no faces.

**SC-09 · The jambiya** — *Ch. 6: "more akin to wearing a school tie or a family crest than carrying a weapon."*
> [MASTER STYLE] Detail photograph of a sheathed curved dagger (jambiya) worn on an embroidered belt at the waist of a man in traditional clothing, cropped at chest and hip so no face is visible; ornate silver-work on the sheath, never drawn; shallow depth of field, a warm window glow behind. Heritage object, calm tone. 3:2.

**SC-10 · The monsoon route** — *Ch. 8: "The Hadrami migration followed monsoon winds."*
> [MASTER STYLE] A wooden dhow with a large triangular lateen sail on an open indigo sea at dawn, a lone warm lantern on deck, rolling swells, the sail catching the first gold light; in the far distance a thin line of coast; sense of long distance and the monsoon wind. 3:2.

**SC-11 · The grandmother in Jakarta** — *Closing: "a Hadrami grandmother in Jakarta who still speaks the dialect of Wadi Do'an."*
> [MASTER STYLE] An elderly woman seen from behind, seated at an open window in a modest Jakarta apartment at dusk, a framed old photograph of a mud-brick tower town on the sill, the skyline of the city's rooftops and a distant minaret in indigo twilight, a warm lamp behind her. Intimate, quiet, nostalgic; no face. 3:2.

**SC-12 · Headlines versus reality (concept)** — *Opening: "Both facts are true. Neither is the whole story."*
> [MASTER STYLE] A split composition: the left half is a grayscale, grainy layer of overlapping blurred newsprint with no readable text; the right half transitions into full warm color — the glowing stained-glass fanlight of a Sana'a tower house, then terraces and a dragon's blood tree behind it. The boundary is a torn paper edge where the colors begin to spill across. Strong center focus, calm negative space. 3:2.

**SC-13 · Closing dawn** — *Closing: "It is Sana'a's stained-glass fanlights glowing at dusk."*
> [MASTER STYLE] Sana'a rooftops at first light: tower houses with white gypsum tracery in cool blue shadow, a few fanlights still faintly glowing as the sun rises behind the old city, a thin line of warm gold on the horizon, quiet. Bookends the cover. 3:2.

### 10.6 Continuity checks before accepting any image

- Does it show **one** warm light source against a cool field?
- Is the architecture correct for the place named? (§9.1 #5)
- No text, no flags, no weapons, no faces, no damage?
- Is there calm space for type (cover, openers)?
- Does it still read at 160 px wide (cover only)?
- Does the caption describe it honestly (§9.1 #6)?

---

## 11. EPUB / Kindle technical notes

- **Structure:** one H1 for the book; `## Chapter…` headings generate the navigation (NCX/Nav). A logical TOC page must also exist in the book body (included).
- **Images:** inline `<img>` with `alt`; max width 100 %; no baked-in page margins; JPEG ≤ 1600 px (§9.4).
- **Fonts:** embed DM Serif Display for headings only; body inherits the reader's device font.
- **Boxes:** implement as `<aside>` or `<div class>` with border and background from tokens; ensure dark-mode readers keep sufficient contrast (avoid `lamp` text on light backgrounds).
- **Drop caps / running heads / folios:** print only.
- **Look Inside:** the first ~10 % of the file is what a shopper previews. The file is ordered so the preview shows the title page, the honest note, the hook ("Start Here"), "Yemen at a Glance", and the ten myths — the book's strongest, most shareable content.
- **Metadata:** title and subtitle exactly as in §1.4; author name identical to the cover; language English (US); the description and 7 backend keywords are a separate deliverable.

---

## 12. Hand-off checklist, open items, change log

### 12.1 Hand-off checklist for Claude InDesign

- [ ] `YEMEN-BEYOND-THE-HEADLINES.md` (text) and this file (system).
- [ ] Install fonts: DM Serif Display, Source Serif 4, Source Sans 3, Reem Kufi, Amiri.
- [ ] Create swatches from §3 and paragraph/character/object styles from §4, §7, §8.
- [ ] Build master pages: Title, Part Opener, Chapter Opener, Body Recto/Verso, Back Matter.
- [ ] Import text; apply styles per §7; place images per §9.3; set captions and alt text.
- [ ] Build the cover from CV-1 at 1600 × 2560 using §5.2; run the thumbnail test.
- [ ] Redraw both maps as vectors; export ebook JPEG/PNG at the sizes in §9.4.
- [ ] Export: EPUB (reflowable), print PDF (after KDP template with final page count), cover files.
- [ ] Replace every `[bracketed placeholder]` (ISBN/edition, author bio, CTA links) before export.

### 12.2 Open items — verify before publishing (not changed silently)

1. **Southern Yemen, 2025–26.** Chapter 10 states that the Southern Transitional Council "in late 2025 made rapid advances across southern governorates." Events in the south moved quickly; **re-check the current situation** and update the "Who Holds What" paragraph. (The original also said the advances included "Aden itself"; that phrase was dropped because it needs confirmation.)
2. **Shibam height.** The text says buildings "reach up to eight stories." Several sources give a higher range; verify against UNESCO.
3. **Sana'a house count.** Changed from "roughly 6,500" to "more than 6,000" to match the commonly cited UNESCO wording; verify.
4. **Socotra separation date.** The text now says "millions of years" in all summary references and keeps the hedged "at least six million years, and possibly twenty" in Chapter 2.
5. **Coffee figures.** "~20,000 tonnes per year" and "exceeding $100 per kilogram" — add a source.
6. **"Reportedly more Hadramis abroad than at home"** by the early twentieth century — add a source.
7. **Sources list.** Confirm: *Tribes in Yemen: An Anthology* attribution to Marieke Brandt; the publication year of Jacobsen's book; the vague "Najwa Adra, contributions…" entry; and that the four 2025–2026 online sources exist as cited.
8. **Qat restriction** in the former South before 1990 (the original said "banned"; now "restricted") — verify the precise policy.
9. **"Level 4" wording** — only the U.S. uses "Level 4: Do Not Travel"; others use their own highest-warning wording (now reflected).
10. **Author name** — "Moohialdin Al-Qudaimi" (book/cover) vs "MOOHIALDIN ALQUDAIMI" (KDP). Choose one and match everywhere. Consider whether the author wants a spelling that readers search for.
11. **KDP pricing bands** and **AI-content disclosure** — confirm on KDP's help pages.
12. **Placeholders** — ISBN/edition line, author bio, next-book link, email sign-up link.

### 12.3 Editorial change log (content kept, structure changed)

| Change | Why |
|---|---|
| New title and subtitle; "Before You Go" becomes Chapter 11 | Match what the book is; remove travel-guide promise |
| Added: *A Note Before You Begin*, *Start Here* outcomes list, *Yemen at a Glance*, *Ten Things Most People Get Wrong* moved to the front | Hook and Look-Inside value; reader knows the payoff in the first minutes |
| Chapters reordered into five parts: Land → Deep Past & Built World → People → Yemen & the World → Today; Socotra moved up as Chapter 2 | A narrative arc from place to people to present; strongest visual material early |
| Chapter 11 (misconceptions) removed from the end and moved to the front with chapter pointers | Avoids repetition; makes the book skimmable |
| Section headings (H3) added inside each chapter; kickers and decks added; "In Brief" boxes added | Scannability; same facts, easier to digest |
| Aden/Ch. 10 politics de-duplicated | Same paragraphs appeared twice |
| Added: Timeline, Glossary, About the Author (placeholder), CTA | Reference value; conversion path |
| Wording edits: "Twenty-five pages…" → "A short book…"; "Western visitor/readers" → "outsiders" where it did not refer to Western media; "twenty million years" → "millions of years" (summary references); "Every cup of coffee … descends" → "Most of the world's Arabica coffee descends…"; "Level 4" phrasing; "Steve/Steven Caton" unified; "reportedly" added to the Hadrami population claim; "banned" → "restricted" for qat; Sana'a house count; "including Aden itself" removed | Accuracy and consistency; no change to the book's message |
| Ten myths: wording unchanged | Preserved verbatim |

---

## 13. Forward compatibility with the video phase

Nothing is decided here about animation, duration, sequence, music or voice. What this system prepares so the next phase can start quickly:

- **Tokens** (§3) are named and valued so a video design system can import them unchanged; all text/background pairs are pre-checked for contrast.
- **Type** (§4) uses open-licence fonts that can be embedded.
- **Prompts** (§10) are grounded in book passages, composed at 3:2 with the subject centered so they can be reframed to vertical later, and share one light logic so scenes cut together.
- **Hook candidates** already exist in the book: *"You already know a Yemeni word"* · *"Both facts are true. Neither is the whole story."* · *"Yemen is not waiting to be discovered."*
- The pipeline and checkpoints in `Claude Video Guide.pdf` and `video-production.skill` were read for context only and were **not** run.
