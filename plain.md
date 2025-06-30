# Product Language for AI Notation Explained

This document represents a structured, AI-readable product definition format known as PLAIN (Product Language for AI Notation).
It is designed to be both human-friendly and machine-parseable. Each section of this document provides key information that enables AI tools to generate user interfaces, code, or product artifacts with minimal ambiguity.

Use this as the single source of truth to describe your product idea — and let both teams and AI agents build from it.

## Initial Prompt for the Agent
👇 The following section provides an initial prompt tailored for AI agents. It defines their role, tone, and responsibilities when interpreting and generating this document.

```
You are an expert UI/UX designer with strong experience in product discovery, information architecture, rapid prototyping, and frontend technologies. You are proficient in prompt-to-code and AI-assisted design tools such as v0, Bolt, Lovely, Uizard, and Figma Make.

Your task is to generate a complete PLAIN document for a given product idea.

- Begin by crafting a clear and concise **Idea Statement** that defines the core value, purpose, and problem the product addresses.
- Based on this idea, complete the rest of the PLAIN sections logically and consistently.
- Use your knowledge to make reasonable assumptions when information is missing.
- Write in a natural, human-readable tone suitable for both AI design tools and human product teams.
- Do not alter section titles or order. Fill in each one with clarity and purpose.

🎯 Your ultimate goal is to create a complete and structured product definition that serves as a blueprint for generating entire digital applications — including user interfaces, page structures, component systems, and frontend logic — usable by both AI tools and human teams throughout the design and development process.
```

## 1. Idea Statement 🤔
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

## 2. Design Language 📐
The Design Language defines the foundational **values**, **tone**, and **guiding attitudes** of the product’s user experience. It combines abstract principles (such as clarity or simplicity) with emotional cues (such as playful, calming, or serious) to inform every visual and interaction-related decision.

This section is not about specific colors, components, or layout rules—that comes later. Instead, it sets the **philosophical direction** behind the design: how the product should make people feel, how it behaves under pressure, and what it chooses to emphasize or ignore. Both human designers and AI agents use this section to align decisions with the intended personality of the product.

It should include 3–5 principles and a short narrative that conveys the **emotional tone** and **interaction style** of the product.

### Output Example 1: Productivity App (Calm & Focused)
```
Our design approach is grounded in clarity, calm, and cognitive efficiency.
The interface avoids unnecessary distractions, emphasizes whitespace, and guides the user toward key tasks with minimal friction.

Core principles:
- Show only what matters: every screen should reduce information overload.
- Invisible speed: interactions should feel fast without being flashy.
- Subtle delight: animations and sounds exist only to affirm, never to impress.

Visual tone: calm, mature, confident. The product should feel like a quiet assistant that respects your focus, not an energetic coach demanding attention.
```

### Output Example 2: Wellness App (Warm & Empathetic)
```
The product embraces a human-first design mindset, encouraging users to feel safe, accepted, and in control of their emotional journey.
Every interface element is designed to reduce stress and invite self-reflection.

Core principles:
- Soft by default: colors, motion, and typography should feel gentle and supportive.
- Empathy over efficiency: friction is acceptable if it improves emotional clarity.
- Honesty in UI: no dark patterns, no forced engagement, no urgency bias.

Visual tone: warm, empathetic, and intimate—like a well-designed journal that understands you but never judges.
```

## 3. Color 🎨
The Color section defines the product’s **visual identity** through a structured palette of colors. This includes **brand colors**, **semantic colors** (like success, warning, danger), backgrounds, and surface tones. It may also include references to light and dark modes, grayscale ranges, and theming strategies.

For AI tools, clear naming conventions (e.g. primary, surface-100, error-light) and logical token groupings are critical to automate and scale consistent UI generation. For humans, this section provides the visual backbone of the product’s mood and branding.

If possible, describe:
- The primary/secondary brand palette
- Semantic roles (info, success, warning, danger)
- Grayscale steps and naming conventions
- Mode support (light, dark, auto)
- Any unique thematic color behavior (e.g. gradients, transparency, motion-linked color shifts)

### Output Example 1: SaaS Dashboard (Light/Dark Theme)
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
### Output Example 2: Mobile Health App (Soft Neutrals, No Dark Mode)
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

## 4. Design System 🚧
The Design System section defines the structural and visual rules that shape the entire UI. It includes design tokens, reusable components, spacing logic, naming conventions, and theming strategy. This section is crucial for both human teams and AI agents, as it governs the consistency, scalability, and efficiency of the product’s design execution.

This section should state whether you’re:
- Using an existing system (e.g. Tailwind, Shadcn/UI, Material 3)
- Creating a custom system
- Extending a hybrid of both

Include:
- Token conventions (e.g. --space-md, text-primary)
- Component strategies (atomic, molecular, etc.)
- UI frameworks or CSS methodologies in use
- Dark/light mode behavior (if governed by system)

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

## 5. Icons 🚸
The Icons section defines the visual style, system, and usage rules for all iconography in the product. Icons are not just decorative—they convey meaning, indicate actions, and support accessibility. This section should specify:
- The icon library in use (e.g. Lucide, Tabler, Feather, custom)
- The visual style (e.g. stroke, filled, two-tone)
- Size and grid system (typically 24px or 20px grid)
- Whether you allow custom icons, and if so, how they should be integrated
- Rules for usage: filled vs. outline, brand-safe icons, interactive vs. decorative, etc.
- Accessibility considerations (labeling, fallback behavior)

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

## 6. Typography 📑
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

## 7. Layout 🗞️
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

## 8. Core Components 🎼
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

## 9. Accessibility 🙌
The Accessibility section defines the standards, practices, and priorities that ensure the product can be used by people with a wide range of abilities and assistive technologies. This includes color contrast, keyboard navigation, screen reader support, and more. It guides both design and development decisions to ensure inclusivity and compliance (e.g. WCAG 2.1 AA).

This section should address:
- Minimum contrast ratios (e.g. 4.5:1 for text)
- Keyboard support (tab order, focus rings, skip links)
- Screen reader compatibility (ARIA roles, alt text, semantic markup)
- Motion sensitivity (reduced motion settings)
- Accessible components (e.g. modals, toasts, menus)
- Any additional commitment to inclusive design (e.g. dyslexia support, font scaling)

AI agents can use this section to automatically apply accessibility constraints when generating UI.

### Output Example 1: Standard Compliance (WCAG 2.1 AA)
```
The interface is designed to meet WCAG 2.1 AA guidelines. All components are tested for contrast, keyboard operability, and screen reader support.

- Text contrast: minimum 4.5:1 ratio  
- All interactive elements have a visible focus state  
- Form fields include labels, `aria-describedby`, and proper validation feedback  
- Modals use `role="dialog"` and `aria-modal="true"`  
- Navigation is keyboard-friendly and skip links are provided  
- Animations respect `prefers-reduced-motion` and are not essential for task completion  
- Tooltips, icons, and buttons use descriptive `aria-labels` where text is not visible
```
### Output Example 2: Inclusive-first Design with Extended Support
```
Accessibility is treated as a first-class feature. Beyond WCAG AA compliance, we also consider neurodiverse and motion-sensitive users.

- Typography supports scaling up to 200% without breaking layout  
- Dyslexia-friendly mode (in progress): toggles font family and adjusts letter spacing  
- All components tested with VoiceOver, NVDA, and TalkBack  
- Icon buttons always include visible or assistive text  
- Content sections are landmarked with ARIA roles (`main`, `complementary`, `navigation`)  
- Keyboard testing is part of QA process; visual focus outlines are custom-designed  
- Reduced motion mode disables parallax, page transitions, and auto-playing animations
```

## 10. Stylistic References 🎭
The Stylistic References section points to visual sources that inspire or inform the look and feel of the product. These may include existing apps, design systems, websites, dribbble shots, or specific UI patterns. This section gives both AI tools and human designers a sense of visual benchmarks, tone alignment, and aesthetic direction.

You can include:
- Links to websites or design portfolios
- Descriptions of what you’re borrowing (e.g. card layout, microinteractions, typography style)
- Moodboard-style keywords or tags (e.g. “editorial”, “brutalist”, “pastel”)
- Screenshots (if possible) or Figma frames linked via URL
- Comments about what not to emulate (optional but helpful)

This section is especially useful when multiple designers or tools need to align on the same visual direction.

### Output Example 1: Task App Inspired by Notion & Linear
```
Linear: For clarity, keyboard-first navigation, and focus states
- Link: https://linear.app

Notion: For minimalist UI, smooth typography, and subtle transitions
- Link: https://www.notion.so

Superlist: For playful but clean interface layering
- Link: https://superlist.com

Mood keywords: “calm productivity”, “elegant contrast”, “grayscale dominance”

We want to avoid overly playful or colorful UIs like Trello or Miro.
```
### Output Example 2: E-commerce Inspired by Aesop & Apple
```
Aesop: For premium editorial styling and muted palette
- Link: https://www.aesop.com

Apple Store: For product card hierarchy and focus on white space
- Link: https://www.apple.com/store

Everlane: For photography styling and tonal consistency
- Link: https://www.everlane.com

Mood keywords: “elegant minimalism”, “soft edges”, “organic feel”

We intentionally avoid skeuomorphic styles or heavily animated UIs.
```

## 11. Target Audience and Personas 🥷
This section defines who the product is for and why they need it. It should include clear descriptions of the primary user types — their goals, pain points, behaviors, and contexts of use. Rather than vague demographics (like “millennials” or “tech-savvy users”), focus on functional archetypes with motivations and constraints.

You can include:
- Persona names or roles (e.g. “Freelance Designer”, “Warehouse Manager”)
- Key goals (what they’re trying to achieve)
- Frustrations (what blocks or annoys them)
- Usage context (device, location, frequency)
- Quotes or attitudinal traits (optional, but humanizing)

This section helps AI and human designers prioritize use cases, interaction styles, tone of voice, and device considerations.

### Output Example 1: Productivity App
```
Maya (Freelance UX Designer)
- Goal: Stay organized across multiple projects and clients  
- Frustrations: Overwhelmed by notifications, loses track of priorities  
- Devices: Uses MacBook and iPhone interchangeably  
- Traits: Visually organized, values minimal UI  
- Frequency: Daily use throughout the workday

Darius (Remote Project Manager)
- Goal: Track team progress and delegate tasks with clarity  
- Frustrations: Hard to see blockers across multiple tools  
- Context: Mostly desktop use, some mobile on commute  
- Traits: Pragmatic, prefers dashboards over lists
```
### Output Example 2: AI Tool Directory Platform
```
Jess (Creative Coder)
- Goal: Discover new AI tools to accelerate creative projects  
- Pain Points: Too many tools, unclear pricing or capabilities  
- Behavior: Frequently shares tools with Twitter audience  
- Context: Uses desktop, often bookmarks tools in batches

Amir (Startup Founder)
- Goal: Compare AI productivity tools before onboarding team  
- Pain Points: Distrust of paid ads, wants side-by-side comparisons  
- Device: Mostly mobile during travel  
- Traits: Fast decision-maker, values clarity and transparency
```

## 12. Functional Requirements ⚙️
Functional requirements define what the product should do — the essential features and behaviors that support user goals. Each requirement should be specific, testable, and directly tied to either a core user flow or product promise.

Focus on:
- Primary and secondary features
- Platform-specific behaviors (e.g. web, mobile, responsive)
- Actions the user can perform
- System responses to those actions
- Any feature dependencies (e.g. search requires login)

Avoid implementation details — this is about what the system does, not how it does it. This section acts as the foundational checklist for design, development, and validation.

### Output Example 1: Personal Task Manager
```
- Users can create, edit, and delete tasks  
- Tasks can include optional due dates, tags, and priority levels  
- Tasks can be marked as completed or archived  
- Users can view tasks by today, upcoming, or tag  
- Tasks sync automatically across devices  
- Users can search tasks by keyword  
- Users can set daily reminders via push notification
```
### Output Example 2: AI Tool Curation Platform
```
- Visitors can browse AI tools by category or tag  
- Users can search for tools using free text input  
- Each tool has a dedicated profile page with metadata (features, pricing, link)  
- Users can upvote, bookmark, or share a tool  
- Users can suggest a new tool via a submission form  
- Tool lists can be sorted by popularity, date added, or relevance  
- Admins can approve, reject, or edit tool submissions
```

## 13. Non-Functional Requirements ⚙️
Non-functional requirements define how the product performs and behaves under the hood — qualities that affect the user experience, technical performance, and long-term maintainability, but aren’t user-facing features per se.

These often include:
- Performance (e.g. page load time, latency)
- Scalability (e.g. can handle X users simultaneously)
- Accessibility standards (e.g. WCAG 2.1 AA compliance)
- Security expectations (e.g. GDPR compliance, encryption)
- Localization & internationalization
- Reliability & availability
- Mobile responsiveness or offline support
- Maintainability (ease of codebase updates or design system evolution)

This section helps both product and engineering teams align on non-visible expectations that influence architectural and design decisions.

### Output Example 1: SaaS Task Manager
```
- Must load initial view within 2 seconds on 3G networks  
- Designed for mobile-first usage with full responsiveness  
- Must support offline mode with task sync upon reconnect  
- All user data is encrypted in transit and at rest (AES-256)  
- Adheres to WCAG 2.1 AA accessibility guidelines  
- Supports light and dark mode  
- Localized versions required for EN, TR, and DE  
- Error rate under 0.1% across all major flows
```
### Output Example 2: AI Tool Platform MVP
```
- Pages should render in <1.5 seconds on average  
- Site must be responsive on desktop, tablet, and mobile  
- No third-party cookies allowed; GDPR-compliant analytics only  
- SEO-optimized URLs, meta tags, and Open Graph support  
- Core web vitals: LCP < 2.5s, CLS < 0.1, FID < 100ms  
- High-availability hosting: 99.9% uptime  
- Minimal motion effects for accessibility compliance  
- Design system should be maintainable and token-based
```

## 14. User Flows 🏂
User flows describe the step-by-step paths users take to accomplish specific goals within the product. These flows help both designers and AI tools understand how screens are sequenced, what decisions users make, and what UI elements they interact with.

A strong user flow should:
- Focus on one clear user goal
- List steps sequentially, including actions and system responses
- Optionally include branching paths, conditions, or failure states
- Be presented in either numbered lists, bullet points, or diagrams
- Reference specific pages or components if known (e.g. “Login Page”, “CTA Button”)

You don’t need to document every possible flow — just the core experiences like sign-up, onboarding, purchasing, or key interactions.

### Output Example 1: Sign-Up Flow for Productivity App
```
1. User clicks “Sign Up” CTA on the homepage  
2. System presents modal with Email, Password, Confirm Password fields  
3. User fills out the form and clicks “Create Account”  
4. System validates inputs  
   → If invalid: shows error messages next to fields  
   → If valid: account is created  
5. User is redirected to onboarding screen (choose plan or skip)  
6. A welcome toast appears confirming success
```
### Output Example 2: Search and Bookmark AI Tools
```
1. User enters a keyword into the search bar on the homepage  
2. System displays filtered tool cards in real time  
3. User clicks on a tool card  
4. Tool profile page opens with detailed info  
5. User clicks the “Bookmark” icon  
6. System adds tool to the user’s saved list and shows confirmation toast  
7. User navigates to “Bookmarks” via top nav to verify it's saved
```

## 15. User Stories 📓
User stories describe product requirements from the user’s perspective, framed in a simple, structured sentence. They are commonly used in agile teams to express what users want to do and why. The format is intentionally informal and flexible — user stories are not specs, but rather conversation starters and design triggers.

The classic format is:

“As a [type of user], I want to [do something] so that [benefit or outcome].”

Best practices:
- Focus on goals, not just actions
- Avoid technical jargon
- Make stories testable and traceable to product functionality
- Group related stories by feature or persona, if needed
- Can be followed by acceptance criteria (optional, but helpful)

### Output Example 1: Task Manager
```
- As a freelancer, I want to quickly add tasks with deadlines so that I don’t forget client work.
- As a user, I want to mark tasks as completed so that I can track progress.
- As a mobile user, I want my tasks to sync across devices so that I can switch between phone and laptop.
- As a project manager, I want to organize tasks by tag so that I can filter my focus.
```
### Output Example 2: AI Tool Directory
```
- As a creative professional, I want to browse AI tools by category so that I can find ones relevant to my workflow.  
- As a new visitor, I want to search tools using natural language so that I can explore without knowing exact names.  
- As a registered user, I want to bookmark tools so that I can revisit them later.  
- As an admin, I want to approve user-submitted tools so that only quality entries appear publicly.
```

## 16. Page Map 📑
The Page Map provides a structural overview of all screens or pages in the product. It acts as a sitemap for the UI, helping teams and AI tools understand which pages exist, what each one does, and how users might navigate between them.

Each entry should include:
- Page name (e.g. “Login”, “Dashboard”)
- URL or route (e.g. /dashboard, /settings/:id)
- Type (e.g. full page, modal, drawer, popup)
- Purpose or description of its role in the product

Optionally, you can group pages by flows (onboarding, dashboard, admin) or features (search, profile). This section is especially useful for auto-generating UI skeletons or navigation systems.

### Output Example 1: Productivity App
```
- **Homepage** (`/`) – Landing page with feature overview and CTA  
- **Sign Up** (`/signup`) – Account creation form  
- **Login** (`/login`) – Login with email and password  
- **Dashboard** (`/dashboard`) – Overview of tasks and upcoming events  
- **Task Detail Modal** (`/task/:id`) – Modal overlay with task fields and comments  
- **Settings** (`/settings`) – Profile info, notification prefs  
- **404** (`/not-found`) – Error screen for invalid routes
```
### Output Example 2: AI Tools Directory
```
- **Home** (`/`) – Featured tools and search bar  
- **Search Results** (`/search?query=`) – Filtered tool list  
- **Tool Profile** (`/tools/:slug`) – Detailed page for a single AI tool  
- **Submit Tool** (`/submit`) – Form for users to suggest a tool  
- **Bookmarks** (`/saved`) – User’s saved tools  
- **Login** (`/auth/login`) – Email/password or OAuth login  
- **Admin Review** (`/admin/tools`) – Admin view for pending tool approvals  
- **Not Found** (`*`) – Catch-all error page
```

## 17. Architecture Pattern 🏛️
This part defines the overall structural paradigm of the product’s codebase and application logic. Architecture choices affect how maintainable, scalable, and testable the system is. Typical patterns include:
- MVC (Model-View-Controller)
- MVVM (Model-View-ViewModel)
- Monolithic vs Microservices
- Serverless
- Client-heavy SPA or SSR apps

Specify:
- Whether the architecture is modular or tightly coupled
- Frontend/backend separation (e.g. monorepo, separate services)
- Key patterns or conventions used in the codebase

AI systems can use this section to determine file structure, data boundaries, and rendering strategies.

### Output Example 1: Modular Monolith with MVC
```
The system uses a modular monolithic architecture with clear domain boundaries. MVC pattern is used in both frontend (React + MVC-style routing) and backend (Node.js + Express).
All modules share a common codebase in a monorepo, but are logically separated (e.g. Auth, Tasks, Users, Notifications).

Frontend and backend are deployed together but versioned independently via CI/CD pipelines.  
```
### Output Example 2: Microservices + Serverless API
```
The application uses a microservices architecture where each feature (tools, bookmarks, search, admin) is its own service.
Services are deployed as serverless functions (Vercel Functions + Firebase) with API Gateway routing.
Frontend is a React SPA hosted separately, communicating via GraphQL over HTTPS.
Services scale independently and use event-driven architecture for data sync.
```

## 18. State Management 🚥
The State Management section defines how the product handles and synchronizes internal data across components, views, and sessions. Whether you’re building a single-page application (SPA) or a hybrid SSR system, defining where the state lives, how it flows, and how it’s updated is essential for maintainability and scalability.

This section helps AI tools decide:
- Which libraries or frameworks (e.g. Redux, Zustand, MobX, Vuex) to use
- Whether state is global, local, or server-driven
- How to model persistent vs ephemeral state
- Whether to use context APIs, hooks, observables, or external services (e.g. Firebase)

You can also mention loading strategies (e.g. optimistic updates), error handling policies, and how authentication or user preferences are stored.

### Output Example 1: React App Using Zustand
```
We use Zustand as the primary global state manager for shared data (auth state, user profile, tasks). Local UI state (modal open/close, hover) is handled with React useState.

- Global state: Zustand stores are colocated with feature folders  
- Persisted state: Auth state is saved to localStorage with auto-rehydration  
- Data fetching is handled via React Query, with caching and stale-while-revalidate policies  
- Optimistic updates are used for task reordering and inline editing
```
### Output Example 2: Vue App Using Pinia
```
Pinia is used as the centralized state management solution across the Vue 3 app.

- Modular store architecture: one store per domain (user, bookmarks, tools)  
- SSR-safe hydration handled through Pinia plugin  
- Global state includes session info, saved tools, and user preferences  
- Local state like tooltip visibility handled within component scope  
- Uses Vue Devtools for debugging and inspection
```

## 19. Data Flow 🏄‍♂️
The Data Flow section describes how data moves between different parts of the application — from backend to frontend, between components, and across user interactions. This section is crucial for ensuring clarity of logic, traceability of changes, and data consistency in both code and interface design.

You should clarify:
- Whether the flow is unidirectional (common in React apps) or bidirectional (common in forms, collaborative tools)
- How data mutations happen — through actions, hooks, or API calls
- If the architecture uses event-driven, pub-sub, or observable models
- How state updates propagate (e.g. prop drilling, context, store bindings)
- Whether the app uses real-time data streams, WebSockets, or polling

AI tools use this to determine update patterns, reactivity logic, and component hierarchy decisions.

### Output Example 1: Unidirectional Flow with React
```
The application follows a unidirectional data flow. Data originates from the backend (via REST API) and is fetched using React Query. Fetched data is stored in Zustand and passed down as props to UI components.

- Data mutations (e.g. task updates) trigger optimistic updates in the store  
- Component updates are triggered via shallow state subscriptions  
- All form state is local and submitted on demand via API  
- No bidirectional sync — always fetch fresh on focus
```

### Output Example 2: Bidirectional Flow with Firebase
```
The app uses Firebase’s real-time database and authentication. State is synchronized bidirectionally:

- User actions (e.g. bookmarking tools) immediately update local store  
- Changes are pushed to Firebase and reflected in other client sessions via real-time listeners  
- Local state acts as an intermediate cache layer  
- Shared context is provided through React Context for cross-feature sync
```

## 20. Technical Stack 📚
The Technical Stack outlines the core technologies used to build and run the product. This includes frameworks, libraries, tools, and platforms across both frontend and backend — as well as databases, hosting environments, and testing utilities.

A good stack description helps AI tools and developers:
- Choose compatible components
- Generate boilerplate code with the right dependencies
- Understand constraints and integration patterns
- Align design outputs (e.g. Tailwind tokens, component libraries) with implementation tech

Organize the stack by layer (frontend, backend, data, CI/CD, etc.) and be clear about versions or notable choices.

### Output Example 1: Full Stack React + Node
```
- **Frontend**: React 18, Vite, Tailwind CSS, Zustand for state, React Query for data  
- **Backend**: Node.js (Express), RESTful APIs  
- **Database**: PostgreSQL via Prisma ORM  
- **Auth**: Firebase Authentication  
- **CI/CD**: GitHub Actions, Vercel Deploy Hooks  
- **Hosting**: Vercel (frontend), Render (backend API)
```

### Output Example 2: Jamstack with Headless CMS
```
- **Frontend**: Next.js 14 (App Router), TypeScript, Tailwind CSS  
- **Backend**: None — static content with client-side hydration  
- **CMS**: Sanity.io (structured content, real-time preview)  
- **Database**: Firestore (only for bookmarks)  
- **Auth**: Auth0 (social login)  
- **CI/CD**: Vercel (auto deploy from GitHub)  
- **Analytics**: Plausible (privacy-focused, cookie-free)
```

## 21. Authentication Process 🔒
The Authentication Process defines how users securely log in, register, and manage sessions. It’s a critical part of user access and personalization, and often dictates the structure of protected routes, state persistence, and UI feedback patterns.

In this section, describe:
- The authentication method (email/password, OAuth, magic links, SSO, etc.)
- Whether the app supports signup, login, logout, forgot password, and session persistence
- How tokens (JWT, refresh tokens) are handled
- Whether auth is managed via third-party services (e.g. Firebase Auth, Auth0)
- UI states such as “loading,” “error,” or role-based access

This helps AI tools scaffold protected routes, login forms, and conditional UI logic.

### Output Example 1: Firebase Email/Password + Social Login
```
- Users can register using email/password or sign in via Google or GitHub  
- Firebase Auth is used for user session management  
- JWT tokens are automatically managed by Firebase SDK  
- Auth state is stored globally in Zustand and persists via localStorage  
- On login, user data is fetched and cached; on logout, state is cleared  
- “Forgot password” redirects to Firebase’s recovery flow  
- Certain routes (e.g. `/dashboard`) are protected by an auth guard
```

### Output Example 2: Auth0 with Role-Based Access
```
- Users authenticate via Auth0 using Google, LinkedIn, or email/password  
- Auth0 handles sessions with refresh tokens stored in HttpOnly cookies  
- After login, user metadata and roles are retrieved via Auth0 Management API  
- Admin-only routes are conditionally shown based on `user.role`  
- Auth flow includes login, logout, token refresh, and MFA for admin users  
- Protected routes redirect unauthenticated users to `/auth/login`
```

## 22. Route Design 🧭
The Route Design section defines the structure of URLs and how different parts of the application are accessed through navigation. Good routing strategy ensures logical grouping, clean paths, and supports SEO, localization, or deep linking if applicable.

Describe:
- Overall route strategy (e.g. nested routes, flat routes, dynamic routes)
- Naming conventions (/tools/:slug, /users/:id/settings)
- Whether routes are public, protected, or restricted
- Modal routes, popups, or multi-step flows
- Integration with frameworks like React Router, Next.js App Router, Vue Router, etc.

This section enables AI tools to generate sensible navigation patterns, breadcrumbs, and page-level components.

### Output Example 1: Nested Routes in React Router
```
- `/` → Homepage  
- `/login` → Login form  
- `/dashboard` → Main dashboard (requires auth)  
   └ `/dashboard/settings` → Account settings  
   └ `/dashboard/tasks/:id` → Task detail page  
- `/admin/users` → Admin-only route  
- `/404` → Catch-all error page

All routes are handled via React Router v6 with nested layouts and lazy loading. Modals are mounted via `location.state.background` technique.
```

### Output Example 2: Next.js App Router with Static & Dynamic Segments
```
- `/` → Home  
- `/tools` → Tool listing (with filters)  
- `/tools/[slug]` → Dynamic tool detail  
- `/submit` → Tool submission form  
- `/saved` → Bookmarked tools (requires login)  
- `/auth/login` → Auth page  
- `/admin` → Admin dashboard (role-protected)

Built using Next.js App Router. Each route maps to a folder in `app/`. Dynamic routes like `[slug]` enable SSR and metadata injection for SEO.
```

## 23. API Design 🗞️
The API Design section defines how the frontend and backend communicate. Whether you’re using REST, GraphQL, or something custom, this section helps standardize endpoint structures, data formats, and request/response conventions — critical for frontend-backend alignment and for AI tools that generate integration logic.

Describe:
- API type: REST, GraphQL, RPC, etc.
- Naming and versioning conventions (/api/v1/tasks, /graphql)
- How data is modeled: resources, collections, nested relations
- Auth headers, tokens, or cookie handling
- Rate limits or pagination strategies
- Error structure (e.g. error codes, message format)

You don’t need to list every endpoint — just describe the pattern and logic behind how your APIs work.

### Output Example 1: RESTful API with Versioning
```
We use a RESTful API architecture with versioned endpoints under `/api/v1/`. Each resource has its own route:

- `/api/v1/tasks` – GET (list), POST (create)  
- `/api/v1/tasks/:id` – GET, PATCH, DELETE  
- `/api/v1/users/:id/preferences` – GET, PUT  

All requests use bearer tokens in the `Authorization` header. Pagination is cursor-based (`?after=`), and responses include metadata for total count and next page.

Errors follow a standardized JSON format:

json
{
  "error": {
    "code": "NOT_FOUND",
    "message": "Task not found"
  }
}
```

### Output Example 2: GraphQL API with Typed Schema
```
The app uses a GraphQL API with a typed schema defined in SDL. There is a single endpoint: `/graphql`.

- Frontend queries and mutations are generated using GraphQL Code Generator  
- All requests include JWT in headers (`Authorization: Bearer`)  
- Nested queries enable batching (e.g. user → bookmarks → tool details)  
- Errors are returned in GraphQL spec-compliant format with `errors[]`

Schema example:

graphql
type Tool {
  id: ID!
  name: String!
  category: String
  description: String
}

type Query {
  tools(category: String): [Tool]
  tool(id: ID!): Tool
}
```

## 24. Database Design 💾
The Database Design section outlines the data model structure of your product — which entities exist, how they relate to one another, and how the database is organized. While you don’t need a full ER diagram, this section should give AI tools and developers a solid understanding of how data is stored and queried.

Describe:
- Core entities (e.g. User, Task, Tool) and their key fields
- Relationships: one-to-many, many-to-many, etc.
- Normalization or denormalization approach
- Special structures: document stores, time series, JSON blobs
- Whether you use SQL (PostgreSQL, MySQL), NoSQL (MongoDB, Firestore), or a hybrid
- Any indexing, partitioning, or performance considerations (optional)

This section is critical for generating database schemas, migrations, or data mocks.

### Output Example 1: SQL Schema with Prisma
```
We use PostgreSQL with Prisma as the ORM. The database is fully normalized and follows relational design principles.

**Entities:**
- `User` – id, name, email, createdAt  
- `Task` – id, title, status, dueDate, userId (FK)  
- `Comment` – id, taskId (FK), text, createdAt  

**Relationships:**
- One `User` has many `Tasks`  
- One `Task` has many `Comments`

All tables use UUID primary keys and created/updated timestamps. Foreign keys are indexed for fast joins.
```
### Output Example 2: Firestore NoSQL Structure
```
We use Firestore as a NoSQL document database with the following collections:

- `users/{userId}` → user profile data  
- `tools/{toolId}` → metadata about each tool  
- `users/{userId}/bookmarks/{toolId}` → nested subcollection for saved tools  

Data is denormalized to reduce read costs. Documents are flat and use camelCase keys.  
Indexed fields include `category`, `tags`, and `createdAt` for efficient filtering.
```

## 25. Deployment (CI/CD) 🚜
The Deployment (CI/CD) section describes how your application is automatically built, tested, and delivered to production (or staging) environments. It outlines the tooling and pipeline logic used to ship changes quickly and safely.

Include details about:
- CI/CD platforms (e.g. GitHub Actions, GitLab CI, Vercel, Netlify)
- Build and test stages (e.g. lint, unit test, e2e test)
- Deployment triggers (e.g. push to main, PR merge, tag release)
- Environments (staging, production)
- Rollback strategies or preview deployments
- Secrets management, caching, and optimization techniques

AI tools can use this to infer how to format deployment scripts, optimize asset delivery, or create infrastructure scaffolds.

### Output Example: GitHub Actions + Vercel
```
- CI/CD is handled via GitHub Actions  
- Workflow runs on push to `main` or pull requests  
- Steps include linting (ESLint), unit tests (Vitest), and build  
- Vercel automatically deploys the frontend (Next.js) from `main`  
- Preview deployments are created for each PR  
- Secrets are managed in GitHub repo settings  
- Backend API (Node.js) is deployed separately to Render
```

### Output Example 2: Netlify + Turborepo
```
- CI pipeline is run via Netlify Build with monorepo support (Turborepo)  
- Auto-deployment is triggered on commits to `main` and `dev` branches  
- Linting, unit tests, and Cypress E2E tests run before build  
- Netlify deploys to CDN with atomic deployments and instant rollback  
- Each PR creates a preview deployment with contextual comments  
- Environment variables are managed via Netlify UI and encrypted storage
```

## 26. Serve Method 🥙
The Serve Method defines how your application’s content is rendered and delivered to users. This includes strategies like SSR (Server-Side Rendering), SSG (Static Site Generation), SPA (Single-Page App), and ISR (Incremental Static Regeneration).

Clarify:
- Which rendering approach(es) you use
- Why it was chosen (e.g. SEO, performance, dynamic content)
- What framework supports it (e.g. Next.js, Nuxt, Astro)
- Which routes are dynamic vs. static
- Whether content is cached, prebuilt, or revalidated on-demand

This helps AI tools understand hydration strategies, fallback behavior, and layout generation across devices and routes.

### Output Example 1: Static + Server-Side Hybrid (Next.js)
```
We use Next.js with a hybrid rendering approach:

- `/` and `/tools` are statically generated at build time (SSG)  
- `/tools/[slug]` uses ISR with a 5-minute revalidation window  
- Authenticated routes like `/saved` use client-side rendering (SPA)  
- Pages are optimized with edge caching via Vercel  
- Fallback pages are shown while ISR content is loading
```
### Output Example 2: Fully Client-Side SPA
```
The app is a pure SPA built with React and served from a CDN via Vite:

- All routes are client-side rendered (CSR)  
- On initial load, a shell layout is hydrated  
- Data is fetched on-demand via REST APIs  
- Pages like `/login` and `/dashboard` are lazy-loaded for performance  
- Content is cached using SWR on the frontend
```

## 27. Rendering and Navigation 🧭
The Rendering and Navigation section defines how views are composed and how users move between them. It addresses both technical rendering strategy and user-facing navigation patterns — ensuring a smooth, intuitive, and performant experience across the app.

Cover both the mechanics and UX perspective of navigation:
- Navigation model: client-side, server-side, or hybrid
- Link behavior: prefetching, transitions, breadcrumbs
- Layout persistence: shared shells, route-aware components
- Scroll restoration, anchor link support
- How modal or nested navigation is handled
- Framework-specific behaviors (Next.js, React Router, Nuxt, etc.)

This helps AI generate skeleton layouts, route-based transitions, and understand how components are mounted/unmounted across views.

### Output Example 1: Next.js App Router
```
We use Next.js App Router for routing and layout rendering.

- `/app` directory maps to routes and layout structure  
- Shared layout shells persist across route transitions (e.g. sidebar, navbar)  
- Navigation is handled via `<Link />` with prefetching enabled  
- Scroll position is restored automatically except for modals  
- Modal routes are nested (`/tool/[id]?modal=share`) and use `useSearchParams`  
- 404 and error boundaries are handled at layout level
```
### Output Example 2: React SPA with React Router
```
The app uses React Router v6 with client-side rendering and route-based layout.

- Nested routes provide layout scoping  
- Route transitions are animated using Framer Motion  
- Navigation state is preserved via URL query params  
- Scroll restoration is implemented manually for some pages  
- Modals and drawers are mounted via `location.state` and do not affect main route  
- Top-level routes include `/home`, `/tool/:id`, `/login`, `/dashboard/settings`
```

## 28. Content Management Approach
The Content Management Approach defines how dynamic, structured, or editorial content is created, stored, and rendered in the product. It includes any CMS (Content Management System) integration, markdown pipelines, static file handling, and localization strategies.

Outline:
- Whether you’re using a headless CMS (e.g. Sanity, Contentful), in-app editor, or hardcoded JSON
- Who manages content (e.g. admins via dashboard, developers via code)
- Whether content is static, dynamic, or regenerated (SSG/ISR)
- If there’s multi-language or multi-brand support
- How rich media, metadata, or page structure is managed
- Content versioning, scheduling, or moderation if relevant

This section guides AI tools to scaffold content models, admin interfaces, or data bindings between UI and content.

### Output Example 1: Headless CMS (Sanity)
```
We use Sanity.io as the headless CMS to manage structured content across the platform.

- Editors can update tool descriptions, tags, banners, and homepage sections  
- Content is fetched via GROQ queries and rendered statically via ISR  
- Rich text, image galleries, and CTA blocks are supported as modular content  
- CMS schema includes preview thumbnails and slug validation  
- Multi-language support is planned for v2 using i18n fields in Sanity
```
### Output Example 2: Static JSON Content
```
Content is currently managed via static JSON files stored in the `data/` directory.

- Product data (tools, categories) is written and maintained by developers  
- Each JSON file maps to a component view (e.g. tools.json, tags.json)  
- Files are pre-processed at build time using Vite  
- No CMS integration — faster build, but not editor-friendly  
- Future versions may migrate to Notion API or a lightweight headless CMS
```

## 29. Structured Content
The Structured Content section defines the core content types your product relies on — such as “Blog Post,” “Tool,” “Task,” or “Product” — and outlines the fields, formats, and relationships that structure this content. This helps both humans and AI tools understand what gets stored, displayed, and edited in the system.

Include:
- Main content types (e.g. Tool, Event, Testimonial)
- For each type: the fields it contains, their types (string, boolean, reference), and validations
- Optional fields, repeatable fields, localized fields, etc.
- Relationships (e.g. Tool has many Tags, Author has many Articles)
- Whether any of the content is modular (e.g. page sections composed from blocks)
- Format: Markdown, WYSIWYG, Rich Text, JSON, etc.

This enables AI-assisted tools to generate appropriate CMS schemas, data bindings, and mock content.

### Output Example 1: CMS-Driven Modular Content
```
We use Sanity.io and define the following content types:

- **Tool**
  - name (string, required)
  - slug (auto-generated from name)
  - description (rich text)
  - websiteURL (string, validated as URL)
  - tags (array of references to Tag)
  - createdAt (datetime)

- **Tag**
  - title (string)
  - color (enum)
  - icon (string)

- **HomepageBlock**
  - type (hero | cta | testimonial)
  - content (modular block field)
  - order (number)

All content is modular and can be previewed in real-time. Field-level validations ensure clean data entry.
```

### Output Example 2: Flat JSON Content for Tools
```
Content is manually maintained in flat JSON format. The main types are:

- **Tool**
  - id (string)
  - title (string)
  - description (string, 240 char max)
  - category (string)
  - link (string)
  - tags (array of strings)

- **Category**
  - id (string)
  - name (string)
  - icon (optional string)

These types are used to populate listings and detail pages. No rich text or dynamic relationships are used at this stage.
```

## 30. SEO Strategy
The SEO Strategy section outlines how your product is optimized for search engines. Even in AI-generated or hybrid systems, SEO is critical for discoverability, ranking, and structured content presentation across platforms like Google, Bing, and social media.

Describe:
- Metadata strategies (titles, descriptions, Open Graph, Twitter Cards)
- URL structure and cleanliness (/tools/ai-writer, not /tool?id=123)
- Sitemap generation and submission
- Canonical URLs and duplicate content handling
- Structured data (JSON-LD, Schema.org types like Product, Article, etc.)
- How dynamic content is pre-rendered or hydrated (especially for SPAs)
- Robots.txt and meta tags for indexing control

This guides AI to scaffold metadata fields, layout slots for head tags, and logic for crawlers.

### Output Example 1: Static SEO with Next.js + Schema.org
```
- Titles and meta descriptions are dynamically generated per page using `next/head`  
- Open Graph and Twitter Card meta tags are included for all detail pages  
- Canonical URLs are defined based on slug to avoid duplicate content  
- JSON-LD structured data is added for each Tool using the `SoftwareApplication` schema  
- Sitemap is automatically generated via `next-sitemap` and submitted to Google  
- Dynamic pages (`/tools/[slug]`) are statically generated (ISR) for SEO compliance  
- Robots.txt allows full indexing except for `/admin` routes
```

### Output Example 2: Minimal SEO for SPA
```
- Basic SEO is handled via `react-helmet`  
- Static meta tags are set on homepage and key routes  
- Slugs are clean (`/tool/ai-designer`) and reflect tool names  
- No structured data or sitemap yet — planned for v2  
- Crawling is allowed for all public pages; private routes are gated by auth  
- Social sharing previews are set manually for homepage and landing pages
```

## 31. Inspirations 🧚‍♀️
The Inspirations section highlights external references — apps, design systems, patterns, or even specific features — that influenced the product’s design, functionality, or tone. These references help guide creative direction and provide alignment between designers, developers, and AI systems.

Include:
- Products or tools you admire and why (UX flow, color scheme, animations, etc.)
- Screenshots or links to specific pages, if possible
- Design systems (e.g. Polaris, Material 3, Apple HIG)
- Motion or microinteraction examples
- Copywriting or tone references
- Anything that helps paint the creative “north star”

This section allows AI systems to interpret stylistic or behavioral preferences and generate UI elements accordingly.

### Output Example 1: UX + Visual Reference Stack
```
- **Linear** – for its minimal interface, clean typography, and fluid transitions  
- **Notion** – for the modular content blocks and calm color palette  
- **Raycast** – for tight keyboard navigation and native-feeling UX  
- **Shadcn/UI** – component structure and API design  
- **Stripe Docs** – layout clarity and left-aligned navigation patterns  
- Dribbble shot: https://dribbble.com/shots/21524350-Tool-Dashboard  
- Motion reference: https://lottieflow.com/animations/dashboard-interactions

These serve as creative benchmarks for tone, spacing, motion, and UI density.
```

### Output Example 2: Playful Visual Identity
```
- **Duolingo** – for friendly illustrations and microcopy  
- **Headspace** – for soft colors and calming motion  
- **Framer** – for smart onboarding flows  
- **Lucide Icons** – line icon style reference  
- Color palette inspired by: https://coolors.co/palette/fefae0-fae588-d4a373-6c584c

This helps guide our brand tone toward playful but functional — aiming for clarity and engagement without visual clutter.
```

## 32. Acceptance Criteria 🤝
Explanation

The Acceptance Criteria section defines specific conditions that must be met for a product feature, flow, or interface to be considered “done.” These criteria serve as validation gates for AI-generated output or human implementation — ensuring that functionality aligns with the intent described in earlier sections.

You can think of them as:
- Clear success conditions for each feature or requirement
- Behavioral expectations (e.g. error handling, responsiveness)
- Edge cases that must be supported
- UX quality or accessibility thresholds
- Performance or compatibility benchmarks

Good acceptance criteria help both humans and AI tools know when to stop iterating. They can be reused as test specs, automated checks, or QA validation guides.

### Output Example 1: Task Creation Flow
```
- Users can add a new task from the dashboard in under 2 clicks  
- Title is required; form cannot be submitted if empty  
- Tasks are instantly visible in the list after creation  
- If offline, task is stored locally and synced when online  
- Form fields are accessible via keyboard and screen reader  
- Error state shown when API fails with retry option  
```

### Output Example 2: Tool Detail Page
```
- Tool page loads within 2 seconds on mobile (3G simulated)  
- URL follows pattern: `/tools/{slug}` and is crawlable  
- Metadata (title, description, og:image) is set correctly  
- “Visit Website” button opens in new tab and is tracked  
- Image gallery is swipeable on mobile  
- Content is readable at 200% zoom and color contrast passes WCAG AA  
```

## 33. Additional Notes 📝
The Additional Notes section is a flexible space for capturing any information that doesn’t neatly fit into the other sections — but is still important for design, development, or AI interpretation.

Use this section for:
- Edge cases or known constraints
- Stakeholder preferences or political realities
- Pending decisions, to-dos, or unresolved assumptions
- Tooling quirks, legacy concerns, or dev handoff notes
- Any helpful reminders or clarifications

This section is especially valuable for aligning context between different team members (or AI tools), even when the data is informal.

### Output Example 1: Design Edge Cases
```
- On very narrow screens (<320px), the sidebar will be hidden by default  
- There’s an internal debate on whether to allow guest task creation — not implemented yet  
- Tool cards may include video previews in future; keep layout flexible  
- Sanity slug generation currently has a bug with Turkish characters — flagged to devs  
- We may consider light/dark toggle in a future sprint (v1 is light-only)
```

### Output Example 2: Unresolved Questions
```
- Should we support third-party login via GitHub or just email for v1?  
- We're not yet sure if ratings/reviews will be included on tool pages  
- There's a dependency on the marketing team for final brand assets  
- Waiting on legal approval for Terms of Use before launch  
- No translation planned for MVP, but flag strings for i18n just in case
```

