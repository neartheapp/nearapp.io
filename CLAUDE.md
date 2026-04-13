# nearapp.io

## Overview
Static marketing website for the **Near** mobile app — a location-based social app that shows you who crossed your path today. Pure HTML/CSS with no build system, no frameworks, and no package manager. Hosted on GitHub Pages at nearapp.io.

## Quick Start
This is a static site — no build step required.
```bash
open index.html
# or use a local server:
python3 -m http.server 8000
```

## Project Structure
- `index.html` — Main landing page (hero, how it works, features, pricing, download CTA)
- `privacy.html` — Privacy policy
- `terms.html` — Terms of service
- `support.html` — FAQ / help center with expandable questions
- `CNAME` — Custom domain config for GitHub Pages (nearapp.io)
- `nearblue1.png` — Blue logo variant
- `near white (1).png` — White logo variant

## Design System
- **Colors:** `--navy: #050d1a`, `--blue: #378ADD`, `--red: #E03030`, `--silver: #A8A8A8`, `--white: #ffffff`
- **Headings:** Unbounded font (weights: 300, 400, 700, 900)
- **Body text:** DM Sans font (weights: 300, 400, 500)
- **Fonts loaded via:** Google Fonts CDN

## Architecture Principles
- **Self-contained pages** — Each HTML file contains its own styles in `<style>` tags unless a shared CSS file exists.
- **No duplication** — If the same HTML pattern appears on multiple pages, keep it consistent across files.
- **Consistent patterns** — Follow the existing structure. Use the same CSS class naming and layout conventions.
- **No build system** — This is intentionally a zero-dependency static site. Do not add npm, webpack, or frameworks.
- **Search before creating** — Always check if a CSS class or HTML pattern already exists before building a new one.
- See `.claude/architecture.json` for specific rules and boundaries.

## Conventions
- All CSS is inline in `<style>` tags within each HTML file (unless a shared CSS file exists)
- Keep HTML files self-contained — each page has its own styles
- Responsive design using media queries within each file
- Follow existing CSS class naming patterns
- Images are typically in the project root or an assets directory

## Common Mistakes to Avoid
- Do not add a package.json or build system — this is intentionally a zero-dependency static site
- Do not create external .css or .js files unless the project architecture changes
- Do not hardcode API keys, tokens, or secrets in HTML files
- Do not break the hosting deployment (keep index.html at root, preserve CNAME if present)
- Do not add files that static hosting cannot serve (no server-side code)

## Communication Style
- Write all commit messages, PR descriptions, and summaries in **plain language** that a non-technical person can understand.
- Explain WHAT changed, WHY it matters, and WHAT it means for the project — not just technical details.
- Use simple analogies when helpful. Avoid jargon. If you must use a technical term, explain it in parentheses.
- Structure summaries with: "What changed" → "Why we did it" → "What this means for you"

## Commands
- `/test` — Write and run tests for your code (tests first, then implementation)
- `/audit` — Check the project for code quality and architecture issues
- `/save` — Save your work (commits and pushes to GitHub)
- `/share` — Share your work for review (creates a pull request)

## Session Workflow
- Changes are auto-tracked in `.claude/sessions/`
- You'll be reminded to save checkpoints after significant changes
- Review `PROJECT_LESSONS.md` at the start of each session for past corrections

## References
- `PROJECT_LESSONS.md` — Corrections and learnings from past sessions
- `.claude/architecture.json` — Architecture rules and boundaries
- `README.md` — Project README
