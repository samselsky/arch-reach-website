# ARCH REACH website

Source for the ARCH REACH research center website, hosted via GitHub Pages at
**arch-reach.uw.edu**.

## What's here

- `index.html` — the entire site (single self-contained file: all CSS and JS
  are inline, no build step, no external dependencies besides Google Fonts).
  It's a lightweight single-page app: sections for Home, About Us (with
  sub-tabs for Team, the three Cores, and the three research projects),
  Papers, News, and Contact are all in this one file, shown/hidden with a
  little JavaScript router keyed off the URL hash (`#papers`, `#about:era`,
  etc.).
- `CNAME` — tells GitHub Pages which custom domain to serve the site on.

## Before this goes fully live

This started as an internal review draft, so a few things should be cleaned
up before we call it done:

- Remove the tan "Draft preview" banner at the very top of `index.html`
  (search for `draftbar`).
- Remove or replace the "Sample posts shown for layout" note on the News
  page, and swap in real news items.
- Fill in the "Our Team" page (currently a placeholder note).
- Replace the Contact form's `mailto:` behavior (see the `formfoot` note and
  the `contactForm` submit handler at the bottom of the file) with a real
  form backend or inbox before launch — right now it just opens the
  visitor's own email client.
- Double check the Papers list is still current — it reflects the team's
  published papers as of late September 2026.

## Making changes

Everything lives in `index.html`, organized with comment headers
(`<!-- ============ ABOUT ============ -->` etc.) for each page section, and
a `<style>` block at the top using CSS custom properties (`--teal`,
`--terracotta`, `--paper`, etc.) for the color palette — change a value once
at the top and it updates everywhere that color is used.

## Publishing changes

Push to the branch GitHub Pages is configured to deploy from (see the repo's
Settings → Pages) and the live site updates automatically within a minute or
two.
