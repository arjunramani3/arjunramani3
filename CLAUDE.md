# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a personal website for Arjun Ramani (arjunramani.com), built with Jekyll and hosted on GitHub Pages. The site showcases research, writing, and professional work in economics and technology journalism.

## Development Commands

### Building and Testing
```bash
# Build the site locally
bundle exec jekyll build

# Serve the site locally with live reload
bundle exec jekyll serve

# The site will be available at http://localhost:4000
```

### Dependencies
```bash
# Install Ruby dependencies
bundle install

# Update dependencies
bundle update
```

## Site Architecture

### Build System
- **Static Site Generator**: Jekyll with GitHub Pages
- **Dependencies**: Managed via Gemfile using `github-pages` gem bundle
- **Build Output**: Generated to `_site/` directory (not committed to git)
- **Configuration**: `_config.yml` contains site metadata and Jekyll plugins

### Content Structure
The site uses static HTML files rather than Jekyll's typical Markdown approach:
- `index.html` - Homepage with bio and links
- `research.html` - Academic research and publications
- `writing.html` - Journalism and writing portfolio
- `portfolio.html` - Comprehensive list of articles by publication
- `cv.html` - CV with PDF link
- `india-dispatch.html` - Long-form essay on India reporting

All pages share a common navigation structure in the `top-nav` div.

### Styling
- **Single Stylesheet**: `styles.css` contains all styling
- **Design System**:
  - Primary color: `#008080` (teal) for links and navigation
  - Hover state: `#005959` (darker teal)
  - Font: Georgia serif for body text
  - Max content width: 800px
  - Responsive breakpoints at 768px and 480px for mobile

### RSS/Feed
- `feed.xml` - Manually maintained RSS feed for new content
- Update this file when publishing new essays or major updates

### Assets
- Images stored in root directory and `images/` subdirectory
- Cover images from The Economist articles (webp/jpg format)
- `headshot-uk.jpg` - Profile photo
- `Ramani, Arjun CV.pdf` - CV document

## Content Maintenance

### Adding New Research
Edit `research.html` and add to the appropriate section:
- Published work
- In progress
- Policy work
- Seminars & talks

### Adding New Writing
1. Add to `writing.html` under "Best work" if featured
2. Always add to `portfolio.html` with full citation and date
3. Update `feed.xml` if it's a major essay or dispatch

### Navigation Changes
The top navigation is duplicated across all HTML files. When modifying navigation:
1. Update the `top-nav` div structure in all files
2. Maintain consistency of links: Research, Writing, CV, Subscribe/RSS

### Analytics
All pages include Google Analytics (gtag.js) with ID `G-N1YFKE5YHG` at the bottom of each file.

## Key Conventions

### Link Styling
All links use consistent teal color scheme (`#008080`) with visited state maintained. This applies to:
- Navigation links
- Content links
- Sidebar links
- Subscribe/RSS links

### Responsive Design
The site has three layouts:
1. Desktop (>768px): Full navigation, 800px content width
2. Tablet/Mobile (≤768px): Stacked navigation, full-width content
3. Small mobile (≤480px): Reduced fonts, compressed spacing

### Jekyll Configuration
Important settings in `_config.yml`:
- SEO tags enabled via `jekyll-seo-tag`
- Sitemap generation via `jekyll-sitemap`
- No theme applied (`theme: null`) - custom HTML/CSS only

## Deployment

The site is deployed via GitHub Pages automatically when changes are pushed to the master branch. The CNAME file contains `arjunramani.com` for custom domain routing.
