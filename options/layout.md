# Layout

Layout systems and responsive strategies that organize content and create consistent structure across devices. Each approach offers different benefits for content organization and user flow.

## Layout Patterns

Choose a layout system that supports your content needs and adapts gracefully across screen sizes:

### Grid System
Structured layouts using CSS Grid for complex, two-dimensional arrangements.
- **Best for:** Dashboards, magazines, galleries, complex interfaces
- **Characteristics:** Precise control, gap management, area templates
- **Breakpoints:** Mobile (360px), Tablet (768px), Desktop (1024px), Wide (1440px)
- **Examples:** The New York Times, Pinterest, Behance

### Flexbox Flow
Flexible one-dimensional layouts that adapt to content and container.
- **Best for:** Navigation bars, card layouts, form controls, toolbars
- **Characteristics:** Dynamic sizing, alignment control, wrapping behavior
- **Breakpoints:** Fluid with min/max constraints
- **Examples:** Medium, Linear, Stripe

### Container Queries
Content-responsive layouts that adapt based on container size, not viewport.
- **Best for:** Component libraries, design systems, modular interfaces
- **Characteristics:** True component isolation, context-aware sizing
- **Breakpoints:** Component-specific (300px, 500px, 700px containers)
- **Examples:** Modern design systems, widget-based apps

### Sidebar Layout
Classic sidebar navigation with main content area.
- **Best for:** Admin panels, documentation, dashboards, email clients
- **Characteristics:** Fixed or collapsible sidebar, focus on content hierarchy
- **Mobile:** Hamburger menu or bottom navigation
- **Examples:** Notion, Slack, Discord

### Single Column
Content-focused layout with optimal reading width.
- **Best for:** Blogs, articles, landing pages, mobile-first designs
- **Characteristics:** 65-75 character line length, centered content
- **Max width:** 650-750px for readability
- **Examples:** Medium, Substack, Ghost

### Masonry/Pinterest
Dynamic column layouts with variable height items.
- **Best for:** Image galleries, social feeds, portfolio sites
- **Characteristics:** Optimal space usage, visual interest, flexible items
- **Columns:** Responsive (1-5 based on viewport)
- **Examples:** Pinterest, Unsplash, Dribbble

### Full-Width Sections
Edge-to-edge sections with constrained content.
- **Best for:** Marketing sites, landing pages, storytelling
- **Characteristics:** Visual impact, section separation, scroll-based
- **Content width:** 1200-1400px max within full sections
- **Examples:** Apple, Tesla, Spotify

### Card-Based
Modular cards that reorganize based on screen size.
- **Best for:** E-commerce, dashboards, social platforms, app stores
- **Characteristics:** Self-contained units, consistent spacing, scannable
- **Grid:** Auto-fit with minmax(300px, 1fr)
- **Examples:** YouTube, Amazon, Trello

### Split Screen
Two-column layouts with equal or weighted divisions.
- **Best for:** Comparisons, onboarding, product showcases
- **Characteristics:** Visual balance, dual focus, storytelling
- **Mobile:** Stacked vertical sections
- **Examples:** Dropbox, Todoist, Sketch

### Horizontal Scroll
Side-scrolling sections for specific content types.
- **Best for:** Media galleries, timelines, category navigation
- **Characteristics:** Touch-friendly, preserves vertical flow
- **Implementation:** CSS scroll-snap for smooth experience
- **Examples:** Netflix, App Store, Instagram Stories

### Fixed + Scrollable
Fixed elements (header/footer) with scrollable content area.
- **Best for:** Apps, tools, persistent navigation needs
- **Characteristics:** Always-accessible controls, maximized content area
- **Scroll:** Main content only, fixed elements stay
- **Examples:** Gmail, VS Code, Figma

### Asymmetric Layout
Intentionally unbalanced layouts for visual interest.
- **Best for:** Creative portfolios, agencies, artistic sites
- **Characteristics:** Dynamic tension, unique personality, memorable
- **Balance:** 2/3 + 1/3 or golden ratio divisions
- **Examples:** Awwwards sites, design studios

### Bento Box
Mixed-size rectangular sections fitting together like a puzzle.
- **Best for:** Dashboards, feature showcases, product pages
- **Characteristics:** Visual hierarchy through size, efficient space use
- **Grid:** Typically 12 or 24 column base grid
- **Examples:** Windows 11, iOS widgets, Vercel dashboard

### Mobile-First Stacked
Everything stacks vertically on mobile, progressively enhanced for larger screens.
- **Best for:** Content sites, forms, simple interfaces
- **Characteristics:** Predictable mobile experience, progressive complexity
- **Enhancement:** Add columns and features as space allows
- **Examples:** Government sites, documentation, forms

### Desktop Application
Traditional application layout with menubar, toolbar, and panels.
- **Best for:** Complex tools, productivity apps, professional software
- **Characteristics:** Familiar patterns, extensive controls, workspace customization
- **Panels:** Resizable, dockable, collapsible
- **Examples:** Photoshop, IDEs, Slack desktop

## Responsive Strategy

Define how your layout adapts across different screen sizes and devices:

### Mobile-First
Start with the smallest screen and progressively enhance for larger displays.
- **Philosophy:** Essential content first, add features as space allows
- **Breakpoints:** 640px (sm), 768px (md), 1024px (lg), 1280px (xl)
- **Best for:** Content sites, most modern web apps
- **Benefits:** Performance focused, forces prioritization

### Desktop-First
Design for desktop then simplify for smaller screens.
- **Philosophy:** Full experience first, gracefully degrade
- **Breakpoints:** 1440px, 1024px, 768px, 480px (descending)
- **Best for:** Complex applications, data-heavy interfaces
- **Benefits:** Easier for feature-rich applications

### Fluid/Liquid
Percentage-based widths that scale smoothly with viewport.
- **Philosophy:** Continuous adaptation, no fixed breakpoints
- **Implementation:** %, vw/vh units, clamp(), min/max
- **Best for:** Simple layouts, reading-focused sites
- **Benefits:** Smooth scaling, no jarring breakpoint jumps

### Adaptive
Fixed layouts at specific breakpoints with no in-between states.
- **Philosophy:** Optimized designs for specific devices
- **Breakpoints:** 320px, 768px, 1024px, 1440px (fixed widths)
- **Best for:** Device-specific experiences, precise control
- **Benefits:** Predictable layouts, easier QA testing

### Content-First
Breakpoints based on content needs rather than devices.
- **Philosophy:** Let content determine when layout breaks
- **Breakpoints:** Wherever content needs it (e.g., 45em for line length)
- **Best for:** Typography-heavy sites, unique layouts
- **Benefits:** Optimal reading experience, content-driven design

### Component-Based
Each component defines its own responsive behavior.
- **Philosophy:** Modular responsive design, container queries
- **Implementation:** Container queries, component breakpoints
- **Best for:** Design systems, reusable components
- **Benefits:** True component isolation, predictable behavior

### Hybrid Approach
Combination of strategies for different parts of the interface.
- **Philosophy:** Right tool for each job
- **Example:** Fluid typography + adaptive layout + responsive images
- **Best for:** Complex products with varied content
- **Benefits:** Maximum flexibility, optimized per section

### Progressive Disclosure
Show/hide features based on screen size and capability.
- **Philosophy:** Core features always visible, advanced features conditional
- **Implementation:** Priority+ pattern, off-canvas menus, accordions
- **Best for:** Feature-rich applications, complex navigation
- **Benefits:** Maintains usability across all devices

---

*Layout is the foundation of user experience. Choose a system that not only organizes your content effectively but also guides users naturally through their tasks. Your responsive strategy should align with your users' devices and your content's needs.*