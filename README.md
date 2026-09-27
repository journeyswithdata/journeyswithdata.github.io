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

- [ ] `_quarto.yml` — real GitHub and LinkedIn URLs in the navbar (two `TODO`s)
- [ ] `index.qmd` — the contact strip at the bottom (email / LinkedIn / GitHub)
- [ ] `index.qmd` — confirm the three hero facts are how you want to be described
- [ ] `work.qmd` — the contact strip
- [ ] `about.qmd` — **rewrite in your own voice**; three TODOs marked inline
- [ ] `posts/hello-again/` — replace with a real post, remove `draft: true`
- [ ] Add your name somewhere — I deliberately did not guess your surname

## Structure

    index.qmd      home: hero, what I work on, latest 3 posts, contact
    writing.qmd    full post listing with categories + RSS
    work.qmd       the substance, positioned as work not CV
    about.qmd      you, in your own words
    posts/         one post per folder
    custom.css     all styling
