# journeyswithdata.dev

Quarto website. Chart-room styling lives entirely in `custom.css`.

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
- [ ] Contact strips (`index.qmd`, `work.qmd`) and `about.qmd` "Elsewhere" — add email / LinkedIn when ready
- [ ] Add your name somewhere (deliberately not guessed)

## Structure

    index.qmd           home: hero, focus areas, principles, latest posts, contact
    writing.qmd         full post listing with categories, search + RSS (writing.xml)
    work.qmd            the substance, writing by theme, ways to work together
    about.qmd           you, in your own words
    posts/              one post per folder
    posts/_metadata.yml shared post settings: contents sidebar, reading time, footer
    custom.css          all styling

## Writing a new post

Create `posts/<slug>/index.qmd` with `title`, `description`, `date` and
`categories`. Add `draft: true` to keep it out of the published site until ready.
Code blocks use plain ```` ```python ```` fences, so the site renders without Python or R installed.
