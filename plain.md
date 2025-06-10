# PLAIN
This document defines a structured and AI-readable product specification format called **PLAIN (Product Language for AI Notation)**.

It is designed to serve as a common language between human product teams and AI design/code generation tools. By using clearly defined sections, natural language prompts, and modular instructions, PLAIN helps both parties understand the scope, structure, and design intent of a product.

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

🎯 Your ultimate goal is to create a product definition that can be used as a blueprint for generating high-quality design systems, UI components, and frontend code — both by AI tools and design teams.
```

## Idea Statement
Describe the core idea and value proposition of the product in 1–2 short paragraphs. Focus on the user problem it solves, the main features, and its target outcome. Avoid generic phrasing — be specific about the product’s intent.

## Design Language
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

## Target Audience and Personas
Identify the key user types. Describe their goals, pain points, contexts, and motivations. Keep it persona-level, not demographic fluff.

## Functional Requirements
List what the product must do. These are the features — not technical, but functional. Be specific and testable.

## Non-Functional Requirements
Define performance, accessibility, localization, scalability, and other systemic expectations that affect experience but aren’t features.

## User Flows
Describe step-by-step user journeys for key tasks (e.g. “Sign Up”, “Book a Trip”, “Upload a Photo”). Use numbered steps or diagrams.

## User Stories
Define product needs from the user’s perspective in the format:
“As a [persona], I want to [action], so that [outcome].”
Focus on the why, not just the action.

## Page Map
List all pages/screens in the product. Include: page name, URL (if known), type (modal, full-page, popup), and purpose.

## Technical Requirements
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

## Inspirations
List products, tools, or design systems that inspired your approach. Add screenshots or links if possible.

## Acceptance Criteria
Define measurable outcomes or conditions for each key requirement. These criteria will help validate that the AI-generated or team-produced output meets the intended goal.

## Additional Notes
Include anything that doesn’t fit elsewhere — edge cases, caveats, stakeholder notes, technical unknowns.
