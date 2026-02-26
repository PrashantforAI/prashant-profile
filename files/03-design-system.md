# Design System — Prashant Mishra Profile Page

## Design Philosophy
Dark, minimal, intentional. Every element earns its place. One pastel accent does all the heavy lifting for colour. No clutter, no noise — let the content breathe.

---

## Colour Palette

| Role | Value | Usage |
|------|-------|-------|
| Background (primary) | `#0A0A0A` | Main page background |
| Background (card/surface) | `#111111` | Cards, sections, containers |
| Background (subtle) | `#1A1A1A` | Hover states, borders, dividers |
| Text (primary) | `#F0F0F0` | Headings, body text |
| Text (secondary) | `#888888` | Subtitles, labels, dates |
| Text (muted) | `#555555` | Placeholders, less important info |
| Accent (pastel green) | `#A8E6CF` | CTAs, highlights, tags, hover states, underlines |
| Accent (muted green) | `#6BBF9A` | Secondary accent, borders on hover |

---

## Typography

### Font Family
- **Primary:** `Inter` (Google Fonts) — clean, modern, highly legible
- **Monospace (optional):** `JetBrains Mono` — for tags, tech stack labels

### Scale
| Element | Size | Weight | Colour |
|---------|------|--------|--------|
| Hero Name | 64px / 4rem | 700 | `#F0F0F0` |
| Hero Tagline | 20px / 1.25rem | 400 | `#888888` |
| Section Heading | 32px / 2rem | 600 | `#F0F0F0` |
| Card Title | 20px / 1.25rem | 600 | `#F0F0F0` |
| Body Text | 16px / 1rem | 400 | `#CCCCCC` |
| Labels / Tags | 12px / 0.75rem | 500 | `#A8E6CF` |
| Dates / Meta | 14px / 0.875rem | 400 | `#888888` |

---

## Layout

- **Max width:** 900px centered
- **Padding (mobile):** 24px
- **Padding (desktop):** 0 (centered container handles it)
- **Section spacing:** 100px–120px between major sections
- **Line height (body):** 1.7

---

## Components

### Navigation (Sticky Top Bar)
- Background: `#0A0A0A` with subtle bottom border `#1A1A1A`
- Logo/Name: left-aligned, `#F0F0F0`
- Nav links: right-aligned, `#888888` → hover `#A8E6CF`
- No border-radius, flat and minimal

### Hero Section
- Full viewport height (100vh)
- Profile photo: circular, 120px, subtle green border `#A8E6CF`
- Name in large weight
- Tagline below in muted colour
- One-liner paragraph
- Two CTA buttons side by side

### CTA Buttons
- **Primary:** Background `#A8E6CF`, text `#0A0A0A`, no border-radius (or 4px max), bold
- **Secondary:** Border `1px solid #A8E6CF`, text `#A8E6CF`, transparent background
- Hover: subtle opacity shift or background fill

### Project Cards
- Background: `#111111`
- Border: `1px solid #1A1A1A`
- Hover: border becomes `1px solid #A8E6CF`, subtle glow
- Title, description, tags, live link
- Tags: small pill style, `#A8E6CF` text, `#1A1A1A` background
- Border-radius: 8px

### Experience Timeline
- Left border line in `#1A1A1A`
- Dot markers in `#A8E6CF`
- Company name bold, role in muted colour
- Date range right-aligned or below in `#555555`

### Skills / Tech Stack
- Tag cloud or grid of pill badges
- Background `#1A1A1A`, text `#A8E6CF`
- Grouped by category with a small label header

### Contact Section
- Clean, centered
- Email as a styled link in `#A8E6CF`
- Social icons minimal, no colour — just `#888888` → hover `#A8E6CF`

---

## Motion & Interaction
- Keep animations minimal and purposeful
- Fade-in on scroll for sections (subtle, 0.3s)
- Hover transitions: 0.2s ease
- No bouncy or distracting animations

---

## Do's and Don'ts

### Do:
- Use lots of whitespace
- Let the accent green be the only colour that pops
- Keep cards flat with subtle borders
- Use consistent section spacing

### Don't:
- Use gradients (except a very subtle one on the hero if needed)
- Add multiple accent colours
- Use drop shadows heavily
- Crowd elements together
