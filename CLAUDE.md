# NVY Creations — Portfolio Website

Web design agency portfolio site built with Next.js 16, React 19, Tailwind v4, Framer Motion, Spline 3D, and shadcn/ui.

---

## Execution Workflow

All work follows a two-phase pipeline:

1. **GSD builds it** — planning, research, phased execution, and building flows through the GSD framework and its agents
2. **Subagents check it** — code-reviewer, security-auditor, performance-engineer, accessibility-tester, architect-reviewer, and seo-specialist verify the output before work is considered done

---

## Always Do First

- **Invoke the `frontend-design` skill** before writing any frontend code, every session, no exceptions.
- Check `Brand-assets/` folder before designing — use real assets over placeholders.

## Tech Stack

- **Framework:** Next.js 16 (App Router) + React 19
- **Styling:** Tailwind CSS v4 (via @tailwindcss/postcss)
- **Animation:** Framer Motion / Motion
- **3D:** @splinetool/react-spline
- **Components:** shadcn/ui + Radix UI primitives
- **Icons:** Lucide React
- **Language:** TypeScript 5 (strict mode)
- **Fonts:** Orbitron (display/headings) + Outfit (body) via Google Fonts

## Brand Identity

- **Primary background:** `--obsidian: #06060b`
- **Chrome palette:** `#8a9bb0`, `#b8c6d6`, `#d4dde8`, `#e8edf2`
- **Accent:** `--accent-cyan: #3d8b9e`
- **Fonts:** Orbitron (headings, tight tracking), Outfit (body, generous line-height)
- Never use default Tailwind palette colors — always use these brand tokens

## Component Patterns

- Use functional components with hooks
- Keep components small and composable
- Co-locate styles, tests, and types with their components
- PascalCase for components, camelCase for functions/variables
- Files: kebab-case for utilities, PascalCase for components

## Reference Images & Matching

- If a reference image is provided: match layout, spacing, typography, and color exactly
- Screenshot output, compare against reference, fix mismatches, re-screenshot — at least 2 comparison rounds
- Do not improve or add to a reference design — match it

## Local Server

- **Always serve on localhost** — never screenshot a `file:///` URL
- For the Next.js app: `cd portfolio && npm run dev`
- For standalone HTML: `node serve.mjs` at `http://localhost:3000`
- If the server is already running, do not start a second instance

## Screenshot Workflow

- Puppeteer is installed at `C:/Users/nateh/AppData/Local/Temp/puppeteer-test/`
- Screenshot from localhost: `node screenshot.mjs http://localhost:3000`
- Screenshots save to `./temporary screenshots/screenshot-N.png` (auto-incremented)
- After screenshotting, read the PNG with the Read tool to analyze
- Check: spacing/padding, font size/weight, colors (exact hex), alignment, border-radius, shadows, image sizing

## Anti-Generic Guardrails

- **Colors:** Never default Tailwind palette. Use brand tokens above.
- **Shadows:** Layered, color-tinted shadows with low opacity — never flat `shadow-md`
- **Typography:** Orbitron for headings (tight tracking `-0.03em`), Outfit for body (line-height `1.7`)
- **Gradients:** Layer multiple radial gradients. Add grain/texture via SVG noise filter
- **Animations:** Only animate `transform` and `opacity`. Never `transition-all`. Spring-style easing.
- **Interactive states:** Every clickable element needs hover, focus-visible, and active states
- **Images:** Gradient overlay (`bg-gradient-to-t from-black/60`) + color layer with `mix-blend-multiply`
- **Spacing:** Use consistent spacing tokens, not random Tailwind steps
- **Depth:** Surfaces need a layering system (base → elevated → floating)

## SEO Requirements

- Every page: unique `<title>` and `<meta name="description">`
- Proper heading hierarchy (single H1, structured H2-H6)
- JSON-LD schema markup for relevant content types
- Open Graph and Twitter Card meta tags
- Core Web Vitals targets: LCP < 2.5s, FID < 100ms, CLS < 0.1
- Semantic HTML elements (`nav`, `main`, `article`, `section`)
- All images: descriptive alt text, WebP/AVIF formats, lazy loading

## TypeScript

- Strict mode always
- Prefer `interface` over `type` for object shapes
- Avoid `any` — use `unknown` or proper generics

## Git

- Concise commit messages in imperative mood
- Keep commits focused on a single change
- Branch naming: `feature/`, `fix/`, `chore/` prefixes

## Hard Rules

- Do not add sections, features, or content not in the reference
- Do not "improve" a reference design — match it
- Do not stop after one screenshot pass
- Do not use `transition-all`
- Do not use default Tailwind blue/indigo as primary color
- Always read existing code before modifying it
- Test changes before considering them done

## Deployment Rules

- This workspace is a **test environment**. All changes are local only.
- **Never push to GitHub or deploy without explicit user permission.**
- Before any `git push` or deployment: ask "¿Confirmas que quieres publicar estos cambios en el sitio en vivo?"
- User must confirm before proceeding.

## Installed Resources

- **Framework:** GSD (Get Shit Done) — see `get-shit-done/` for commands, workflows, templates
- **Skills (14):** frontend-design, seo-audit, webapp-testing, web-artifacts-builder, playground, canvas-design, brand-guidelines, theme-factory, algorithmic-art, slack-gif-creator, docx, pdf, claude-md-improver, skill-creator
- **Agents (42):** GSD agents (15) + specialist subagents (27) covering frontend, Next.js, React, TypeScript, code review, security, performance, accessibility, architecture, QA, testing, debugging, SEO, UX research, content marketing, refactoring, documentation, git workflow, dependency management, orchestration
