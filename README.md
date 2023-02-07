# About

The code for HackWashU's org website. Generated from the [terminal](https://github.com/panr/hugo-theme-terminal) theme, and built with [Hugp](https://gohugo.io/).

# Contributing

## Structure
Everything is handled by the `/content` directory and `config.toml`.

`Config.toml` controls the menu bar. Each menu bar links to the url, ie `hackwashu.com/url`
It also controls a bunch of other stuff, see [terminal](https://github.com/panr/hugo-theme-terminal) for more info.

The `/content` directory has a bunch of subdirectories and a bunch of markdown files.

Every `name.md` in the `/content` directory is generated as a static site at `hackwashu.com/name`.

Every `name.md` in a `content/subdirectory/` is generated as a static site at `hackwashu.com/subdirectory/name`.

The framed welcome text is in `_index.md`, to remove the frame you remove the `framed = true` parameter in the frontmatter.

Hugo uses the terminal theme to generate the static site files, the template is linked in `config.toml`.

Served with a github actions script in `.github/workflows`, served from `/public`

## Available scripts

Make sure you're in the `general-website/` directory (the same directory as the `config.toml` file).

## Build and run server for testing

    hugo server

## Create new content

    hugo new name.md

In case you want to create content in a subdirectory, do

    hugo new subdirectory/name.md

## Steps to Contribute

1. (Optional) Install [Hugo](https://gohugo.io/installation/)
2. Fork the repository
3. Make your changes
4. Create a pull request

Installing Hugo is only necessary if you'd like to test & view your changes before submitting. For simple edits, this is not required.

For complex changes (anything involving site structure rewrites or custom HTML), please ensure you've tested your changes before you commit.

Building & Deployment is done on the `main` branch automatically via a Github Action.
