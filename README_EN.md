<p align="center">
  <img src="./docs/assets/contextgo-readme-header.png" alt="ContextGo Releases" width="100%">
</p>

<p align="center">
  <img src="./docs/assets/contextgo-logo.png" alt="ContextGo Logo" width="108">
</p>

<p align="center">
  <strong>ContextGo Releases</strong><br>
  The public release and distribution endpoint for ContextGo.
</p>

<p align="center">
  <a href="./README.md">中文</a> ·
  <a href="https://github.com/contextgo/contextgo">Main ContextGo Repo</a> ·
  <a href="https://github.com/contextgo/contextgo-releases">GitHub</a>
</p>

---

## What This Is

`contextgo-releases` is the public release repository in the ContextGo product matrix.

Its job is simple, but important:

- publish installers and GitHub Releases
- publish version metadata, manifests, and updater-consumable release facts
- publish website-readable public release content

It is not the main product source repository, and it is not the place for internal engineering documents.

---

## Why It Exists Separately

The main product repository can continue to own product code, website code, internal plans, and release automation, while the public release surface needs a cleaner and more stable endpoint.

Splitting that boundary makes it possible to:

- keep installers and public release history visible
- give the desktop updater and download center a stable source of truth
- let the website consume structured public content
- avoid exposing private source code, unfinished implementation details, and internal documents

---

## What Lives Here

This repository should carry:

- GitHub Releases and attached installers
- release metadata
- checksums and distribution manifests
- exported public website content under `site/`

For website-facing content:

- `site/docs/` stores versioned documentation payloads
- `site/blog/` stores public blog payloads
- each article directory includes:
  - `article.json`
  - `source.mdx`

---

## What Does Not Live Here

This repository should not carry:

- main product source code
- internal engineering plans or design records
- the source-of-truth build system for the website itself

It is a **public distribution endpoint**, not a replacement for the main development repository.

---

## How It Is Consumed

`contextgo-releases` mainly serves three audiences:

- end users
  - download installers from Releases
- desktop updater / download-center flows
  - consume version and distribution metadata
- the website
  - consume exported public content under `site/`

This repository exists to make release facts public, stable, and machine-consumable.

---

## Relationship To The Main Repository

The responsibility split is:

- [`contextgo`](https://github.com/contextgo/contextgo)
  - product code
  - WebUI and mobile shell
  - Agent Packages
  - Context Engine
  - website source and release automation
- [`contextgo-releases`](https://github.com/contextgo/contextgo-releases)
  - public artifacts
  - public manifests
  - public release history
  - exported public docs and blog payloads

The main repository produces. The release repository publishes.

---

## User Entry Points

If you only want to get ContextGo:

- browse this repository's GitHub Releases

If you want the full product:

- see the [main ContextGo repository](https://github.com/contextgo/contextgo)

If you want the related open subprojects:

- [Connector](https://github.com/contextgo/connector)
- [SkillMarket](https://github.com/contextgo/skillmarket)

---

## Public Release Principles

This repository follows a few long-lived rules:

- Git tags plus GitHub Releases are the public source of truth
- the website should consume release metadata rather than inventing a second version source
- the public release repository may stay separate from the source repository while preserving one brand and one product identity

That gives ContextGo a stable public endpoint while the product itself continues to evolve quickly.
