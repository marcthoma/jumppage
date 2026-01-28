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
- Mobile responsive at 768px breakpoint (tabs stack vertically, columns become single-column)

**Custom Layout:**
- `_layouts/two-columns.html` provides a tabbed navigation and two-column content layout
- Content is split into columns using the `<!--SPALTE2-->` marker in markdown files
- Navigation tabs are data-driven from `_data/navigation.yml`

**Content Pages:**
- Each `.markdown` file in the root (e.g., `KI.markdown`, `development.markdown`) represents a tab
- Pages must use front matter with `layout: two-columns`
- Link lists are organized by category using `## Heading` sections

## Adding a New Tab

1. Create a new `.markdown` file in the root directory with front matter:
   ```yaml
   ---
   layout: two-columns
   ---
   ```
2. Add the tab to `_data/navigation.yml` with `title` and `url` (e.g., `/filename.html`)
3. Use `<!--SPALTE2-->` marker to split content between left and right columns

## Deployment

Hosted on GitHub Pages at `https://marcthoma.github.io/jumppage/`
