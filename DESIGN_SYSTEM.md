# DESIGN SYSTEM — INDIA: THE ARCHITECTURE OF GLOBAL TRADE

## Color Palette

### Primary Colors
| Name | Hex | Usage |
|------|-----|-------|
| Midnight Navy | `#0a0e27` | Primary background, deep scenes |
| Deep Navy | `#111633` | Secondary background, cards |
| Dark Slate | `#1a1f3a` | Elevated surfaces, panels |

### Accent Colors
| Name | Hex | Usage |
|------|-----|-------|
| Indian Saffron | `#e8732a` | Primary accent, highlights, CTA |
| Warm Saffron | `#f59e3f` | Secondary accent, gradients |
| Muted Gold | `#c9a84c` | Tertiary accent, subtle highlights |
| Metallic Gold | `#d4a853` | Data visualization, emphasis |

### Supporting Colors
| Name | Hex | Usage |
|------|-----|-------|
| Restrained Emerald | `#2d8a6e` | Positive indicators, secondary data |
| Deep Emerald | `#1b6b52` | Supporting green elements |
| Soft White | `#f0ece4` | Primary text on dark backgrounds |
| Muted Cream | `#d4cfc5` | Secondary text, subtitles |
| Cool Grey | `#8a8d9c` | Tertiary text, labels |
| Border Grey | `#2a2f4a` | Subtle borders, dividers |

### Semantic Colors
| Name | Hex | Usage |
|------|-----|-------|
| Positive/Growth | `#2d8a6e` | Upward trends, exports |
| Negative/Decline | `#c44b3f` | Downward trends, deficit |
| Neutral | `#5c6080` | Neutral data, baseline |
| Warning | `#d4a853` | Attention, important notes |

## Typography

### Font Stack
```css
--font-display: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
--font-mono: 'JetBrains Mono', 'Fira Code', 'Consolas', monospace;
```

### Type Scale
| Element | Size | Weight | Letter Spacing | Line Height |
|---------|------|--------|---------------|-------------|
| Chapter Title | 72px | 800 | -0.03em | 1.0 |
| Slide Title | 42px | 700 | -0.02em | 1.15 |
| Section Subtitle | 28px | 600 | -0.01em | 1.3 |
| Body Large | 22px | 400 | 0 | 1.6 |
| Body | 18px | 400 | 0 | 1.65 |
| Caption/Label | 14px | 500 | 0.03em | 1.4 |
| Data/Stats | 56px | 700 | -0.02em | 1.0 |
| Stat Unit | 18px | 500 | 0.05em | 1.0 |

### Typography Rules
- All display text uses sentence case
- Chapter numbers use large, muted display numerals
- Data labels are uppercase with wide letter spacing
- Uzbek text uses Latin script throughout
- No text smaller than 14px on presentation slides

## Layout System

### Grid
- Base unit: 8px
- Slide dimensions: 1920 × 1080px (16:9)
- Safe margins: 80px on all sides (4.2% of width)
- Content max width: 1760px
- Two-column gap: 64px
- Card padding: 40px
- Section spacing: 48px

### Visual Hierarchy
1. **Hero Elements:** Full-bleed, centered, maximum visual impact
2. **Primary Content:** Left-aligned, within safe margins
3. **Supporting Data:** Right column or bottom third
4. **Citations/Sources:** Bottom margin, small, muted

## Animation Language

### Timing Functions
```css
--ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
--ease-in-out-smooth: cubic-bezier(0.4, 0, 0.2, 1);
--ease-subtle: cubic-bezier(0.25, 0.1, 0.25, 1);
```

### Duration Scale
| Type | Duration | Usage |
|------|----------|-------|
| Micro | 200ms | Hover states, button feedback |
| Fast | 400ms | Element reveals, fades |
| Medium | 700ms | Slide transitions, chart animations |
| Slow | 1200ms | Scene transitions, map animations |
| Dramatic | 2000ms | Opening sequence, chapter reveals |

### Motion Principles
1. Elements enter from the direction of narrative flow (usually bottom or right)
2. Stagger children by 80ms for list/grid reveals
3. Maps always animate from a global view to a focused view
4. Charts build data progressively, never all at once
5. Text reveals line by line for key statements
6. Transitions between scenes use a subtle fade-through-dark

### Slide Transitions
- Default: 600ms cross-fade with subtle scale (0.98 → 1.0)
- Chapter transitions: 800ms fade to near-black, then reveal new chapter
- Data transitions: Elements morph/transform when data changes

## Data Visualization Style

### Chart Colors (ordered)
1. Indian Saffron `#e8732a`
2. Muted Gold `#d4a853`
3. Restrained Emerald `#2d8a6e`
4. Cool Blue `#4a7fb5`
5. Warm Rose `#c44b3f`
6. Slate Purple `#7c6fa0`
7. Teal `#3a9e8f`
8. Amber `#d4963a`

### Chart Rules
- Always include axis labels and units
- Animate data entry progressively
- Use horizontal bar charts over vertical when possible for readability
- Donut charts over pie charts
- Include data source and reporting period as caption
- Gridlines at 20% opacity, never solid
- Chart backgrounds match slide background (no white boxes on dark slides)

## Iconography
- No cartoonish icons
- Use subtle, line-based icons where necessary
- Prefer typographic or geometric symbols
- Icons at 24px or 32px, stroke width 1.5px
- Color: Cool Grey or Muted Cream, never fully white

## Citation Format
- In-slide: Small text, bottom-right, format: "Source: [Organization], [Year]"
- Full references: APA-style in references slide
