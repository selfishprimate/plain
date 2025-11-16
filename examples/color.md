# Color Palettes: Examples & Strategies

This guide provides color palette examples and helps you choose colors for your product.

---

## Color Psychology

Colors evoke emotions and set the tone for your product.

| **Color** | **Emotion/Association** | **Best For** |
|---|---|---|
| **Blue** | Trust, calm, professional | SaaS, finance, healthcare |
| **Green** | Growth, nature, success | Wellness, environment, money |
| **Purple** | Creative, luxury, wisdom | Creative tools, premium products |
| **Red** | Energy, urgency, passion | Food, fitness, entertainment |
| **Orange** | Friendly, enthusiastic | Social, children, creative |
| **Yellow** | Optimistic, happy, attention | Fun, educational, warnings |
| **Black/Gray** | Sophisticated, modern, minimal | Luxury, tech, professional |
| **Pink** | Playful, compassionate | Beauty, wellness, youth |

---

## Example 1: Modern SaaS (Blue & Neutral)

**Visual Tone:** Professional, trustworthy, clean

**Palette:**
```
Primary: #2563EB (Blue 600)
Secondary: #10B981 (Emerald 500)
Background: #FFFFFF (White)
Surface: #F9FAFB (Gray 50)
Text: #111827 (Gray 900)
Text Secondary: #6B7280 (Gray 500)

Semantic Colors:
Success: #10B981 (Green)
Warning: #F59E0B (Amber)
Error: #EF4444 (Red)
Info: #3B82F6 (Blue)

Dark Mode:
Background: #111827 (Gray 900)
Surface: #1F2937 (Gray 800)
Text: #F9FAFB (Gray 50)
Text Secondary: #9CA3AF (Gray 400)
```

**Usage:**
- Primary: CTAs, links, focus states
- Secondary: Success states, positive actions
- Background: Page background
- Surface: Cards, modals, elevated elements

**Tools/Tailwind:**
```css
bg-blue-600
bg-emerald-500
text-gray-900
```

---

## Example 2: Wellness App (Warm & Calming)

**Visual Tone:** Soothing, empathetic, natural

**Palette:**
```
Primary: #C084FC (Purple 400)
Accent: #A5F3FC (Cyan 200)
Background: #FFFBEB (Amber 50)
Surface: #FFFFFF (White)
Text: #1F2937 (Gray 800)
Text Secondary: #6B7280 (Gray 500)

Semantic Colors:
Success: #34D399 (Emerald 400)
Warning: #FBBF24 (Amber 400)
Error: #F87171 (Red 400)
Info: #60A5FA (Blue 400)

No Dark Mode (intentional)
```

**Why these colors:**
- Purple: Calm, introspective
- Cyan accent: Fresh, uplifting
- Warm background: Comforting, gentle

---

## Example 3: Bold Creative Tool (Vibrant & Playful)

**Visual Tone:** Energetic, fun, inspiring

**Palette:**
```
Primary: #F97316 (Orange 500)
Secondary: #8B5CF6 (Violet 500)
Accent: #10B981 (Emerald 500)
Background: #FFFFFF (White)
Dark BG: #0F172A (Slate 900)
Surface: #F1F5F9 (Slate 100)
Text: #0F172A (Slate 900)

Gradients:
Sunrise: linear-gradient(135deg, #F97316, #FBBF24)
Violet: linear-gradient(135deg, #8B5CF6, #EC4899)
Ocean: linear-gradient(135deg, #06B6D4, #3B82F6)

Dark Mode: Dark with neon accents
```

**Features:**
- Gradients for hero sections
- Vibrant CTAs
- Customizable accent colors

---

## Example 4: Minimal Luxury (Monochrome + Accent)

**Visual Tone:** Refined, elegant, premium

**Palette:**
```
Primary: #000000 (Black)
Accent: #D4AF37 (Gold)
Background: #FFFFFF (White)
Surface: #F5F5F5 (Gray 100)
Text: #000000 (Black)
Text Secondary: #737373 (Gray 600)

Minimal semantic colors:
Success: #22C55E (Subtle green)
Error: #EF4444 (Subtle red)
```

**Usage:**
- Heavy use of whitespace
- Black text on white
- Gold for premium features/highlights
- Grayscale images

---

## Example 5: Dark Mode First (Tech Product)

**Visual Tone:** Modern, developer-focused, sleek

**Palette:**
```
Primary: #3B82F6 (Blue 500)
Secondary: #8B5CF6 (Purple 500)
Background (Dark): #0F172A (Slate 900)
Surface (Dark): #1E293B (Slate 800)
Border: #334155 (Slate 700)
Text: #F8FAFC (Slate 50)
Text Secondary: #94A3B8 (Slate 400)

Light Mode (Secondary):
Background: #FFFFFF
Surface: #F8FAFC
Text: #0F172A
```

**Features:**
- Dark by default
- High contrast for code
- Syntax highlighting friendly

---

## Example 6: E-commerce (Warm & Inviting)

**Visual Tone:** Approachable, trustworthy, organic

**Palette:**
```
Primary: #059669 (Emerald 600)
Secondary: #F59E0B (Amber 500)
Background: #FEFCE8 (Yellow 50)
Surface: #FFFFFF (White)
Text: #1F2937 (Gray 800)
Text Secondary: #6B7280 (Gray 500)

Semantic:
Add to Cart: #059669 (Green)
Sale/Discount: #EF4444 (Red)
Out of Stock: #9CA3AF (Gray)
```

**Usage:**
- Green: Primary actions (Add to Cart, Buy)
- Amber: Secondary actions (Wishlist)
- Red: Sales and urgency

---

## Color Palette Strategies

### Strategy 1: 60-30-10 Rule

**60% Dominant color** (background, large surfaces)
**30% Secondary color** (supporting elements)
**10% Accent color** (CTAs, highlights)

**Example:**
```
60%: White/Gray background
30%: Blue for sections and cards
10%: Orange for CTAs and accents
```

---

### Strategy 2: Analogous Colors

**Use colors next to each other on color wheel.**

**Example:**
```
Blue ’ Blue-Green ’ Green
#3B82F6 ’ #06B6D4 ’ #10B981
```

**Best for:** Harmonious, calm designs

---

### Strategy 3: Complementary Colors

**Use opposite colors on color wheel.**

**Example:**
```
Blue + Orange
#2563EB + #F97316
```

**Best for:** High contrast, bold designs

---

### Strategy 4: Monochromatic

**Different shades of one color.**

**Example (Blue):**
```
Blue 50: #EFF6FF (lightest)
Blue 100: #DBEAFE
Blue 500: #3B82F6 (base)
Blue 700: #1D4ED8
Blue 900: #1E3A8A (darkest)
```

**Best for:** Cohesive, professional designs

---

## Semantic Colors

**Always define these:**

```
Success: #10B981 (Green)  confirmations, positive actions
Warning: #F59E0B (Amber)  cautions, important notices
Error: #EF4444 (Red)  errors, destructive actions
Info: #3B82F6 (Blue)  informational messages
```

**Important:** Don't rely on color alone (add icons).

---

## Light & Dark Mode

### Approach 1: Full Mirroring

**Light and dark versions of every color.**

```css
/* Light Mode */
--bg-primary: #FFFFFF;
--text-primary: #111827;

/* Dark Mode */
--bg-primary: #111827;
--text-primary: #F9FAFB;
```

---

### Approach 2: Adaptive Accents

**Same brand colors, adjusted backgrounds.**

```css
/* Both modes */
--color-primary: #2563EB; /* Blue stays same */

/* Light Mode */
--bg: #FFFFFF;

/* Dark Mode */
--bg: #0F172A;
--color-primary-adjusted: #60A5FA; /* Lighter blue for dark BG */
```

---

### Approach 3: Single Mode Only

**Choose light OR dark, not both.**

**Light Mode Only:**
- Wellness, healthcare, family apps
- Softer, warmer feel

**Dark Mode Only:**
- Developer tools, gaming, media
- Edgy, modern feel

---

## Accessibility (Contrast)

**WCAG AA Requirements:**
- Normal text: 4.5:1 contrast
- Large text (18pt+): 3:1 contrast
- UI components: 3:1 contrast

**Tools:**
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- Coolors Contrast: https://coolors.co/contrast-checker

**Example (Good):**
```
White (#FFFFFF) on Blue (#2563EB): 4.9:1 
```

**Example (Bad):**
```
Light gray (#D1D5DB) on White (#FFFFFF): 1.8:1 L
```

---

## Color Tools

**Palette Generators:**
- Coolors: https://coolors.co
- Adobe Color: https://color.adobe.com
- Realtime Colors: https://realtimecolors.com
- Paletton: https://paletton.com

**Tailwind CSS:**
- Full color palette: https://tailwindcss.com/docs/customizing-colors

**Gradient Generators:**
- CSS Gradient: https://cssgradient.io
- Mesh Gradients: https://meshgradient.com

**Accessibility:**
- Contrast Checker: https://webaim.org/resources/contrastchecker/
- Who Can Use: https://whocanuse.com

---

## Naming Conventions

### Approach 1: Functional Names
```css
--color-primary
--color-secondary
--color-accent
--color-success
--color-error
```

### Approach 2: Semantic Names
```css
--color-brand
--color-cta
--color-link
--color-destructive
```

### Approach 3: Tailwind-Style
```css
--blue-50
--blue-500
--blue-900
```

---

## Quick Start Templates

### Startup SaaS
```
Primary: Tailwind Blue 600 (#2563EB)
Success: Tailwind Green 500 (#10B981)
Background: White (#FFFFFF)
Text: Gray 900 (#111827)
```

### Creative Agency
```
Primary: Custom Purple (#8B5CF6)
Accent: Custom Orange (#F97316)
Background: Off-white (#FAFAFA)
Gradients: Yes
```

### E-commerce
```
Primary: Green (#059669)
Sale: Red (#EF4444)
Background: Warm gray (#FAFAF9)
Accent: Amber (#F59E0B)
```

### Developer Tool
```
Primary: Blue (#3B82F6)
Background (Dark): Slate 900 (#0F172A)
Syntax colors: VS Code theme
Monospace-friendly
```

---

## Checklist

- [ ] Choose 1-2 primary colors
- [ ] Define semantic colors (success, error, warning)
- [ ] Create grayscale palette (50-900)
- [ ] Decide: light mode, dark mode, or both
- [ ] Test color contrast (WCAG AA minimum)
- [ ] Name colors consistently
- [ ] Document in design system
- [ ] Test with colorblindness simulator

---

## Resources

- **Coolors:** https://coolors.co
- **Tailwind Colors:** https://tailwindcss.com/docs/customizing-colors
- **Color Psychology:** https://www.colorpsychology.org
- **Material Design Colors:** https://m2.material.io/design/color
