# Type Scale

Typographic scale systems that create consistent hierarchy and rhythm in your typography. Each scale uses mathematical ratios to generate harmonious size relationships.

Choose a type scale that creates clear hierarchy while maintaining visual harmony:

## Musical Scales

### Minor Second (1.067)
The smallest perceptible step, creating subtle hierarchy.
- **Ratio:** 1.067
- **Sizes:** 12, 13, 14, 15, 16, 17, 18, 19px...
- **Best for:** Minimal designs, dense content, subtle differences
- **Character:** Gentle progression, understated elegance

### Major Second (1.125)
A comfortable step that's noticeable but not dramatic.
- **Ratio:** 1.125
- **Sizes:** 12, 14, 15, 17, 19, 21, 24, 27px...
- **Best for:** Body text heavy sites, documentation
- **Character:** Balanced progression, highly readable

### Minor Third (1.2)
Classic typographic scale, widely used in print and web.
- **Ratio:** 1.2
- **Sizes:** 12, 14, 17, 21, 25, 30, 36, 43px...
- **Best for:** Most websites, versatile use cases
- **Character:** Noticeable hierarchy, professional look

### Major Third (1.25)
Strong hierarchy without being overwhelming.
- **Ratio:** 1.25
- **Sizes:** 12, 15, 19, 24, 30, 37, 46, 58px...
- **Best for:** Marketing sites, clear hierarchy needs
- **Character:** Confident steps, clear distinction

### Perfect Fourth (1.333)
Bold steps that create strong visual hierarchy.
- **Ratio:** 1.333
- **Sizes:** 12, 16, 21, 28, 37, 50, 66, 88px...
- **Best for:** Headlines, marketing pages, bold designs
- **Character:** Strong contrast, impactful headers

### Augmented Fourth (1.414)
The √2 ratio, creating dramatic size differences.
- **Ratio:** 1.414
- **Sizes:** 12, 17, 24, 34, 48, 68, 96, 136px...
- **Best for:** Posters, hero sections, artistic layouts
- **Character:** Dramatic jumps, high impact

### Perfect Fifth (1.5)
The golden mean of type scales, very noticeable steps.
- **Ratio:** 1.5
- **Sizes:** 12, 18, 27, 40, 60, 90, 135, 203px...
- **Best for:** Display type, presentations, bold statements
- **Character:** Powerful hierarchy, commanding presence

### Golden Ratio (1.618)
The mathematical golden ratio for maximum harmony.
- **Ratio:** 1.618
- **Sizes:** 12, 19, 31, 50, 81, 131, 212, 343px...
- **Best for:** Luxury brands, artistic designs, special emphasis
- **Character:** Natural harmony, aesthetically pleasing

## Custom Scales

### Fibonacci Scale
Based on the Fibonacci sequence for natural progression.
- **Sizes:** 8, 13, 21, 34, 55, 89, 144px...
- **Best for:** Organic designs, natural layouts
- **Character:** Nature-inspired, unique rhythm

### Modular Scale (Custom Ratio)
Define your own ratio based on your design needs.
- **Common ratios:** 1.15, 1.3, 1.35, 1.4
- **Best for:** Brand-specific requirements
- **Character:** Tailored to your exact needs

### Pixel Perfect Scale
Hand-picked sizes that work well on screens.
- **Sizes:** 11, 12, 14, 16, 18, 21, 24, 28, 32, 36, 48, 64px...
- **Best for:** UI design, system fonts
- **Character:** Screen-optimized, clean rendering

### Fluid Type Scale
Scales that adapt based on viewport width.
- **Formula:** clamp(min, preferred, max)
- **Example:** clamp(1rem, 4vw, 3rem)
- **Best for:** Responsive design, modern web
- **Character:** Smooth scaling, no breakpoints

## Implementation Guidelines

### Base Size Selection
Choose your base font size carefully:
- **14px:** Compact, more content visible
- **15px:** Balanced readability and density
- **16px:** Browser default, excellent readability
- **17px:** Enhanced readability, modern standard
- **18px:** Accessibility-first, comfortable reading

### Scale Application
How to apply your chosen scale:
- **H1:** Base × ratio^5 or ratio^6
- **H2:** Base × ratio^4
- **H3:** Base × ratio^3
- **H4:** Base × ratio^2
- **H5:** Base × ratio^1
- **H6:** Base × ratio^0.5 or base
- **Body:** Base size
- **Small:** Base ÷ ratio

### Line Height Ratios
Pair your type scale with appropriate line heights:
- **Headers:** 1.1 - 1.3 (tighter for large sizes)
- **Body text:** 1.5 - 1.7 (comfortable reading)
- **Small text:** 1.4 - 1.5 (maintains readability)

### Responsive Considerations
Adjust your scale for different screen sizes:
- **Mobile:** Consider smaller ratio (1.2 instead of 1.25)
- **Desktop:** Full scale for maximum impact
- **Large screens:** Potentially larger base size

---

*A well-chosen type scale creates visual rhythm and hierarchy that guides users through your content naturally. The key is consistency—once you choose a scale, stick to it throughout your design.*