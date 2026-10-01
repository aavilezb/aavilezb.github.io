# Notebook

Static blog built with Jekyll for GitHub Pages.

- Posts: `_posts/YYYY-MM-DD-title.md`
- Drafts: `_drafts/` (not published; preview with `bundle exec jekyll serve --drafts`)
- Sections: set `category:` to `projects`, `notes`, `ctf` or `personal`
- Site title and author: `_config.yml`
- Styles: `assets/style.css`
- Photos: put .jpg files under 1 MB in `assets/img/` and use `![alt]({{ '/assets/img/file.jpg' | relative_url }})`

`published: false` in a post's header also hides it. In a public repo the source files stay visible either way.

Local preview: `bundle install && bundle exec jekyll serve`

## Optional features
- GitHub repos on the Projects page: set `github_username` in `_config.yml`.
- Comments: enable Discussions on the repo, install the giscus app, then fill the `giscus` block in `_config.yml` with the values from https://giscus.app. Add `comments: false` to a post's header to turn them off there.
- Resume: edit `resume.md` and put your PDF at `assets/resume.pdf`.

## CTF log
Add one entry per solved challenge to `_data/ctf_log.yml` (the file has a template). The CTF log page shows your total, day streak, week streak and a 20-week activity grid.

## Navigation, footer links and "Start here"
- Menu items live in `_data/nav.yml`.
- Footer links (GitHub, LinkedIn, email): `links` block in `_config.yml`.
- Put `featured: true` and a one-line `summary:` in a post's header to list it under "Start here" on the home page.
- Tag beginner-friendly posts with `beginner`.
- Give every image a short `alt` text: `![what the picture shows](...)`.

## Visit counter
1. Sign up at goatcounter.com (free for personal sites) and pick a code, e.g. `alex`.
2. In GoatCounter: Settings, then turn on "Allow adding visitor counts on your website".
3. Put the code in `goatcounter:` in `_config.yml`. The footer then shows the total views, and the GoatCounter dashboard shows pages, referrers and countries.
