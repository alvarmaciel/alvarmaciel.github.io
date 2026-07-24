# Agent Instructions for alvarmaciel.github.io

This repository contains Alvar Maciel's personal Hugo website.

Start by reading:

1. `.agents/project-context.json`
2. `config/_default/hugo.toml`
3. `config/_default/params.es.toml`
4. `content/media/lento_es_normal/_index.es.md`
5. `layouts/media/lento_es_normal/rss.xml`
6. `layouts/shortcodes/archiveaudio.html`
7. `docs/archive-audio.md`

## Project summary

- Static site built with Hugo.
- Uses the Blowfish theme as a git submodule under `themes/blowfish/`.
- Deployed to GitHub Pages through `.github/workflows/gh-pages.yml`.
- Spanish is the default language; English content also exists.
- Content lives under `content/`.
- Custom project-level layouts/shortcodes live under `layouts/`.
- Static files live under `static/` and assets under `assets/`.
- Generated output is in `public/`.

## Important content areas

- Home:
  - `content/_index.es.md`
  - `content/_index.en.md`
- Bio:
  - `content/bio/`
- Blog posts:
  - `content/posts/`
- Media:
  - `content/media/`
- Lento es normal:
  - `content/media/lento_es_normal/`
  - custom RSS: `layouts/media/lento_es_normal/rss.xml`

## Podcast / Archive.org conventions

This repo has:

```txt
layouts/shortcodes/archiveaudio.html
scripts/archive_metadata.py
docs/archive-audio.md
```

Current usage:

```md
{{< archiveaudio id="ARCHIVE_ID" >}}
```

For future Archive.org audio episodes, prefer front matter like:

```yaml
archive:
  id: "ARCHIVE_ID"
  url: "https://archive.org/details/ARCHIVE_ID"
  image: "https://archive.org/download/ARCHIVE_ID/image.jpg"
audio:
  - "https://archive.org/download/ARCHIVE_ID/audio.mp3"
enclosures:
  - url: "https://archive.org/download/ARCHIVE_ID/audio.mp3"
    type: "audio/mpeg"
    length: 123456789
duration: "51:26"
tags:
  - "tag"
```

Important:

- Keep `audio` as a list of URL strings.
- Do **not** put objects/maps inside `audio`; Hugo themes often use `.Params.audio` for OpenGraph and expect strings.
- Put rich podcast RSS metadata in `enclosures`.
- `enclosures.length` means file size in bytes.
- `duration` means episode duration.

Archive.org metadata:

```txt
https://archive.org/metadata/ARCHIVE_ID
```

Mapping:

- RSS enclosure length = `files[].size`
- podcast duration = `files[].length`, converted from seconds
- tags = `metadata.subject`
- direct MP3 URL = `https://archive.org/download/ARCHIVE_ID/FILENAME.mp3`

## Do not edit unless explicitly asked

- `themes/blowfish/`
- `public/`
- `.git/`
- `.hugo_build.lock`

## Working guidelines

- Do not assume the Radio San Javier site structure applies here.
- This site does **not** use program-specific CMS collections from Radio San Javier.
- Prefer project-level overrides in `layouts/` instead of modifying Blowfish.
- Before changing podcast RSS, inspect:
  - `layouts/media/lento_es_normal/rss.xml`
  - `content/media/lento_es_normal/`
  - `[params.podcast]` in `config/_default/hugo.toml`
- Archive.org helper script exists at `scripts/archive_metadata.py`.
- Archive.org audio docs live at `docs/archive-audio.md`; update them when the workflow changes.
- Keep user-facing Spanish in Argentinian/Rioplatense Spanish unless the user asks otherwise.

## Known cleanup areas

- Root `hugo.toml` has placeholder values; real config appears to be in `config/_default/hugo.toml`.
- `public/` is committed/generated output; avoid editing manually.
- `layouts/media/lento_es_normal/rss.xml` was modernized for `enclosures`, enclosure length, fallback to `audio`, and `content:encoded`; validate after changes with Hugo and a podcast feed validator.
