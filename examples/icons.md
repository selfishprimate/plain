# Icons: Options & Examples

This guide helps you choose and implement icons for your product.

---

## Option 1: Lucide Icons

**Best for:** Modern web apps, React/Vue/Svelte projects, clean design

**Description:**
Lucide is a community-maintained fork of Feather Icons with 1000+ icons. It's clean, consistent, and actively maintained.

**Style:**
- Stroke-based (outline style)
- 24x24px default grid
- Customizable stroke width
- Rounded corners
- Consistent visual language

**Pros:**
- Beautiful, modern design
- Actively maintained
- Multiple framework support (React, Vue, Svelte)
- Tree-shakeable (import only what you need)
- Consistent stroke width
- MIT license (free for commercial use)

**Cons:**
- Smaller set than some alternatives
- Stroke-only (no filled variants)

**Installation:**
```bash
# React
npm install lucide-react

# Vue
npm install lucide-vue-next

# Svelte
npm install lucide-svelte
```

**Usage:**
```jsx
import { Heart, User, Search } from 'lucide-react';

<Heart size={24} strokeWidth={1.5} />
```

**Customization:**
- Size: Any pixel value
- Stroke width: 1, 1.5, 2, etc.
- Color: Inherits `currentColor` by default

**Learn More:** https://lucide.dev

---

## Option 2: Heroicons

**Best for:** Tailwind CSS projects, modern UI

**Description:**
Created by the makers of Tailwind CSS. Beautiful, hand-crafted icons with both outline and solid variants.

**Style:**
- Two variants: Outline (24x24) and Solid (20x20)
- Clean, minimal design
- Consistent with Tailwind design language

**Pros:**
- Created by Tailwind team
- Two styles (outline + solid)
- Beautiful design
- Framework support (React, Vue)
- MIT license

**Cons:**
- Smaller icon set (~300 icons)
- Tailwind-centric (but works anywhere)

**Installation:**
```bash
npm install @heroicons/react
```

**Usage:**
```jsx
import { HeartIcon } from '@heroicons/react/24/outline'
import { HeartIcon as HeartSolid } from '@heroicons/react/24/solid'

<HeartIcon className="w-6 h-6" />
<HeartSolid className="w-5 h-5" />
```

**Learn More:** https://heroicons.com

---

## Option 3: Tabler Icons

**Best for:** Large icon needs, diverse styles

**Description:**
4500+ free icons with a consistent 24x24px grid. One of the largest open-source icon sets.

**Style:**
- Stroke-based
- 24x24px grid
- 2px stroke width default
- Rounded corners
- Huge variety

**Pros:**
- Massive icon library (4500+)
- Consistent design
- Framework support
- React, Vue, Svelte, Angular
- Free and open-source

**Cons:**
- Can feel generic
- Large library can be overwhelming

**Installation:**
```bash
# React
npm install @tabler/icons-react

# Vue
npm install @tabler/icons-vue
```

**Usage:**
```jsx
import { IconHeart } from '@tabler/icons-react';

<IconHeart size={24} stroke={1.5} />
```

**Learn More:** https://tabler-icons.io

---

## Option 4: Phosphor Icons

**Best for:** Versatile styles, multiple weights

**Description:**
Flexible icon family with 6 weights (thin to bold). Clean, geometric design.

**Style:**
- 6 weights: Thin, Light, Regular, Bold, Fill, Duotone
- 32x32px grid
- Geometric, consistent

**Pros:**
- Multiple weights for hierarchy
- Filled and outline versions
- Duotone style available
- Clean, modern design
- Framework support

**Cons:**
- Medium-sized library (~1200 icons)
- Can be heavier if using all weights

**Installation:**
```bash
npm install phosphor-react
```

**Usage:**
```jsx
import { Heart } from "phosphor-react";

<Heart size={32} weight="bold" />
```

**Learn More:** https://phosphoricons.com

---

## Option 5: Material Icons (Google)

**Best for:** Material Design projects, Android apps

**Description:**
Google's official icon set for Material Design. Comprehensive and widely recognized.

**Style:**
- Filled, Outlined, Rounded, Two-tone, Sharp variants
- 24x24px grid
- Material Design language

**Pros:**
- Huge library (2000+ icons)
- 5 style variants
- Official Google icons
- Recognizable
- Well-documented

**Cons:**
- Very Material Design-specific
- Can look generic
- Heavier than minimal alternatives

**Installation:**
```bash
npm install @mui/icons-material
```

**Usage (with MUI):**
```jsx
import FavoriteIcon from '@mui/icons-material/Favorite';

<FavoriteIcon fontSize="large" />
```

**Or use CDN:**
```html
<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
<span class="material-icons">favorite</span>
```

**Learn More:** https://fonts.google.com/icons

---

## Option 6: Font Awesome

**Best for:** Wide variety, brand icons, legacy projects

**Description:**
One of the oldest and most comprehensive icon libraries. Free and Pro versions.

**Style:**
- Solid, Regular, Light, Duotone, Brands
- Consistent grid
- Huge variety

**Pros:**
- Massive library (2000+ free, 16000+ pro)
- Brand icons (social media, companies)
- Multiple styles
- Very mature

**Cons:**
- Pro version required for best icons
- Heavier than modern alternatives
- Less modern aesthetic
- Complex licensing for pro

**Installation:**
```bash
# Free version
npm install @fortawesome/fontawesome-free
```

**Usage:**
```html
<i class="fas fa-heart"></i>
```

**Learn More:** https://fontawesome.com

---

## Option 7: Custom Icons (SVG)

**Best for:** Unique branding, full control

**Description:**
Create or commission custom icons for your brand.

**Tools:**

**Design:**
- **Figma** — design and export SVGs
- **Illustrator** — professional icon design
- **Inkscape** — free, open-source

**Optimization:**
- **SVGO** — optimize SVG files
- **SVGOMG** — web-based optimizer (https://jakearchibald.github.io/svgomg/)

**Implementation:**
```jsx
// Inline SVG
export const CustomIcon = () => (
  <svg width="24" height="24" viewBox="0 0 24 24" fill="none">
    <path d="M12 21.35l-1.45-1.32C5.4 15.36 2 12.28 2 8.5 2 5.42 4.42 3 7.5 3c1.74 0 3.41.81 4.5 2.09C13.09 3.81 14.76 3 16.5 3 19.58 3 22 5.42 22 8.5c0 3.78-3.4 6.86-8.55 11.54L12 21.35z" fill="currentColor"/>
  </svg>
);
```

**React Component Library:**
```bash
npm install @svgr/webpack
# Auto-converts SVG to React components
```

**Pros:**
- Complete brand control
- Unique to your product
- Optimized for your needs
- No licensing concerns

**Cons:**
- Time-consuming to create
- Requires design skills
- Maintenance overhead
- Consistency challenges

**Best Use Cases:**
- Strong brand identity
- Unique product needs
- Marketing sites
- Agencies

---

## Icon Size Guide

**Common Sizes:**

```
16px — tiny icons, dense UIs
20px — small buttons, inline icons
24px — standard UI icons (most common)
32px — larger buttons, emphasis
48px — feature cards, empty states
64px+ — hero sections, illustrations
```

**Responsive:**
```css
/* Mobile */
.icon {
  width: 20px;
  height: 20px;
}

/* Desktop */
@media (min-width: 1024px) {
  .icon {
    width: 24px;
    height: 24px;
  }
}
```

---

## Icon Usage Best Practices

**1. Consistency**
- Use one icon library throughout your app
- Maintain consistent stroke width
- Use same style (all outline or all filled)

**2. Accessibility**
- Add `aria-label` for interactive icons
- Use descriptive alt text
- Don't rely on color alone

```jsx
// Good
<button aria-label="Add to favorites">
  <HeartIcon />
</button>

// Bad
<button>
  <HeartIcon />
</button>
```

**3. Color**
- Use `currentColor` to inherit text color
- Semantic colors for actions (red for delete, green for success)

```css
.icon {
  color: currentColor; /* Inherits from parent */
}
```

**4. Alignment**
- Vertically center icons with text
- Use consistent spacing

```css
.icon-text {
  display: flex;
  align-items: center;
  gap: 8px;
}
```

**5. Interactive States**
- Hover, focus, active states for clickable icons
- Visual feedback

```css
.icon-button:hover .icon {
  opacity: 0.8;
  transform: scale(1.1);
}
```

---

## Icon Types by Purpose

**Navigation:**
- Home, Menu, Search, Settings, User

**Actions:**
- Edit, Delete, Add, Save, Download, Upload

**Status:**
- Success (check), Error (x), Warning (alert), Info (i)

**Social:**
- Twitter, Facebook, GitHub, LinkedIn

**Media:**
- Play, Pause, Volume, Image, Video

**E-commerce:**
- Cart, Wishlist, Filter, Star (rating)

**Communication:**
- Mail, Message, Phone, Notification

---

## Decision Guide

| **Your Need** | **Recommended Library** |
|---|---|
| Modern React/Vue app | Lucide Icons |
| Tailwind CSS project | Heroicons |
| Large icon variety | Tabler Icons |
| Multiple weights/styles | Phosphor Icons |
| Material Design | Material Icons |
| Brand/social icons | Font Awesome (Free) |
| Custom brand | Custom SVG Icons |

---

## Comparison Table

| **Library** | **Count** | **Style** | **Framework Support** | **License** |
|---|---|---|---|---|
| Lucide | 1000+ | Stroke | React, Vue, Svelte | MIT |
| Heroicons | 300+ | Outline + Solid | React, Vue | MIT |
| Tabler | 4500+ | Stroke | React, Vue, Svelte | MIT |
| Phosphor | 1200+ | 6 weights | React, Vue | MIT |
| Material Icons | 2000+ | 5 styles | React (MUI) | Apache 2.0 |
| Font Awesome | 2000+ free | Multiple | All | Various |

---

## Implementation Checklist

- [ ] Choose icon library
- [ ] Install and configure
- [ ] Define default size (usually 24px)
- [ ] Set stroke width or style
- [ ] Create icon wrapper component (optional)
- [ ] Document icon usage in design system
- [ ] Add accessibility labels
- [ ] Test with screen readers

---

## Example Icon Systems

**Minimal (Lucide)**
```jsx
import { Heart, User, Settings } from 'lucide-react';

const Icon = ({ name, size = 24 }) => {
  const icons = { Heart, User, Settings };
  const Component = icons[name];
  return <Component size={size} strokeWidth={1.5} />;
};
```

**Multi-Style (Heroicons)**
```jsx
import { HeartIcon } from '@heroicons/react/24/outline';
import { HeartIcon as HeartSolid } from '@heroicons/react/24/solid';

// Use outline by default, solid for active state
```

**Custom SVG System**
```jsx
// icons/index.js
export { default as HeartIcon } from './heart.svg';
export { default as UserIcon } from './user.svg';

// Usage
import { HeartIcon } from '@/icons';
```

---

## Resources

- **Lucide:** https://lucide.dev
- **Heroicons:** https://heroicons.com
- **Tabler Icons:** https://tabler-icons.io
- **Phosphor:** https://phosphoricons.com
- **Material Icons:** https://fonts.google.com/icons
- **Font Awesome:** https://fontawesome.com
- **Icon Search:** https://icones.js.org (search across libraries)
