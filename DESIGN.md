# Design

<!-- impeccable:design-schema 1 -->

## World

Botánica de herbario prensado (pressed-herbarium botanical). The site reads as a hand-mounted herbarium field journal: pressed-specimen photo frames, catalog-style "Espécimen"/"N.º" labels, thin hairline rules, and a paper-grain ivory ground — not the generic boho default of loose watercolor washes and swirly cursive script.

## Palette

Color strategy: Committed accents on a warm-neutral ground.

- `papel` `#FBF7ED` — primary page ground (lightest paper tone)
- `crema` `#F3ECDC` / `crema-dark` `#E8DCC3` / `crema-darker` `#DBC9A3` — secondary section grounds, alternated with `papel` for rhythm
- `tinta` `#2E2A22` — primary text ink
- `terracota` `#B0602F` / `terracota-dark` `#7C3F1E` / `terracota-light` `#CE8354` — primary accent (buttons, eyebrow labels, links)
- `salvia` `#5F6E4C` / `salvia-dark` `#404B32` / `salvia-light` `#8A9873` — secondary accent (icons, secondary CTA)
- `mostaza` `#C79A3E` / `mostaza-dark` `#9C7729` — tertiary accent, reserved (selection highlight)

All confirmed body/label text pairs verified ≥4.5:1 (see Accessibility below).

## Typography

- Display/heading: **Cormorant** (italic, medium weight) — editorial serif with real commitment, not a script face. Headings max `text-5xl` (48px) at desktop.
- Small-caps eyebrow/label voice: **Cormorant SC** at `0.14em` tracking — used only for short catalog-style labels (2–4 words: "Nos casamos", "Espécimen I · Primavera de 2019", "N.º 01", countdown unit labels). Never applied to body paragraphs.
- Body: **Nunito Sans** — measure capped at 66ch via `.prose-measure` / `p`.

## Components & Motifs

- **Specimen frame** (`.specimen-frame`): double-inset hairline border around timeline/story photos, mimicking a pressed-plate mount.
- **Sheet frame** (`.sheet-frame`): inset border overlay on the hero, echoing a herbarium sheet's mounting margin.
- **Paper grain** (`.paper-grain`): subtle SVG-noise multiply texture on alternating section backgrounds.
- **Catalog labels**: `serif-sc` eyebrows ("Cuaderno de campo", "Plano de campo", "Lámina de herbario", "Notas de campo", "Ficha de asistencia", "Índice") replace the banned numbered-eyebrow pattern with a botanical-record voice; ceremony cards use "N.º 01 / N.º 02" as specimen catalog numbers, not generic section numbering.
- **Hairline dividers**: 1px `rgba(46,42,34,0.14)` borders throughout, no drop shadows except `card-hover` lift.
- **Botanical line marks**: hand-authored inline SVG leaf-sprig dividers (hero, historia section divider, footer) — no stock icon substitutes.
- Flat rectangular geometry throughout (no rounded corners) — reinforces the "mounted plate" character; intentional departure from the previous rounded-organic boho system.

## Motion

- `.reveal`: opacity + `translateY(16px)` → visible, GSAP/ScrollTrigger, `power2.out`, 0.6s, trigger at `top 88%`.
- Header solidifies on scroll past 40px.
- Anchor navigation: smooth-scroll attempt with a 700ms instant-correction fallback (see script at end of `index.html`) — guards against silent smooth-scroll failures on some mobile contexts.

## Accessibility

WCAG AA verified via computed relative-luminance contrast (Node.js script, not assumed):
- `tinta` on `papel`: 13.35:1
- `terracota-dark` on `papel`: 7.59:1
- `salvia-dark` on `papel`: 8.65:1
- White button text on `btn-hover` state (`#5C2E15`): 11.31:1
- Footer `crema/65` on `tinta`: ≥4.5:1 (raised from an initial `/50` that measured 4.18:1)

## Responsive

- Hero: `min-h-[100svh]` (not `100vh`) so mobile browser chrome doesn't clip the viewport-filling photo.
- `section#inicio` explicitly overrides the global `scroll-margin-top` to `0` — only section that should align flush to the viewport top.
- Mobile gallery: Swiper carousel (`slidesPerView: 1.15`, `spaceBetween: 14`) with visible inter-slide margin.
- Verified live on mobile (375×812) and desktop (1440×900): hero fill, anchor nav from deep scroll positions, gallery grid ↔ swiper breakpoint switch, RSVP form, FAQ accordion.

## Relationship to sibling demos

This is one of several wedding-invitation demo "models" (`demo-boda-boho`, `demo-boda-elegante`, ...) shown to prospective clients. Each model must stay visually self-distinct. This model owns the botanical/herbarium boho world; it must never converge toward `demo-boda-elegante`'s dark-editorial-serif-on-architecture identity.
