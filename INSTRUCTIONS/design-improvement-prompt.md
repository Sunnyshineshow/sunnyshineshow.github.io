# Design Improvement Prompt — Sunnyshineshow Static Website

You are improving the design of this static personal website:

- Repo: `sunnyshineshow.github.io`
- Main page: `index.html`
- Akane profile page: `project-akane.html`
- Assets: `images/`
- Deployment target: GitHub Pages / static hosting
- Do not introduce a frontend framework unless absolutely necessary.
- Keep the site simple, fast, static, and easy to maintain.

## Goal

Refine the visual design, UX, accessibility, motion, and polish of the website while preserving its current identity:

- `index.html` should feel like a sharp, confident personal portfolio for Sunnyshineshow.
- `project-akane.html` should feel like a premium editorial anime character/profile page for Akane Sakurai.
- Both pages should feel related, but not identical.
- The design must look handcrafted and intentional, not like a generic AI-generated template.

The target quality is closer to an official anime character website than a normal static profile page: layered, atmospheric, animated, responsive, and memorable.

## Reference Inspiration

Use these sites as inspiration for motion and dynamic presentation:

- `https://kaoruhana-anime.com/`
- `https://makeine-anime.com/`

Do not copy their assets, layouts, branding, or exact style. Study their principles:

- layered key visuals
- character foreground/background depth
- scroll-triggered reveals
- animated decorative motifs
- section-by-section visual choreography
- official-site style navigation and labels
- interactive focal elements
- visual banners and update cards
- subtle ambient movement
- strong first-screen staging

The goal is not to add random animation. The goal is to add **page choreography**.

## Current Design Notes

The site already has strong visual direction:

- Warm cream / editorial palette.
- Custom cursor and motion details.
- Large typographic hero sections.
- Strong Akane page atmosphere with sakura, Japanese editorial styling, gallery, Instagram section, and multilingual identity.
- Good image assets are already available.

However, the design can be improved in these areas:

1. Visual consistency between pages.
2. Navigation clarity and active states.
3. Mobile responsiveness and spacing.
4. Accessibility, keyboard focus, and reduced-motion support.
5. Content hierarchy and readability.
6. CTA clarity.
7. Placeholder links and unfinished footer actions.
8. Image loading behavior and performance.
9. More intentional section transitions.
10. Stronger polish in small details.
11. A cinematic opening scene.
12. Layered foreground/midground/background depth.
13. Scroll-triggered reveal choreography.
14. Anime official-site style graphic framing.
15. A signature interaction that makes the page feel alive.

## Design Direction

Use this direction:

**“Warm editorial portfolio meets personal operating system, with anime official-site motion staging.”**

The website should feel like a carefully designed personal dossier: quiet, refined, technical, intimate, polished, and alive.

For Akane specifically, the page should feel like:

**“A premium official character site for a gentle virtual secretary stationed inside Sunshineshow's Conference Rooms.”**

Avoid these generic patterns:

- Random glassmorphism cards.
- Overused gradient blobs.
- Excessive animated decorations.
- Generic SaaS-style hero sections.
- Bland centered layouts with no personality.
- Cramped cards or edge-to-edge mobile layouts.
- Decorative numbers that do not add meaning.
- Motion that exists only because animation is possible.

## Improvements to Make

### 1. Global Design System

Create a small, consistent design token system shared across both pages:

- Background colors
- Surface colors
- Border colors
- Text colors
- Accent colors
- Spacing scale
- Border radius scale
- Shadow style
- Typography roles
- Motion timing values
- Reveal animation values

The two pages may have different moods, but should share a subtle family resemblance.

Suggested direction:

- `index.html`: more technical, bold, portfolio-focused.
- `project-akane.html`: softer, editorial, elegant, sakura-inspired, anime official-site influenced.

Do not make everything identical. Create harmony, not sameness.

### 2. Typography

Improve type hierarchy.

For `index.html`:

- Keep the strong large name treatment.
- Improve readability in body sections.
- Make section headings more structured and intentional.
- Use consistent letter spacing for labels and nav items.
- Avoid overly tiny text on mobile.

For `project-akane.html`:

- Preserve the Japanese editorial feel.
- Keep serif/Japanese type personality.
- Improve long paragraph readability.
- Make captions and metadata more consistent.
- Ensure Japanese/English language switch does not cause awkward spacing.
- Use vertical Japanese text sparingly as a graphic element where it reinforces the official-character-site feeling.

### 3. Layout and Spacing

Audit all sections for spacing.

Fix:

- Sections that feel too close together.
- Cards that feel cramped.
- Text blocks that are too wide.
- Mobile spacing near viewport edges.
- Any vertical rhythm inconsistencies.
- Hero content alignment on smaller screens.

Use generous but disciplined spacing.

Mobile layout must feel intentionally designed, not just stacked.

### 4. Navigation

Improve navigation UX:

- Add clearer hover states.
- Add keyboard focus states.
- Make fixed nav readable over all backgrounds.
- Ensure mobile nav does not disappear without replacement if important.
- Consider a compact mobile menu or simplified anchor navigation.
- Add active/section-aware styling if feasible without overengineering.

For `project-akane.html`, ensure language toggle remains easy to find and use.

### 5. Hero Sections

Improve the first impression.

For `index.html`:

- The hero should clearly communicate:
  - Who Sunnyshineshow is.
  - What he does.
  - Why the visitor should continue.
- Add or refine a short supporting line under the main name.
- Make the certifications/badges feel more intentional and less floating-random.
- Ensure the CTA is visually strong but not loud.

For `project-akane.html`:

- Keep the cinematic Akane hero.
- Improve image/text balance.
- Ensure the hero still works beautifully on mobile.
- Make the first screen feel like an editorial anime cover, not just a web section.
- Add a layered key visual structure:
  - background environment layer
  - midground atmosphere layer
  - foreground Akane portrait / character layer
  - title/name typography layer
  - UI/dossier label layer
- Add a staged entrance sequence:
  - background appears first
  - Akane image eases in
  - Japanese name/title appears
  - profile metadata fades in
  - scroll cue appears last

### 6. Cinematic Layering and Parallax

Add controlled visual depth inspired by official anime websites.

Use multiple visual planes:

- background texture / environment
- faded character silhouette or scene image
- floating motifs
- main content cards
- foreground character/image accents
- fixed or sticky UI labels

Add subtle parallax where appropriate:

- background moves slower than scroll
- floating motifs drift gently
- section labels shift slightly
- gallery images reveal from alternating directions

Keep it lightweight. Use vanilla JavaScript and CSS transforms only. Avoid heavy libraries.

Respect `prefers-reduced-motion` and disable or greatly simplify parallax/reveals for users who request reduced motion.

### 7. Scroll-Triggered Reveal Choreography

Add a reusable reveal system with `IntersectionObserver`.

Each section should enter like a small scene:

1. Section label appears.
2. Heading slides/fades in.
3. Main visual/card appears.
4. Supporting copy follows.
5. Decorative motif settles last.

Use staggered reveals for:

- skill cards
- project cards
- profile facts
- language cards
- gallery images
- footer links

Do not reveal everything with the same animation. Keep the system consistent but vary direction and timing gently.

### 8. Anime Official-Site Graphic Framing

Add more graphic devices commonly seen in anime official sites, adapted to Akane's identity:

- oversized character name treatment
- vertical Japanese name strip: `桜井 茜`
- subtle official-profile labels
- special section banners
- small “status” or “dossier” labels
- soft decorative seals/stamps
- visual dividers between sections
- layered image cutouts
- section headers with English title + Japanese subtitle

Do not overdecorate. Spend boldness in a few key places.

### 9. Signature Interaction

Add one memorable interaction that makes the Akane page feel alive.

Recommended concept:

## Akane Dossier Panel

A floating or sticky profile panel that updates its active state based on the current section:

- Hero: `Personal Secretary`
- About: `Quiet Presence`
- Profile: `Dossier Open`
- Tasks: `Double-Checked`
- Languages: `EN / JP / TH`
- Gallery: `Memories`
- Origin: `Creator's Note`
- Instagram: `Daily Window`

It should feel like a quiet secretary status interface, not a loud game HUD.

If a sticky panel would clutter mobile, convert it to a compact section indicator or hide it gracefully.

### 10. Ambient Motion

Add subtle persistent motion to keep the page alive:

- layered sakura petals with varied size, speed, blur, and opacity
- slow floating paper slips or desk-note motifs
- soft light sweep on the hero
- very subtle rotating seal/stamp mark
- marquee/ticker divider with Akane identity text

Suggested ticker text:

```text
AKANE SAKURAI · PERSONAL SECRETARY · SUNSHINESHOW'S CONFERENCE ROOMS · EN / JP / TH
```

Keep ambient motion calm, sparse, and premium.

### 11. Foreground / Background Overlap

Add tasteful overlaps to move beyond flat section blocks:

- portrait partially overlaps a section boundary
- heading sits behind or beside image composition
- vertical text runs beside cards
- gallery images slightly break out of the grid
- background character silhouette sits behind copy
- decorative motifs cross section boundaries

Avoid overlap that harms readability.

### 12. Cards and Sections

Improve card design:

- Make skill/project/profile cards feel tactile and deliberate.
- Use consistent border, shadow, hover, and spacing behavior.
- Avoid generic equal-height boxes unless useful.
- Make hover states subtle and premium.
- Improve content scannability.

Each section should have a clear role:

- About: personal context.
- Skills: capability overview.
- Experience: timeline / credibility.
- Projects: artifacts and links.
- Contact: clear next action.
- Akane profile: character, role, capabilities, gallery, origin, Instagram.

For Akane, consider styling profile/task cards like:

- secretary desk notes
- dossier cards
- appointment slips
- character sheet panels
- soft editorial magazine blocks

### 13. CTA and Links

Improve all calls to action.

Current issues:

- Some footer links in `project-akane.html` are placeholders: `Email` and `Schedule` point to `#`.
- Contact actions should be clearer.
- External links should be visually distinguished.
- Buttons should have consistent styling.

Fix or clearly mark placeholder links.

Suggested actions:

- Main page:
  - Contact email
  - GitHub
  - Project Akane link

- Akane page:
  - Instagram
  - Email/contact if available
  - Back to Sunnyshineshow homepage
  - Optional “Return to top”

### 14. Accessibility

Add accessibility improvements:

- Visible keyboard focus states for links, buttons, language toggle, gallery items.
- Respect `prefers-reduced-motion`.
- Ensure sufficient contrast for muted text.
- Add meaningful `aria-label`s where needed.
- Ensure lightbox can close via Escape.
- Ensure lightbox focus behavior is reasonable.
- Do not hide the native cursor on touch devices.
- Avoid motion that makes reading difficult.
- Ensure image alt text is meaningful.
- Ensure animated decorative elements are hidden from screen readers.

### 15. Motion and Interaction

Keep motion elegant and restrained.

Preserve:

- Custom cursor where appropriate.
- Petal atmosphere on Akane page.
- Smooth transitions.
- Gallery lightbox.

Improve:

- Reduce excessive scattered animations.
- Make motion serve the page's story.
- Add reduced-motion fallback.
- Ensure hover effects do not cause layout shift.
- Keep performance smooth.
- Add section-aware reveal choreography.
- Add a clear motion hierarchy: hero animation > section reveals > hover feedback > ambient motion.

### 16. Image Handling

Improve image usage:

- Add `loading="lazy"` to non-critical images.
- Add dimensions where practical to reduce layout shift.
- Ensure hero images are prioritized visually.
- Avoid stretched or awkward image crops.
- Make gallery presentation more consistent.
- Check that every referenced image exists.

Do not replace the existing image assets unless explicitly asked.

### 17. Mobile Design

Mobile must be treated as first-class.

Check:

- Hero readability.
- Navigation access.
- Section padding.
- Card width.
- Gallery layout.
- Instagram embed behavior.
- Language toggle placement.
- Footer layout.
- Tap targets.
- Dossier panel behavior.
- Parallax/reveal behavior.

No clipped text, cramped cards, or viewport-edge crowding.

### 18. Performance

Keep the site lightweight.

Do:

- Keep it static.
- Avoid large new dependencies.
- Avoid framework migration.
- Avoid unnecessary JavaScript.
- Prefer CSS improvements.
- Keep animations GPU-friendly using `transform` and `opacity`.
- Lazy-load non-critical images.
- Use `IntersectionObserver` for reveal logic.

Do not:

- Add React/Vue/Next.
- Add build tooling.
- Add heavy animation libraries.
- Add external UI kits.
- Add large new media assets unless asked.

## Implementation Guidance

Use a small vanilla JavaScript layer for:

- scroll reveals
- parallax values
- active section detection
- dossier panel state
- lightbox improvements
- language toggle preservation
- reduced-motion handling

Use CSS for:

- keyframe animations
- hover states
- responsive layout
- section transitions
- custom properties/design tokens
- reduced-motion overrides

Prefer progressive enhancement:

- The site should still be readable if JavaScript fails.
- Animation should enhance, not carry, the design.

## Files to Edit

Primary files:

- `index.html`
- `project-akane.html`

Only edit assets if necessary:

- `images/`

Optional if useful:

- Create `README.md` with simple site notes.
- Create `CLAUDE.md` or project notes only if asked.

## Verification Requirements

After editing, verify the work by:

1. Serving the site locally with:

   ```bash
   python3 -m http.server 8026
   ```

2. Opening:

   ```text
   http://127.0.0.1:8026/
   http://127.0.0.1:8026/project-akane.html
   ```

3. Checking browser console for JavaScript errors.

4. Checking responsive layout at:
   - Mobile width
   - Tablet width
   - Desktop width

5. Checking keyboard navigation:
   - Tab through nav links
   - Tab through buttons
   - Open/close gallery lightbox
   - Use language toggle

6. Checking reduced motion behavior if possible.

7. Checking that all decorative motion does not interfere with reading.

8. Checking that all placeholder links are fixed or intentionally documented.

## Quality Bar

The final result should feel:

- More premium.
- More intentional.
- More readable.
- More accessible.
- More coherent across both pages.
- More dynamic without becoming noisy.
- More like an official anime character/profile site.
- Still personal and distinctive.
- Still simple to deploy.

Do not flatten the personality of the site. Improve polish without making it generic.

## Core Diagnosis to Address

The current site has:

```text
Good visual style
Good assets
Good typography
Good atmosphere
Basic interaction
```

The reference anime sites have:

```text
Layered key visual
Scroll choreography
Persistent ambient motion
Interactive focal elements
Official-site graphic language
Section-by-section reveal pacing
```

Therefore, the missing piece is:

> A choreographed motion system and layered key-visual structure that makes Akane feel like a living official character site, not only a beautiful static profile.

## Deliverable

Make the design improvements directly in the repo.

Then provide a concise summary:

- What changed.
- Which files changed.
- What was verified.
- Any remaining recommended follow-ups.
