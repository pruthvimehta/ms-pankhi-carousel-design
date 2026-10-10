# ms-pankhi-carousel-design

A Claude skill that designs and renders Instagram carousels for @ms_pankhi: 4:5 portrait slides (1080 x 1350), warm cream backgrounds, Playfair Display italics, red keyword highlights, and a clear CTA on the last slide.

## How to trigger it

- "Design a carousel for @ms_pankhi"
- "Render these slides as images"
- "Build the visuals for this carousel"
- "Export the carousel slides"

## How to install

1. Click **`<> Code`** → **`Download ZIP`**
2. Go to **[claude.ai](https://claude.ai)** → **Skills** → **Create Skill**
3. Upload the **ZIP file** directly → **Save**

## Requirements

- Slides are exported with Puppeteer (headless Chrome), so Node.js and Puppeteer are needed for image export.

## Repository structure

```
ms-pankhi-carousel-design/
├── SKILL.md
├── README.md
└── .claude-plugin/
    └── plugin.json
```

## How it works

The skill holds the layout rules, colour palette, typography, slide structure and export specs. Claude follows its checklist for every slide, then renders the slides as HTML and exports them as 1080 x 1350 images.

---

## Connect with Pruthvi

- Instagram: [instagram.com/ca.pruthvimehta](https://instagram.com/ca.pruthvimehta)
- LinkedIn: [linkedin.com/in/pruthvimehta](https://linkedin.com/in/pruthvimehta)
- YouTube: [youtube.com/@ca.pruthvimehta](https://youtube.com/@ca.pruthvimehta)
