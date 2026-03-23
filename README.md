# Hello GitHub Models

A minimal example showing how to use [GitHub Models](https://github.com/marketplace/models) to run AI inference, automated with **GitHub Actions** and published to **GitHub Pages**.

## What it does

1. **`hello_models.py`** — Calls a GitHub Model (GPT-4o-mini) to generate a fun greeting.
2. **GitHub Actions** — Runs the script on push and on a daily schedule, writing the output to `docs/`.
3. **GitHub Pages** — Serves the generated page so anyone can see the latest AI greeting.

## Quick start

### Run locally

```bash
pip install -r requirements.txt
export GITHUB_TOKEN="your_github_token"
python hello_models.py
```

### Run via GitHub Actions

The workflow runs automatically on push to `main`. You can also trigger it manually from the **Actions** tab.

> **Note:** The `GITHUB_TOKEN` provided by Actions has access to GitHub Models by default — no extra secrets needed.

## Setup GitHub Pages

1. Go to **Settings → Pages**
2. Set source to **GitHub Actions** (or deploy from `docs/` on `main`)

## Project structure

```
├── hello_models.py          # Calls GitHub Models API
├── requirements.txt         # Python dependencies
├── docs/
│   └── index.html           # Generated page (updated by Actions)
└── .github/workflows/
    └── hello-models.yml     # CI/CD workflow
```
