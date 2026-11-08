# BranchBooks website

Source for [branchbooks.dev](https://branchbooks.dev/): the BranchBooks landing page, docs and brand
guide. Built with [Hugo](https://gohugo.io/) and the [Hextra](https://github.com/imfing/hextra) theme,
hosted on Cloudflare Pages. No Node or npm.

## Structure

```
content/
├── _index.md     # landing page
├── docs/         # the docs, one .md per page; weight sets the sidebar order
└── brand.md      # logo, wordmark, colours and type
assets/css/custom.css   # ledger green, and the brand page's swatches
static/           # favicons and brand images
themes/hextra/    # git submodule, pinned to a release tag
hugo.toml         # site config: menu, logo, search
```

The brand images in `static/` are copies of the app's, in `crates/branchbooks-ui/icons/` in the
[app repository](https://gitlab.com/branchbooks/branchbooks). Change them there first.

## Local development

Clone with the theme:

```bash
git clone --recurse-submodules https://gitlab.com/branchbooks/branchbooks.dev.git
# or, after a plain clone:
git submodule update --init --recursive
```

Run the dev server with Docker (no Hugo install needed):

```bash
docker compose up
```

On a Windows Dev Drive (ReFS), Docker Desktop can't mount the folder from Windows, so run the same
command from a WSL distro with Docker Desktop's WSL integration, in the `/mnt/d/...` path.

Or run it with Hugo extended (`winget install Hugo.Hugo.Extended`):

```bash
hugo server --buildDrafts --buildFuture
```

The site runs at <http://localhost:1313>.

## Deployment

Cloudflare Pages builds from `main`, and builds a preview for each pull request. Its settings live in
the Cloudflare dashboard, not this repo:

| Setting | Value |
| --- | --- |
| Build command | `hugo --minify` |
| Output directory | `public` |
| Env var | `HUGO_VERSION` = `0.169.0`, set in **both** the Production and Preview environments |

CI (`.gitlab-ci.yml`) runs the same build on every merge request, with GitLab's secret detection, SAST and IaC
scanning. Cloudflare Pages deploys from the
GitHub mirror of `main` (BranchBooks/branchbooks.dev), which GitLab pushes to.

## Upgrading

- **Hugo:** bump the `ghcr.io/gohugoio/hugo` image tag in `compose.yaml` and
  `.gitlab-ci.yml`, and the Cloudflare `HUGO_VERSION` (Production **and** Preview). Hextra
  needs Hugo 0.146.0 or later.
- **Hextra:** `git -C themes/hextra checkout <tag>`, read its release notes, build, then commit the
  submodule pointer.

## Licence

The site's code (config, layouts, CSS and redirects) is under the [MIT licence](LICENSE). Its text, in
`content/` and `i18n/`, is under [CC BY 4.0](LICENSE-CONTENT). The Hextra theme is under its own MIT
licence. The BranchBooks name, logo and wordmark identify the project and aren't covered by any of
these: see the [brand page](https://branchbooks.dev/brand/).

## Privacy

No analytics or trackers. Search runs in the browser, and its script is fetched at build time and
served from this site.
