# PLAIN LITE: Lightweight Product Definition Format

PLAIN LITE is a simplified version of the full PLAIN specification, designed for early-stage ideas, solo makers, rapid prototyping, and non-technical product owners. It focuses on the essential sections needed to communicate a product vision clearly to both humans and AI tools — without overwhelming technical depth.

**⏱️ Estimated completion time:** 30–60 minutes
**🎯 Best for:** MVPs, side projects, early concept validation, AI-powered prototyping
**📚 Examples:** See [examples/](./examples/) folder for detailed guides and options

---

## Initial Prompt for the Agent

👇 Use this prompt when asking an AI to generate a PLAIN LITE document for you.

```
You are an expert product designer and strategist. Your task is to generate a complete PLAIN LITE document based on a product idea provided by the user.

- Start by understanding the core idea and target audience
- Fill in each section with clarity, simplicity, and purpose
- Use natural, human-readable language
- Make reasonable assumptions when details are missing
- Avoid jargon — write for both technical and non-technical readers
- Do not alter section titles or order
- Focus on what matters most for an MVP or early prototype

Your goal is to create a structured, AI-ready blueprint that can be used by design tools like v0, Bolt, Figma Make, Lovable, or Cursor to generate UI, code, or prototypes.
```

---

# 1. 💡 Idea Statement

**Purpose:** A clear, concise description of your product idea — what it is, who it's for, what problem it solves, and how it delivers value.

**Format:** 2–4 short paragraphs

**What to include:**
- **What:** Brief description of the product
- **Who:** Target users (roles, demographics, context)
- **Problem:** What pain points or needs it addresses
- **Solution:** How it solves the problem
- **Value:** Why it's better or different from alternatives

**📖 See:** [examples/idea-statements.md](./examples/idea-statements.md) for 10 complete examples

---

# 2. 🎨 Design Language

**Purpose:** Define the emotional tone, design principles, and overall aesthetic of your product.

**Format:** Short descriptions (1-2 sentences each)

**What to include:**

### Visual Tone
Describe the overall aesthetic (e.g., "minimal and calm", "bold and energetic", "warm and friendly")

### Design Principles
2-4 core principles that guide design decisions (e.g., "Clarity over cleverness", "Mobile-first", "Accessible by default")

### Personality
How should the product feel to users? (e.g., "professional but approachable", "playful and encouraging")

**📖 See:** [examples/design-language.md](./examples/design-language.md) for 5 complete design language examples

---

# 3. 🎨 Color

**Purpose:** Define your color palette — primary, secondary, semantic colors, and light/dark mode approach.

**Format:** List of colors with hex codes or descriptive names

**What to include:**

### Primary Colors
Main brand color(s) that define your product's identity

### Secondary Colors
Supporting colors for variety and hierarchy

### Semantic Colors
- Success (e.g., green)
- Warning (e.g., orange/yellow)
- Error (e.g., red)
- Info (e.g., blue)

### Neutrals
Gray scale for text, backgrounds, borders

### Light/Dark Mode
Specify if you'll support dark mode, or stick to light mode only

**📖 See:** [examples/color.md](./examples/color.md) for 6 palette examples and strategies

---

# 4. ✍️ Typography

**Purpose:** Select fonts, define typescale, and set hierarchy for text.

**Format:** Font families + scale approach

**What to include:**

### Font Families
- **Headings:** Font name and weights (e.g., "Inter, weights 600-700")
- **Body:** Font name and weights (e.g., "Inter, weights 400-500")
- **Monospace (optional):** For code or data (e.g., "JetBrains Mono")

### Typescale
How text sizes relate (e.g., "Modular scale (1.25 ratio)", "Fixed scale", "Tailwind defaults")

### Line Height & Spacing
General approach (e.g., "1.5 for body, 1.2 for headings")

**📖 See:** [examples/typography.md](./examples/typography.md) for font selection and pairing guides

---

# 5. 🎯 Icons

**Purpose:** Choose an icon style and library.

**Format:** Icon library name + style description

**What to include:**
- Icon library (e.g., "Lucide", "Heroicons", "Material Icons", "Custom SVG")
- Style (e.g., "Outlined", "Filled", "Duotone")
- Size guidelines (e.g., "16px, 20px, 24px")

**📖 See:** [examples/icons.md](./examples/icons.md) for icon library comparisons

---

# 6. 📐 Layout

**Purpose:** Define grid system, spacing scale, and responsive breakpoints.

**Format:** Short descriptions or values

**What to include:**

### Grid System
- Type (e.g., "12-column", "CSS Grid", "Flexbox-based")
- Container max-width (e.g., "1280px", "1440px", "Full-width")

### Spacing Scale
How spacing is structured (e.g., "8pt grid (8, 16, 24, 32...)", "Tailwind scale (4, 8, 12, 16...)")

### Breakpoints
Responsive design breakpoints (e.g., "Mobile: 320px, Tablet: 768px, Desktop: 1024px")

### Layout Patterns
Common patterns used (e.g., "Sidebar + main content", "Full-width cards", "Centered column")

**📖 See:** [examples/layout.md](./examples/layout.md) for grid and spacing strategies

---

# 7. ✨ Inspiration

**Purpose:** Share visual or functional examples that inspire your product's design.

**Format:** Links + brief descriptions of what you like about each

**What to include:**
- Product/website URLs
- Screenshots or Figma links (optional)
- What you like (e.g., "clean navigation", "color palette", "micro-interactions")
- Mood keywords (e.g., "calm productivity", "editorial elegance", "playful creativity")
- What to avoid (optional)

**📖 See:** [examples/inspirations.md](./examples/inspirations.md) for gathering and documenting inspiration

---

# 8. 📖 User Stories

**Purpose:** Describe key features from the user's perspective — what they want to do and why.

**Format:** "As a [user], I want [goal], so that [benefit]"

**What to include:**
- 5–10 core user stories for MVP
- Group by feature area if helpful (e.g., Authentication, Task Management, Settings)
- Include acceptance criteria if known (optional)

**Example:**
```
As a freelance designer,
I want to quickly capture tasks as they come to mind,
So that I don't forget important work.
```

**📖 See:** [examples/user-stories.md](./examples/user-stories.md) for detailed examples and templates

---

# 9. ⚙️ Functional Requirements

**Purpose:** List what your product must do — specific features and capabilities.

**Format:** Grouped list of features with brief descriptions

**What to include:**
- **Must-Have Features** (MVP essentials)
- **Should-Have Features** (important but not critical)
- **Could-Have Features** (nice-to-haves, post-MVP)
- For each feature, specify:
  - What it does
  - Any key behaviors or constraints
  - Acceptance criteria (optional)

**Example:**
```
**FR-1: User Registration**
- Users can create accounts with email and password
- Password must be minimum 8 characters
- Verification email sent upon registration
```

**📖 See:** [examples/functional-requirements.md](./examples/functional-requirements.md) for detailed FR examples

---

# 10. 🗺️ Page Map

**Purpose:** Map out the core screens or pages in your product and their hierarchy.

**Format:** Hierarchical list or tree structure

**What to include:**
- **Public Pages** (logged-out users can access)
- **App Pages** (requires authentication)
- **Utility Pages** (404, settings, etc.)
- For each page:
  - Page name
  - Route/URL (e.g., `/`, `/about`, `/app/dashboard`, `/products/:id`)
  - Brief purpose

**Example:**
```
Public:
- / (Homepage)
- /features (Product features)
- /pricing (Pricing page)
- /login (Login page)

App (Authenticated):
- /app/dashboard (Main dashboard)
- /app/tasks (Task list)
- /app/tasks/:id (Task detail)
- /app/settings (User settings)
```

**📖 See:** [examples/page-map.md](./examples/page-map.md) for complete site structure examples

---

# 11. 📦 Structured Content

**Purpose:** Define content types (data models) if your product has structured data like blog posts, products, tasks, etc.

**Format:** List of content types with fields

**What to include:**
- Content type name (e.g., "Blog Post", "Task", "Product")
- Fields for each type (e.g., title, description, date, status)
- Field types (text, rich text, number, date, image, relation)
- Required vs optional fields

**Example:**
```
**Content Type: Blog Post**
- title (text, required)
- slug (slug, required, unique)
- body (rich text, required)
- author (relation to Author, required)
- publishedAt (date, required)
- status (select: draft/published)
```

**📖 See:** [examples/structured-content.md](./examples/structured-content.md) for schema examples

---

# 12. 🖥️ Frontend Technology

**Purpose:** Choose the framework or tool to build your interface.

**What to include:** Pick one (or specify your own)

**Options:**

### React
- **Next.js** (SSR/SSG, recommended for production apps)
- **Vite + React** (SPA, fast dev experience)
- Best for: SaaS, dashboards, complex UIs

### Vue
- **Nuxt** (SSR/SSG)
- **Vite + Vue** (SPA)
- Best for: Interactive apps, beginner-friendly

### Svelte
- **SvelteKit** (SSR/SSG)
- Best for: Performance-focused apps, minimal bundle size

### Static Site Generators
- **Astro** (multi-framework support)
- **Hugo** (ultra-fast, Go-based)
- **11ty** (JavaScript-based)
- Best for: Blogs, docs, marketing sites

### No-Code
- **Webflow** (visual builder)
- **Framer** (design-to-code)
- Best for: Non-developers, landing pages

**📖 See:** [examples/frontend-technology.md](./examples/frontend-technology.md) for detailed comparison

---

# 13. 🎨 UI Kit

**Purpose:** Choose a component library or design system to speed up development.

**What to include:** Pick one (or specify your own)

**Options:**

### Shadcn/UI
- Headless, Tailwind-based, copy-paste components
- Highly customizable
- Best for: Modern apps, developers who want control

### Material UI (MUI)
- Comprehensive, Google's Material Design
- Large ecosystem
- Best for: Enterprise apps, familiar design language

### Chakra UI
- Accessible by default, themeable
- React-focused
- Best for: Accessible apps, quick prototyping

### DaisyUI
- Tailwind plugin with ready-made components
- Minimal JS, theme support
- Best for: Tailwind users who want pre-built components

### Tailwind CSS
- Utility-first, build your own components
- Best for: Full design control, custom systems

### Custom Design System
- Build from scratch
- Best for: Unique branding, long-term products

**📖 See:** [examples/ui-library.md](./examples/ui-library.md) for UI kit comparison

---

# 14. 🧩 Core Components

**Purpose:** List the essential UI components your product needs.

**What to include:** Check components you'll use

**Common Components:**
- [ ] Button
- [ ] Input (text, email, password)
- [ ] Textarea
- [ ] Select / Dropdown
- [ ] Checkbox / Radio
- [ ] Toggle / Switch
- [ ] Modal / Dialog
- [ ] Toast / Notification
- [ ] Card
- [ ] Table
- [ ] Tabs
- [ ] Accordion
- [ ] Avatar
- [ ] Badge
- [ ] Alert
- [ ] Tooltip
- [ ] Date Picker
- [ ] File Upload
- [ ] Pagination
- [ ] Breadcrumb
- [ ] Progress Bar
- [ ] Skeleton Loader

**📖 See:** [examples/core-components.md](./examples/core-components.md) for component documentation

---

# 15. 📂 Content Management

**Purpose:** Define how you'll manage and store content.

**What to include:** Pick one (or specify your own)

**Options:**

### Static JSON Files
- Simple, version-controlled
- No CMS needed
- Best for: Small datasets, static content

### Markdown Files
- Great for blogs, docs
- Supports frontmatter metadata
- Best for: Text-heavy content, version control

### Headless CMS
- **Sanity** (flexible, real-time)
- **Contentful** (enterprise-grade)
- **Strapi** (open-source, self-hosted)
- **Prismic** (developer-friendly)
- Best for: Editor-friendly workflows, multi-channel

### Database
- **Firestore** (NoSQL, real-time)
- **Supabase** (PostgreSQL-based)
- **MongoDB** (NoSQL, flexible schema)
- Best for: Dynamic, user-generated content

### Hybrid
- Static files + CMS for some sections
- Best for: Mixed content types

**Also specify:**
- **Authentication** (None, Email/Password, OAuth, Magic Links, Auth0/Clerk/Supabase)
- **Hosting** (Vercel, Netlify, GitHub Pages, Cloudflare Pages, Firebase)
- **Database** (None, Firestore, Supabase, PostgreSQL, MongoDB, localStorage)

**📖 See:**
- [examples/content-management.md](./examples/content-management.md)
- [examples/authentication.md](./examples/authentication.md)
- [examples/hosting-deployment.md](./examples/hosting-deployment.md)
- [examples/database.md](./examples/database.md)

---

# 16. 📝 Additional Notes

**Purpose:** Capture anything that doesn't fit elsewhere — constraints, open questions, future ideas.

**Format:** Freeform notes

**What to include:**
- **Open Questions:** Pending decisions or areas needing clarification
- **Constraints:** Budget, timeline, technical limitations
- **Future Ideas:** Features to consider post-MVP
- **Accessibility:** Key requirements (WCAG level, keyboard nav, screen readers)
- **Performance:** Target metrics (page load < 2s, etc.)
- **Success Criteria:** What "done" looks like (all features work, deployed, accessible)
- **Dependencies:** Third-party services, APIs, team constraints

**📖 See:**
- [examples/accessibility.md](./examples/accessibility.md)
- [examples/non-functional-requirements.md](./examples/non-functional-requirements.md)

---

## How to Use PLAIN LITE

### Step 1: Write Your Idea Statement
Start with a clear 2–3 paragraph description of your product.

### Step 2: Feed It to an AI (Optional)
Use the **Initial Prompt for the Agent** at the top of this file. Paste your idea statement and ask the AI to generate a full PLAIN LITE document.

### Step 3: Fill Out Each Section
Work through sections 1–16, using the [examples/](./examples/) folder for guidance and inspiration.

### Step 4: Review & Refine
Read through your completed document. Ensure it's clear, specific, and aligned with your vision.

### Step 5: Use It with AI Tools
Feed your completed PLAIN LITE document to tools like **v0**, **Bolt**, **Cursor**, **Lovable**, or **Figma Make** to generate UI, components, or code.

### Step 6: Iterate
Update your PLAIN LITE file as your product evolves. Keep it as your single source of truth.

---

## When to Use PLAIN LITE vs Full PLAIN

| **PLAIN LITE** | **Full PLAIN** |
|---|---|
| Early-stage ideas | Production-ready products |
| Solo makers, small teams | Larger teams with designers + devs |
| MVPs and prototypes | Complex apps with multiple flows |
| 30–60 min to complete | 2–4 hours to complete |
| ~16 core sections | 33 detailed sections |
| Light technical detail | Deep technical specs (API, DB, state) |
| Good for rapid prototyping | Good for comprehensive planning |

---

## Examples & References

All sections link to detailed examples in the [examples/](./examples/) directory:

- **Product:** idea-statements, personas, user-stories, functional-requirements, non-functional-requirements, user-flows, page-map, inspirations, structured-content
- **Design:** design-language, color, typography, icons, layout, core-components
- **Technical:** frontend-technology, ui-library, content-management, authentication, database, hosting-deployment, state-management, rendering-navigation, api-design, architecture-pattern, route-design
- **Quality:** accessibility, seo-strategy

**📚 Browse all examples:** [examples/README.md](./examples/README.md)

---

## License

This document is part of the PLAIN project, licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Contributing

Want to improve PLAIN LITE? Read the [Contribution Guidelines](./CONTRIBUTING.md) and submit a PR!
