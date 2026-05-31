# Portfolio — GitHub Pages

A minimal Jekyll portfolio site deployable to GitHub Pages.

## Local preview

```bash
cd /Users/nikolaskarefyllidis/Desktop/15_GitPage
bundle config set --local path 'vendor/bundle'
bundle config set --local bin 'vendor/bundle/bin'
bundle install
bundle exec jekyll serve
```

Open [http://localhost:4000](http://localhost:4000) in your browser.

## Customize

Edit these files to personalize the site:

| File | What to change |
|------|----------------|
| `_config.yml` | Name, email, bio, tagline, social links, skills |
| `_data/projects.yml` | Your project cards |
| `assets/css/main.scss` | Colors and styling (optional) |

When deploying, your site URL is:

```yaml
url: "https://karefyllidis.github.io"
```

## Deploy to GitHub Pages

1. Create a **public** repository on GitHub named exactly `karefyllidis.github.io`.
2. Initialize git and push:

```bash
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin https://github.com/karefyllidis/karefyllidis.github.io.git
git push -u origin main
```

3. GitHub builds and publishes the site automatically. It will be live at [https://karefyllidis.github.io](https://karefyllidis.github.io) within a few minutes.

## Build only (no server)

```bash
bundle exec jekyll build
```

Output is written to `_site/`.
