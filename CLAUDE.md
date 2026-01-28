# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal "Jumppage" (link portal) built with Jekyll. It serves as a quick-access page for frequently used websites, organized into thematic tabs.

## Development Commands

```bash
# Install dependencies
bundle install

# Run local development server (http://localhost:4000/jumppage/)
bundle exec jekyll serve

# Build site for production
bundle exec jekyll build
```

Note: After changing `_config.yml`, you must restart the server.

## Architecture

**Theme & Styling:**
- Uses the Minima theme with custom SCSS in `_sass/two-columns.scss`
- Custom styles are imported via `assets/main.scss`

**Custom Layout:**
- `_layouts/two-columns.html` provides a tabbed navigation and two-column content layout
- Content is split into columns using the `<!--SPALTE2-->` marker in markdown files
- Navigation tabs are data-driven from `_data/navigation.yml`

**Content Pages:**
- Each `.markdown` file in the root (e.g., `KI.markdown`, `development.markdown`) represents a tab
- Pages use the `two-columns` layout and contain link lists organized by category

## Deployment

Hosted on GitHub Pages at `https://marcthoma.github.io/jumppage/`
