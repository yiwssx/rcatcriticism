# RCAT Complaint Form (React)

React + Vite frontend for complaint submission, deployed to GitHub Pages from a `gh-pages` branch (no GitHub Actions).

## Project structure

```text
.
|- index.html
|- package.json
|- vite.config.js
|- .env.example
|- src/
|  |- App.jsx
|  |- main.jsx
|  `- index.css
`- public/
   `- assets/rcat-logo.jpg
```

## API config

This app reads API URL from `.env` using:

1. `VITE_API_URI`

Recommended for this repo:

1. Copy `.env.example` to `.env`
2. Put your Google Apps Script `/exec` URL in `.env`

`.env` is ignored by git, so your local value is not committed.

## Local development

1. Install dependencies:
   - `npm install`
2. Create env file:
   - `Copy-Item .env.example .env`
3. Start dev server:
   - `npm run dev`

## Deploy to GitHub Pages (branch, no Actions)

1. First-time GitHub Pages setting:
   - Go to `Settings` -> `Pages`
   - In `Build and deployment` -> `Source`, choose `Deploy from a branch`
   - Branch: `gh-pages`
   - Folder: `/ (root)`
2. Deploy from local machine:
   - `npm run deploy`

`npm run deploy` will:
1. Build with Vite (`dist/`)
2. Push `dist/` content to branch `gh-pages`

## Notes

- Use `/exec`, not `/dev`, for Apps Script URL.
- Like any frontend config, API URL is visible in deployed client code.
