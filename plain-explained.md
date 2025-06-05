# PLAIN

This document represents a structured, AI-readable product definition format known as PLAIN (Product Language for AI Notation).
It is designed to be both human-friendly and machine-parseable. Each section of this document provides key information that enables AI tools to generate user interfaces, code, or product artifacts with minimal ambiguity.

Use this as the single source of truth to describe your product idea — and let both teams and AI agents build from it.

## Idea
A summary of the product’s core purpose, the problem it solves, and its main value proposition. It anchors all further design and development decisions. Use the following format.

## Design Language
Describes the overall visual tone, interaction aesthetics, and design attitude of the interface. It covers motion feedback (e.g. smooth shadows, hover transitions), layout style (e.g. card-based design), and overarching design philosophy (e.g. brutalist, minimal, skeuomorphic). This helps align designers, developers, and AI tools on the emotional and perceptual direction of the product.
- **Design Principles:** Defines the overall visual attitude of the interface — whether it’s minimalist, brutalist, playful, or corporate. This sets the aesthetic tone and informs component styling decisions.
- **Color:** Defines the core visual identity of the product using functional color roles.
- **Design System:** Defines the foundational visual and behavioral rules for building consistent and scalable UI components. May include the use of established systems (like Material, Shadcn), a custom-built atomic design structure, or token-based setups. This helps AI understand how components should look, feel, and behave across the product.
- **Icons:** Specifies the icon set used for visual labels and interaction cues.
- **Typography:** Specifies the primary typeface and base text size used throughout the UI. Use clean, modern fonts optimized for screen readability.
- **Typescale:** Determines the size relationships between different text levels (headings, body, captions).
- **Layout:** The grid structure and responsiveness strategy applied across screens.
- **Core Components:** Reusable building blocks of the UI system. Each component should follow accessibility and responsive rules.
- **Elevation System:** Outlines visual layering techniques like shadows, elevation, borders, and background contrast to create hierarchy and depth in the UI.
- **Interaction Feedback:** Specifies how the interface responds to user interactions like hover, click, or focus — including animations, visual states, or transitions that convey interactivity.
- **Motion and Transition:** Defines the tone and behavior of animations used for page loads, content changes, and micro-interactions. Helps maintain a consistent rhythm across the experience.
- **Visual Tone:** Describes the emotional feel of the interface — such as formal, fun, calm, or dynamic — conveyed through colors, typography, and spacing.
- **Animation:** Defines the animation library and feedback patterns.
- **Accessibility:** Accessibility ensures that the product can be used by people of all abilities, including those with visual, motor, cognitive, or auditory impairments. Designing for accessibility improves usability for everyone and helps meet legal standards like WCAG (Web Content Accessibility Guidelines).
- **Stylistic References:** Lists brands, tools, or design systems that inspire the visual direction. Useful for aligning AI-generated outputs with familiar visual benchmarks.

## Target Audience and Personas
Defines the primary user groups, their needs, motivations, and behaviors. Helps guide UX decisions, feature prioritization, and tone of voice.

## Functional Requirements
Outlines the essential features the product must perform, along with their acceptance criteria. These form the basis for interface design and testing. 

## Non-Functional Requirements
Describes system-level qualities such as performance, security, and accessibility. These guide technical decisions and constraints for both developers and AI tools.

## User Flows

## User Stories
Realistic, narrative examples that show how different users will interact with the product. Helps translate abstract requirements into concrete experiences.

## Page Map
This section provides a comprehensive list of all unique pages within the application, along with their **URL patterns**, **page names**, and **primary purposes**. It helps both product teams and AI tools understand the routing logic, navigation structure, and SEO architecture of the product.

Each entry should reflect how the page functions, how users reach it, and what dynamic segments (like slugs or IDs) are used. This information is crucial for sitemap generation, front-end routing, and server-side rendering strategies.

## Technical Requirements
This section outlines the technical foundation of the product, detailing key architectural decisions, system design, APIs, authentication methods, state management, routing, and database structure.
- **Architecture Pattern:** Defines the frontend-backend structure, deployment model, and how services are modularized.
- **State Management:** Explains how local and global application state is handled, including tools and patterns used.
- **Data Flow:** Outlines the journey of data from user input to final output, including what services interact and when.
- **Technical Stack:** Lists the technologies used in the frontend, backend, database, and integrations.
- **Authentication Process:** Details how user accounts, sessions, and third-party auth (e.g., OAuth) are managed.
- **Route Design:** Outlines the structure of all front-end routes and how they correspond to functionality or page types.
- **API Design:** Specifies available endpoints, what they do, how they interact, and expected formats.
- **Database Design:** Explains the relational structure of data—main entities, relationships, and purpose of each table.
- **SEO Strategy:** Describes how the application is optimized for search engine visibility. Includes decisions about rendering (SSR/SSG/CSR), URL structure, metadata, backlink readiness, and redirect handling. Sitemap generation is also part of this strategy.
- **Content Management Approach:** Defines how content is created, stored, and managed across the platform. This includes whether a CMS, headless CMS, custom admin panel, static files, or AI-assisted systems are used to handle content workflows.
- **Structured Content:** Defines how the platform supports both traditional structured data standards (like Schema.org) and modern AI comprehension through LLM-friendly content structuring. This includes semantic markup, component-level metadata, contextual tagging, and prompt-aware design to enable both SEO and AI systems to better interpret and utilize content.
- **Deployment (CI/CD):** Covers how the project is built, tested, and deployed automatically using Continuous Integration and Continuous Deployment pipelines.
- **Serve Method:** Defines how the application serves content to users: Server-Side Rendering (SSR), Static Site Generation (SSG), or Client-Side Rendering (CSR). This impacts performance, SEO, and complexity.
- **Rendering and Navigation:** This section defines how content is rendered and how users navigate through the app. It clarifies whether the platform uses SPA (Single Page Application), MPA (Multi Page Application), or a hybrid approach such as SSR (Server-Side Rendering), SSG (Static Site Generation), or CSR (Client-Side Rendering). It may also include modern strategies like ISR (Incremental Static Regeneration) or Islands Architecture. These choices affect SEO, performance, and overall user experience.

## Inspirations
A collection of visual and conceptual inspirations (e.g., moodboards, competitor UIs). Guides layout, style, and interaction patterns.

## Additional Notes
Captures any special constraints, risks, future considerations, or project-specific remarks that don’t fit into other sections.
