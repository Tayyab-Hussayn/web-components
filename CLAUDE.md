# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a web components repository containing standalone HTML files that implement interactive 3D graphics using Three.js-based libraries. Each component is a self-contained HTML file with embedded JavaScript, CSS, and HTML.

## Code Architecture

- **Components Directory**: All components are located in `/components/` directory
- **Standalone HTML Files**: Each component is a single HTML file with embedded JavaScript
- **CDN Dependencies**: Libraries are loaded from CDNs (Tailwind CSS, Three.js components, Lucide icons)
- **No Build Process**: Components are vanilla HTML/JS/CSS with no build tools required

## Current Components

- `liquid-effect`: Interactive liquid background animation using Three.js
- `image-sphere`: 3D image sphere with dark/light mode toggle and animated text
- `tubes-cursor`: Interactive 3D tubes cursor effect that responds to clicks

## Development Commands

### Running Components
- Serve files directly from the file system or use a local HTTP server
- For local development: `npx http-server` (if available) or any static file server
- Open HTML files directly in browser (some features may require HTTP server due to module imports)

### Adding New Components
- Create new component directory in `/components/`
- Include a standalone HTML file with all necessary code
- Follow the same pattern of CDN imports and embedded JavaScript
- Use Tailwind CSS for styling via CDN

## Key Technologies

- **Three.js Components**: Imported from CDN (e.g., `https://cdn.jsdelivr.net/npm/threejs-components@x.x.x/`)
- **Tailwind CSS**: Loaded via CDN script tag
- **Lucide Icons**: For UI icons (where applicable)
- **Google Fonts**: For typography
- **Vanilla JavaScript**: No frameworks, uses native modules for Three.js components

## Development Patterns

- Components use ES6 modules for importing Three.js libraries
- DOM manipulation and event handling with vanilla JavaScript
- Intersection Observer API for animations (e.g., blur animations)
- Responsive design using Tailwind CSS classes
- Dark/light mode toggle functionality
- Cleanup of resources using `beforeunload` event listeners