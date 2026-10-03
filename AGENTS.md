# Copilot instructions

## Project overview

- This is a single-file, dependency-free space exploration quiz.
- `index.html` contains the markup, styles, quiz questions, and interaction logic.
- Keep the app runnable directly from `file://`; do not introduce a server, build step, or external runtime dependency.

## Implementation guidelines

- Keep changes focused and consistent with the existing visual design: a pink-and-blue mission-control display with light and dark color-scheme support.
- Preserve semantic HTML, visible keyboard focus, keyboard operation, screen-reader announcements, and `prefers-reduced-motion` support.
- Keep quiz state, the score, progress indicator, answer feedback, results screen, and replay behavior in sync.
- Use the existing CSS custom properties and responsive patterns when adjusting the interface.

## Validation

- For JavaScript changes, check the inline script syntax with Node:
  `node -e 'const h=require("fs").readFileSync("index.html","utf8"); const s=h.match(/<script>([\s\S]*?)<\/script>/); if(!s) throw Error("Inline script missing"); new Function(s[1]);'`
- For interaction or visual changes, open `index.html` in the integrated browser and verify the affected behavior, including keyboard access where relevant.
