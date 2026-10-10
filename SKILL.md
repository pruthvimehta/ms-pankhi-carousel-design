---
name: ms-pankhi-carousel-design
description: >
  Design and render visual Instagram carousels for Pruthvi Mehta (@ms_pankhi) — a CA and content creator based in Ahmedabad. Use this skill whenever a carousel needs to be visually designed, rendered as slides, or exported as images. Covers layout rules, color palette, typography, slide structure, and export specs. Always use this skill when building carousel visuals for @ms_pankhi — never skip it.
---

# @ms_pankhi Carousel Design Skill

## Quick-Start Checklist

Before rendering any carousel, verify every slide has:

- Warm cream background #f5f0e8 on content slides (never pure white)
- Black rounded pill for category label at the top of each content slide
- Italic serif for slide number or title (Playfair Display)
- One red keyword #d63031 per content slide
- Arrows using → (never - or > or em dashes)
- @ms_pankhi handle, bottom centre, on every slide
- Thin separator line #d4cfc6 above handle
- Page number bottom right
- No emojis. No em dashes.
- Gold accent #e6b830 used sparingly (max 2 elements per slide)
- Cover: photo slot + black pill headline + SWIPE>> button
- Last slide: explicit save/comment/share CTA

---

## Format and Dimensions

- Aspect ratio: 4:5 portrait — 1080 × 1350px — all slides, always
- Slide count: 6–9 slides. Always ends with a CTA slide.
- Export: Puppeteer headless Chrome, deviceScaleFactor 2, viewport 540×675 → output 1080×1350

---

## Colour Palette

| Role | Hex | Usage |
|---|---|---|
| Background (warm cream) | #f5f0e8 | All content slide backgrounds |
| Pure off-white | #faf8f4 | Alternate bg, some CTA slides |
| Black | #1a1a1a | Pills, labels, body text |
| Red accent | #d63031 | Keyword highlights in body text |
| Gold/amber accent | #e6b830 | Cover title highlight, decorative dots |
| Orange accent | #f5820a | Career/LinkedIn carousels only |
| White | #ffffff | Text inside black pills |
| Handle grey | #888888 | @ms_pankhi bottom text |
| Ghost photo overlay | rgba(245,240,232,0.55) | Over faded Pruthvi photo in content slides |

**Rule:** Never use cold grey. Never use green or blue as accents.

---

## Typography

| Element | Font | Size | Weight |
|---|---|---|---|
| Cover headline | DM Sans bold | 52–60px | 800 |
| Category pill | DM Sans uppercase | 14px | 600 |
| Slide number/title | Playfair Display italic | 42–52px | 400 |
| Body term | DM Sans | 18–22px | 700 |
| Body definition | DM Sans | 18–22px | 400 |
| Red keyword | DM Sans | 18–22px | 400 |
| Handle / page num | DM Sans | 13px | 300 |
| SWIPE>> button | DM Sans | 13px | 500 |
| Prompt text | Space Mono | 15px | 400 |

Google Fonts import:

```html
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital@0;1&family=DM+Sans:wght@300;400;500;600;700;800&family=Space+Mono&display=swap" rel="stylesheet">
```

---

## Slide 1: Cover Rules

- Full-bleed personal photo of Pruthvi (fills entire slide). If no photo provided → placeholder box: "ADD YOUR PHOTO HERE". Never generate a fake face.
- Optional: thin gold border inset ~30px (1.5px solid #e6b830)
- Black pill headline overlaid on lower third:
  - Line 1: hook word/number in gold #e6b830
  - Line 2: rest of title in white
  - Pill: background #1a1a1a, border-radius 14px, padding 12px 24px
- SWIPE>> black pill, bottom right
- @ms_pankhi small, bottom centre, white

**Cover headline pattern:**

```
[Number or hook — gold]
[Topic phrase — white]
```

Examples:
- "5 Ways / I use AI to save 10 hours"
- "7 Money Mistakes / you're making in your 20s"
- "10 CA Facts / nobody tells you"

---

## Content Slides (Slides 2 to second-last)

### Background
Warm cream #f5f0e8. Ghost photo of Pruthvi centred, opacity 10–15%, slightly desaturated. If no photo → plain cream only.

### Category Pill (top of slide)

```css
background: #1a1a1a;
color: #ffffff;
border-radius: 20px;
padding: 6px 16px;
font: 600 13px/1 'DM Sans';
letter-spacing: 0.15em;
text-transform: uppercase;
```

Position: top-left or top-centre, 36px from top.

### Content Format A — Term or List Style
Used in: Money, CA Life, AI tools, Career tips

```
[Bold term] → [Regular definition — one keyword in red]
```

- 5–8 items per slide
- Line spacing: 1.8–2.2
- Left aligned, 44px left margin
- One word per slide in #d63031 (not bold)

### Content Format B — Numbered Card Style
Used in: AI productivity, Creator Life, LinkedIn carousels

White rounded card (border-radius 20px, border 1.5px solid #e0dbd2):

- Amber icon square (40×40px, border-radius 10px, background #f5c542)
- Italic serif number title: One, Two, Three…
- "Time saved: ~X hours" — right-aligned, monospace, small (for AI carousels)
- Body paragraph with one red keyword
- "Example prompt:" section with quoted text (for AI carousels)
- "Tools: X, Y" at bottom of card (for AI carousels)

### Bottom Strip (all content slides)

```css
border-top: 0.5px solid #d4cfc6;   /* 36px from bottom */
.handle { color: #888; font: 300 13px 'DM Sans'; text-align: center; }
.page-num { color: #888; font: 300 13px 'DM Sans'; float: right; }
```

### Optional: Left-Edge Gold Dot
8px circle #e6b830 on left edge at vertical midpoint (progress indicator).

---

## CTA Slide (Last Slide)

Default style for @ms_pankhi: minimal text on plain cream, centred, no photo.

Example:
```
I don't use many AI tools.
Just 2–3.
And that's enough.

Save. Share. Follow.
```

CTA must include one of:
- "Save this"
- "Comment [X]"
- "Share with [someone]"
- "Drop in comments"

---

## HTML/CSS Quick Reference

```css
:root {
  --bg-cream: #f5f0e8;
  --bg-offwhite: #faf8f4;
  --text-black: #1a1a1a;
  --text-muted: #888888;
  --text-white: #ffffff;
  --accent-red: #d63031;
  --accent-gold: #e6b830;
  --accent-orange: #f5820a;
  --border-light: #d4cfc6;
  --border-card: #e0dbd2;
  --font-serif: 'Playfair Display', serif;
  --font-sans: 'DM Sans', sans-serif;
  --font-mono: 'Space Mono', monospace;
  --slide-width: 1080px;
  --slide-height: 1350px;
  --slide-padding: 44px;
}

.slide {
  width: var(--slide-width);
  height: var(--slide-height);
  background: var(--bg-cream);
  position: relative;
  overflow: hidden;
  padding: var(--slide-padding);
  box-sizing: border-box;
  font-family: var(--font-sans);
}

.category-pill {
  display: inline-block;
  background: var(--text-black);
  color: var(--text-white);
  border-radius: 20px;
  padding: 6px 16px;
  font-size: 13px;
  font-weight: 600;
  letter-spacing: 0.15em;
  text-transform: uppercase;
}

.content-row {
  display: flex;
  align-items: baseline;
  gap: 10px;
  margin-bottom: 20px;
  line-height: 1.9;
}
.term { font-weight: 700; font-size: 20px; }
.arrow { color: var(--text-black); }
.definition { font-weight: 400; font-size: 20px; }
.keyword { color: var(--accent-red); }

.bottom-strip {
  position: absolute;
  bottom: 36px;
  left: var(--slide-padding);
  right: var(--slide-padding);
  border-top: 0.5px solid var(--border-light);
  padding-top: 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.handle { font-size: 13px; font-weight: 300; color: var(--text-muted); }
.page-num { position: absolute; right: 0; font-size: 13px; font-weight: 300; color: var(--text-muted); }
```

---

## Puppeteer Export

```js
const browser = await puppeteer.launch({
  executablePath: '/opt/google/chrome/chrome',
  args: ['--no-sandbox']
});
const page = await browser.newPage();
await page.setViewport({ width: 540, height: 675, deviceScaleFactor: 2 });
await page.goto(`file://${htmlPath}`);
await page.evaluateHandle('document.fonts.ready');
await page.waitForTimeout(300);

for (let i = 0; i < slideCount; i++) {
  await page.screenshot({
    path: `slide_${i+1}.png`,
    clip: { x: 0, y: i * 675, width: 540, height: 675 }
  });
}
await browser.close();
```

---

## Topic-Specific Overrides

| Topic | Background | Accent | Format |
|---|---|---|---|
| Money / Finance / Indian context | White or light grey acceptable | Gold or none | Format A, styled stat cards |
| AI tools / productivity | Strictly cream | Gold | Format A or B, ghost photo mandatory |
| Career / LinkedIn / Creator Life | Cream or off-white | Orange #f5820a | Format B, centred layout |
| CA Life | Strictly cream | Gold | Format A, ghost photo mandatory |

For money and finance carousels: add "Source: [name]" in tiny muted text at bottom of relevant slides.

---

## Category Pills by Topic

| Topic | Pill Label |
|---|---|
| Money and Finance | MONEY |
| AI and Tools | AI |
| Career and Work | CAREER |
| CA Life | CA LIFE |
| Creator Life | CREATOR |

---

## Common Mistakes to Avoid

- Pure white #ffffff as content background → use cream #f5f0e8
- Handle in a coloured box → plain text only
- Green or blue accents → only red for keywords, gold for highlights
- Em dashes anywhere → remove them
- Emojis → never in carousels
- Dashes instead of arrows → always use →
- Skipping category pill → mandatory on every content slide
- Cover without photo slot → always include placeholder if no photo given
- Gold used on more than 2 elements per slide → keep it sparingly decorative
