# Typography: Options & Examples

This guide helps you choose and define typography for your product.

---

## Font Selection Strategies

### Option 1: System Fonts

**Best for:** Performance, native feel, accessibility

**Description:**
Use fonts already installed on users' devices. No downloads needed, instant rendering.

**System Font Stack:**
```css
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI",
             Roboto, "Helvetica Neue", Arial, sans-serif;
```

**Pros:**
- Zero load time
- Best performance
- Familiar to users
- Works offline
- Accessible

**Cons:**
- Less distinctive
- Platform-dependent
- Limited branding

**Best Use Cases:**
- Performance-critical apps
- Dashboards and tools
- Mobile apps
- Accessibility-first products

---

### Option 2: Google Fonts

**Best for:** Free, variety, easy to implement

**Description:**
Google Fonts offers 1000+ free, open-source fonts. Easy to integrate, well-optimized.

**Popular Choices:**

**Sans-Serif (Modern, Clean):**
- **Inter** — versatile, excellent readability, UI-focused
- **Roboto** — neutral, widely used, Material Design
- **Open Sans** — friendly, approachable
- **Poppins** — geometric, modern
- **Work Sans** — clean, professional

**Serif (Editorial, Premium):**
- **Merriweather** — readable, elegant
- **Playfair Display** — dramatic, headlines
- **Lora** — balanced, body text
- **Crimson Pro** — book-like, refined

**Monospace (Code, Technical):**
- **Fira Code** — ligatures, coding
- **JetBrains Mono** — excellent for code
- **Source Code Pro** — Adobe, clean

**Display (Headlines, Branding):**
- **Montserrat** — geometric, bold
- **Bebas Neue** — condensed, impactful
- **Oswald** — narrow, strong

**Pros:**
- Free and open-source
- Easy to implement
- Well-optimized
- Variable fonts available
- Large selection

**Cons:**
- Requires external request (slight delay)
- Common (less unique)
- Privacy concerns (Google tracking)

**Implementation:**
```html
<!-- In HTML head -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Inter', sans-serif;
}
```

**Self-Hosting (Privacy + Performance):**
```bash
# Download from Google Fonts
# Host locally
@font-face {
  font-family: 'Inter';
  src: url('/fonts/Inter-Regular.woff2') format('woff2');
}
```

**Learn More:** https://fonts.google.com

---

### Option 3: Premium Fonts

**Best for:** Unique branding, high-quality typography

**Description:**
Paid fonts from foundries like Adobe Fonts, Fontshare, or independent designers.

**Sources:**

**Adobe Fonts**
- Included with Adobe Creative Cloud
- High-quality, professional
- https://fonts.adobe.com

**Fontshare (Free)**
- Professional fonts, free for commercial use
- Small but curated selection
- https://fontshare.com

**Fonts.com, MyFonts**
- Huge selection
- Pay per license
- Commercial use

**Independent Foundries:**
- **Grilli Type** — Swiss, modern
- **Colophon Foundry** — experimental
- **Klim Type Foundry** — refined

**Pros:**
- Unique and distinctive
- High quality
- Professional branding
- Better control

**Cons:**
- Costs money
- Licensing can be complex
- Self-hosting required

**Best Use Cases:**
- Brand-focused products
- Marketing sites
- Premium products
- Agency work

---

## Typescale Strategies

### Option 1: Modular Scale

**Description:**
Use a mathematical ratio to create harmonious sizes.

**Common Ratios:**
- **1.125 (Major Second)** — subtle, compact
- **1.25 (Major Third)** — balanced, versatile
- **1.333 (Perfect Fourth)** — strong contrast
- **1.5 (Perfect Fifth)** — dramatic
- **1.618 (Golden Ratio)** — classic

**Example (1.25 ratio, 16px base):**
```
Base: 16px
xs: 13px (16 ÷ 1.25)
sm: 14px
md: 16px (base)
lg: 20px (16 × 1.25)
xl: 25px (20 × 1.25)
2xl: 31px (25 × 1.25)
3xl: 39px
4xl: 49px
```

**Tools:**
- Type Scale Generator: https://typescale.com
- Modular Scale Calculator: https://modularscale.com

---

### Option 2: Fixed Scale (Tailwind-style)

**Description:**
Predefined sizes with consistent naming.

**Example:**
```
text-xs: 12px
text-sm: 14px
text-base: 16px
text-lg: 18px
text-xl: 20px
text-2xl: 24px
text-3xl: 30px
text-4xl: 36px
text-5xl: 48px
text-6xl: 60px
```

**Pros:**
- Predictable
- Easy to remember
- Works well with design systems

**Cons:**
- Less mathematical harmony
- Can feel arbitrary

---

### Option 3: Fluid Typography (Responsive)

**Description:**
Font sizes scale smoothly between breakpoints using `clamp()`.

**Example:**
```css
/* Scales from 16px to 20px between 320px and 1440px viewport */
font-size: clamp(1rem, 0.8rem + 0.5vw, 1.25rem);
```

**Tools:**
- Utopia Fluid Type: https://utopia.fyi/type/calculator

**Pros:**
- Smooth scaling
- No breakpoint jumps
- Better responsive UX

**Cons:**
- More complex
- Browser support (IE11 doesn't support clamp)

---

## Typography Pairing

### Pairing Strategies

**1. Same Family (Different Weights)**
```
Headlines: Inter 700
Body: Inter 400
```
- Safe, cohesive
- Minimal variety

**2. Serif + Sans-Serif**
```
Headlines: Playfair Display (serif)
Body: Inter (sans-serif)
```
- Classic contrast
- Editorial feel

**3. Display + Neutral**
```
Headlines: Bebas Neue (display)
Body: Open Sans (neutral)
```
- Strong hierarchy
- Modern

**Good Pairings:**
- **Inter + Lora** — modern + editorial
- **Montserrat + Merriweather** — geometric + serif
- **Poppins + Open Sans** — playful + clean
- **Playfair Display + Source Sans Pro** — luxury + readable

**Tools:**
- Font Pair: https://fontpair.co
- Google Font Pairings: https://fontpair.co

---

## Font Weights & Usage

**Typical Weight Scale:**
```
100 - Thin
200 - Extra Light
300 - Light
400 - Regular (default body text)
500 - Medium (emphasized text, buttons)
600 - Semi-Bold (subheadings)
700 - Bold (headings)
800 - Extra Bold
900 - Black
```

**Usage Guidelines:**

**Body Text:**
- Use 400 (Regular) or 500 (Medium)
- Line height: 1.5–1.7

**Headings:**
- Use 600–700
- Line height: 1.2–1.4

**Buttons:**
- Use 500–600
- Often uppercase or sentence case

**Captions/Labels:**
- Use 400–500
- Smaller size, higher line height

---

## Line Height & Spacing

**Line Height (leading):**

**Body Text:**
- 1.5–1.7 (relaxed, readable)
- Example: 16px font → 24-27px line height

**Headings:**
- 1.1–1.3 (tighter, more impact)
- Example: 48px font → 53-62px line height

**Buttons/UI:**
- 1–1.2 (compact)

**Letter Spacing (tracking):**

**Uppercase Text:**
- Slightly increase: 0.05em–0.1em

**Body Text:**
- Default (0) or very subtle

**Tight Headlines:**
- Slightly reduce: -0.02em

**Tools:**
- Line Height Calculator: https://baseline.is

---

## Responsive Typography

**Mobile-First Approach:**

**Example:**
```css
/* Mobile */
h1 {
  font-size: 32px;
  line-height: 1.2;
}

/* Tablet */
@media (min-width: 768px) {
  h1 {
    font-size: 40px;
  }
}

/* Desktop */
@media (min-width: 1024px) {
  h1 {
    font-size: 48px;
  }
}
```

**Or use fluid typography:**
```css
h1 {
  font-size: clamp(32px, 4vw, 48px);
}
```

---

## Accessibility

**Best Practices:**

- **Minimum size:** 16px for body text
- **Contrast:** 4.5:1 for normal text, 3:1 for large text (WCAG AA)
- **Line length:** 50-75 characters per line
- **Scalability:** Allow browser zoom up to 200%
- **Avoid all-caps for long text** (harder to read)

**Tools:**
- Contrast Checker: https://webaim.org/resources/contrastchecker/

---

## Example Typography Systems

### Minimal (One Font)
```
Font: Inter (400, 500, 600, 700)
Scale: 12px, 14px, 16px, 20px, 24px, 32px, 48px
Line Height: 1.5 (body), 1.2 (headings)
```

### Editorial (Two Fonts)
```
Headlines: Playfair Display (600, 700)
Body: Lora (400, 500)
Scale: 1.25 modular scale
```

### Brand-Heavy (Display + Body)
```
Display: Bebas Neue (700) — headlines only
Body: Open Sans (400, 600)
Monospace: Fira Code (400) — code snippets
```

### SaaS Dashboard
```
Font: Inter (system font stack fallback)
Weights: 400, 500, 600
Scale: Tailwind default
Dark mode optimized
```

---

## Implementation Checklist

- [ ] Choose font family (or families)
- [ ] Define weights needed (don't load unused weights)
- [ ] Create typescale (modular or fixed)
- [ ] Define line heights per size
- [ ] Set responsive breakpoints
- [ ] Check accessibility (contrast, size)
- [ ] Optimize loading (preload, font-display: swap)
- [ ] Document in design system

---

## Tools & Resources

- **Google Fonts:** https://fonts.google.com
- **Fontshare:** https://fontshare.com
- **Type Scale:** https://typescale.com
- **Font Pair:** https://fontpair.co
- **Modular Scale:** https://modularscale.com
- **Utopia (Fluid):** https://utopia.fyi
- **Contrast Checker:** https://webaim.org/resources/contrastchecker/
