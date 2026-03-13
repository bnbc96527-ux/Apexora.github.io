# Follow the prompt

This is a code bundle for Follow the prompt. The original project is available at:
https://www.figma.com/design/sPun6oQJJFMpUS6ZC9MyM7/Follow-the-prompt

## Local development

Run `npm i` to install dependencies.

Run `npm run dev` to start the dev server.

## Host on GitHub Pages

This repo now includes a GitHub Actions workflow that builds and deploys the Vite app to GitHub Pages.

### 1) Push to `main`

Deployment is triggered on pushes to `main` (or manually from Actions tab).

### 2) Enable Pages in repository settings

In GitHub:

- Go to **Settings → Pages**
- Under **Build and deployment**, choose **GitHub Actions**

### 3) Wait for deployment workflow

The workflow `.github/workflows/deploy.yml` will:

- install dependencies with `npm ci`
- run `npm run build`
- publish `dist/` to GitHub Pages

### 4) Your site URL

GitHub Pages URL will be shown in the deploy job output, usually:

`https://<your-username>.github.io/<repo-name>/`

## Notes

- `vite.config.ts` automatically sets the correct `base` path during GitHub Actions builds.
- Local development keeps `base: /` so routing and assets work normally.
