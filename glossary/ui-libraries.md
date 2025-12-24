# UI Libraries

Component libraries and design systems that accelerate development with pre-built, customizable components. Choose based on design philosophy, customization needs, framework compatibility, and project requirements.

## Utility-First CSS Frameworks

CSS frameworks that provide low-level utility classes to build custom designs without writing CSS. These offer maximum flexibility but require more design decisions.

### Tailwind CSS
The utility-first CSS framework that's taken the web by storm.
- **Best for:** Custom designs, rapid prototyping, design systems
- **Philosophy:** Utility classes for everything, no pre-built components
- **Key Features:** JIT compiler, arbitrary values, dark mode, responsive utilities
- **Framework Compatibility:**
  - **React:** Perfect (with Tailwind UI, Headless UI)
  - **Vue:** Excellent support
  - **Svelte:** Great integration
  - **Angular:** Good with setup
  - **All frameworks:** Universal support
- **When to use:**
  - Building custom designs from scratch
  - Want complete control over styling
  - Need consistent design tokens
  - Building a design system
  - Want to avoid CSS conflicts
- **Customization:** Highly customizable via config
- **Learning curve:** Medium
- **Bundle size:** Only includes used utilities
- **Community:** Massive, extensive plugins

### UnoCSS
The instant on-demand atomic CSS engine.
- **Best for:** Performance-critical apps, Vite projects
- **Philosophy:** Atomic CSS with presets, faster than Tailwind
- **Key Features:** No parsing, instant HMR, attributify mode, pure CSS icons
- **Framework Compatibility:**
  - **Vite projects:** Perfect integration
  - **Nuxt:** First-class support
  - **Astro:** Great support
  - **All frameworks:** Works everywhere
- **When to use:**
  - Need fastest CSS generation
  - Want Tailwind-like utilities with better performance
  - Building with Vite
  - Want pure CSS icons
- **Customization:** Preset-based system
- **Learning curve:** Low (if you know Tailwind)
- **Bundle size:** Minimal, on-demand
- **Community:** Growing rapidly

### WindiCSS (Deprecated)
Tailwind CSS compatible utility-first framework.
- **Note:** Development ceased, migrate to UnoCSS or Tailwind
- **Legacy projects only**

## Component Libraries - Multi-Framework

Libraries that provide versions for multiple frameworks, maintaining consistent design across different tech stacks.

### Headless UI
Unstyled, accessible UI components by Tailwind team.
- **Best for:** Custom designs with Tailwind, accessibility focus
- **Philosophy:** Behavior without styles, pair with Tailwind
- **Components:** Limited but essential (Dialog, Dropdown, Toggle, etc.)
- **Framework Compatibility:**
  - **React:** Full support
  - **Vue:** Full support
  - **Alpine.js:** Via plugins
- **When to use:**
  - Building with Tailwind CSS
  - Need accessible components
  - Want complete styling control
  - Building custom design system
- **Customization:** 100% styleable
- **Learning curve:** Low
- **Accessibility:** WCAG compliant
- **Bundle size:** Tiny, tree-shakeable

### DaisyUI
Semantic component classes for Tailwind CSS.
- **Best for:** Rapid prototyping, themed applications
- **Philosophy:** Semantic classes on top of Tailwind
- **Components:** 50+ components, multiple themes
- **Framework Compatibility:**
  - **All frameworks:** CSS-only, works everywhere
  - **React/Vue/Svelte:** Excellent
- **When to use:**
  - Want Tailwind with pre-built components
  - Need multiple themes
  - Rapid prototyping
  - Don't want to build components from scratch
- **Customization:** Theme-based, CSS variables
- **Learning curve:** Low
- **Themes:** 30+ built-in themes
- **Bundle size:** Moderate (purges unused)

## React UI Libraries

Component libraries specifically built for React applications, leveraging React's ecosystem and patterns.

### Shadcn/UI
Copy-paste React components built with Radix and Tailwind.
- **Best for:** Modern React apps, Next.js projects, custom design systems
- **Philosophy:** Copy-paste ownership, not a dependency
- **Components:** 40+ beautifully designed components
- **Key Features:** Dark mode, TypeScript, Radix primitives, customizable
- **When to use:**
  - Building with Next.js or Vite
  - Want to own your components
  - Need modern, accessible components
  - Like Tailwind CSS
  - Want to customize everything
- **Customization:** Complete control (you own the code)
- **Learning curve:** Low-Medium
- **Bundle size:** Only what you use
- **Community:** Rapidly growing, very popular

### Material-UI (MUI)
React components implementing Google's Material Design.
- **Best for:** Enterprise apps, admin dashboards, Google-like UIs
- **Philosophy:** Material Design specification
- **Components:** 100+ components, comprehensive
- **Key Features:** Theming system, CSS-in-JS, data grid, date pickers
- **When to use:**
  - Building enterprise applications
  - Want Material Design aesthetic
  - Need comprehensive component set
  - Building admin dashboards
  - Need advanced data tables
- **Customization:** Powerful theming, sx prop
- **Learning curve:** Medium-High
- **Bundle size:** Large (tree-shakeable)
- **Pricing:** Free core, paid advanced components

### Ant Design (AntD)
Enterprise-focused React UI library from Alibaba.
- **Best for:** Enterprise apps, admin panels, B2B products
- **Philosophy:** Enterprise design language
- **Components:** 60+ high-quality components
- **Key Features:** Form validation, tables, date/time pickers, charts
- **When to use:**
  - Building enterprise software
  - Need comprehensive form handling
  - Want professional, clean design
  - Building data-heavy interfaces
  - Need internationalization
- **Customization:** Theme variables, ConfigProvider
- **Learning curve:** Medium
- **Bundle size:** Large (tree-shakeable)
- **Community:** Huge in Asia, growing globally

### Chakra UI
Modular and accessible React component library.
- **Best for:** Modern web apps, startups, design-conscious projects
- **Philosophy:** Simplicity, modularity, accessibility
- **Components:** 50+ components, hooks, utilities
- **Key Features:** Dark mode, responsive styles, emotion CSS-in-JS
- **When to use:**
  - Want modern, clean aesthetic
  - Need excellent DX
  - Building accessible applications
  - Like prop-based styling
  - Want good TypeScript support
- **Customization:** Theme-based, style props
- **Learning curve:** Low-Medium
- **Bundle size:** Moderate (tree-shakeable)
- **Community:** Active, friendly

### Mantine
Full-featured React components and hooks library.
- **Best for:** Modern applications, rapid development
- **Philosophy:** Developer experience first
- **Components:** 100+ components and 50+ hooks
- **Key Features:** Dark theme, form management, notifications, hooks collection
- **When to use:**
  - Want batteries-included library
  - Need lots of hooks
  - Building feature-rich apps
  - Want modern design
  - Need form management
- **Customization:** Extensive theming, styles API
- **Learning curve:** Medium
- **Bundle size:** Moderate to large
- **Community:** Growing rapidly

### Arco Design
Comprehensive React UI library by ByteDance.
- **Best for:** Modern apps, international projects
- **Philosophy:** Inclusive design system
- **Components:** 60+ high-quality components
- **Key Features:** Design tokens, dark mode, pro components
- **When to use:**
  - Want modern alternative to Ant Design
  - Building international products
  - Need comprehensive components
  - Like clean, modern aesthetic
- **Customization:** CSS variables, theme tokens
- **Learning curve:** Medium
- **Bundle size:** Moderate (tree-shakeable)
- **Community:** Growing

### React Bootstrap
Bootstrap components built for React.
- **Best for:** Bootstrap-based projects, traditional web apps
- **Philosophy:** Bootstrap design in React
- **Components:** All Bootstrap components as React
- **When to use:**
  - Migrating from Bootstrap
  - Want familiar Bootstrap look
  - Need Bootstrap ecosystem
  - Working with designers using Bootstrap
- **Customization:** Bootstrap theming
- **Learning curve:** Low (if you know Bootstrap)
- **Bundle size:** Moderate
- **Community:** Large, established

### Semantic UI React
React integration of Semantic UI.
- **Best for:** Content-focused sites, readable interfaces
- **Philosophy:** Human-friendly HTML
- **Components:** 50+ components
- **When to use:**
  - Want semantic naming
  - Building content sites
  - Like Semantic UI design
- **Customization:** Theming system
- **Learning curve:** Low-Medium
- **Bundle size:** Large
- **Community:** Stable

### Blueprint
React UI toolkit for desktop applications by Palantir.
- **Best for:** Data-heavy desktop apps, complex interfaces
- **Philosophy:** Desktop-first design
- **Components:** Complex components (tables, date ranges, select)
- **When to use:**
  - Building desktop-like web apps
  - Need complex data tables
  - Building analytics dashboards
  - Want information-dense UI
- **Customization:** Sass variables
- **Learning curve:** Medium-High
- **Bundle size:** Large
- **Community:** Niche but dedicated

## Vue UI Libraries

Component libraries optimized for Vue.js applications, leveraging Vue's reactive system and composition API.

### Vuetify
Material Design component framework for Vue.
- **Best for:** Material Design apps, rapid prototyping
- **Philosophy:** Material Design specification
- **Components:** 80+ Material components
- **Version:** Vuetify 3 for Vue 3
- **When to use:**
  - Want Material Design
  - Building with Vue 3/Nuxt 3
  - Need comprehensive components
  - Want quick prototyping
- **Customization:** SASS variables, theme system
- **Learning curve:** Medium
- **Bundle size:** Large (tree-shakeable)
- **Community:** Largest Vue UI community

### Element Plus
Desktop-oriented Vue 3 UI library.
- **Best for:** Enterprise apps, admin panels
- **Philosophy:** Clean, professional design
- **Components:** 60+ components
- **When to use:**
  - Building enterprise Vue apps
  - Need comprehensive form components
  - Want clean, minimal design
  - Building admin interfaces
- **Customization:** CSS variables, theme tool
- **Learning curve:** Low-Medium
- **Bundle size:** Moderate (on-demand import)
- **Community:** Large, especially in Asia

### Naive UI
TypeScript-first Vue 3 component library.
- **Best for:** Modern Vue 3 apps, TypeScript projects
- **Philosophy:** TypeScript-first, tree-shakeable
- **Components:** 80+ well-crafted components
- **When to use:**
  - Building with Vue 3 + TypeScript
  - Want modern design
  - Need excellent TypeScript support
  - Want tree-shaking by default
- **Customization:** CSS variables, theme editor
- **Learning curve:** Medium
- **Bundle size:** Excellent tree-shaking
- **Community:** Growing rapidly

### Quasar
Full-featured Vue framework with components.
- **Best for:** Cross-platform apps (web, mobile, desktop)
- **Philosophy:** Write once, deploy everywhere
- **Components:** 70+ Material components
- **When to use:**
  - Building for multiple platforms
  - Want all-in-one solution
  - Need mobile app with Capacitor
  - Want desktop app with Electron
- **Customization:** Sass variables, theme builder
- **Learning curve:** Medium-High
- **Bundle size:** Large but optimized
- **Community:** Active, helpful

### PrimeVue
Rich UI component suite for Vue.
- **Best for:** Enterprise apps, feature-rich interfaces
- **Philosophy:** Comprehensive component suite
- **Components:** 90+ components
- **When to use:**
  - Need rich components (charts, trees, etc.)
  - Building enterprise applications
  - Want multiple theme options
  - Need advanced data tables
- **Customization:** Multiple themes, theme designer
- **Learning curve:** Medium
- **Bundle size:** Large (modular)
- **Community:** Cross-framework (Prime family)

### Vant
Mobile-first Vue component library.
- **Best for:** Mobile web apps, PWAs
- **Philosophy:** Mobile-first design
- **Components:** 70+ mobile components
- **When to use:**
  - Building mobile web apps
  - Creating PWAs
  - Need touch-optimized components
  - Building e-commerce mobile sites
- **Customization:** CSS variables, theme customization
- **Learning curve:** Low-Medium
- **Bundle size:** Lightweight for mobile
- **Community:** Huge in Asia

### Ant Design Vue
Ant Design for Vue applications.
- **Best for:** Enterprise Vue apps
- **Philosophy:** Enterprise design language
- **Components:** Port of React Ant Design
- **When to use:**
  - Want Ant Design in Vue
  - Building enterprise apps
  - Need consistent with React version
- **Customization:** Less variables, ConfigProvider
- **Learning curve:** Medium
- **Bundle size:** Large (tree-shakeable)
- **Community:** Growing

## Angular UI Libraries

Component libraries built specifically for Angular applications, utilizing Angular's powerful features.

### Angular Material
Official Material Design components for Angular.
- **Best for:** Material Design apps, Google-style interfaces
- **Philosophy:** Official Material Design implementation
- **Components:** 40+ Material components, CDK
- **When to use:**
  - Want official Angular components
  - Building Material Design apps
  - Need accessibility (a11y)
  - Want Google's design language
- **Customization:** Theming system, CSS variables
- **Learning curve:** Medium
- **Bundle size:** Moderate (tree-shakeable)
- **Community:** Official, well-supported

### PrimeNG
Comprehensive Angular UI suite.
- **Best for:** Enterprise Angular apps, data-heavy interfaces
- **Philosophy:** Rich component collection
- **Components:** 90+ components
- **When to use:**
  - Building enterprise Angular apps
  - Need advanced components
  - Want multiple themes
  - Need charts and data visualization
- **Customization:** Theme designer, CSS variables
- **Learning curve:** Medium
- **Bundle size:** Large (modular)
- **Community:** Active, enterprise-focused

### NG-ZORRO
Ant Design for Angular.
- **Best for:** Enterprise apps, admin dashboards
- **Philosophy:** Enterprise design language
- **Components:** 60+ high-quality components
- **When to use:**
  - Want Ant Design in Angular
  - Building enterprise software
  - Need internationalization
  - Want comprehensive components
- **Customization:** Less variables, theme system
- **Learning curve:** Medium
- **Bundle size:** Large (tree-shakeable)
- **Community:** Strong in enterprise

### Clarity
VMware's Angular component library.
- **Best for:** Enterprise apps, data-dense interfaces
- **Philosophy:** Enterprise clarity design
- **Components:** 30+ enterprise components
- **When to use:**
  - Building VMware-style apps
  - Need enterprise components
  - Want clean, professional design
- **Customization:** CSS custom properties
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Enterprise-focused

### Nebular
Customizable Angular UI library.
- **Best for:** Admin dashboards, SaaS applications
- **Philosophy:** Flexible and customizable
- **Components:** 40+ components, 4 themes
- **When to use:**
  - Building admin dashboards
  - Want multiple theme options
  - Need authentication components
  - Building SaaS products
- **Customization:** Multiple themes, CSS variables
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Growing

## Svelte UI Libraries

Component libraries designed for Svelte's compile-time optimization and reactivity.

### Skeleton
Tailwind + Svelte UI toolkit.
- **Best for:** Modern Svelte apps, SvelteKit projects
- **Philosophy:** Tailwind-powered Svelte components
- **Components:** 40+ components, themes
- **When to use:**
  - Building with SvelteKit
  - Using Tailwind CSS
  - Want modern design
  - Need theme system
- **Customization:** Tailwind config, themes
- **Learning curve:** Low-Medium
- **Bundle size:** Small (Svelte compiled)
- **Community:** Growing rapidly

### Carbon Components Svelte
IBM's Carbon Design System for Svelte.
- **Best for:** Enterprise Svelte apps, IBM projects
- **Philosophy:** IBM's design language
- **Components:** 50+ Carbon components
- **When to use:**
  - Building enterprise Svelte apps
  - Want IBM's design system
  - Need accessible components
  - Building data applications
- **Customization:** Carbon themes
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** IBM-backed

### Svelte Material UI
Material Design for Svelte.
- **Best for:** Material Design Svelte apps
- **Philosophy:** Material Design in Svelte
- **Components:** Material components
- **When to use:**
  - Want Material Design
  - Building with Svelte/SvelteKit
  - Need comprehensive components
- **Customization:** Theme customization
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Active

### Attractions
Svelte UI kit with attention to detail.
- **Best for:** Modern Svelte applications
- **Philosophy:** Clean, modern components
- **Components:** 30+ components
- **When to use:**
  - Want unique design
  - Building modern apps
  - Need clean components
- **Customization:** CSS variables
- **Learning curve:** Low
- **Bundle size:** Small
- **Community:** Small but dedicated

## Solid UI Libraries

Component libraries for SolidJS applications, leveraging fine-grained reactivity.

### Hope UI
Chakra-inspired component library for SolidJS.
- **Best for:** Modern Solid apps
- **Philosophy:** Port of Chakra UI design
- **Components:** 40+ components
- **When to use:**
  - Building with SolidJS
  - Like Chakra UI design
  - Want modern components
- **Customization:** Theme system
- **Learning curve:** Low-Medium
- **Bundle size:** Small (Solid optimized)
- **Community:** Growing

### SUID
Material Design components for SolidJS.
- **Best for:** Material Design Solid apps
- **Philosophy:** Material You design
- **Components:** Material components
- **When to use:**
  - Want Material Design
  - Building with SolidJS
  - Need familiar components
- **Customization:** Material theming
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Active

### Kobalte
Headless UI primitives for SolidJS.
- **Best for:** Custom design systems
- **Philosophy:** Unstyled, accessible primitives
- **Components:** Core UI primitives
- **When to use:**
  - Building custom components
  - Need full control
  - Want accessibility
- **Customization:** 100% custom styles
- **Learning curve:** Medium
- **Bundle size:** Tiny
- **Community:** Growing

## Mobile-First Libraries

UI libraries optimized for mobile experiences and touch interactions.

### Ionic
Cross-platform mobile UI components.
- **Best for:** Mobile apps, PWAs
- **Philosophy:** Native-like mobile components
- **Framework Support:** React, Vue, Angular
- **Components:** 100+ mobile components
- **When to use:**
  - Building mobile apps
  - Creating PWAs
  - Need native-like UI
  - Want cross-platform
- **Customization:** CSS variables, themes
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Large, established

### Framework7
Full-featured mobile HTML framework.
- **Best for:** Mobile web apps, hybrid apps
- **Philosophy:** iOS and Android native look
- **Framework Support:** React, Vue, Svelte
- **Components:** Complete mobile UI
- **When to use:**
  - Building mobile-first
  - Want native look/feel
  - Need mobile gestures
- **Customization:** Multiple themes
- **Learning curve:** Medium-High
- **Bundle size:** Large
- **Community:** Active

### OnsenUI
Mobile app development framework.
- **Best for:** Hybrid mobile apps
- **Philosophy:** Native mobile patterns
- **Framework Support:** React, Vue, Angular
- **Components:** Mobile-specific components
- **When to use:**
  - Building Cordova apps
  - Need mobile components
  - Want native patterns
- **Customization:** Theme roller
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Stable

## Web Components Libraries

Framework-agnostic component libraries built with Web Components standards.

### Shoelace (Web Awesome)
Framework-agnostic web components.
- **Best for:** Multi-framework projects, design systems
- **Philosophy:** Web standards, framework-agnostic
- **Components:** 50+ web components
- **When to use:**
  - Need framework independence
  - Building design system
  - Using multiple frameworks
  - Want future-proof components
- **Customization:** CSS custom properties
- **Learning curve:** Low-Medium
- **Bundle size:** Tree-shakeable
- **Community:** Growing

### Fast
Web Components by Microsoft.
- **Best for:** Enterprise design systems
- **Philosophy:** Adaptive design system
- **Components:** Core components, design tokens
- **When to use:**
  - Building design systems
  - Need Microsoft quality
  - Want adaptive components
- **Customization:** Design tokens
- **Learning curve:** Medium-High
- **Bundle size:** Modular
- **Community:** Microsoft-backed

### Vaadin Components
Enterprise web components.
- **Best for:** Enterprise applications
- **Philosophy:** Production-ready components
- **Components:** 40+ components
- **When to use:**
  - Building enterprise apps
  - Need reliable components
  - Want long-term support
- **Customization:** CSS properties, themes
- **Learning curve:** Medium
- **Bundle size:** Moderate
- **Community:** Enterprise-focused

## Specialized Libraries

Libraries focused on specific use cases or design philosophies.

### Radix UI
Low-level UI primitives for React.
- **Best for:** Building design systems
- **Philosophy:** Unstyled, accessible primitives
- **Components:** 30+ primitive components
- **When to use:**
  - Building custom design system
  - Used by Shadcn/UI
  - Need accessibility
  - Want complete control
- **Customization:** 100% custom styling
- **Learning curve:** Medium
- **Bundle size:** Tiny, modular
- **Community:** Design system focused

### Reakit (Ariakit)
Accessible React components.
- **Best for:** Accessibility-focused apps
- **Philosophy:** WAI-ARIA compliant
- **Components:** Accessible primitives
- **When to use:**
  - Accessibility is critical
  - Building inclusive apps
  - Need ARIA compliance
- **Customization:** Unstyled or themed
- **Learning curve:** Medium
- **Bundle size:** Small
- **Community:** Accessibility-focused

### React Spectrum
Adobe's design system components.
- **Best for:** Adobe-style applications
- **Philosophy:** Adobe's Spectrum design
- **Components:** Enterprise components
- **When to use:**
  - Want Adobe's design
  - Building creative tools
  - Need enterprise components
- **Customization:** Spectrum themes
- **Learning curve:** Medium-High
- **Bundle size:** Large
- **Community:** Adobe-backed

### Fluent UI
Microsoft's design system for web.
- **Best for:** Microsoft-style apps, Office 365
- **Philosophy:** Microsoft's Fluent Design
- **Components:** Office-like components
- **Framework Support:** React (mainly), Web Components
- **When to use:**
  - Building Microsoft-style apps
  - Need Office-like UI
  - Enterprise applications
- **Customization:** Theme designer
- **Learning curve:** Medium
- **Bundle size:** Large
- **Community:** Microsoft-backed

## Selection Criteria

Consider these factors when choosing a UI library:

- **Design Philosophy:** Opinionated vs flexible
- **Component Coverage:** Number and variety of components
- **Customization Level:** Theming vs complete control
- **Bundle Size:** Impact on performance
- **Framework Compatibility:** Native vs ports
- **Learning Curve:** Team onboarding time
- **Community Support:** Documentation, examples, help
- **Accessibility:** WCAG compliance level
- **Mobile Support:** Responsive vs mobile-first
- **TypeScript Support:** Type definitions quality
- **Maintenance:** Update frequency, long-term viability
- **License & Cost:** Open source vs commercial

---

*Choose a UI library that balances development speed with customization needs. Start with established libraries for production apps, but don't overlook newer options that might better fit your specific requirements.*