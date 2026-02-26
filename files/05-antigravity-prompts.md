# Antigravity Prompts — Prashant Mishra Profile Page

Use these prompts in sequence. Each prompt builds on the previous. Reference the design system and page structure files alongside these.

---

## PROMPT 1 — Project Setup & Base Layout

```
Create a single-page personal portfolio website for Prashant Mishra, an AI Product Builder and Operations Leader based in Mumbai.

Tech stack: HTML, CSS (no frameworks), vanilla JS. Single file.

Design system:
- Background: #0A0A0A
- Surface/cards: #111111
- Borders/dividers: #1A1A1A
- Primary text: #F0F0F0
- Secondary text: #888888
- Accent colour: #A8E6CF (pastel green) — use this sparingly for highlights, CTAs, tags, and hover states
- Font: Inter (Google Fonts)
- Max content width: 900px, centered

Set up the full page skeleton with these sections in order:
1. Sticky navigation bar
2. Hero
3. About
4. Projects
5. Experience
6. Skills
7. Contact
8. Footer

Use section IDs: #hero, #about, #projects, #experience, #skills, #contact

Leave placeholder content in each section for now. Focus on getting the layout, spacing, and dark aesthetic right.
```

---

## PROMPT 2 — Navigation Bar

```
Build the sticky navigation bar for the page.

- Left: "Prashant Mishra" in white, font-weight 600, acts as scroll-to-top link
- Right: nav links — About · Projects · Experience · Skills · Contact
- Nav link colour: #888888, hover: #A8E6CF, transition 0.2s
- Background: transparent when at top of page, #0A0A0A with border-bottom 1px solid #1A1A1A when scrolled
- Use JS to add/remove a .scrolled class on scroll
- No border-radius, flat and clean
- Mobile: collapse links to a minimal hamburger or hide below 600px with a toggle
```

---

## PROMPT 3 — Hero Section

```
Build the Hero section (#hero).

Layout: centered, min-height 100vh, flexbox column, centered content

Elements (top to bottom):
1. Circular profile photo placeholder — 120px diameter, border 2px solid #A8E6CF, background #1A1A1A, show initials "PM" in #A8E6CF as placeholder
2. Name: "Prashant Mishra" — 56px, font-weight 700, color #F0F0F0
3. Role line: "AI Product Builder · Operations Leader · Freelance AI Consultant" — 18px, color #888888
4. One-liner: "I run every facet of business with AI as my strategic assistant — building products, automating workflows, and shipping things that work." — 16px, color #AAAAAA, max-width 600px, line-height 1.7, centered
5. Two buttons side by side:
   - Primary: "View My Work" — background #A8E6CF, color #0A0A0A, font-weight 600, padding 12px 28px, no border-radius (or 4px max), links to #projects
   - Secondary: "Get In Touch" — border 1px solid #A8E6CF, color #A8E6CF, transparent background, same sizing, links to #contact
6. Subtle gap between each element

No background image. Very subtle noise texture or faint dot grid on the background is acceptable but keep it extremely minimal.
```

---

## PROMPT 4 — About Section

```
Build the About Me section (#about).

Section label above heading: "// about" — 13px, color #A8E6CF, font monospace, letter-spacing 0.1em
Section heading: "About Me" — 32px, font-weight 600, color #F0F0F0

Layout: Two columns on desktop — text (left, 60%) and stats (right, 40%)

Left column — three short paragraphs:
"I'm a Mumbai-based AI generalist who bridges the gap between business operations and AI product development. With nearly a decade of experience across tech publishing, EdTech, cybersecurity, and short-term rentals — I've always been close to the product, the process, and the people."

"Over the last few years, I've gone deep on AI: building custom automation pipelines, shipping AI-native web apps, and helping D2C brands create high-quality AI-generated media. I don't just consult on AI — I build with it daily."

"Currently building my own AI projects through AiTribe while actively looking for a full-time role where I can bring this rare mix of operational leadership and AI product thinking to a team."

Right column — 4 stat highlights displayed as large number + label:
- "40%" → "Workload reduction via AI tools"
- "18" → "Technical titles published"
- "29" → "Live training sessions delivered"
- "3+" → "Live AI products shipped"

Stats: Number in 40px bold #A8E6CF, label in 13px #888888 below it. 2x2 grid layout.

Body text colour: #CCCCCC, line-height: 1.8
```

---

## PROMPT 5 — Projects Section

```
Build the Projects section (#projects).

Section label: "// projects" — monospace, 13px, #A8E6CF
Section heading: "Projects" — 32px, 600 weight

Layout: 2-column grid on desktop, 1-column on mobile. Gap: 24px.

Build 4 project cards. Each card:
- Background: #111111
- Border: 1px solid #1A1A1A
- Border-radius: 8px
- Padding: 28px
- Hover: border-color transitions to #A8E6CF, transition 0.2s

Card contents:
1. Status badge (top right): "Live" in #A8E6CF or "Building" in #888888 — small, 11px, uppercase, letter-spacing 0.1em
2. Project title — 18px, 600 weight, #F0F0F0
3. Short description — 14px, #888888, line-height 1.7
4. Tags — small pill badges, background #1A1A1A, color #A8E6CF, 11px, padding 4px 10px, border-radius 4px
5. Link button at bottom — "View Project →" in #A8E6CF, no background, 14px, hover underline

Projects data:

1. AIBNB — AI-Native Short-Term Rental Platform
Status: Live
URL: https://ai-bnb-india-883495399816.us-west1.run.app/
Description: A modular AI agent system for the Indian short-term rental market. Features LLM-native chat for 24/7 guest support and dynamic pricing models.
Tags: AI Agents · LLM · Short-Term Rentals

2. FrameFlow — AI Storyboarding App
Status: Service Available
URL: https://github.com/PrashantforAI/frameflow-production
Description: An AI-powered storyboarding tool for brands and creators. Currently offered as a done-for-you service while being refined based on real-world use cases.
Tags: AI Storyboarding · Generative AI · Content

3. AiTribe D2C Photography
Status: Live
URL: https://aitribe-d2-c-photography.vercel.app/
Description: AI-generated product photography for D2C clothing brands — consistent, high-quality images at a fraction of traditional photography costs.
Tags: AI Photography · D2C · Generative Media

4. AiTribe Agency
Status: Building
URL: https://aitribe.co.in
Description: My AI agency offering AI-native app development, automation pipelines, and AI media services for businesses.
Tags: AI Agency · Automation · Consulting
```

---

## PROMPT 6 — Experience Section

```
Build the Work Experience section (#experience).

Section label: "// experience" — monospace, 13px, #A8E6CF
Section heading: "Experience" — 32px, 600 weight

Layout: Vertical timeline. Left vertical line in #1A1A1A. Each entry has a dot marker in #A8E6CF on the line.

Experience entries (newest first):

1. Pine Stays · Head of Business Operations
Nov 2022 – Jan 2026 · Mumbai
- Led end-to-end operations for a short-term rental platform
- Built custom AI tools reducing manual workload by 40%
- AI-driven lead scoring and channel attribution across Airbnb and B2B channels
- Google automation pipelines for demand forecasting and price prediction
- Personalized guest experience using AI behavior analysis

2. KnowledgeHut upGrad · Content Acquisition & Strategy
Nov 2021 – Oct 2022 · Mumbai
- Market research and competitive analysis for EdTech content in emerging tech categories

3. EC-Council · Senior Executive Acquisition Specialist
Apr 2020 – May 2021 · Mumbai
- Delivered cybersecurity training programs
- Negotiated author contracts and partnered with industry thought leaders

4. Packt · Acquisition Editor & Technical Editor
Aug 2016 – Mar 2020 · Mumbai
- Published 18 technical titles ensuring accuracy and quality
- Delivered 29 live training sessions (Avg CSAT 8.2/10)
- Managed key account partnerships and mentored 5 new consultants

5. Appco Group India · Corporate Trainer
Jul 2015 – May 2016 · Mumbai

Styling:
- Company name: 16px, 600 weight, #F0F0F0
- Role: 14px, #A8E6CF
- Date/location: 13px, #555555
- Bullets: 14px, #888888, line-height 1.7
```

---

## PROMPT 7 — Skills Section

```
Build the Skills & Tech Stack section (#skills).

Section label: "// skills" — monospace, 13px, #A8E6CF
Section heading: "Skills & Stack" — 32px, 600 weight

Layout: 4 groups in a 2x2 grid on desktop, stacked on mobile.

Each group:
- Group label: 11px, uppercase, letter-spacing 0.1em, color #555555, monospace
- Tags below label: pill badges — background #1A1A1A, color #A8E6CF, 12px, padding 5px 12px, border-radius 4px, gap 8px, flex-wrap

Groups:

AI & Automation:
Google AI Studio · Google Antigravity · Vertex AI · AI Agents · Prompt Engineering · LLM Integration · Zapier · Make · Weavy.ai · Vibe Coding

Operations & Business:
Business Operations · Revenue Optimization · Demand Forecasting · Lead Scoring · Multi-Channel Sales · Customer Experience

Tools & Platforms:
Looker Studio · Google Workspace · Zoho CRM · Notion · Vercel · GitHub

Product & Strategy:
Rapid Prototyping · Agentic Workflow Design · AI-Native Product Development · Market Research · Content Strategy
```

---

## PROMPT 8 — Contact Section & Footer

```
Build the Contact section (#contact) and Footer.

CONTACT SECTION:
- Background: slightly different from page — use #0D0D0D or a subtle border-top in #1A1A1A
- Section label: "// contact" — monospace, 13px, #A8E6CF
- Heading: "Open to Full-Time Roles & Freelance Projects" — 32px, 600 weight
- Subtext: "Whether you're looking for an AI-savvy operations leader, a product builder, or an AI consultant for your brand — I'd love to talk." — 16px, #888888

Contact options (horizontal row, centered):
- Email: 735prashant@gmail.com — styled as link in #A8E6CF
- LinkedIn: linkedin.com/in/prashant-m — styled as link
- Phone: +91-9820882232

Optional simple contact form:
- Name input, Email input, Message textarea, Send button (primary style)
- Input background: #111111, border: 1px solid #1A1A1A, focus border: #A8E6CF, text #F0F0F0
- No backend needed — form can use mailto: action

FOOTER:
- Minimal, 60px height
- Left: "© 2026 Prashant Mishra"
- Right: GitHub + LinkedIn icon links, color #555555 → hover #A8E6CF
- Center or right: "Built with AI" in #333333
- Border-top: 1px solid #1A1A1A
```

---

## PROMPT 9 — Polish & Animations

```
Add final polish and subtle animations to the page:

1. Fade-in-up on scroll: All sections fade in (opacity 0 → 1, translateY 20px → 0) when they enter the viewport. Use IntersectionObserver. Duration: 0.5s ease.

2. Smooth scroll: Add scroll-behavior: smooth to html.

3. Active nav link: Highlight the current section's nav link in #A8E6CF as user scrolls.

4. Project card hover: Already has border colour change — also add a very subtle box-shadow: 0 0 20px rgba(168, 230, 207, 0.05) on hover.

5. Button hover states:
   - Primary button: slight brightness increase
   - Secondary button: fill with #A8E6CF, text becomes #0A0A0A

6. Profile photo: When the real photo is added, replace the PM initials placeholder. The circular crop and green border should remain.

7. Meta tags: Add proper Open Graph and meta description tags for the page:
   - Title: "Prashant Mishra — AI Product Builder & Operations Leader"
   - Description: "Mumbai-based AI generalist building AI-native products and automations. Open to full-time roles and freelance projects."
   - og:image: placeholder for now

8. Final check: Ensure mobile responsiveness — test at 375px, 768px, 1200px breakpoints.
```

---

## PROMPT 10 — Profile Photo Integration

```
Replace the profile photo placeholder in the Hero section.

The profile photo has been provided. Update the circular image element:
- Replace the initials "PM" placeholder with the actual <img> tag
- Maintain: width 120px, height 120px, border-radius 50%, border 2px solid #A8E6CF
- Add object-fit: cover to ensure the photo crops cleanly
- Ensure it looks good on both dark backgrounds and mobile screens
```

---

## NOTES FOR ANTIGRAVITY USE

- Run prompts 1–9 in sequence before deploying
- Prompt 10 is run separately once Prashant provides his headshot
- After each prompt, review the output and tweak before moving to the next
- Keep all code in a single HTML file
- The final file should be deployable directly to Vercel or any static host
