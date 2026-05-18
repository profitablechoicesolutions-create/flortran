# Contributing to Flortran Website

Thanks for your interest in contributing. This is a small static site; contributions are welcome whether you're fixing a typo, polishing a component, or adding a new section.

## Ways to contribute

- **Report a bug** — open an issue with steps to reproduce.
- **Suggest an enhancement** — open an issue describing the idea.
- **Fix something** — open a pull request.

## Workflow

1. Fork the repository.
2. Create a branch off `main`:
   ```bash
   git checkout -b fix/short-description
   ```
3. Make your changes. Keep edits focused — one logical change per PR.
4. Test locally by opening `index.html` or running a local server.
5. Commit with a clear message:
   ```bash
   git commit -m "Fix: typo in services page comparison table"
   ```
6. Push and open a pull request against `main`.

## Style guidelines

- **HTML** — semantic tags, 4-space indentation, alphabetized attributes where reasonable.
- **CSS** — keep design tokens in `:root`. Use CSS custom properties rather than hard-coded values. Group related selectors.
- **JavaScript** — vanilla JS, no frameworks. Keep `js/main.js` minimal.
- **Copy** — match the existing editorial tone: confident, restrained, financial.

## What not to change without discussion

- Brand colors and typography (`:root` tokens).
- The luxury navy/gold aesthetic.
- Existing page structure.

Open an issue first if you want to propose larger changes — happy to discuss.
