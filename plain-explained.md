# Product Language for AI Notation Explained

This document represents a structured, AI-readable product definition format known as PLAIN (Product Language for AI Notation).
It is designed to be both human-friendly and machine-parseable. Each section of this document provides key information that enables AI tools to generate user interfaces, code, or product artifacts with minimal ambiguity.

Use this as the single source of truth to describe your product idea — and let both teams and AI agents build from it.

## 1. Idea Statement
The Idea Statement introduces the product concept in a way that clearly communicates its purpose, target audience, problems it solves, and core benefits. It should be written in 2–3 short paragraphs and focus on clarity, relevance, and specificity. The goal is not to impress with buzzwords, but to inform and orient the reader (or the AI) by answering key questions:

- Who is the product for?
- What does it enable them to do?
- What problems does it solve?
- How does it solve them?
- Why is it better/different from alternatives?

It is important to include both the functional and experiential aspects of the product. Do not generalize—describe key features, workflows, or value drivers that make the idea meaningful.

### Few-shot Examples

The following examples illustrate the expected format and level of detail for an Idea Statement. Each should be written in 2–3 concise paragraphs, clearly describing the product’s purpose, target users, key problems it solves, and how it delivers value.

> **Curato** is a curated web platform designed to help creative professionals discover, explore, and share AI tools tailored to their needs. By browsing through categorized collections, users can access detailed tool profiles, visit official websites, or share tools directly on social media. The platform streamlines tool discovery by combining smart filters, tag-based navigation, and clean UI previews—making it easier than ever to find the right AI tool for any creative workflow. Whether you're a designer looking for image generators or a writer exploring language models, Curato offers a structured and visual way to navigate the AI landscape.

> **Taskly** is a cross-platform task management tool designed for freelancers and remote teams who need a fast and reliable way to organize their workday. The app focuses on simplicity and speed—allowing users to quickly capture tasks, assign deadlines, and mark progress with minimal friction. What sets Taskly apart is its intelligent scheduling assistant, offline syncing, and support for recurring task templates. Whether you're juggling multiple clients or trying to stick to personal deadlines, Taskly reduces the cognitive load of planning by offering clean interfaces, smart reminders, and adaptive daily overviews.

> **Wellnest** is a mobile-first journaling app aimed at young adults navigating stress, decision-making, and personal growth. It offers guided prompts, mood tracking, and daily reflections to help users better understand their mental and emotional state over time. Designed with a calming aesthetic and interaction-focused UI, Wellnest makes self-reflection accessible and rewarding. Features like streak tracking, visual mood summaries, and optional anonymous sharing enable users to stay consistent while building emotional resilience.

## 2. Design Language
The Design Language defines the foundational **values**, **tone**, and **guiding attitudes** of the product’s user experience. It combines abstract principles (such as clarity or simplicity) with emotional cues (such as playful, calming, or serious) to inform every visual and interaction-related decision.

This section is not about specific colors, components, or layout rules—that comes later. Instead, it sets the **philosophical direction** behind the design: how the product should make people feel, how it behaves under pressure, and what it chooses to emphasize or ignore. Both human designers and AI agents use this section to align decisions with the intended personality of the product.

It should include 3–5 principles and a short narrative that conveys the **emotional tone** and **interaction style** of the product.

### Output Example 1
```
Our design approach is grounded in clarity, calm, and cognitive efficiency.
The interface avoids unnecessary distractions, emphasizes whitespace, and guides the user toward key tasks with minimal friction.

Core principles:
- Show only what matters: every screen should reduce information overload.
- Invisible speed: interactions should feel fast without being flashy.
- Subtle delight: animations and sounds exist only to affirm, never to impress.

Visual tone: calm, mature, confident. The product should feel like a quiet assistant that respects your focus, not an energetic coach demanding attention.
```
### Output Example 2
```
The product embraces a human-first design mindset, encouraging users to feel safe, accepted, and in control of their emotional journey.
Every interface element is designed to reduce stress and invite self-reflection.

Core principles:
- Soft by default: colors, motion, and typography should feel gentle and supportive.
- Empathy over efficiency: friction is acceptable if it improves emotional clarity.
- Honesty in UI: no dark patterns, no forced engagement, no urgency bias.

Visual tone: warm, empathetic, and intimate—like a well-designed journal that understands you but never judges.
```

## 3. Color
The Color section defines the product’s **visual identity** through a structured palette of colors. This includes **brand colors**, **semantic colors** (like success, warning, danger), backgrounds, and surface tones. It may also include references to light and dark modes, grayscale ranges, and theming strategies.

For AI tools, clear naming conventions (e.g. primary, surface-100, error-light) and logical token groupings are critical to automate and scale consistent UI generation. For humans, this section provides the visual backbone of the product’s mood and branding.

If possible, describe:
* The primary/secondary brand palette
* Semantic roles (info, success, warning, danger)
* Grayscale steps and naming conventions
* Mode support (light, dark, auto)
* Any unique thematic color behavior (e.g. gradients, transparency, motion-linked color shifts)

### Output Example 1
SaaS Dashboard (Light/Dark Theme)
```
Primary: #2563EB
Secondary: #10B981
Error: #EF4444  
Warning: #F59E0B  
Info: #3B82F6  
Success: #22C55E

Grayscale:
- surface-50: #F9FAFB  
- surface-100: #F3F4F6  
- surface-200: #E5E7EB  
- surface-900: #111827

Mode support: full light/dark support  
- Dark mode backgrounds use gray-900 with primary color tints  
- Accent components adapt to theme automatically  
- Surface tokens are used instead of raw hex values across the design system
```
### Output Example 2
Mobile Health App (Soft Neutrals, No Dark Mode)
```
Primary: #C084FC 
Accent: #A5F3FC 
Success: #34D399  
Warning: #FBBF24  
Error: #F87171
Background: #FFFFFF  
Surface: #F7F7F7  
Text: #111111

No dark mode: Designed intentionally with a single-mode interface to reduce cognitive switching. All visual contrast meets WCAG 2.1 AA. Semantic colors are always paired with iconography to improve clarity for colorblind users.
```

## 4. Design System
The Design System section defines the structural and visual rules that shape the entire UI. It includes design tokens, reusable components, spacing logic, naming conventions, and theming strategy. This section is crucial for both human teams and AI agents, as it governs the consistency, scalability, and efficiency of the product’s design execution.

This section should state whether you’re:
* Using an existing system (e.g. Tailwind, Shadcn/UI, Material 3)
* Creating a custom system
* Extending a hybrid of both

Include:
* Token conventions (e.g. --space-md, text-primary)
* Component strategies (atomic, molecular, etc.)
* UI frameworks or CSS methodologies in use
* Dark/light mode behavior (if governed by system)

### Output Example 1: Tailwind-Inspired Utility System
```
We use a Tailwind-based utility-first system adapted with our own naming tokens. Design tokens are created in Figma and exported as JSON using Style Dictionary.
All components follow atomic design principles and are grouped by interaction pattern.

- Spacing: 4px scale, named `space-0` to `space-80`  
- Typography: modular scale, named `text-xs` to `text-3xl`  
- Colors: `primary-500`, `surface-100`, `error-300`, etc.  
- Component variants defined via modifier tokens (e.g. `button--danger--sm`)  
- Dark mode supported via token flipping  
- Tokens are mirrored between design and code using GitHub sync and Tokens Studio
```
### Output Example 2: Shadcn-Based Component System
```
The project uses [Shadcn/UI](https://ui.shadcn.com/) as the baseline design system, enriched with custom tokens and interaction rules.
We override default colors and sizes to match our brand language, while keeping the core composability intact.

- Base framework: Next.js + Tailwind + Radix  
- Components follow headless architecture  
- Tokens are defined in Tailwind config and design tokens JSON  
- Color tokens match brand guidelines and semantic use  
- All core components (Button, Input, Card, Modal) are themed in both light and dark  
- Documentation generated using Storybook and Figma components
```

## 5. Icons
The Icons section defines the visual style, system, and usage rules for all iconography in the product. Icons are not just decorative—they convey meaning, indicate actions, and support accessibility. This section should specify:
* The icon library in use (e.g. Lucide, Tabler, Feather, custom)
* The visual style (e.g. stroke, filled, two-tone)
* Size and grid system (typically 24px or 20px grid)
* Whether you allow custom icons, and if so, how they should be integrated
* Rules for usage: filled vs. outline, brand-safe icons, interactive vs. decorative, etc.
* Accessibility considerations (labeling, fallback behavior)

This section helps AI tools map icon names to visuals and use them consistently across components like buttons, navigation, and alerts.

### Output Example 1: Lucide-Based Icon System
```
We use the [Lucide](https://lucide.dev/) icon library with a 24px grid and stroke-style visuals.
All icons are 1.5px stroke width, with rounded caps and corners to match our typography.

- Primary set: Lucide  
- Size: 24x24px, with built-in padding for optical balance  
- Interactive icons (e.g. edit, delete) use hover states and semantic colors  
- Decorative icons (e.g. empty states) are used with reduced opacity  
- All icons must have a descriptive `aria-label` or be wrapped in a labeled element  
- Custom icons are added in SVG format and follow Lucide's visual conventions
```
### Output Example 2: Mixed Set with Custom Additions
```
The product uses a hybrid icon system: core interface icons come from Tabler Icons (stroke-based), and marketing or brand-specific icons are created in-house as filled SVGs.

- System icons (actions, UI controls): Tabler, 20px grid, 1.5px stroke  
- Brand icons (for hero sections, illustrations): Custom-made, filled, 48px+  
- All icons support `currentColor` to inherit parent text color  
- Stroke icons are used for controls, filled icons for context or emphasis  
- Icons used as buttons have tooltips and accessible labels  
- Custom icon naming follows kebab-case (e.g. `icon-save-draft`)
```

## 6. Typography
The Typography section defines the font system, text hierarchy, and typescale used throughout the product. This includes font families, weights, sizes, line heights, and responsive behavior. Typography plays a critical role in readability, brand tone, and overall UI clarity.

This section should include:
- Font family choices (including fallbacks)
- Usage rules for headings, body, captions, and buttons
- Font weights and styles
- Typescale: how font sizes scale across breakpoints or levels
- Naming conventions (e.g. text-sm, heading-xl)
- Responsive rules (fluid scaling, mobile/desktop size shifts)
- Accessibility notes like minimum size or contrast ratio

If relevant, include whether the typography is mapped to tokens or utility classes.

### Output Example 1: Inter-Based Modular Scale
```
We use the Inter font family for both UI and brand usage, chosen for its modern feel and high legibility. Font rendering is optimized for web display (font-smoothing enabled).

Font Stack: `Inter, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif`

Heading weights: 600–700  
Body weights: 400–500  
Button weights: 500 (all caps)

Typescale (based on 1.25 modular scale):
- display-xl: 48px / 56px  
- heading-lg: 32px / 40px  
- heading-md: 24px / 32px  
- body-lg: 18px / 28px  
- body-md: 16px / 24px  
- body-sm: 14px / 20px

All text tokens are prefixed as `text-[size]`, mapped to Tailwind config and Figma text styles. Line heights follow a 1.4–1.6 rhythm. Typography adapts responsively starting from 768px breakpoint.
```
### Output Example 2: Serif-Brand Hybrid with Static Scale
```
We use a dual-font strategy: `DM Serif Display` for branding and headlines, and `Roboto` for body content. This contrast gives the interface a premium yet approachable tone.

- Headlines: `DM Serif Display`, 600–700 weight  
- Body: `Roboto`, 400–500 weight  
- Captions: `Roboto`, 300 weight  
- Button text: uppercase, 500 weight

Fixed typescale:
- h1: 40px  
- h2: 28px  
- h3: 22px  
- body: 16px  
- caption: 12px

All text has at least 4.5:1 contrast against background. No fluid scaling; mobile adjusts only heading sizes by 1 level down.
```

## 7. Layout
The Layout section defines how content is structured, aligned, and spaced across the interface. It sets rules for grid systems, spacing scales, breakpoints, container widths, and general spatial rhythm. This section ensures consistency in responsiveness, balance, and visual clarity across screen sizes.

Include the following if relevant:
- Grid system (e.g. 12-column, 4-point grid)
- Spacing scale (e.g. space-0 to space-80, based on 4px increments)
- Container widths (for mobile, tablet, desktop)
- Breakpoints and responsive behavior
- Margin/gap rules for vertical and horizontal stacking
- Utility classes or layout tokens (if systemized)

This section helps AI tools generate predictable and scalable layout scaffolding and guides designers in structuring content with consistent rhythm.

### Output Example 1: 12-Column Grid with Fluid Spacing
```
The design uses a responsive 12-column grid with a 4-point spacing scale. All spacing is tokenized and follows a consistent rhythm across devices.

- Grid: 12 columns, 16px gutter, 8px column gap  
- Spacing: space-0 (0px) to space-80 (320px) in 4px increments  
- Container widths:
  - Mobile (≤ 640px): full width  
  - Tablet (641–1024px): 768px container  
  - Desktop (≥ 1025px): 1280px container, max 1440px

Breakpoints:
- sm: 640px  
- md: 768px  
- lg: 1024px  
- xl: 1280px  
- 2xl: 1536px

Vertical rhythm is maintained using margin/padding tokens. Auto Layout is used in Figma with Hug/Fill behaviors based on content role.
```

### Output Example 2: Fixed Layout with Limited Breakpoints
```
Our layout strategy favors predictability over full responsiveness. We use fixed containers and a simplified breakpoint system.

- Grid: 8-column layout, 24px gutter, 12px padding  
- Container max width: 1140px  
- Breakpoints:
  - Mobile: 360px  
  - Tablet: 768px  
  - Desktop: 1140px

Spacing scale: 8px, 16px, 24px, 32px, 48px, 64px  
No fluid resizing — components snap to breakpoints. Padding and margins follow fixed spacing tokens like `layout-md` (24px) or `gap-sm` (12px).

Used primarily in a marketing website with strong visual symmetry.
```

## 8. Core Components
The Core Components section lists and describes the essential reusable UI components that form the foundation of the product interface. These are the building blocks used across screens and flows, often standardized in both design and code.

This section should:
- List commonly used UI components (e.g. Button, Input, Modal, Card)
- Mention variations or states (e.g. Button: primary, secondary, disabled)
- Optionally describe interaction patterns (e.g. expandable, collapsible, draggable)
- Indicate design system source (e.g. Shadcn, custom, Figma components)
- Help AI tools reuse visual patterns correctly and infer structural roles (e.g. buttons vs. links)

You don’t need to include every component, but highlight the ones that are critical to your product’s experience or architecture.

### Output Example 1: Productivity Tool
```
Button
- Variants: Primary, Secondary, Ghost, Danger
- States: Hover, Focus, Loading, Disabled
- Sizes: sm, md, lg

Input Field
- Types: Text, Email, Password
- States: Error, Success, Disabled
- Includes icons and helper text support

Card
- Used for grouping task items, dashboard widgets
- Optional: with shadow, with border, with toggle header

Modal
- Centered overlay with scroll lock
- Variants: AlertModal, FormModal
- Closes on background click or escape key

Toast Notification
- Position: top-right
- Types: Success, Error, Info
- Auto-dismiss after 3 seconds

Navigation Tabs
- Horizontal alignment
- Active state emphasized by underline and color shift
- Keyboard accessible
```
### Output Example 2: E-commerce Product Page
```
Product Card
- Contains: Image, Title, Price, Tag
- Interaction: hover scale, add to wishlist icon

Button
- Types: Buy Now, Add to Cart, Wishlist
- Sizes: sm, md, icon-only
- States: Disabled, Loading, In-cart

Rating Stars
- Interactive, 0.5 increments, accessible labels per star
- Supports keyboard navigation

Accordion
- Used in product FAQ
- Expand/collapse animation with 200ms ease-in-out

Dropdown Filter
- Multi-select or single-select
- Used in category sidebar

Breadcrumb
- Optional for category-level navigation
- Responsive collapse on mobile
```






## 9. Accessibility
## 10. Stylistic References

## 11. Target Audience and Personas

## 12. Functional Requirements

## 13. Non-Functional Requirements

## 14. User Flows

## 15. User Stories

## 16. Page Map

## 17. Technical Requirements

  ### Architecture Pattern
  
  ### State Management
  
  ### Data Flow
  
  ### Technical Stack
  
  ### Authentication Process
  
  ### Route Design
  
  ### API Design
  
  ### Database Design
  
  ### SEO Strategy
  
  ### Content Management Approach
  
  ### Structured Content
  
  ### Deployment (CI/CD)
  
  ### Serve Method
  
  ### Rendering and Navigation

## 18. Inspirations

## 19. Acceptance Criteria

## 20. Additional Notes
