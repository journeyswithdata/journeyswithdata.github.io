# journeyswithdata.dev

Quarto website, built with Quarto's standard features:

- `_brand.yml` sets colours and Google Fonts (Quarto's brand file).
- `_quarto.yml` sets column widths (`grid:`) and site options.
- `theme.scss` styles the site's own components only.
- Main pages use `page-layout: custom`; card rows use Bootstrap's `.grid` / `.g-col-*`;
  About uses the `trestles` about template; posts use `title-block-banner`.
- The one custom layout rule is `.wrap` in `theme.scss`: Quarto has no fluid-width
  option, so it keeps the main pages at 88% of the screen (max 2000px) on large displays.

## Run it

    quarto preview          # live reload
    quarto render           # build into _site/

## Publish

    quarto publish gh-pages

`CNAME` and `.nojekyll` are listed under `project.resources` in `_quarto.yml`,
so they are copied into the published output and the custom domain keeps working.

## Before you publish — checklist

- [ ] Read all five posts and rewrite anything that doesn't sound like you
- [ ] `work.qmd` — "Ways to work together": keep only what you're happy to offer
- [ ] `about.qmd` — "What I believe about data work": make sure you do
- [ ] Contact cards (`index.qmd`, `work.qmd`) and the `links:` in `about.qmd` — add email / LinkedIn when ready
- [ ] Add your name somewhere (deliberately not guessed)

## Structure

    index.qmd           home: hero, focus areas, principles, latest posts, contact
    writing.qmd         full post listing with categories, search + RSS (writing.xml)
    work.qmd            the substance, writing by theme, ways to work together
    about.qmd           you, in your own words
    posts/              one post per folder
    posts/_metadata.yml shared post settings: title banner, contents sidebar
    posts/_post-end.md  closing note included at the end of each post
    _brand.yml          colours and fonts
    theme.scss          component styling

## Writing a new post

Create `posts/<slug>/index.qmd` with `title`, `description`, `date` and
`categories`. Add `draft: true` to keep it out of the published site until ready.
Code blocks use plain ```` ```python ```` fences, so the site renders without Python or R installed.
