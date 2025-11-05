# Legible Labs Website

Modern, animated website for Legible Labs built with [Astro](https://astro.build).

## Features

- **Animated Hero Section**: Eye-catching landing page with floating elements and gradient animations
- **Case Studies**: Detailed project showcases including Squidgies, Rori, legible, and Refold Languages
- **Publications**: Filterable list of research, case studies, and technical articles
- **Social Proof**: Recognition and impact metrics including Schmidt Futures award
- **Responsive Design**: Mobile-first design that works beautifully on all devices

## Development

### Prerequisites

- Node.js 18+
- npm or yarn

### Getting Started

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## Project Structure

```
/
├── public/           # Static assets (CNAME, .nojekyll, images)
├── src/
│   ├── components/   # Reusable Astro components
│   ├── layouts/      # Page layouts
│   └── pages/        # Page routes
├── astro.config.mjs  # Astro configuration
└── package.json
```

## Deployment

The site automatically deploys to GitHub Pages when changes are pushed to the `main` branch via GitHub Actions.

Custom domain: www.legiblelabs.com

## Technologies

- **Astro** - Static site generator
- **TypeScript** - Type safety
- **CSS** - Custom animations and styling (no framework dependencies)

## Previous Version

The previous MkDocs-based site has been backed up to `_old_mkdocs/` directory.
