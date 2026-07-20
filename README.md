# cv

Personal CV built from [`resume.json`](resume.json) using
[`resumed`](https://github.com/rbardini/resumed) and a locally vendored copy of the
`jsonresume-theme-macchiato` theme.

## Theme

The theme lives in [`themes/macchiato/`](themes/macchiato) and is wired up as a local
`file:` dependency. It is a fork of
[`biosan/jsonresume-theme-macchiato`](https://github.com/biosan/jsonresume-theme-macchiato)
(MIT), vendored here so layout fixes can be made directly — upstream is inactive and does
not accept pull requests. The original MIT `LICENSE` is preserved in the theme directory.

## Build locally

```sh
npm install
npm run build   # renders resume.json -> public/index.html
npm run watch   # rebuild on every change to resume.json
```

## Deploy

Every push to `master` triggers [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml),
which builds the site and publishes it to GitHub Pages.
