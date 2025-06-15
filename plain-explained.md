# Product Language for AI Notation Explained

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

### Few-shot Examples

The following examples illustrate the expected format and level of detail for an Idea Statement. Each should be written in 2–3 concise paragraphs, clearly describing the product’s purpose, target users, key problems it solves, and how it delivers value.

> **Curato** is a curated web platform designed to help creative professionals discover, explore, and share AI tools tailored to their needs. By browsing through categorized collections, users can access detailed tool profiles, visit official websites, or share tools directly on social media. The platform streamlines tool discovery by combining smart filters, tag-based navigation, and clean UI previews—making it easier than ever to find the right AI tool for any creative workflow. Whether you're a designer looking for image generators or a writer exploring language models, Curato offers a structured and visual way to navigate the AI landscape.

> **Taskly** is a cross-platform task management tool designed for freelancers and remote teams who need a fast and reliable way to organize their workday. The app focuses on simplicity and speed—allowing users to quickly capture tasks, assign deadlines, and mark progress with minimal friction. What sets Taskly apart is its intelligent scheduling assistant, offline syncing, and support for recurring task templates. Whether you're juggling multiple clients or trying to stick to personal deadlines, Taskly reduces the cognitive load of planning by offering clean interfaces, smart reminders, and adaptive daily overviews.

> **Wellnest** is a mobile-first journaling app aimed at young adults navigating stress, decision-making, and personal growth. It offers guided prompts, mood tracking, and daily reflections to help users better understand their mental and emotional state over time. Designed with a calming aesthetic and interaction-focused UI, Wellnest makes self-reflection accessible and rewarding. Features like streak tracking, visual mood summaries, and optional anonymous sharing enable users to stay consistent while building emotional resilience.

## 2. Design Language
The Design Language defines the foundational **values**, **tone**, and **guiding attitudes** of the product’s user experience. It combines abstract principles (such as clarity or simplicity) with emotional cues (such as playful, calming, or serious) to inform every visual and interaction-related decision.

This section is not about specific colors, components, or layout rules—that comes later. Instead, it sets the **philosophical direction** behind the design: how the product should make people feel, how it behaves under pressure, and what it chooses to emphasize or ignore. Both human designers and AI agents use this section to align decisions with the intended personality of the product.

It should include 3–5 principles and a short narrative that conveys the **emotional tone** and **interaction style** of the product.

### Example 1
```
Our design approach is grounded in clarity, calm, and cognitive efficiency.
The interface avoids unnecessary distractions, emphasizes whitespace, and guides the user toward key tasks with minimal friction.

Core principles:
- Show only what matters: every screen should reduce information overload.
- Invisible speed: interactions should feel fast without being flashy.
- Subtle delight: animations and sounds exist only to affirm, never to impress.

Visual tone: calm, mature, confident. The product should feel like a quiet assistant that respects your focus, not an energetic coach demanding attention.
```
### Example 2
```
The product embraces a human-first design mindset, encouraging users to feel safe, accepted, and in control of their emotional journey.
Every interface element is designed to reduce stress and invite self-reflection.

Core principles:
- Soft by default: colors, motion, and typography should feel gentle and supportive.
- Empathy over efficiency: friction is acceptable if it improves emotional clarity.
- Honesty in UI: no dark patterns, no forced engagement, no urgency bias.

Visual tone: warm, empathetic, and intimate—like a well-designed journal that understands you but never judges.
```

## 3. Color
The Color section defines the product’s **visual identity** through a structured palette of colors. This includes **brand colors**, **semantic colors** (like success, warning, danger), backgrounds, and surface tones. It may also include references to light and dark modes, grayscale ranges, and theming strategies.

For AI tools, clear naming conventions (e.g. primary, surface-100, error-light) and logical token groupings are critical to automate and scale consistent UI generation. For humans, this section provides the visual backbone of the product’s mood and branding.

If possible, describe:
	•	The primary/secondary brand palette
	•	Semantic roles (info, success, warning, danger)
	•	Grayscale steps and naming conventions
	•	Mode support (light, dark, auto)
	•	Any unique thematic color behavior (e.g. gradients, transparency, motion-linked color shifts)

### Example 1
SaaS Dashboard (Light/Dark Theme)
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
### Example 2
Mobile Health App (Soft Neutrals, No Dark Mode)
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




## 4. Design System
## 5. Icons
## 6. Typography
## 7. Layout
## 8. Core Components
## 9. Accessibility
## 10. Stylistic References

## 11. Target Audience and Personas

## 12. Functional Requirements

## 13. Non-Functional Requirements

## 14. User Flows

## 15. User Stories

## 16. Page Map

## 17. Technical Requirements

  ### Architecture Pattern
  
  ### State Management
  
  ### Data Flow
  
  ### Technical Stack
  
  ### Authentication Process
  
  ### Route Design
  
  ### API Design
  
  ### Database Design
  
  ### SEO Strategy
  
  ### Content Management Approach
  
  ### Structured Content
  
  ### Deployment (CI/CD)
  
  ### Serve Method
  
  ### Rendering and Navigation

## 18. Inspirations

## 19. Acceptance Criteria

## 20. Additional Notes
