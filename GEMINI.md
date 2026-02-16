# Gemini Project Context: My Awesome Blog

## Project Overview

This directory contains a Jekyll-based static website project for a personal blog titled "My Awesome Blog". The site is configured to be built and deployed via GitHub Pages using a Docker-based GitHub Actions workflow.

The main technologies used are:
- **Jekyll:** A static site generator written in Ruby.
- **Bundler:** For managing Ruby gem dependencies.
- **GitHub Actions:** For continuous integration and deployment.
- **Docker:** The build environment is containerized.

The website has a simple structure with a home page that lists blog posts, an about page, and a basic blog post layout. The styling is done via a single CSS file.

## Building and Running

### Building the site

The site is built automatically by a GitHub Actions workflow defined in `.github/workflows/jekyll-docker.yml`. The build command is:
```bash
jekyll build --future
```
This command is executed within a `jekyll/builder` Docker container.

To build the site manually, you can use the same Docker command or run it locally if you have Jekyll and Bundler installed:
```bash
bundle exec jekyll build
```

### Running the site locally

To preview the site locally, you can use the Jekyll `serve` command. This will start a local web server at `http://localhost:4000`.
```bash
bundle exec jekyll serve
```

## Development Conventions

The project follows the standard Jekyll directory structure:
- `_config.yml`: Main Jekyll configuration.
- `_layouts/`: HTML layouts for pages and posts.
- `_posts/`: Blog post files in Markdown format.
- `assets/`: For CSS, images, and other assets.
- `index.html`, `about.md`: Site pages.

When adding new posts, create a new Markdown file in the `_posts` directory with the naming convention `YYYY-MM-DD-title.md`.
