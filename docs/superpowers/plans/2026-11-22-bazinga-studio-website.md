# Bazinga Studio Website Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Build a responsive, motion-led static landing page presenting Bazinga as a mobile game studio.

**Architecture:** Serve a semantic `index.html` and a single `styles.css` directly from the repository root for GitHub Pages. Use CSS-only decorative motion, with a reduced-motion fallback; do not add a framework, JavaScript, or external assets.

**Tech Stack:** HTML, CSS, GitHub Pages.

**Spec:** `docs/superpowers/specs/2026-11-22-bazinga-studio-website-design.md`

## Global Constraints

- Publishable on GitHub Pages as a static site.
- No server-side functionality or required secrets.
- No confirmed logo, game assets, or contact/social URLs are available; keep these easy to replace and do not fabricate real destinations.
- Use **Bazinga** as the studio brand.
- No game titles or project details have been provided. Use a neutral, clearly editable in-development presentation rather than invented names, dates, or claims.
- Honor `prefers-reduced-motion`, retain readable contrast, and ensure the content remains usable without animation.
- No heavy framework, runtime, third-party dependency, remote image, or remote font.

## Review Focus

- At 320px-wide viewports, the layout has no horizontal overflow; verify in the browser at 320px.
- With reduced motion enabled, nonessential animation is disabled; emulate `prefers-reduced-motion: reduce` and inspect computed animation behavior.
- Each in-page navigation link reaches a real section; click all nav links and confirm the URL fragment and target.
- The page remains understandable without decorative CSS motion; inspect text and section order with motion disabled.
- Missing project/contact details are not invented; inspect rendered copy for only neutral in-development and forthcoming-links language.

---

### Task 1: Build the static studio landing page

**Files:**
- Create: `index.html`
- Create: `styles.css`

**Interfaces:**
- Consumes: none.
- Produces: a root-level static site; section anchors `#games`, `#studio`, and `#contact`; stylesheet linked from `index.html`.

- [ ] **Step 1: Create semantic page structure in `index.html`**

Add a responsive viewport declaration, a meaningful page title, a keyboard-accessible skip link, a header with Bazinga wordmark and section navigation, and a `main` containing:

1. A studio hero identifying Bazinga as a mobile game studio.
2. A games section with one generic, clearly labeled “In development” presentation and no invented title or release details.
3. A short studio/about section that makes no unprovided factual claims.
4. A contact/social section with clearly replaceable forthcoming-details copy, but no fabricated destination.

Use the exact section IDs `games`, `studio`, and `contact`. Keep all essential content in HTML.

- [ ] **Step 2: Style the responsive visual identity and motion in `styles.css`**

Create a distinctive, polished game-studio look using system fonts, strong typography, a high-contrast palette, and CSS-drawn decoration rather than unavailable image assets. Support narrow mobile and desktop layouts. Add restrained CSS-only ambient or entrance motion, visible keyboard focus styles, and a `prefers-reduced-motion: reduce` rule that removes nonessential animation and transitions.

- [ ] **Step 3: Verify the static page and required behaviors**

Run: `git diff --check`
Expected: no whitespace errors.

Serve from the repository root with `python3 -m http.server 8000 --bind 127.0.0.1` and inspect the page in a browser at desktop width, 390px, and 320px. Verify no horizontal overflow, all three navigation anchors reach their sections, keyboard focus is visible, the page has no browser-console errors, and reduced-motion emulation suppresses nonessential animation. Check that project and contact copy contains no invented titles, details, or destinations.

- [ ] **Step 4: Commit the static landing page**

```bash
git add index.html styles.css
git commit -m "feat: add Bazinga studio landing page"
```

### Task 2: Document local preview and GitHub Pages publishing

**Files:**
- Modify: `README.md`

**Interfaces:**
- Consumes: the root-level `index.html` and `styles.css` from Task 1.
- Produces: concise instructions for local preview and publishing the static site.

- [ ] **Step 1: Replace the placeholder README with project and publishing instructions**

Describe Bazinga as a mobile game studio, state that the site is static and dependency-free, document local preview using `python3 -m http.server 8000`, and explain that GitHub Pages can publish from the repository root so `index.html` is the entry point. Do not promise unavailable project or contact information.

- [ ] **Step 2: Verify documentation and final changes**

Run: `git diff --check`
Expected: no whitespace errors. Confirm the README preview command and GitHub Pages source match the root-level site structure.

- [ ] **Step 3: Commit the README**

```bash
git add README.md
git commit -m "docs: explain GitHub Pages publishing"
```
