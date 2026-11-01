# HANDOFF — INDIA: THE ARCHITECTURE OF GLOBAL TRADE

**Last Updated:** 2026-11-01T17:48:00+05:00
**Current Developer:** AI Assistant (Stage 1)
**Development Stage:** Stage 1 — Technical Reconnaissance & Creative Direction

## Technical Architecture

### Chosen Technology: Self-Contained HTML/CSS/JS Presentation

**Rationale:**
- No Node.js, npm, or build tools available on target machine
- Self-contained = zero dependencies, zero installation
- Full animation control via CSS animations + Canvas API + SVG
- Works offline by default (no CDN dependencies in final build)
- Opens directly in any browser (Edge confirmed available)
- Supports fullscreen via Fullscreen API
- Keyboard navigation built-in
- Export to PDF via browser print
- Single folder = easy to transfer via USB/email

**Rejected Alternatives:**
- React/Reveal.js: Requires Node.js (not available)
- PowerPoint: Cannot achieve required animation quality (trade routes, map reveals, particle systems)
- Python-based tools: Python not properly available
- Hosted web apps: Must work offline

### Project Folder Structure

```
INDIA THE ARCHITECTURE OF GLOBAL TRADE/
├── index.html                 # Main presentation file
├── css/
│   └── presentation.css       # All styles
├── js/
│   ├── engine.js              # Presentation engine (navigation, transitions, fullscreen)
│   ├── animations.js          # Animation controllers
│   ├── charts.js              # Data visualization (Canvas-based)
│   ├── maps.js                # India map + trade routes (SVG/Canvas)
│   └── data.js                # All data (trade stats, survey placeholders)
├── assets/
│   ├── india-map.svg          # India outline SVG
│   └── fonts/                 # Self-hosted Inter font files (woff2)
├── docs/
│   ├── presenter-script.md    # Full 17-minute Uzbek presenter script
│   ├── questionnaire.md       # Distributable survey in Uzbek
│   └── survey-template.md     # Template for entering actual survey responses
├── PROJECT_BRIEF.md
├── DESIGN_SYSTEM.md
├── PROJECT_STATUS.md
├── RESEARCH_SOURCES.md
├── HANDOFF.md
└── README.md                  # Launch instructions
```

### Key Implementation Decisions

1. **Single HTML entry point** — `index.html` loads all CSS/JS. No build step.
2. **Slide-based architecture** — Each slide is a `<section>` with `data-slide` attribute
3. **CSS-driven animations** — Intersection Observer triggers slide entry animations
4. **Canvas for complex visuals** — Map particles, trade route animations, chart rendering
5. **SVG for India map** — Scalable, animatable, precise
6. **No external CDN** — All fonts and assets bundled locally for offline use
7. **Keyboard controls** — Arrow keys, Space, Escape (fullscreen), number keys (jump)
8. **Touch support** — Swipe gestures for tablet presentation

### Dependencies

- **None.** Zero npm packages. Zero build tools. Pure browser APIs.
- Fonts: Inter (Google Fonts, self-hosted as woff2)
- Browser: Any modern browser (Edge, Chrome, Firefox)

### How to Run

1. Open `index.html` in Microsoft Edge (or any modern browser)
2. Press F11 or click fullscreen button for presentation mode
3. Use arrow keys or click to navigate
4. Press Escape to exit fullscreen

### How to Build/Modify

- Edit `index.html` for slide content
- Edit `js/data.js` to update statistics or survey data
- Edit `css/presentation.css` to adjust styling
- No compilation or build step needed

## Current Development Stage

**Stage 1 — Complete**
- Technology selected
- Design system defined
- Project structure planned
- Research initiated

## Exact Next Steps

1. **Receive research data** from research subagent
2. **Build Stage 2 opening prototype:**
   - Create `index.html` with presentation engine
   - Implement cinematic opening (India map reveal, particle system, title sequence)
   - Build one representative content slide
   - Build one data visualization slide
   - Implement keyboard navigation and fullscreen
3. **Present prototype for review** (Stage 3)
4. **Full production** of all 20+ slides (Stage 4)
5. **QA and delivery** (Stage 5)

## Known Bugs / Unfinished Features

- None yet (project not started beyond planning)

## Important Notes for Continuation

- All text content must be in **Uzbek Latin**
- Survey data must use **placeholders** (never fabricated)
- Statistics must cite **source and reporting period**
- Distinguish **merchandise trade** from **services trade**
- Distinguish **calendar year** from **fiscal year** (India FY = April–March)
- The presentation must **actually work** — test before delivering
