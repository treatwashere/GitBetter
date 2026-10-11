# GitBetter

A GitHub-inspired developer workspace for discovering repositories, code, users, issues, pull requests, and managing GitHub Pages. No Vercel deployment features.

## Included in this starter
- Responsive dashboard with light/dark theme.
- Search UI for repositories, code, users, issues, and pull requests using GitHub's search API.
- Search results with links, save/pin interactions, and suggested searches.
- GitHub Pages management entry point and setup-flow UI.
- GitHub Pages Actions workflow for building and publishing this app.
- OAuth-ready layout; authentication and privileged actions are intentionally left for the repository owner to wire up.

## Run locally
Requires Node.js 20+.

    npm install
    npm run dev

Build the static site with `npm run build`. Output is written to `dist/`.

## OAuth and API integration TODO
This is a starter, not a fully authenticated GitHub client yet. Add OAuth before wiring private repository, code search, write, and Pages-setting actions. Keep client secrets on a server; never ship a GitHub client secret or personal access token in browser code. Use minimum permissions and ask for confirmation before writes.

Next integrations: authenticated profile/session; repository list and file browser; branches, commits, and diffs; issue/PR workflows; GitHub Pages source selection, enable/disable, status and URL; repository settings and activity feed; pagination and rate-limit handling.

## GitHub Pages
The workflow at `.github/workflows/pages.yml` builds the Vite app and publishes `dist/` when pushed to `main`. In the GitHub repository settings, set **Pages → Build and deployment → Source** to **GitHub Actions**. The expected project URL is `https://treatwashere.github.io/GitBetter/` after a successful workflow run.

The Pages manager inside the app is currently UI-only until OAuth/API calls are connected. The app does not include Vercel deployment features.
