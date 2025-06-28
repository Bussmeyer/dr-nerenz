# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a Hugo static site for Dr. Heike Nerenz's aesthetic medicine practice in Oldenburg, Germany. The site is built using the Hugo static site generator with a custom theme based on the Landkit framework.

## Development Commands

### Building and Serving
- `hugo server` - Start development server with live reload
- `hugo server -D` - Start development server including draft content  
- `hugo` - Build the static site for production (outputs to `public/`)
- `hugo -D` - Build including draft content

### Content Management
- `hugo new content/page-name.md` - Create new content page
- `hugo new content/section/page-name.md` - Create new page in a section

## Architecture

### Site Structure
- **hugo.toml** - Main Hugo configuration file with site settings, menus, and parameters
- **content/** - Markdown content files and images
  - `_index.html` - Homepage content (HTML format for complex layouts)
- **layouts/** - Hugo template files
  - `_default/baseof.html` - Base template with HTML structure
  - `_default/home.html` - Homepage template
  - `partials/` - Reusable template components (navbar, footer, head, etc.)
  - `shortcodes/` - Custom Hugo shortcodes for shapes and sections
- **assets/** - Source assets (CSS, images)
- **static/** - Static files copied directly to output (pre-built CSS/JS, fonts, images)
- **public/** - Generated static site (not committed to git)

### Theme Integration
The site uses a custom theme based on Landkit with:
- Bootstrap-based responsive design
- Pre-built CSS/JS bundles in `static/assets/`
- Custom color scheme (brown/beige as per recent commit)
- German language content
- Medical practice-specific navigation and content structure

### Key Configuration
- Site language: German (de-DE)
- Base URL: https://www.dr-nerenz.de/
- Menu structure defined in hugo.toml with main navigation and footer links
- Contact information and practice details in params section
- Minification enabled for production builds

### Content Structure
- Homepage combines HTML sections for complex layouts
- Menu-driven navigation with services (Leistungen) and contact sections
- Placeholder content still present from Landkit template (needs customization)
- Medical services include Botulinum toxin, Hyperhidrosis, and Allergology treatments

## Development Notes
- Hugo must be installed and available in PATH
- The site uses HTML content files for complex layouts rather than Markdown
- Static assets are pre-built and included in the repository
- Images are stored both in content/ and static/ directories depending on usage