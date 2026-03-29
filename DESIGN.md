# Design System — Jon's ALS Protocol

## Product Context
- **What this is:** A D2C content platform where Jon Edy (6+ year ALS survivor, still walking) shares his exact supplement protocol, mindset framework, and daily routine with other ALS patients and caregivers.
- **Who it's for:** ALS patients (many with motor limitations, fatigue) and their caregivers (overwhelmed, time-poor, making purchasing decisions)
- **Space/industry:** ALS health / patient-led supplement guidance
- **Project type:** Personal brand editorial site with digital product sales
- **Competitor gap:** Simplesa Nutrition is a cold Shopify store; ALS Health Journey is a text-wall WordPress blog. Nobody has built anything warm, human, or trust-driven.

## Aesthetic Direction
- **Direction:** Organic/Warm Editorial
- **Decoration level:** Intentional — subtle warmth signals (soft shadows, rounded corners, warm backgrounds). Every visual element earns its place by making the visitor feel safer.
- **Mood:** Sitting down with a friend who's been through it. Warm, grounded, unhurried. Not clinical, not raw. Like a well-designed memoir.
- **Reference sites:** Maven Clinic (warmth + credibility), The ALS Association (awareness colors)

## Typography
- **Display/Hero:** Fraunces (variable, optical sizing) — soft humanist serif with warmth. Says "personal story" not "newspaper." Google Fonts, free.
- **Body:** Source Sans 3 (400, 600, 700) — readable, accessible, familiar. 18px minimum, 1.8 line height.
- **UI/Labels:** Source Sans 3 600
- **Data/Tables:** Source Sans 3 (tabular-nums)
- **Code:** Not applicable
- **Loading:** Google Fonts CDN: `family=Fraunces:opsz,wght@9..144,400;9..144,600;9..144,700;9..144,800;9..144,900&family=Source+Sans+3:wght@300;400;500;600;700;800&display=swap`
- **Scale:**
  - Hero H1: 56px / 3.5rem, Fraunces 800
  - H1: 40px / 2.5rem, Fraunces 700
  - H2: 32px / 2rem, Fraunces 700
  - H3: 24px / 1.5rem, Fraunces 600
  - Body: 18px / 1.125rem, Source Sans 3 400
  - Body large: 20px / 1.25rem, Source Sans 3 400
  - Small/Caption: 15px / 0.9375rem, Source Sans 3 400
  - Button: 18px / 1.125rem, Source Sans 3 700

## Color
- **Approach:** Restrained — navy carries authority, red is accent-only for CTAs/emphasis. Warm neutrals create safety.
- **Primary (Navy):** #1E3A5F — trust, authority, calm. Used for headers, nav, text accents.
- **Accent (ALS Red):** #C41E3A — urgency, action. Used sparingly: CTA buttons, badges, emphasis only. Never as a surface/background color.
- **Accent hover:** #A91B32
- **Background (Warm Cream):** #FAF8F5 — living room, not hospital. Main page background.
- **Surface (White):** #FFFFFF — cards, content blocks, modals.
- **Surface Alt:** #F5F3F0 — section breaks, alternating backgrounds.
- **Text Primary:** #1A1A1A — warm near-black, not pure #000.
- **Text Secondary:** #4A4A4A — body text, descriptions.
- **Text Muted:** #727272 — captions, disclaimers, metadata. (Updated from #7A7A7A to pass WCAG AA 4.5:1 on cream background.)
- **Border:** #E8E4E0 — warm gray border, not cold gray.
- **Semantic:**
  - Success: #1A7431 (bg: #E8F5EC)
  - Warning: #92610E (bg: #FFF8E7)
  - Error: #B91C1C (bg: #FEF2F2)
  - Info: #1E3A5F (bg: #EFF4FA)
- **Dark mode:** Not planned for Phase 1. Audience uses default system settings.

## Spacing
- **Base unit:** 8px
- **Density:** Spacious — ALS patients and older caregivers need breathing room
- **Scale:** 2xs(4) xs(8) sm(12) md(16) lg(24) xl(32) 2xl(48) 3xl(64) 4xl(96) 5xl(128)
- **Section padding:** 80-128px vertical (py-20 to py-32 in Tailwind)
- **Card padding:** 24-32px
- **Minimum touch target:** 48px (WCAG)

## Layout
- **Approach:** Single-column narrative flow — this is a story, not a dashboard
- **Grid:** Single column with max-width container. No sidebars.
- **Max content width:** 720px for body text, 1024px for cards/grids, 1280px for full-width sections
- **Border radius:** sm: 6px, md: 10px, lg: 16px, xl: 24px, full: 9999px
- **Cards:** White surface, 1px warm border (#E8E4E0), md radius (10px), subtle shadow on hover

## Motion
- **Approach:** Minimal-functional — ALS patients may have cognitive fatigue. Motion should never distract.
- **Allowed:** Subtle fade-in on scroll (opacity + small translateY), button hover transitions, modal open/close
- **Not allowed:** Parallax, bouncing, auto-playing animations, scroll-jacking, carousel auto-rotation
- **Easing:** enter(ease-out) exit(ease-in) move(ease-in-out)
- **Duration:** micro(100ms) short(200ms) medium(300ms)

## Accessibility (Non-negotiable)
- **Minimum body text:** 18px
- **Minimum touch target:** 48px height and width
- **Color contrast:** WCAG AA minimum (4.5:1 for text, 3:1 for large text)
- **Focus styles:** 2px solid #C41E3A, 2px offset, 4px border-radius
- **Skip-to-content link:** Always present
- **Heading hierarchy:** Strict (no skipping levels)
- **Link text:** Descriptive (never "click here")
- **Images:** Always include alt text
- **Font size controls:** A+/A- buttons in header (match AdvantageGuide pattern)

## Video Integration
- **Hero:** Still photo of Jon with prominent "Watch Jon's Story" play button — never autoplay
- **Blog posts:** Embed YouTube videos inline where they add context
- **Protocol page:** Video testimonial/walkthrough as social proof
- **Technical:** Standard YouTube iframe embeds, lazy-loaded

## Homepage Flow (Narrative Scroll)
1. Hero: Jon's face + "6+ Years with ALS. Still Walking." + dual CTA
2. Trust bar: Key stats (years, supplements, still walking)
3. Jon's story teaser: Photo + brief narrative + "Read full story" link
4. What's inside: 3 cards (Supplement Stack, Daily Routine, Mindset Framework)
5. Supplement preview: 3 featured supplements with "details in full protocol" tease
6. Email capture: Lead magnet offer ("Jon's Top 5 Supplements for ALS")
7. Comparison table: Jon's Protocol vs Simplesa vs DIY Research
8. Medical disclaimer
9. Footer

## Decisions Log
| Date | Decision | Rationale |
|------|----------|-----------|
| 2026-03-28 | Fraunces for display typography | Warmer and more personal than Merriweather. Humanist optical serif says "personal story" not "institution." |
| 2026-03-28 | Red as accent-only, navy as primary | Red triggers urgency/alarm — wrong first impression for scared patients. Navy conveys trust/calm. Red reserved for CTAs. |
| 2026-03-28 | Single-column narrative layout | Homepage is a trust journey, not a product catalog. Linear scroll builds emotional trust sequentially. |
| 2026-03-28 | No dark mode in Phase 1 | Audience primarily uses default settings. Complexity not justified at this stage. |
| 2026-03-28 | Minimal motion only | ALS patients experience cognitive fatigue. Animations must never distract or disorient. |
