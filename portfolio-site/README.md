# Portfolio Site — Setup Instructions

This is a Minimal Mistakes Jekyll site scaffold, set up for a dual
research/industry portfolio.

## 1. Create your repo

On GitHub, create a new repository named exactly:
`yourusername.github.io` (replace `yourusername` with your actual GitHub
username — this exact naming is required for auto-publishing).

## 2. Upload these files

Push all files in this folder to the root of that repo, preserving the
folder structure:

```
yourusername.github.io/
├── _config.yml
├── index.md
├── _data/
│   └── navigation.yml
├── _pages/
│   ├── cv.md
│   ├── projects.md
│   ├── publications.md
│   └── contact.md
├── _projects/
│   └── 2024-01-15-example-project.md
└── assets/
    ├── images/
    └── files/
```

## 3. Enable GitHub Pages

In the repo: **Settings → Pages → Build and deployment → Source** →
select "Deploy from a branch" → branch `main`, folder `/ (root)`.

Because `_config.yml` uses `remote_theme`, GitHub will build the site
automatically — you don't need to install Jekyll or Ruby locally, though
you can (see below) to preview changes before pushing.

## 4. Fill in placeholders

Every file has HTML comments (`<!-- like this -->`) marking exactly what
to replace. Search for these across the repo to find every spot:
- Replace `yourusername`, `Your Name`, `you@email.com` etc. in `_config.yml`
- Fill in `index.md` (About), `_pages/cv.md`, `_pages/publications.md`
- Copy `_projects/2024-01-15-example-project.md` for each real project,
  rename the file, and delete the placeholder text

## 5. Add images/files

- Headshot → `assets/images/headshot.jpg` (referenced in `_config.yml`)
- CV PDF → `assets/files/your-cv.pdf` (referenced in `_pages/cv.md`)
- Project teaser images → `assets/images/`

## 6. (Optional) Preview locally before pushing

Requires Ruby + Bundler installed.

```bash
gem install bundler jekyll
bundle init
echo 'gem "github-pages", group: :jekyll_plugins' >> Gemfile
bundle install
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## 7. Push and check

After pushing to GitHub, your site will be live at
`https://yourusername.github.io` within a minute or two. Check the
**Actions** tab in your repo if it doesn't appear — build errors show up
there.

---

Once you've got real content ready, send it over and I can help you
draft the About page, CV page, or individual project writeups in your
voice.
