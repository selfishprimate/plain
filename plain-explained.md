# PlAIN Explained

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

#### Few-shot Examples

_The following examples illustrate the expected format and level of detail for an Idea Statement. Each should be written in 2–3 concise paragraphs, clearly describing the product’s purpose, target users, key problems it solves, and how it delivers value._

> Curato is a curated web platform designed to help creative professionals discover, explore, and share AI tools tailored to their needs. By browsing through categorized collections, users can access detailed tool profiles, visit official websites, or share tools directly on social media. The platform streamlines tool discovery by combining smart filters, tag-based navigation, and clean UI previews—making it easier than ever to find the right AI tool for any creative workflow. Whether you're a designer looking for image generators or a writer exploring language models, Curato offers a structured and visual way to navigate the AI landscape.

[More Examples](cheat-sheets/idea-statements.md)

#### Prompts
```
Write an Idea Statement for a cross-platform productivity app that helps freelance designers and writers organize tasks, set deadlines, and sync their work across devices. The app should include recurring task templates, a distraction-free interface, and support for offline use. Emphasize how the product reduces cognitive overload and improves daily structure.
```
```
Create a 2–3 paragraph Idea Statement for a web platform designed to help UX researchers discover AI-powered tools and templates. The platform should offer categorized tool listings, smart search and filters, detailed descriptions, and a sharing mechanism. Focus on how it simplifies tool discovery and supports collaborative curation.
```
```
Generate an Idea Statement for a mobile journaling app targeted at Gen Z users who want to track their mood, reflect on daily thoughts, and build emotional resilience. The product should use guided prompts, data visualization, and minimalistic UI to keep users engaged. Mention long-term benefits and core emotional value.
```

## 2. Design Language
Define how the product should look, feel, and behave. Think of it as a visual and interaction manifesto. Fill in as many sub-sections as needed to reflect your vision.

  ### Design Principles
  Define guiding values for the interface — e.g. clarity, speed, minimalism, playfulness.
  
  ### Color
  Specify primary color scheme, semantic colors, background colors. Mention light/dark mode if applicable.
  
  ### Design System
  Specify which system to follow (e.g. “Use Shadcn/UI”, “Follow Tailwind-inspired atomic tokens”), or create a custom one.

  ### Icons
  Define icon style (e.g. stroke, filled, 24px grid) and reference a library if needed (e.g. Lucide, Tabler).
  
  ### Typography
  Define font families, usage rules (e.g. headings vs body), line heights, font weights.
  
  ### Typescale
  Describe the vertical rhythm — e.g. modular scale system, responsive variants, naming convention (xs, sm, base…).
  
  ### Layout
  Define container widths, grid structure, spacing scale, breakpoints.
  
  ### Core Components
  List essential components (buttons, inputs, cards, etc.) and their visual tone.
  
  ### Elevation System
  Define how layering and shadows are used for depth and interaction cues.
  
  ### Interaction Feedback
  Describe visual or motion feedback (e.g. hover, tap, loading states).
  
  ### Motion and Transition
  Outline key transitions, durations, easing curves. Define where motion should be used and where it shouldn’t.
  
  ### Visual Tone
  Define the emotional tone of visuals — friendly, serious, playful, etc. (especially relevant for illustrations and imagery).
  
  ### Animation
  Specify rules or restrictions on animated elements. Are microinteractions allowed? Should transitions be subtle?
  
  ### Accessibility
  State key accessibility goals — e.g. color contrast levels, keyboard navigation, screen reader support.
  
  ### Stylistic References
  Mention any visual benchmarks — apps, websites, or dribbble shots that inspired the look.

## 3. Target Audience and Personas
Identify the key user types. Describe their goals, pain points, contexts, and motivations. Keep it persona-level, not demographic fluff.

## 4. Functional Requirements
List what the product must do. These are the features — not technical, but functional. Be specific and testable.

## 5. Non-Functional Requirements
Define performance, accessibility, localization, scalability, and other systemic expectations that affect experience but aren’t features.

## 6. User Flows
Describe step-by-step user journeys for key tasks (e.g. “Sign Up”, “Book a Trip”, “Upload a Photo”). Use numbered steps or diagrams.

## 7. User Stories
Define product needs from the user’s perspective in the format:
“As a [persona], I want to [action], so that [outcome].”
Focus on the why, not just the action.

## 8. Page Map
List all pages/screens in the product. Include: page name, URL (if known), type (modal, full-page, popup), and purpose.

## 9. Technical Requirements
Each subsection defines key implementation choices for developers and AI tools. Fill in only what’s relevant — you can skip or simplify as needed.

  ### Architecture Pattern
  Define if the project uses MVC, MVVM, monolith, microservices, etc.
  
  ### State Management
  Define approach for managing application state — e.g. Redux, Zustand, Context API.
  
  ### Data Flow
  Describe how data moves between components/layers — one-way, bidirectional, event-driven.
  
  ### Technical Stack
  List technologies: frontend, backend, DB, CI/CD, etc.
  
  ### Authentication Process
  Define login flows, SSO, token refresh, etc.
  
  ### Route Design
  List route structure and naming logic, especially for nested routes.
  
  ### API Design
  Define REST vs GraphQL, endpoint structure, versioning rules.
  
  ### Database Design
  Basic schema ideas if relevant, especially entity relationships.
  
  ### SEO Strategy
  Define meta data handling, sitemap, canonical rules, if SEO matters.
  
  ### Content Management Approach
  Describe whether it’s headless CMS, static, markdown, etc.
  
  ### Structured Content
  List core content types and their fields — especially if modular.
  
  ### Deployment (CI/CD)
  List core content types and their fields — especially if modular.
  
  ### Serve Method
  SSR, SSG, ISR, SPA — define how content is delivered.
  
  ### Rendering and Navigation
  Describe navigation model: client-side, server-side, hybrid.

## 10. Inspirations
List products, tools, or design systems that inspired your approach. Add screenshots or links if possible.

## 11. Acceptance Criteria
Define measurable outcomes or conditions for each key requirement. These criteria will help validate that the AI-generated or team-produced output meets the intended goal.

## 12. Additional Notes
Include anything that doesn’t fit elsewhere — edge cases, caveats, stakeholder notes, technical unknowns.
