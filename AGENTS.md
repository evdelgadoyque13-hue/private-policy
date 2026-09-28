# Base44 Setup Notes

## Project Type
Static HTML site (single Privacy Policy page for "Analyst Canvas" app). No build step, no backend, no dependencies.

## Structure
The site content lives in `index.html` at the repo root. The GitHub Pages deploy workflows (deploy.yml, deploy1.yml, deploy2.yml) upload the repo root to GitHub Pages. The original HTML was previously buried in `.github/workflows/deploy3.yml` (an HTML file mislabeled as a GitHub Actions workflow) — it has been moved to a proper `index.html`.

## Running Locally
`docker compose -f docker-compose.base44.yml up -d` — uses nginx:alpine, mounts `index.html` directly, and serves it on port 3000.

## No Secrets Required
This is a purely static site with no external service dependencies.
