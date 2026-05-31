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

Live site: [https://karefyllidis.github.io](https://karefyllidis.github.io)

## Deploy to GitHub Pages

Repository: **`karefyllidis.github.io`** (user site — served at the root URL).

```bash
cd /Users/nikolaskarefyllidis/Desktop/15_GitPage
git remote set-url origin git@github.com:karefyllidis/karefyllidis.github.io.git
git push -u origin main
```

## Build only (no server)

```bash
bundle exec jekyll build
```

Output is written to `_site/`.
