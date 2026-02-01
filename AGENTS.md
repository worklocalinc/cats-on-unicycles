# Cats on Unicycles

> A delightful website celebrating the majestic art of cats riding unicycles

## Overview

Cats on Unicycles is a fun, visual website showcasing the whimsical world of felines balancing on single-wheeled contraptions. The site features a gallery of cats on unicycles, fun facts, a history timeline, and community submissions. Perfect for cat lovers and unicycle enthusiasts alike!

## Tech Stack

| Layer | Technology | Why |
|-------|------------|-----|
| Frontend | HTML5 + CSS3 + Vanilla JS | Lightweight, fast, no build step needed |
| Styling | Tailwind CSS (via CDN) | Modern utility-first styling |
| Animations | CSS animations + GSAP | Smooth, engaging interactions |
| Images | Unsplash + user uploads | High-quality cat photos |
| Deployment | Cloudflare Pages | Fast global CDN, free SSL |

## Project Structure (Expected)

```
/
├── index.html              # Homepage with hero + featured cats
├── gallery.html            # Full photo gallery with filters
├── history.html            # Timeline of cats on unicycles
├── facts.html              # Fun facts page
├── submit.html             # Community submission form
├── css/
│   └── styles.css          # Custom styles beyond Tailwind
├── js/
│   ├── main.js             # Main interactions
│   ├── gallery.js          # Gallery filtering/lightbox
│   └── animations.js       # Scroll animations
├── assets/
│   ├── images/             # Cat photos (organized by category)
│   │   ├── hero/
│   │   ├── gallery/
│   │   └── thumbnails/
│   └── icons/              # Unicycle/cat icons
└── data/
    └── cats.json           # Gallery data (titles, descriptions)
```

## Pages Design

### 1. Homepage (index.html)
**Purpose:** Landing page with wow factor

**Sections:**
| Section | Content | Animation |
|---------|---------|-----------|
| Hero | Large unicycle cat image, tagline "Balance. Grace. Whiskers." | Parallax scroll |
| Featured | 3-4 highlighted cat photos | Fade in on scroll |
| Stats | "1,337 cats unicycling worldwide" counter | Number count-up |
| CTA | "Explore Gallery" + "Submit Your Cat" buttons | Hover bounce |

### 2. Gallery (gallery.html)
**Purpose:** Browse all cat photos

**Features:**
- Filter by: All, Orange Cats, Black Cats, Tabby, Multi-cat, Action shots
- Lightbox view for full-size images
- Lazy loading for performance
- Masonry/grid layout

**Data Structure (cats.json):**
```json
{
  "cats": [
    {
      "id": 1,
      "name": "Whiskers",
      "breed": "Orange Tabby",
      "image": "assets/images/gallery/whiskers.jpg",
      "thumbnail": "assets/images/thumbnails/whiskers.jpg",
      "category": "orange",
      "description": "Master of the one-wheeled arts",
      "submitted_by": "@catmom99",
      "date_added": "2026-01-15"
    }
  ]
}
```

### 3. History (history.html)
**Purpose:** Timeline of cats on unicycles through history

**Timeline Events:**
| Year | Event |
|------|-------|
| 1867 | First documented cat on unicycle (Paris) |
| 1923 | Silent film "The Unicycling Feline" premieres |
| 1969 | Moon landing broadcast interrupted by unicycle cat |
| 1995 | First internet cat unicycle GIF goes viral |
| 2010 | International Cat Unicycle Day established |
| 2024 | AI generates first photorealistic unicycle cat |

### 4. Facts (facts.html)
**Purpose:** Educational fun facts

**Fact Cards (6-8 facts):**
- "Cats have better balance than humans on unicycles"
- "The world record: 47 seconds of continuous unicycling"
- "Orange cats are 23% more likely to ride unicycles"
- "Unicycle cats purr 15% louder than regular cats"
- Each fact has an icon and share button

### 5. Submit (submit.html)
**Purpose:** Community photo submissions

**Form Fields:**
| Field | Type | Required |
|-------|------|----------|
| Cat Name | text | Yes |
| Your Name | text | Yes |
| Email | email | Yes |
| Photo | file (jpg/png, max 5MB) | Yes |
| Cat Breed | select | No |
| Story | textarea | No |
| Terms checkbox | checkbox | Yes |

**Features:**
- Image preview before upload
- File size validation
- Success message animation

## UI/UX Requirements

### Color Palette
| Color | Hex | Usage |
|-------|-----|-------|
| Primary | #FF6B35 | Buttons, accents, highlights |
| Secondary | #4ECDC4 | Links, secondary buttons |
| Background | #FFF8F0 | Page background |
| Dark | #2D3436 | Text, headers |
| Accent | #FFE66D | Highlights, badges |

### Typography
- **Headings:** Poppins (Google Fonts) - bold, playful
- **Body:** Inter - clean, readable
- **Accent:** Comic Neue - for fun quotes/facts

### Animations
| Element | Animation | Trigger |
|---------|-----------|---------|
| Hero image | Subtle float | Always |
| Cards | Fade up + scale | Scroll into view |
| Buttons | Bounce on hover | Mouse hover |
| Gallery items | Stagger fade in | Page load |
| Nav links | Underline slide | Hover |

### Responsive Breakpoints
- Mobile: < 640px (single column)
- Tablet: 640px - 1024px (2 columns)
- Desktop: > 1024px (3-4 columns)

## External Services

| Service | Purpose | Notes |
|---------|---------|-------|
| Cloudflare Pages | Hosting | Auto-deploy on git push |
| Unsplash API | Stock cat photos | Free tier: 50 requests/hour |
| Formspree | Form handling | For submit page (free tier) |

## Development Conventions

### File Naming
- HTML: lowercase with hyphens (`gallery.html`)
- CSS: lowercase (`styles.css`)
- JS: lowercase, descriptive (`gallery-filter.js`)
- Images: descriptive with hyphens (`orange-cat-unicycle.jpg`)

### Code Patterns
- Use semantic HTML5 elements
- BEM naming for custom CSS classes
- Vanilla JS, no frameworks needed
- Progressive enhancement (works without JS)

### Performance
- Lazy load images below fold
- Optimize images (WebP with JPG fallback)
- Minify CSS/JS for production
- Use CDN for libraries

## Development

```bash
# No build step needed - just open in browser
# For local development with live reload:
npx live-server
```

Preview: https://cats-on-unicycles.sha.red

## Status Checklist

- [ ] Project scaffolded (Bootstrap Agent)
- [ ] Homepage built with hero section (@frontend)
- [ ] Gallery page with filtering (@frontend)
- [ ] History timeline page (@frontend)
- [ ] Facts page with cards (@frontend)
- [ ] Submit form with validation (@frontend)
- [ ] Responsive design implemented (@frontend)
- [ ] Animations added (@frontend)
- [ ] Sample cat images added
- [ ] Production deployed
