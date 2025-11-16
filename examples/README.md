# PLAIN Examples & Guides

This directory contains detailed examples, options, and best practices for each section of the PLAIN format. Use these files as reference guides when filling out your PLAIN document or making technical decisions.

---

## 📁 File Overview

### 💡 Product & Strategy

#### `idea-statements.md` (11KB)
**10 complete product idea examples + writing guide**
- Taskly (Productivity for Freelancers)
- Curato (AI Tool Discovery)
- Wellnest (Wellness Journaling)
- Shopmetrics (E-commerce Analytics)
- Designflow (Design Collaboration)
- Plus 5 more examples
- Step-by-step writing template
- Common mistakes to avoid

**When to use:** When writing your initial product idea or need inspiration

---

#### `personas.md` (9.1KB)
**User personas with detailed examples**
- 5 detailed persona examples (Maya, Darius, Jess, Amir, Sarah)
- Demographics, goals, frustrations, motivations
- Persona creation template
- Anti-patterns to avoid
- Using personas in design decisions

**When to use:** Defining target users, making user-centered decisions

---

#### `functional-requirements.md` (13KB)
**Feature and capability requirements**
- 4 complete product examples with detailed FR lists
- Task management, e-commerce, wellness, analytics examples
- Requirement writing templates
- Acceptance criteria patterns
- MoSCoW prioritization framework

**When to use:** Defining what features your product must have

---

#### `non-functional-requirements.md` (12KB)
**Performance, security, and quality requirements**
- Performance benchmarks (page load, API response)
- Security requirements (authentication, encryption, GDPR)
- Reliability and uptime standards
- Accessibility requirements (WCAG)
- Measurement methods and tools

**When to use:** Setting quality standards, compliance requirements

---

#### `user-stories.md` (11KB)
**User story examples and writing guide**
- 8 product categories with detailed stories
- Authentication, task management, e-commerce, social
- User story formats and templates
- INVEST criteria
- Estimation and story mapping

**When to use:** Writing user stories, planning sprints

---

#### `user-flows.md` (12KB)
**Step-by-step user journey examples**
- 8 detailed flow examples (Sign up, Checkout, Search, Onboarding)
- Decision points and error handling
- Alternative paths and edge cases
- Flow visualization tips

**When to use:** Mapping user journeys, identifying friction points

---

#### `page-map.md` (11KB)
**Site structure and navigation**
- 5 complete page map examples (SaaS, e-commerce, blog, social)
- Navigation patterns (flat, hierarchical, hub-spoke)
- URL design best practices
- Mobile navigation considerations

**When to use:** Planning site structure, organizing navigation

---

#### `inspirations.md` (10KB)
**Design inspiration and mood boards**
- 4 product examples with visual references
- Where to find inspiration (Dribbble, Awwwards, Mobbin)
- Creating mood boards
- Documenting design direction

**When to use:** Gathering visual references, aligning on design direction

---

#### `structured-content.md` (12KB)
**Content types and schema design**
- 5 content type examples (Blog, e-commerce, tasks, events, docs)
- Field types reference
- Validation rules
- Content relationships
- Headless CMS schemas (Sanity, Contentful, Strapi)

**When to use:** Defining content models, choosing CMS

---

### 🎨 Design & Visual Identity

#### `color.md` (8.7KB)
**Color palettes, psychology, and strategies**
- 6 complete palette examples (SaaS, Wellness, Creative, Luxury, Dark Mode, E-commerce)
- Color psychology guide
- Light/dark mode approaches
- Accessibility & contrast guidelines
- Color tools and generators

**When to use:** Choosing brand colors, defining semantic colors, setting up dark mode

---

#### `typography.md` (8.7KB)
**Font selection, pairing, and systems**
- System fonts vs Google Fonts vs Premium
- Typescale strategies (modular, fixed, fluid)
- Font pairing examples
- Line height & spacing
- Responsive typography
- Accessibility standards

**When to use:** Selecting fonts, creating typescale, ensuring readability

---

#### `icons.md` (10KB)
**Icon libraries and implementation**
- 7 icon library comparisons (Lucide, Heroicons, Tabler, Phosphor, Material, Font Awesome, Custom)
- Size guidelines
- Usage best practices
- Accessibility for icons
- Decision guide

**When to use:** Choosing icon library, implementing accessible icons

---

#### `design-language.md` (9.2KB)
**Defining design principles and tone**
- 5 complete design language examples (Calm, Warm, Bold, Professional, Minimal)
- Core principles framework
- Emotional tone guidelines
- Interaction philosophy
- Creating your design language

**When to use:** Establishing product personality, aligning team on design direction

---

#### `layout.md` (8.8KB)
**Grid systems and spacing**
- Grid systems (12-column, 8-column, 16-column, freeform)
- Spacing strategies (8pt, 4pt, Tailwind)
- Container widths
- Responsive breakpoints
- Layout patterns (sidebar, holy grail, card grid, split screen)

**When to use:** Setting up grid system, defining spacing scale, responsive design

---

#### `core-components.md` (10KB)
**Essential UI component documentation**
- 10 core components (Button, Input, Card, Modal, Toast, etc.)
- Variants, states, and sizes for each
- Accessibility requirements
- Component patterns (compound, polymorphic)
- Testing guidelines

**When to use:** Building component library, documenting UI patterns

---

### 🔧 Technical Stack

#### `frontend-technology.md` (6.7KB)
**Choosing your frontend framework**
- React (Vite, Next.js)
- Vue (Nuxt)
- Svelte (SvelteKit)
- Static Site Generators (Hugo, 11ty, Astro)
- No-code (Webflow, Framer)
- Decision guide & comparison table

**When to use:** Starting a new project, choosing framework

---

#### `ui-library.md` (7.1KB)
**Component libraries and design systems**
- Shadcn/UI
- Material UI
- Chakra UI
- DaisyUI
- Tailwind CSS
- Headless UI
- Custom design systems
- Comparison table

**When to use:** Selecting UI components, building design system

---

#### `content-management.md` (7.1KB)
**Managing and storing content**
- Static JSON files
- Markdown files
- Headless CMS (Sanity, Contentful, Strapi, Prismic)
- Database-driven
- Hybrid approaches
- Decision guide

**When to use:** Deciding how to manage blog posts, products, or dynamic content

---

#### `authentication.md` (9.2KB)
**User authentication strategies**
- Email & Password
- OAuth / Social Login (Google, GitHub, Twitter)
- Magic Links
- Auth services (Auth0, Clerk, Supabase, Firebase)
- MFA (Multi-Factor Authentication)
- Session management
- Comparison table

**When to use:** Implementing user login, managing sessions

---

#### `database.md` (10KB)
**Choosing a database**
- None (fully static)
- Firestore (Firebase)
- Supabase (PostgreSQL)
- PostgreSQL
- MongoDB
- localStorage / IndexedDB
- Serverless databases (PlanetScale, Neon, Turso)
- Decision guide & comparison

**When to use:** Storing user data, choosing database architecture

---

#### `hosting-deployment.md` (9.8KB)
**Where to host your product**
- Vercel
- Netlify
- GitHub Pages
- Cloudflare Pages
- Firebase Hosting
- Custom servers (VPS, PaaS)
- CI/CD setup
- Comparison table

**When to use:** Deploying your app, setting up auto-deploy

---

#### `state-management.md` (11KB)
**Managing application state**
- React useState (local)
- React Context
- Zustand
- Redux Toolkit
- React Query / TanStack Query
- Jotai
- Recoil
- Decision guide & examples

**When to use:** Managing global state, API data, complex state logic

---

#### `rendering-navigation.md` (9.7KB)
**Rendering strategies and navigation patterns**
- SPA, SSR, SSG, ISR, Hybrid comparison
- Framework examples (Next.js, Nuxt, SvelteKit)
- Navigation patterns (client-side, server-side)
- Performance optimization
- Decision guide

**When to use:** Choosing rendering strategy, implementing navigation

---

#### `api-design.md` (10KB)
**API architecture and patterns**
- REST best practices with examples
- GraphQL schema and queries
- tRPC for TypeScript
- WebSockets for real-time
- Authentication (API Keys, JWT, OAuth)
- Rate limiting and versioning

**When to use:** Designing backend APIs, choosing API paradigm

---

#### `architecture-pattern.md` (11KB)
**System architecture patterns**
- 10 architecture patterns (Monolithic, Microservices, Serverless, JAMstack, etc.)
- When to use each pattern
- Pros/cons comparison
- Decision guide by product type

**When to use:** Choosing system architecture, planning scalability

---

#### `route-design.md` (11KB)
**URL structure and routing patterns**
- Route naming conventions
- Dynamic routes and parameters
- RESTful API routes
- Query parameters vs path segments
- SEO-friendly URLs
- Security and protected routes

**When to use:** Designing URL structure, implementing routing

---

### ♿ Quality & Standards

#### `accessibility.md` (10KB)
**Making your product accessible**
- WCAG guidelines (A, AA, AAA)
- Color contrast requirements
- Keyboard navigation
- Screen readers & ARIA
- Forms and labels
- Images and alt text
- Testing checklist
- Common mistakes

**When to use:** Ensuring accessibility compliance, testing with screen readers

---

#### `seo-strategy.md` (12KB)
**Optimizing for search engines**
- Meta tags (title, description)
- Open Graph & Twitter Cards
- Structured data (Schema.org)
- URL structure
- Technical SEO (sitemap, robots.txt, performance)
- Image SEO
- Analytics setup
- Checklist

**When to use:** Improving search rankings, social media sharing

---

## 🎯 How to Use These Files

### Scenario 1: Starting a New Project

**Read in this order:**
1. `idea-statements.md` — Write your product idea
2. `frontend-technology.md` — Choose framework
3. `ui-library.md` — Choose component library
4. `content-management.md` — Choose CMS/content strategy
5. `authentication.md` — Choose auth method
6. `database.md` — Choose database (if needed)
7. `hosting-deployment.md` — Choose hosting

---

### Scenario 2: Designing Your Product

**Read in this order:**
1. `design-language.md` — Define design principles
2. `color.md` — Choose color palette
3. `typography.md` — Select fonts
4. `icons.md` — Choose icon library
5. `layout.md` — Set up grid and spacing

---

### Scenario 3: Ensuring Quality

**Read:**
- `accessibility.md` — Make it accessible
- `seo-strategy.md` — Optimize for search

---

## 📊 Quick Reference Tables

### By File Size (Largest to Smallest)

| File | Size | Category |
|---|---|---|
| functional-requirements.md | 13KB | Product |
| seo-strategy.md | 12KB | Quality |
| user-flows.md | 12KB | Product |
| non-functional-requirements.md | 12KB | Product |
| structured-content.md | 12KB | Product |
| state-management.md | 11KB | Technical |
| idea-statements.md | 11KB | Product |
| user-stories.md | 11KB | Product |
| page-map.md | 11KB | Product |
| architecture-pattern.md | 11KB | Technical |
| route-design.md | 11KB | Technical |
| accessibility.md | 10KB | Quality |
| database.md | 10KB | Technical |
| icons.md | 10KB | Design |
| core-components.md | 10KB | Design |
| api-design.md | 10KB | Technical |
| inspirations.md | 10KB | Product |
| hosting-deployment.md | 9.8KB | Technical |
| rendering-navigation.md | 9.7KB | Technical |
| design-language.md | 9.2KB | Design |
| authentication.md | 9.2KB | Technical |
| personas.md | 9.1KB | Product |
| layout.md | 8.8KB | Design |
| typography.md | 8.7KB | Design |
| color.md | 8.7KB | Design |
| ui-library.md | 7.1KB | Technical |
| content-management.md | 7.1KB | Technical |
| frontend-technology.md | 6.7KB | Technical |

**Total:** ~290KB of documentation across 29 files

---

### By Category

**💡 Product & Strategy (9 files):**
- idea-statements.md
- personas.md
- functional-requirements.md
- non-functional-requirements.md
- user-stories.md
- user-flows.md
- page-map.md
- inspirations.md
- structured-content.md

**🎨 Design & Visual Identity (6 files):**
- color.md
- typography.md
- icons.md
- design-language.md
- layout.md
- core-components.md

**🔧 Technical Stack (12 files):**
- frontend-technology.md
- ui-library.md
- content-management.md
- authentication.md
- database.md
- hosting-deployment.md
- state-management.md
- rendering-navigation.md
- api-design.md
- architecture-pattern.md
- route-design.md

**♿ Quality & Standards (2 files):**
- accessibility.md
- seo-strategy.md

---

## 💡 Tips for Using Examples

1. **Don't copy blindly** — adapt examples to your needs
2. **Compare options** — each file has decision guides
3. **Check "When to use"** sections
4. **Reference comparison tables** for quick decisions
5. **Follow checklists** to ensure nothing is missed

---

## 🔗 Related Files

- **`/plain.md`** — Full PLAIN specification (33 sections)
- **`/plain-lite.md`** — Lightweight PLAIN template (11 sections)
- **`/README.md`** — Project overview
- **`/CONTRIBUTING.md`** — How to contribute

---

## 🤝 Contributing

Found a mistake? Want to add more examples?

See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines.

---

## 📄 License

All examples are part of the PLAIN project and licensed under the MIT License.
