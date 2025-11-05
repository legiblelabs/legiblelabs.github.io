# Content Management Guide

## Where Content Lives

### Homepage (`src/pages/index.astro`)
- Hero section text
- About section
- Expertise cards (3 cards with icons and descriptions)
- CTA section

### Case Studies (`src/pages/case-studies.astro`)
- Array of case study objects (lines 5-76)
- Each study has: name, tagline, description, challenge, solution, impact, technologies, year

### Publications (`src/pages/publications.astro`)
- Array of publication objects (lines 5-39)
- Each publication has: title, type, date, description, link, tags

### Featured Projects (`src/components/FeaturedProjects.astro`)
- Array of project objects (lines 3-32)
- Each project has: name, url, description, icon, tags

### Social Proof (`src/components/SocialProof.astro`)
- Achievement cards (lines 14-37)
- Statistics section (lines 40-52)
- Testimonial content (lines 56-67)

## How to Update Content

### Option 1: Direct File Editing (Current Setup)

1. **Edit the file** with the content you want to change
   ```bash
   # Open in your editor
   code src/pages/case-studies.astro
   ```

2. **Test locally**
   ```bash
   npm run dev
   # Visit http://localhost:4321
   ```

3. **Build to verify**
   ```bash
   npm run build
   ```

4. **Commit and push**
   ```bash
   git add src/pages/case-studies.astro
   git commit -m "Update case studies content"
   git push
   ```

### Option 2: Separate Content Files (Recommended)

Move content to separate JSON/YAML files for easier management.

**Structure:**
```
src/
  content/
    case-studies.json
    publications.json
    projects.json
  pages/
    case-studies.astro  # Imports from content/
```

### Option 3: Content Collections (Astro Native)

Use Astro's built-in Content Collections for type-safe content management.

**Structure:**
```
src/
  content/
    config.ts           # Define schemas
    case-studies/       # Individual markdown files
      squidgies.md
      rori.md
    publications/
      ai-language-learning.md
```

### Option 4: Headless CMS Integration

Connect a CMS for non-technical team members:
- Decap CMS (free, git-based)
- Sanity.io
- Contentful
- TinaCMS

## Quick Examples

### Add a New Case Study
Edit `src/pages/case-studies.astro`, find the `caseStudies` array, add:

```javascript
{
  name: "New Project",
  tagline: "Project tagline",
  url: "https://project.com",
  description: "Full description...",
  icon: "🚀",
  color: "#3b82f6",
  challenge: "What problem...",
  solution: "How you solved it...",
  impact: [
    "Impact point 1",
    "Impact point 2"
  ],
  technologies: ["AI", "Python"],
  year: "2024"
}
```

### Update Social Proof Stats
Edit `src/components/SocialProof.astro`, find the stats section:

```html
<div class="stat-number" data-target="5">0</div>
<div class="stat-label">Major Projects</div>
```

### Change Hero Text
Edit `src/components/AnimatedHero.astro`:

```html
<h1 class="hero-title">
  Building the Future of
  <span class="gradient-text"> Your New Text</span>
</h1>
```

### Add a New Publication
Edit `src/pages/publications.astro`, add to the `publications` array:

```javascript
{
  title: "New Publication Title",
  type: "Case Study",  // or "Research", "Technical", "Blog"
  date: "2024",
  description: "Description text...",
  link: "https://...",
  tags: ["AI", "Education"]
}
```

## Recommendations

### For You (Technical User)
**Option 2: Separate Content Files** is probably best:
- Easy to find and edit content
- Keeps content separate from layout
- Still simple, no database needed
- Version controlled via Git

### For Non-Technical Team Members
**Option 4: Headless CMS** would be ideal:
- Visual editor interface
- No code editing required
- Still deploys via Git
- Preview changes before publishing

Would you like me to implement either of these approaches?
