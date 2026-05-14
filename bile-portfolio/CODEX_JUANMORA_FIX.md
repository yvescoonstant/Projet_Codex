# Codex Fix — Make Bilé Portfolio closer to juanmora.co

The current version is too generic. Rework the portfolio so it feels much closer to juanmora.co in motion, layout rhythm and visual interaction, while keeping original content for Bilé Didier.

## Main correction
Do not make a standard portfolio template. Build a cinematic, editorial, scroll-driven experience.

## Visual direction to reproduce

### 1. Hero
- Full viewport hero.
- Giant typography taking most of the screen.
- Name split into oversized lines:
  - `Bilé`
  - `Didier`
- Text must be almost poster-like, not centered-card-like.
- Add a custom cursor / floating circular button that reacts to hover.
- Add photo treatment with large mask / crop, not simple profile card.
- Add small UI details: index numbers, tiny labels, coordinates, availability text.

### 2. Typography
- Use huge compressed / grotesk style typography.
- Strong negative letter spacing.
- Use text reveal animation line by line.
- Use kinetic text on scroll.
- Titles should feel like a design studio portfolio, not a SaaS landing page.

### 3. Scroll animation
Use GSAP + ScrollTrigger + Lenis.

Required animations:
- Smooth scroll with Lenis.
- Hero title parallax on scroll.
- Image scale and clip-path reveal.
- Section titles reveal with staggered letters or lines.
- Sticky sections for project showcase.
- Horizontal movement for selected work cards.
- Cursor follower.
- Menu links with magnetic hover.
- Footer huge text animation.

### 4. Layout
- Avoid too many rounded SaaS cards.
- Use large empty space.
- Use editorial grid.
- Project cards should feel like interactive case-study panels.
- Use asymmetry.
- Add section numbering:
  - 01 / About
  - 02 / Work
  - 03 / Expertise
  - 04 / Contact

### 5. Colors
Primary version should be close to:
- Background: #0B0B0B or #F1EEE8 depending on section
- Text: #F4F1EA / #0B0B0B
- Accent: #D7FF3F or royal blue #2457FF
- Use accent very sparingly.

### 6. Page sections
Build the site as one fluid landing page:

1. Loader / intro
2. Hero
3. Manifesto sentence
4. About Bilé
5. Expertise
6. Selected Work
7. Skills / Tools marquee
8. Contact / huge footer

### 7. Replace generic copy with stronger portfolio copy

Hero:
`Bilé Didier`
`Marketing & Communication Analyst`
`I turn market signals into clear communication and measurable growth.`

Manifesto:
`Marketing is not only visibility. It is clarity, timing and measurable impact.`

About:
`Bilé Didier is a Munich-based Communication & Media Management student combining marketing, communication, data analysis and business development.`

Selected work:
- Axis Communications — Demand Generation & Brand Awareness
- Aboisso Rathaus — Digitalization & Financial Process Optimization
- BRASSIVOIRE — Predictive Cost Analysis & Supply Chain Optimization
- Sud Comoé Caoutchouc — Operations & Infrastructure Support

### 8. Technical requirements
Use:
- Next.js App Router
- Tailwind CSS
- GSAP
- ScrollTrigger
- Lenis
- Framer Motion only for small micro-interactions if needed

Install if missing:
```bash
npm install gsap lenis framer-motion lucide-react
```

### 9. Files to update
Update or create:
- `app/page.tsx`
- `app/globals.css`
- `components/SmoothScroll.tsx`
- `components/CustomCursor.tsx`
- `components/AnimatedText.tsx`
- `components/ProjectRail.tsx`

### 10. Important design warning
The current version looks too much like a clean corporate template. Rebuild it to look more like a creative director / Webflow award-style portfolio.

Less:
- SaaS cards
- symmetrical grid
- generic hero buttons
- dashboard style

More:
- huge typography
- scroll choreography
- dramatic spacing
- sticky motion
- custom cursor
- editorial feeling
- immersive project showcase

### 11. Acceptance criteria
The design is accepted only if:
- the hero feels like a poster;
- the page has visible scroll-based motion;
- selected work is not a static card grid;
- typography dominates the layout;
- the design feels closer to juanmora.co than to a normal portfolio template;
- mobile version remains clean and responsive.
