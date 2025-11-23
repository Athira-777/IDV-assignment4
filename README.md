# Adversarial Robustness Heatmap

Interactive D3.js heatmap comparing adversarial attack strength against different
training/defense strategies. The site is completely static (`index.html` + `data.json`),
so it can be previewed locally with any static file server and deployed via GitHub Pages.

## GitHub Pages deployment

Deployment is automated through `.github/workflows/deploy-pages.yml` and works as follows:

1. Push commits (or merge pull requests) to the `main` branch.
2. GitHub Actions checks out the repo, packages all static assets, and uploads them as the
   Pages artifact.
3. `actions/deploy-pages@v4` publishes the artifact to the special `github-pages`
   environment.
4. The live site becomes available at `https://<your-username>.github.io/IDV-assignment4/`
   (replace `<your-username>` accordingly).

> **Tip:** The first time you use this workflow, open **Settings → Pages** and ensure the
> "Build and deployment" source is set to **GitHub Actions**. Subsequent pushes will
> redeploy automatically.

## Customization

- Update `data.json` to reflect new attack/defense accuracy numbers.
- Tweak `index.html` styles or interaction logic directly; no build step is required.
- If you rename the default branch, update the `branches` filter inside
  `deploy-pages.yml` accordingly.
