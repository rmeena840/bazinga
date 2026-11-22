# Bazinga Studio Website Design

## Intent

Create a polished, motion-led static website that presents Bazinga as a
company building mobile games. The site should make the studio feel memorable
and give visitors a clear way to find its games and social/contact links.

## Goals

- Establish Bazinga's identity as a mobile game studio.
- Create an engaging first impression with lightweight motion and game-inspired
  visuals.
- Work well on mobile and desktop, including for visitors who prefer reduced
  motion.
- Publish as a static site on GitHub Pages without a backend or build step.
- Keep game information straightforward to replace as real projects are ready
  to share.

## Non-goals

- Game functionality, accounts, forms requiring a server, or a content
  management system.
- Inventing game titles, release dates, studio history, or other factual claims.
- A multi-page portfolio or elaborate application architecture.

## Anti-goals

- Motion that blocks access to content or causes discomfort.
- A heavy framework, runtime, or third-party dependency for a single landing
  page.
- Presenting unconfirmed project details as real.

## Approaches

1. **Framework-free HTML, CSS, and JavaScript (chosen).** A direct static
   landing page keeps GitHub Pages deployment simple, loads quickly, and allows
   custom visual design and motion without a build pipeline.
2. **Framework app.** Offers component structure but adds build/deployment
   complexity that is not justified for this small static site.
3. **GitHub Pages theme.** Provides a fast starting point but limits the
   distinctive game-studio identity and motion requested.

## Design and content

- Use **Bazinga** as the studio brand.
- Build one responsive page with a studio introduction, a games-in-development
  section, a short studio/about section, and social/contact links.
- No game titles or project details have been provided. Use a neutral,
  clearly editable in-development presentation rather than invented names,
  dates, or claims.
- Create visual interest with CSS-built shapes/graphics and restrained
  transitions or ambient motion; do not depend on remote images or fonts.
- Honor `prefers-reduced-motion`, retain readable contrast, and ensure the
  content remains usable without animation.
- Use semantic HTML, responsive CSS, and small vanilla JavaScript only where
  it materially improves the interaction.

## Constraints

- Publishable on GitHub Pages as a static site.
- No server-side functionality or required secrets.
- No confirmed logo, game assets, or contact/social URLs are available; keep
  these easy to replace and do not fabricate real destinations.

## Left to the builder

- Choose the visual palette, typography from system fonts, page composition,
  and specific CSS motion details in keeping with a modern mobile game studio.
- Use only local/static assets or CSS-generated decoration.
- Verify the static page and its responsive/reduced-motion behavior with the
  available repository tooling.
