---
INSTRUCTIONS FOR AI CODING ASSISTANTS:

You are an expert full-stack developer and UI/UX designer. This document contains a complete PLAIN (Product Language for AI Notation) specification for a digital product.

Your task: Generate production-ready code that accurately implements this specification.

KEY GUIDELINES:
- Follow the specification exactly - use the specified technologies, colors (hex codes), fonts, and design patterns
- Implement all sections in order: Project Overview, Design Language, Color Palette, Typography, Icons, Layout, User Stories, Functional Requirements, Page Map, Structured Content, Content Management, Frontend Technology, UI Kit, Core Components
- Write clean, accessible, well-commented code with proper TypeScript types
- Include loading states, empty states, and error handling
- Ensure responsive design matching the specified strategy
- Implement dark mode if specified in Color Palette
- Build all "Must Have Features" from Functional Requirements
- Create all pages listed in Page Map section
- Use the exact UI Kit and Core Components specified
- Follow design references for visual patterns and UX inspiration

QUALITY REQUIREMENTS:
✅ Semantic HTML and ARIA labels for accessibility
✅ Proper form validation and error messages
✅ Responsive at all specified breakpoints
✅ WCAG AA color contrast ratios
✅ Keyboard navigation support
✅ Optimized images and code splitting
✅ Comprehensive error handling

When specifications use "Let AI Decide", choose modern, popular, well-supported options that fit the overall tech stack.

Study the Design References and Inspirations sections to understand visual patterns and UX flows - capture their essence in your implementation without copying directly.

---

# Project Name

[Enter your project name]

---

## 1. Idea Statement

[Write 2-4 sentences that clearly describe your product:
- What are you building?
- Who is it for?
- What problem does it solve?
- How is it different from existing solutions?]

**Example:**
> Taskly is a minimalist task management app designed for freelancers and remote workers who need to stay organized without complexity. It addresses the common problem of task management tools being either too simple (lacking necessary features) or too complex (overwhelming users with options). Taskly strikes the perfect balance with an intuitive interface that includes smart task categorization, deadline tracking, and priority management—nothing more, nothing less.

---

## 2. Design Language

### Design Style
[Choose your visual design approach: Minimalist, Material Design, Glassmorphism, Brutalism, Neumorphism, Flat Design, etc.]

[Explain why this style fits your product and audience]

### Design Tone
[Select 3-4 adjectives that describe how your product should feel]

**Examples:**
- Clean
- Professional
- Calm
- Modern
- Friendly
- Bold
- Trustworthy
- Playful

### Design References
[Provide 2-3 URLs to websites or products that inspire your design direction]

1. [URL 1] - [What you like about it]
2. [URL 2] - [What you like about it]
3. [URL 3] - [What you like about it]

### Additional Notes
[Any specific design principles, constraints, or considerations]

---

## 3. Color Palette

### Primary Color
[Hex code and purpose]
- **Color:** #______
- **Usage:** [Where this color will be used - buttons, links, highlights, etc.]

### Secondary Color
[Hex code and purpose]
- **Color:** #______
- **Usage:** [Where this color will be used]

### Accent Color (Optional)
[Hex code and purpose]
- **Color:** #______
- **Usage:** [Where this color will be used]

### Neutral Colors
- **Background:** #______
- **Surface:** #______
- **Text Primary:** #______
- **Text Secondary:** #______
- **Border:** #______

### Semantic Colors
- **Success:** #______
- **Warning:** #______
- **Error:** #______
- **Info:** #______

### Notes
[Any color usage guidelines, contrast requirements, or accessibility considerations]

---

## 4. Typography

### Font Families

#### Primary Font
[For headings and display text]
- **Font Name:** [e.g., "Inter", "Roboto", "Poppins"]
- **Weights:** [e.g., 400, 500, 600, 700]
- **Source:** [Google Fonts, Adobe Fonts, Custom, etc.]

#### Secondary Font
[For body text and UI elements]
- **Font Name:** [e.g., "Inter", "Roboto", "Open Sans"]
- **Weights:** [e.g., 400, 600]
- **Source:** [Google Fonts, Adobe Fonts, Custom, etc.]

#### Monospace Font (Optional)
[For code snippets]
- **Font Name:** [e.g., "Fira Code", "JetBrains Mono"]
- **Source:** [Google Fonts, Adobe Fonts, Custom, etc.]

### Type Scale
[Define your font sizes for different text elements]

- **H1:** [size]px / [line-height] / [weight]
- **H2:** [size]px / [line-height] / [weight]
- **H3:** [size]px / [line-height] / [weight]
- **H4:** [size]px / [line-height] / [weight]
- **Body Large:** [size]px / [line-height] / [weight]
- **Body:** [size]px / [line-height] / [weight]
- **Body Small:** [size]px / [line-height] / [weight]
- **Caption:** [size]px / [line-height] / [weight]

### Notes
[Any typography guidelines, readability considerations, or responsive adjustments]

---

## 5. Icons

### Icon System
[Choose your icon approach]
- **Style:** [Outline, Filled, Duotone, Custom]
- **Library:** [Lucide, Heroicons, Font Awesome, Feather, Phosphor, Custom, etc.]
- **Size:** [Default icon size, e.g., 20px, 24px]

### Icon Usage
[Describe how icons should be used]
- **Navigation:** [Icon style for navigation items]
- **Buttons:** [Icon style for buttons]
- **Indicators:** [Icon style for status indicators]
- **Empty States:** [Icon/illustration style for empty states]

### Custom Icons
[List any custom icons needed that aren't in standard libraries]
- [Icon name] - [Purpose]
- [Icon name] - [Purpose]

### Notes
[Any icon guidelines or accessibility considerations]

---

## 6. Layout

### Layout System
[Describe your grid system and spacing]

#### Grid
- **Type:** [Fixed, Fluid, Hybrid]
- **Columns:** [e.g., 12-column grid]
- **Max Width:** [e.g., 1280px]
- **Gutter:** [e.g., 24px]

#### Spacing Scale
[Define your spacing system]
- **xs:** [value]px
- **sm:** [value]px
- **md:** [value]px
- **lg:** [value]px
- **xl:** [value]px
- **2xl:** [value]px

### Breakpoints
[Define responsive breakpoints]
- **Mobile:** [value]px
- **Tablet:** [value]px
- **Desktop:** [value]px
- **Large Desktop:** [value]px

### Layout Patterns

#### Header
[Describe header structure]
- **Position:** [Fixed, Sticky, Static]
- **Height:** [value]px
- **Contents:** [Logo, Navigation, User menu, etc.]

#### Navigation
[Describe navigation structure]
- **Type:** [Sidebar, Top bar, Mobile drawer, etc.]
- **Width:** [For sidebar, e.g., 240px]
- **Behavior:** [Collapsible, Fixed, etc.]

#### Content Area
[Describe main content structure]
- **Max Width:** [value]px
- **Padding:** [value]px
- **Layout:** [Single column, Multi-column, etc.]

#### Footer
[Describe footer structure]
- **Position:** [Static, Sticky]
- **Contents:** [Links, Copyright, Social media, etc.]

### Notes
[Any layout guidelines or responsive behavior notes]

---

## 7. Inspiration

[List 3-5 products, websites, or apps that inspire different aspects of your product. For each, explain what specifically inspires you and what you want to learn from it.]

### 1. [Product/Website Name]
- **URL:** [URL]
- **What inspires you:** [Specific features, design patterns, UX flows, visual style, etc.]
- **What to learn:** [What aspects you want to incorporate or learn from]

### 2. [Product/Website Name]
- **URL:** [URL]
- **What inspires you:** [Specific features, design patterns, UX flows, visual style, etc.]
- **What to learn:** [What aspects you want to incorporate or learn from]

### 3. [Product/Website Name]
- **URL:** [URL]
- **What inspires you:** [Specific features, design patterns, UX flows, visual style, etc.]
- **What to learn:** [What aspects you want to incorporate or learn from]

---

## 8. User Stories

[Define who will use your product and what they need to accomplish. Write in the format: "As a [user type], I want to [action] so that [benefit]"]

### Primary User Personas

#### [Persona 1 Name]
**Role:** [e.g., Freelance Designer]
**Goals:** [What they want to achieve]
**Pain Points:** [Current problems they face]

**User Stories:**
1. As a [persona], I want to [action] so that [benefit]
2. As a [persona], I want to [action] so that [benefit]
3. As a [persona], I want to [action] so that [benefit]

#### [Persona 2 Name]
**Role:** [e.g., Small Business Owner]
**Goals:** [What they want to achieve]
**Pain Points:** [Current problems they face]

**User Stories:**
1. As a [persona], I want to [action] so that [benefit]
2. As a [persona], I want to [action] so that [benefit]
3. As a [persona], I want to [action] so that [benefit]

### Example
> **User Story:** As a freelance designer, I want to quickly capture task ideas on my phone so that I don't forget important to-dos when I'm away from my desk.

---

## 9. Functional Requirements

[Define what your product must do. Be specific about features, behaviors, and edge cases.]

### Core Features

#### Feature 1: [Feature Name]
**Description:** [What this feature does]

**Requirements:**
- [Specific requirement 1]
- [Specific requirement 2]
- [Specific requirement 3]

**Edge Cases:**
- [What happens if...]
- [What happens when...]

#### Feature 2: [Feature Name]
**Description:** [What this feature does]

**Requirements:**
- [Specific requirement 1]
- [Specific requirement 2]
- [Specific requirement 3]

**Edge Cases:**
- [What happens if...]
- [What happens when...]

### User Flows

#### [Flow Name - e.g., "User Registration"]
1. [Step 1]
2. [Step 2]
3. [Step 3]
4. [Result/Outcome]

**Error Handling:**
- [What happens if step fails]
- [Validation requirements]

### Business Rules
- [Rule 1]
- [Rule 2]
- [Rule 3]

### Non-Functional Requirements

#### Performance
- [Page load time requirements]
- [Response time requirements]
- [Concurrent users to support]

#### Security
- [Authentication requirements]
- [Authorization requirements]
- [Data protection requirements]

#### Accessibility
- [WCAG level to meet]
- [Screen reader support]
- [Keyboard navigation]

#### Localization
- [Languages to support]
- [Date/time formats]
- [Currency formats]

---

## 10. Page Map

[Map out all pages and their relationships]

### Public Pages
[Pages anyone can access]

```
/ (Landing page)
/about
/pricing
/contact
/login
/register
/forgot-password
```

### Authenticated Pages
[Pages requiring login]

```
/dashboard
  /dashboard/overview
/[feature-area]
  /[feature-area]/[sub-page]
/settings
  /settings/profile
  /settings/account
  /settings/notifications
```

### Admin Pages (if applicable)
[Pages for administrators]

```
/admin
  /admin/users
  /admin/analytics
  /admin/settings
```

### Dynamic Routes
[Pages with parameters]

```
/[resource]/:id
/[resource]/:id/edit
/blog/:slug
```

### Special Pages
```
/404 (Not found)
/500 (Error)
/maintenance
```

### Navigation Hierarchy

**Primary Navigation:**
- [Nav item 1]
- [Nav item 2]
- [Nav item 3]

**Secondary Navigation:**
- [Sub-item 1]
- [Sub-item 2]

**Utility Navigation:**
- [Help/Docs]
- [User menu]
- [Notifications]

---

## 11. Structured Content

[Define your data models and content types]

### Data Models

#### [Model Name - e.g., "User"]
```typescript
interface User {
  id: string
  email: string
  name: string
  avatar?: string
  role: 'user' | 'admin'
  createdAt: Date
  updatedAt: Date
}
```

**Relationships:**
- [Relationship to other models]

**Validation:**
- [Field validation rules]

#### [Model Name - e.g., "Project"]
```typescript
interface Project {
  id: string
  title: string
  description: string
  status: 'active' | 'completed' | 'archived'
  ownerId: string
  createdAt: Date
  updatedAt: Date
}
```

**Relationships:**
- [Relationship to other models]

**Validation:**
- [Field validation rules]

### Content Types
[Define different content types if you have a CMS]

#### [Content Type Name]
**Fields:**
- [Field name]: [Type] - [Description]
- [Field name]: [Type] - [Description]

**Usage:** [Where this content type is used]

---

## 12. Frontend Technology

### Framework
**Choice:** [React, Vue, Svelte, Next.js, etc.]
**Version:** [Specific version]
**Reasoning:** [Why this framework]

### Build Tool
**Choice:** [Vite, Webpack, Parcel, etc.]
**Reasoning:** [Why this tool]

### Styling
**Approach:** [CSS-in-JS, CSS Modules, Tailwind, Sass, etc.]
**Libraries:** [Styled-components, Emotion, Tailwind CSS, etc.]
**Reasoning:** [Why this approach]

### State Management
**Solution:** [Redux, Zustand, Jotai, Context API, TanStack Query, etc.]
**Reasoning:** [Why this solution]

### Routing
**Solution:** [React Router, Next.js routing, TanStack Router, etc.]
**Reasoning:** [Why this solution]

### Data Fetching
**Solution:** [TanStack Query, SWR, Apollo Client, tRPC, etc.]
**Reasoning:** [Why this solution]

### Form Handling
**Solution:** [React Hook Form, Formik, TanStack Form, etc.]
**Reasoning:** [Why this solution]

### Testing
**Unit Tests:** [Vitest, Jest, etc.]
**E2E Tests:** [Playwright, Cypress, etc.]
**Reasoning:** [Why these tools]

### Additional Libraries
- [Library name] - [Purpose]
- [Library name] - [Purpose]

### Browser Support
- **Minimum versions:** [List minimum browser versions]
- **Progressive enhancement:** [Yes/No]

---

## 13. UI Kit

[Define the base UI components that will be used throughout your product]

### Component Library
**Choice:** [shadcn/ui, Radix UI, Chakra UI, Material-UI, Custom, etc.]
**Reasoning:** [Why this library]

### Core Components

#### Buttons
**Variants:**
- Primary
- Secondary
- Ghost
- Destructive
- Outline

**Sizes:**
- Small
- Medium
- Large

**States:**
- Default
- Hover
- Active
- Disabled
- Loading

#### Inputs
**Types:**
- Text
- Email
- Password
- Number
- Search
- Textarea

**States:**
- Default
- Focus
- Error
- Disabled
- Read-only

#### Form Components
- Checkbox
- Radio button
- Select dropdown
- Date picker
- File upload
- Toggle/Switch

#### Feedback
- Alert
- Toast/Notification
- Modal/Dialog
- Tooltip
- Loading spinner
- Progress bar

#### Navigation
- Tabs
- Breadcrumbs
- Pagination
- Menu/Dropdown

#### Data Display
- Table
- Card
- Badge
- Avatar
- Accordion
- List

### Accessibility Requirements
- [ARIA labels for all interactive elements]
- [Keyboard navigation support]
- [Focus indicators]
- [Color contrast ratios]

---

## 14. Core Components

[Define product-specific components that are unique to your application]

### [Component Name 1]

**Purpose:** [What this component does and why it exists]

**API/Props:**
```typescript
interface ComponentProps {
  // Props definition
}
```

**States:**
- Loading
- Error
- Empty
- Success
- Disabled

**Example Usage:**
```tsx
<ComponentName
  prop1="value"
  prop2="value"
  onAction={handler}
/>
```

**Features:**
- [Feature 1]
- [Feature 2]
- [Feature 3]

**Dependencies:**
- [UI Kit components used]
- [External libraries needed]

### [Component Name 2]

**Purpose:** [What this component does and why it exists]

**API/Props:**
```typescript
interface ComponentProps {
  // Props definition
}
```

**States:**
- Loading
- Error
- Empty
- Success

**Example Usage:**
```tsx
<ComponentName
  prop1="value"
  prop2="value"
/>
```

**Features:**
- [Feature 1]
- [Feature 2]

---

## 15. Content Management

[Define how content will be created, managed, and updated]

### CMS Approach
**Solution:** [Headless CMS, Traditional CMS, Custom, None]
**Platform:** [Contentful, Sanity, Strapi, WordPress, Custom, etc.]
**Reasoning:** [Why this approach]

### Content Types
[List the types of content that need to be managed]

#### [Content Type 1 - e.g., "Blog Posts"]
**Fields:**
- Title (required)
- Slug (required, unique)
- Author (reference to User)
- Published date
- Content (rich text)
- Featured image
- Tags
- Status (draft/published)

**Access Control:**
- Who can create: [Roles]
- Who can edit: [Roles]
- Who can publish: [Roles]

#### [Content Type 2]
**Fields:**
- [Field specifications]

**Access Control:**
- [Permissions]

### Editorial Workflow
1. [Draft creation]
2. [Review process]
3. [Approval]
4. [Publishing]

### Media Management
**Storage:** [Where images/files are stored]
**Optimization:** [How images are processed]
**CDN:** [Yes/No, which service]

### Localization
**Languages supported:** [List of languages]
**Translation workflow:** [How content is translated]

---

## 16. Additional Notes

[Any other important information, constraints, or considerations that don't fit in other sections]

### Technical Constraints
- [Constraint 1]
- [Constraint 2]

### Business Constraints
- [Budget limitations]
- [Timeline requirements]
- [Team size/composition]

### Integration Requirements
- [Third-party services to integrate]
- [API requirements]
- [Authentication providers]

### Deployment
**Hosting:** [Platform - Vercel, Netlify, AWS, etc.]
**CI/CD:** [GitHub Actions, GitLab CI, etc.]
**Environments:** [Development, Staging, Production]

### Analytics & Monitoring
**Analytics:** [Google Analytics, Plausible, etc.]
**Error Tracking:** [Sentry, LogRocket, etc.]
**Performance Monitoring:** [Vercel Analytics, etc.]

### SEO Requirements
- [Meta tags]
- [Structured data]
- [Sitemap]
- [Robots.txt]

### Future Considerations
[Features or improvements planned for later phases]
- [Future feature 1]
- [Future feature 2]

### Open Questions
[Questions that still need to be answered]
- [Question 1]
- [Question 2]

---

## Document Metadata

**Version:** 1.0
**Last Updated:** [Date]
**Author:** [Your name]
**Status:** [Draft, In Progress, Review, Final]

---

**Next Steps:**
1. Fill out each section systematically
2. Review with your team
3. Use this document to generate UI with AI tools
4. Keep this document updated as your product evolves
