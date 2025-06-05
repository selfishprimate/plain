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
- **Architecture Pattern:**
- **State Management:**
- **Data Flow:**
- **Technical Stack:**
- **Authentication Process:**
- **Route Design:**
- **API Design:**
- **Database Design:**
- **SEO Strategy:**
- **Content Management Approach:**
- **Structured Content:**
- **Deployment (CI/CD):**
- **Serve Method:**
- **Rendering and Navigation:**

## Inspirations
