# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Static HTML/CSS/JS, single file (`index.html`), Tailwind CDN with custom config, GSAP/ScrollTrigger, Swiper.js, vanilla-tilt.js. No backend — RSVP submits via FormSubmit. Deployed to GitHub Pages.

## Users

Two audiences: (1) the couple/business who receives this as a demo — Nacho (owner of a wedding-agency web-sales business) shows it to prospective clients (businesses or couples getting married) as a sample of what he can build for them; (2) the fictional end guests of "Lucía & Álvaro" who would browse the live demo to see what an invitation site looks and feels like (countdown, ceremony/venue info, RSVP, gallery, FAQ).

## Product Purpose

A portfolio demo wedding-invitation website, one of several distinct visual "models" Nacho maintains (this one boho/natural themed; a sibling demo `demo-boda-elegante` uses an editorial/elegant world) to show prospective clients a range of styles they could choose from. Success = it looks professional, distinctive, and convincingly production-grade enough that a real couple or business would want to buy something like it.

## Positioning

Distinct from the sibling "elegante" demo (dark editorial serif, architectural photography, Sevilla setting): this model must keep its own identity — boho/natural, countryside, warm earthy palette — while reaching the same bar of polish, responsive correctness, and craft. Not a reskin of the elegante demo; a different visual world at the same quality level.

## Operating Context

Single-page site with anchor nav (Inicio, Nuestra historia, La boda, Galería, Info para invitados, FAQ, Confirmar asistencia). Sections: hero with countdown, love-story timeline, ceremony+celebration details with embedded maps, photo gallery (grid desktop / swiper carousel mobile) with lightbox, guest info (transport/lodging/dress code), gift registry, RSVP form, FAQ accordion, collaborative playlist, contact, footer.

## Capabilities and Constraints

Must remain a single HTML file deployable as-is to GitHub Pages. No real backend/server. All images are real downloaded (not hotlinked) stock photos already present in `img/` — no identifiable real faces. Existing copy (fictional couple Lucía & Álvaro, 12 de diciembre de 2027, Ronda Málaga) is confirmed content and should be preserved as-is; only the visual system is being replaced.

## Brand Commitments

Footer credit reads "NGS" (not the user's real name). Fictional couple name "Lucía & Álvaro" and wedding date 12 de diciembre de 2027 are fixed. Boho/natural theme is the pinned world for this specific demo (one of multiple models in the portfolio) — the redesign must stay within boho/natural, not pivot to a different aesthetic category.

## Evidence on Hand

Existing photo assets in `img/` (hero, 3 timeline photos, 10 gallery photos) — real stock photography already vetted for the boho/natural theme, reusable in the redesign. Sibling demo for responsive-craft reference: https://cowork-nacho.github.io/demo-boda-elegante/ (different visual world, not to be copied stylistically, but its mobile-viewport-filling hero and responsive discipline are the bar to match).

## Product Principles

- Each demo model must be visually self-distinct — this one stays boho/natural, never converges toward the elegante sibling's look.
- Professional/premium craft bar: this is a sales tool, so polish and responsive correctness directly represent Nacho's business capability.
- Preserve all existing confirmed copy/content; this is a visual redesign, not a content or IA rewrite.
- Fully responsive on every device class, verified, not assumed.

## Accessibility & Inclusion

WCAG 2.1 AA text contrast (4.5:1 minimum) was a hard requirement in the original build and must be re-verified after the visual redesign.
