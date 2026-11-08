# Agent notes

Hugo site using Hextra, deployed to Cloudflare Pages from `main`. See README.md for setup and deployment.

- Run `git submodule update --init --recursive` before the first build. Never edit files under
  `themes/hextra`; override a template in `layouts/` or add CSS to `assets/css/custom.css` instead.
- Verify changes with `hugo --minify` (the same build CI and Cloudflare run); it must finish without
  errors or warnings.
- Preview with `hugo server` or `docker compose up` at http://localhost:1313. Both run in the
  foreground, so start them as background processes and stop them when done.
- Write as what BranchBooks is now, in the present tense, with no project history. Claim only what the
  app does today; the app repository's README and `docs/DESIGN.md` are the source of truth.
- No analytics, trackers or third-party requests from visitors' browsers.
- No npm in this repository.
- If the Hugo version changes, update the image tag in `compose.yaml` and `.gitlab-ci.yml`
  and remind the user to update the Cloudflare `HUGO_VERSION` in both Production and Preview.
