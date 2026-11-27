# Divine Match

A single-page Jekyll site for the Divine Match boutique matchmaking practice.

## Preview on this Mac

Open Terminal and run

```sh
cd ~/vscode/divine-match
bin/site serve
```

Open [the local preview](http://127.0.0.1:4000). Jekyll rebuilds the page when its copy or styles change. Restart the command after editing the site configuration. Press Control-C to stop the preview.

## Edit the site

- The homepage copy and the founders’ story live in `index.md`.
- The shared `application_url` in `_config.yml` points both application buttons to the applicant view of the Google Form. Google Forms handles sign-in and sends responses to the existing linked spreadsheet.
- The Liquid layout is in `_layouts/invitation.html`. The styles, locally hosted fonts, and images are in `assets/`.
- The original vision PDF is a local reference and is excluded from both Git and the website.

## Build

Run `bin/site build` to generate static HTML and assets in `_site/`. Only the generated directory is needed for static hosting.

This Mac has a project-local JRuby and Temurin installation in `.tools/`, with gems in `vendor/bundle/`. The lockfile targets JRuby. To reproduce this build from a fresh checkout, install [Temurin 21](https://adoptium.net/temurin/releases/?version=21) and [JRuby 10.0.8.0](https://www.jruby.org/download), then run

```sh
jruby -S bundle config set --local path vendor/bundle
jruby -S bundle install
jruby -S bundle exec jekyll serve
```

## Wedding hero image

The homepage uses the AI-generated wedding invitation background. The desktop image is `assets/images/invitation-soft-shadow-1880.webp`, and the mobile image is `assets/images/invitation-soft-shadow-960.webp`.
