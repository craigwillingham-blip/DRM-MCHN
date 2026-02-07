# Repository Guidelines

## Project Structure & Module Organization

- `index.html`: Single-page drum machine app containing HTML, CSS, and vanilla JS.
- No separate build system, source folders, or assets directories. All logic and styling live in `index.html`.
- Add new assets (if ever needed) under a new `assets/` folder and reference them from `index.html`.

## Build, Test, and Development Commands

- Run locally: open `index.html` directly in a modern browser (Chrome, Edge, Firefox). No server required.
- There is currently no build step and no automated tests.

## Local Tooling (Git/GitHub)

- GitHub CLI (`gh`) is installed at `C:\Program Files\GitHub CLI\gh.exe`.
- No `github.exe` was found in standard install locations (e.g., `C:\Program Files\` or `C:\Users\craig\AppData\Local\Programs`). If you intend to use GitHub Desktop, verify its install path and add it here.

## Coding Style & Naming Conventions

- Use 2-space indentation in HTML, CSS, and JS to match existing formatting.
- Keep functions small and focused (e.g., `synth808Kick`, `createNoiseBuffer`).
- Prefer clear, descriptive names for audio helpers and UI handlers (verb for actions, noun for data), e.g., `triggerSound`, `buildGrid`.
- Avoid external libraries unless explicitly approved; stick to Web Audio and DOM APIs.

## Testing Guidelines

- No test framework is configured.
- Manual smoke checks are required after changes:
  - Load `index.html` in a browser.
  - Toggle steps, press Play, and verify audio output for each kit.
  - Confirm there are no console errors.

## Commit & Pull Request Guidelines

- There is no existing Git history in this repository. Use a simple, consistent convention going forward:
  - `Add 808 + industrial kit`
  - `Fix swing timing jitter`
  - `Refactor synth helpers`
- PRs (if used) should include:
  - A short summary of changes.
  - Screenshots or a short screen capture if UI behavior changes.
  - Notes about any audio changes (what was tuned and why).

## Git Authentication & Push Tips

- To avoid repeated auth prompts, ensure GitHub CLI is authenticated and that Git uses the GitHub credential helper.
- One-time setup (examples):
  - `& "C:\Program Files\GitHub CLI\gh.exe" auth login`
  - `& "C:\Program Files\Git\cmd\git.exe" config --global credential.helper manager`
- After this, `git push` should work without re-auth.

## Configuration & Security Notes

- Audio uses the browser Web Audio API; user interaction is required before audio can start.
- If you add hosted samples, ensure they are from reliable sources and respect licensing.
