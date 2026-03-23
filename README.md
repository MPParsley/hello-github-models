# Hello GitHub Models

A minimal example showing how to use [GitHub Models](https://github.com/marketplace/models) to run **live AI inference in the browser**, deployed with **GitHub Actions** to **GitHub Pages**.

## What it does

1. **`docs/index.html`** — A single-page app that calls GPT-4o-mini via the GitHub Models API directly from your browser.
2. **GitHub Actions** — Deploys the page to GitHub Pages on every push to `main`.
3. **`hello_models.py`** — Optional CLI script to call the same model from the command line.

## Live demo

Visit the GitHub Pages URL for this repo, enter your GitHub token, and click **Generate Greeting** to get a live AI-generated hello world!

> Your token is stored in your browser's `localStorage` and is only sent to the GitHub Models API endpoint — it never touches our servers.

## Getting a token

1. Go to [github.com/settings/tokens](https://github.com/settings/tokens)
2. Create a fine-grained personal access token
3. No special permissions are needed — GitHub Models access is included by default

## Run locally (CLI)

```bash
pip install -r requirements.txt
export GITHUB_TOKEN="your_github_token"
python hello_models.py
```

## Setup GitHub Pages

1. Go to **Settings → Pages**
2. Set source to **GitHub Actions**
3. Push to `main` — the workflow deploys automatically

## Project structure

```
├── hello_models.py              # CLI script (optional)
├── requirements.txt             # Python dependencies for CLI
├── docs/
│   └── index.html               # Live in-browser GitHub Models demo
└── .github/workflows/
    └── hello-models.yml         # Deploys docs/ to GitHub Pages
```
