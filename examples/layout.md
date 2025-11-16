# Layout: Grid Systems & Spacing

This guide helps you define layout structure, grid systems, and spacing for your product.

---

## Grid Systems

### Option 1: 12-Column Grid (Most Common)

**Best for:** Responsive websites, flexible layouts

**Description:**
A 12-column grid divides the screen into 12 equal columns. Content spans multiple columns.

**Why 12?**
12 is divisible by 2, 3, 4, and 6—making it very flexible for layouts.

**Breakpoints:**
```
Mobile: 1-12 columns (stack vertically)
Tablet: 2-6 columns
Desktop: 3-12 columns
```

**Example Layouts:**
```
Sidebar + Content: 3 columns + 9 columns
Two columns: 6 columns + 6 columns
Three columns: 4 + 4 + 4 columns
Four columns: 3 + 3 + 3 + 3 columns
```

**Implementation (CSS Grid):**
```css
.container {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  gap: 24px;
}

.sidebar {
  grid-column: span 3; /* Takes 3 columns */
}

.main-content {
  grid-column: span 9; /* Takes 9 columns */
}

/* Responsive */
@media (max-width: 768px) {
  .sidebar, .main-content {
    grid-column: span 12; /* Full width on mobile */
  }
}
```

**Frameworks using 12-column:**
- Bootstrap
- Tailwind CSS
- Material UI
- Foundation

---

### Option 2: 8-Column Grid

**Best for:** Simpler layouts, less flexibility needed

**Description:**
An 8-column grid is simpler than 12-column but less flexible.

**Divisible by:** 2, 4, 8

**Example Layouts:**
```
Two columns: 4 + 4
Sidebar + Content: 2 + 6
Four columns: 2 + 2 + 2 + 2
```

**Best Use Cases:**
- Marketing websites
- Landing pages
- Simple blogs

---

### Option 3: 16-Column Grid (Complex Layouts)

**Best for:** Dense interfaces, data-heavy dashboards

**Description:**
More granular control with 16 columns.

**Divisible by:** 2, 4, 8, 16

**Best Use Cases:**
- Admin dashboards
- Complex table layouts
- Multi-column data views

---

### Option 4: No Grid (Freeform)

**Best for:** Creative layouts, unique designs

**Description:**
Use CSS Grid or Flexbox without predefined columns. Custom layouts.

**Pros:**
- Complete freedom
- Unique designs
- Not constrained by columns

**Cons:**
- Harder to maintain consistency
- More complex responsive behavior

**Example:**
```css
.container {
  display: grid;
  grid-template-columns: 300px 1fr 200px;
  gap: 32px;
}
```

---

## Spacing Systems

### Option 1: 8-Point Grid (Most Popular)

**Description:**
All spacing uses multiples of 8px. This creates visual consistency and aligns with most screen densities.

**Scale:**
```
0: 0px
1: 8px
2: 16px
3: 24px
4: 32px
5: 40px
6: 48px
8: 64px
10: 80px
12: 96px
16: 128px
```

**Why 8?**
- Aligns with device pixels (most screens are multiples of 8)
- Creates rhythm and consistency
- Easy to scale (8, 16, 24, 32...)

**Usage:**
```css
.card {
  padding: 24px; /* 3 units */
  margin-bottom: 32px; /* 4 units */
  gap: 16px; /* 2 units */
}
```

**Frameworks:**
- Tailwind CSS (default spacing)
- Material UI
- Chakra UI

---

### Option 2: 4-Point Grid (More Granular)

**Description:**
Uses multiples of 4px for finer control.

**Scale:**
```
0: 0px
1: 4px
2: 8px
3: 12px
4: 16px
5: 20px
6: 24px
8: 32px
12: 48px
16: 64px
```

**Pros:**
- More flexibility
- Finer adjustments

**Cons:**
- Can lead to inconsistency
- More decisions to make

**Best For:**
- Custom designs
- Pixel-perfect layouts

---

### Option 3: Tailwind Spacing Scale

**Description:**
Tailwind uses a 0.25rem (4px) base with a predefined scale.

**Scale:**
```
0: 0px
0.5: 2px
1: 4px
2: 8px
3: 12px
4: 16px
5: 20px
6: 24px
8: 32px
10: 40px
12: 48px
16: 64px
20: 80px
24: 96px
32: 128px
```

**Usage:**
```html
<div class="p-4 mb-6 space-y-2">
  <!-- padding: 16px, margin-bottom: 24px, gap: 8px -->
</div>
```

**Pros:**
- Well-thought-out scale
- Works for most use cases
- Standard across Tailwind projects

---

## Container Widths

### Fixed-Width Containers

**Approach:**
Set maximum width for content containers to maintain readability.

**Common Max Widths:**
```
sm: 640px (mobile-first content)
md: 768px (tablet)
lg: 1024px (desktop)
xl: 1280px (large desktop)
2xl: 1536px (extra large)
```

**Example:**
```css
.container {
  max-width: 1280px;
  margin-left: auto;
  margin-right: auto;
  padding-left: 16px;
  padding-right: 16px;
}
```

**Best For:**
- Content-focused sites
- Marketing pages
- Blogs

---

### Full-Width Layouts

**Approach:**
Content spans the full viewport width.

**Example:**
```css
.container {
  width: 100%;
  padding-left: 24px;
  padding-right: 24px;
}
```

**Best For:**
- Dashboards
- Apps with sidebars
- Image-heavy sites

---

### Hybrid (Breakout Sections)

**Approach:**
Some sections are contained, others are full-width.

**Example:**
```css
.container {
  max-width: 1280px;
  margin: 0 auto;
}

.full-width {
  width: 100vw;
  margin-left: calc(-50vw + 50%);
}
```

**Best For:**
- Marketing sites with featured content
- Landing pages

---

## Responsive Breakpoints

### Standard Breakpoints

**Mobile-First Approach (Recommended):**
```css
/* Mobile (default, no media query) */
body {
  font-size: 16px;
}

/* Tablet and up */
@media (min-width: 640px) {
  /* sm */
}

@media (min-width: 768px) {
  /* md */
}

/* Desktop and up */
@media (min-width: 1024px) {
  /* lg */
}

@media (min-width: 1280px) {
  /* xl */
}

@media (min-width: 1536px) {
  /* 2xl */
}
```

**Tailwind Breakpoints:**
```
sm: 640px
md: 768px
lg: 1024px
xl: 1280px
2xl: 1536px
```

**Bootstrap Breakpoints:**
```
sm: 576px
md: 768px
lg: 992px
xl: 1200px
xxl: 1400px
```

---

### Custom Breakpoints

**Approach:**
Define breakpoints based on your content, not devices.

**Example:**
```css
/* When sidebar would be too narrow */
@media (min-width: 900px) {
  .sidebar {
    display: block;
  }
}
```

---

## Vertical Rhythm

**Description:**
Consistent vertical spacing creates visual harmony.

### Approach 1: Baseline Grid

**Concept:**
Align all elements to a baseline (e.g., 8px).

**Example:**
```css
h1 {
  font-size: 48px;
  line-height: 56px; /* Multiple of 8 */
  margin-bottom: 24px; /* Multiple of 8 */
}

p {
  font-size: 16px;
  line-height: 24px; /* Multiple of 8 */
  margin-bottom: 16px;
}
```

---

### Approach 2: Spacing Tokens

**Concept:**
Use predefined spacing values consistently.

**Example:**
```css
.section {
  margin-bottom: var(--space-16); /* 64px */
}

.card {
  padding: var(--space-6); /* 24px */
  gap: var(--space-4); /* 16px */
}
```

---

## Layout Patterns

### Pattern 1: Sidebar + Main Content

**Use Case:** Dashboards, documentation

```css
.layout {
  display: grid;
  grid-template-columns: 256px 1fr;
  gap: 32px;
}

@media (max-width: 1024px) {
  .layout {
    grid-template-columns: 1fr; /* Stack on mobile */
  }
}
```

---

### Pattern 2: Holy Grail Layout

**Use Case:** Header, footer, sidebar, content

```css
.layout {
  display: grid;
  grid-template-areas:
    "header header header"
    "sidebar main aside"
    "footer footer footer";
  grid-template-columns: 200px 1fr 200px;
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
}
```

---

### Pattern 3: Card Grid

**Use Case:** Product listings, galleries

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 24px;
}
```

---

### Pattern 4: Split Screen

**Use Case:** Login pages, feature showcases

```css
.split {
  display: grid;
  grid-template-columns: 1fr 1fr;
  min-height: 100vh;
}

@media (max-width: 768px) {
  .split {
    grid-template-columns: 1fr;
  }
}
```

---

## Layout Tools & Frameworks

**CSS Grid:**
- Native, powerful
- Learn: https://cssgrid.io

**Flexbox:**
- Native, flexible
- Learn: https://flexboxfroggy.com

**Tailwind CSS:**
- Utility-first grid system
- https://tailwindcss.com

**Bootstrap:**
- 12-column grid
- https://getbootstrap.com

**CSS Grid Generator:**
- Visual tool: https://cssgrid-generator.netlify.app

---

## Decision Guide

| **Your Need** | **Recommended Approach** |
|---|---|
| Standard website | 12-column grid + 8pt spacing |
| Simple landing page | 8-column grid + 8pt spacing |
| Dashboard | 12-column grid + 4pt spacing |
| Unique creative layout | Freeform grid + custom spacing |
| Rapid prototyping | Tailwind spacing + grid |

---

## Layout Checklist

- [ ] Choose grid system (12-column recommended)
- [ ] Define spacing scale (8pt or 4pt)
- [ ] Set container max-widths
- [ ] Define responsive breakpoints
- [ ] Establish vertical rhythm
- [ ] Document layout patterns
- [ ] Test on multiple screen sizes

---

## Example Layout Systems

**Minimal (Tailwind Default)**
```
Grid: 12-column
Spacing: Tailwind scale (4px base)
Breakpoints: sm, md, lg, xl, 2xl
Container: max-w-7xl (1280px)
```

**Custom SaaS Dashboard**
```
Grid: 12-column
Spacing: 8pt scale (8, 16, 24, 32...)
Breakpoints: 768px, 1024px, 1440px
Container: Full-width with sidebar
```

**Marketing Site**
```
Grid: 12-column
Spacing: 8pt + custom large spacing (80px, 120px)
Breakpoints: Mobile-first (640px, 1024px)
Container: max-width 1200px
```
