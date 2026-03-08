# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site using the Hyde theme (a two-column responsive blog theme). The site uses Hugo v0.157.0+ and follows the standard Hugo project structure.

## Development Commands

**Build the site:**
```bash
hugo
```

**Run development server:**
```bash
hugo server
```

**Run development server with drafts:**
```bash
hugo server -D
```

**Clean build artifacts:**
```bash
rm -rf public/
```

## Architecture

**Theme Structure:**
- Theme located in `themes/hyde/` (git submodule)
- Custom layouts can override theme layouts by placing them in root `layouts/` directory
- Theme uses base template pattern: `baseof.html` defines overall structure, other templates fill in blocks

**Key Template Files:**
- `themes/hyde/layouts/_default/baseof.html` - Base template with sidebar and main content container
- `themes/hyde/layouts/partials/sidebar.html` - Left sidebar navigation
- `themes/hyde/layouts/_default/single.html` - Individual post/page template
- `themes/hyde/layouts/_default/list.html` - List pages (archives, sections)

**Content Organization:**
- `content/posts/` - Blog posts
- `content/about.md` - About page
- Front matter controls draft status, date, title

**Configuration:**
- `config.toml` - Site configuration including theme settings, analytics, Disqus
- Theme color and layout direction controlled via `params.themeColor` and `params.layoutReverse`

**Static Assets:**
- `static/` - Static files served at site root
- Theme CSS/JS in `themes/hyde/static/`

## Theme Customization

Hyde supports 8 color themes via `themeColor` parameter in config.toml. Layout can be reversed (sidebar on right) with `layoutReverse = true`.
