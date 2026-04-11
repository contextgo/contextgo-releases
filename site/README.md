# ContextGo Public Site Content

This directory is generated automatically from the private source repository.

## Structure

- `site/docs/latest.json` points the website to the latest released docs version
- `site/docs/versions.json` lists all released docs versions
- `site/docs/<version>/<locale>/index.json` contains the docs section metadata and article index
- `site/docs/<version>/<locale>/<slug>/article.json` contains the rendered article payload
- `site/docs/<version>/<locale>/<slug>/source.mdx` keeps the published source content visible in the repository
- `site/blog/<locale>/index.json` contains the blog section metadata and article index
- `site/blog/<locale>/<slug>/article.json` contains the rendered blog article payload
- `site/blog/<locale>/<slug>/source.mdx` keeps the published source content visible in the repository

The website consumes the JSON payloads and links back to the published source files when needed.
