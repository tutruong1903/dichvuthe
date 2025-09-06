# WARP.md

This file provides guidance to WARP (warp.dev) when working with code in this repository.

## Project Overview

This is a static HTML/CSS landing page for "DichVuTheUyTin", a Vietnamese financial services business offering credit card cash advance and payment services in Ho Chi Minh City.

## Development Setup

This is a simple static website with no build process or dependencies. The project consists of:
- `index.html` - Single-page application with all content
- `index.css` - All styles in one CSS file  
- `README.md` - Basic project documentation

### Running the Website

To view the website locally:
```bash
# Option 1: Using Python's built-in server
python3 -m http.server 8000

# Option 2: Using Node.js serve (if available)
npx serve .

# Option 3: Open directly in browser
open index.html
```

The website will be available at `http://localhost:8000` (for Python server).

## Architecture & Structure

### Frontend Structure
- **Single Page Application (SPA)**: All content is contained in `index.html`
- **Vanilla JavaScript**: Minimal JavaScript for mobile menu toggle and smooth scrolling
- **CSS Variables**: Uses CSS custom properties for theming and consistency
- **Responsive Design**: Mobile-first approach with hamburger menu

### CSS Architecture
The CSS is organized into logical sections:
- Global styles and CSS variables (`:root`)
- Button system (`.btn`, `.btn-primary`, `.btn-secondary`)
- Layout components (header, sections, footer)
- Responsive breakpoints for mobile devices

### Key Components
- **Header**: Fixed navigation with mobile hamburger menu
- **Hero Section**: Main call-to-action with contact information
- **Services Section**: Three-card layout highlighting service benefits
- **Benefits Section**: Image + checklist layout
- **Contact Section**: Contact information and basic form
- **Footer**: Company information and copyright
- **Floating Contact**: Sticky phone and Zalo buttons

## Key Features

### Contact Integration
- Phone links: `tel:0909378408` for direct calling
- Zalo integration: `https://zalo.me/0909378408`
- Contact form (basic HTML form, no backend processing)

### External Dependencies
- Google Fonts (Roboto family)
- Font Awesome 6.0.0 for icons
- External images hosted on `dichvutheuytin.site`

### Mobile Responsiveness
- Hamburger menu for mobile navigation
- Responsive grid layouts
- Touch-friendly buttons and spacing

## Content Management

All content is hardcoded in Vietnamese in the HTML file. To update content:

1. **Text Changes**: Edit directly in `index.html`
2. **Styling**: Modify CSS variables in `index.css` for consistent changes
3. **Images**: Update image URLs in the `<img>` tags (currently external links)
4. **Contact Info**: Update phone number `0909378408` in multiple locations

## Testing

Since this is a static site with minimal JavaScript:

```bash
# Validate HTML
# Use an online HTML validator or install a local one

# Test responsive design
# Use browser dev tools to test different screen sizes

# Test contact links
# Verify phone links work on mobile devices
# Test Zalo link functionality
```

## Deployment

This static site can be deployed to any web server or static hosting service:
- GitHub Pages
- Netlify
- Vercel
- AWS S3
- Traditional web hosting

Simply upload all files to the web server root directory.
