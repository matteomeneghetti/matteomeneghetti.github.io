# cv

Personal CV built from [`resume.json`](resume.json) using
[`resumed`](https://github.com/rbardini/resumed) and the
[`jsonresume-theme-macchiato`](https://www.npmjs.com/package/jsonresume-theme-macchiato) theme.

## Build locally

```sh
npm install
npm run build   # renders resume.json -> public/index.html
npm run watch   # rebuild on every change to resume.json
```

## Deploy

Every push to `master` triggers [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml),
which builds the site and publishes it to GitHub Pages.

The custom domain is controlled by the root [`CNAME`](CNAME) file (`meneghetti.cv`), which the
workflow copies into the build output before publishing.

> One-time setup in the repo: **Settings → Pages → Source = "GitHub Actions"**, point the
> `meneghetti.cv` DNS at GitHub Pages, then enable **Enforce HTTPS** after the first deploy.
