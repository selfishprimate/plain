<!--
title: Write your project name.
description: A brief description about your project.
author: Write your full name.
date: YYYY-MM-DD
version: 1.0
projectLink: Link to your AI-generated project or design.
format: PLAIN
plain: https://github.com/selfishprimate/plain
-->

# PLAIN: Product Language for AI Notation

A structured specification format designed to help AI assistants understand and build complete products. PLAIN transforms your ideas into clear, actionable requirements that AI can interpret and implement with precision. From design vision to technical architecture, every aspect of your product is documented in a format optimized for AI comprehension.

## Table of Contents

Navigate quickly to any section of this PLAIN specification. Each section builds upon the previous ones to create a complete product definition.

[🤖 Instructions for AI Coding Assistants](#instructions-for-ai-coding-assistants) • [📋 Project Overview](#1-project-overview) • [🎨 Design Language](#2-design-language) • [🎯 Colors](#3-colors) • [✏️ Typography](#4-typography) • [🔲 Icons](#5-icons) • [📐 Layout](#6-layout) • [✨ Inspirations](#7-inspirations) • [👤 User Stories](#8-user-stories) • [⚙️ Functional Requirements](#9-functional-requirements) • [🗺️ Page Map](#10-page-map) • [📊 Content Structure](#11-content-structure) • [🛠️ Tech Stack](#12-tech-stack) • [🧩 Core Components](#13-core-components) • [📝 Additional Notes](#14-additional-notes)

---

## Instructions for AI Coding Assistants

This document follows the **PLAIN (Product Language for AI Notation)** format—a structured specification system designed to help AI understand and build complete products. PLAIN documents are organized into clear sections covering everything from design vision to technical architecture. Each section contains specific requirements, preferences, and constraints that should be treated as your source of truth.

**How to read this document:** Start by understanding the project metadata in the HTML comment above. Then carefully read this entire "Instructions for AI Coding Assistants" section to understand your role, core principles, implementation approach, and quality standards. After that, work through each numbered section sequentially, as they build upon each other. When you see "Let AI decide for me" in any section, make intelligent choices based on modern best practices and the existing tech stack. Pay special attention to the MoSCoW priorities (Must/Should/Could/Won't) as they define what's essential versus optional.

**Your role:** You are an expert full-stack developer and UI/UX designer with deep knowledge of modern web technologies, design patterns, and user experience principles. **Your task is to generate production-ready, accessible, and performant code that precisely implements every specification in this document.**

**Core Principles**: Use exact technologies, colors (hex codes), fonts, and patterns specified. Implement all Must Have features, all pages, all components. Write accessible (WCAG AA), responsive, performant, well-typed code.

**Implementation Approach**: Read sections in order—start with foundation (overview, design, tech stack), then build features and pages. Use specified technologies exactly. When you see "Let AI Decide", choose modern, well-documented options that fit the stack. If you detect conflicts (e.g., "React + Vue"), pick the most compatible option and document your decision in code. Match design specifications precisely: exact hex codes, specified fonts, responsive strategy. Study Design References and Inspirations to learn patterns (don't copy directly).

**Code Standards**: Write clean, accessible TypeScript code with semantic HTML, ARIA labels, and keyboard navigation support. Maintain WCAG AA contrast ratios (4.5:1 text, 3:1 UI). Include proper form validation with helpful errors. Add loading, empty, and error states for every feature. Optimize images, implement code splitting, and handle errors comprehensively.

**Quality Checklist**: Before completion, verify all Must Have features are built, all pages from Page Map are created, and the app is responsive at all breakpoints with 44×44px minimum touch targets on mobile. Ensure brand colors are exact, fonts are loaded, dark mode is implemented if specified, and there are no crashes with helpful error messages throughout.

## 1. Project Overview

What you're building, who it's for, and the value it delivers.

### Project Name

A clear, memorable name that reflects your product's identity and purpose.

**Example:**

```
Taskly
```

### Idea Statement

Describe your product's essence: what it is, who it serves, and what makes it unique in the market. Write 2-4 sentences covering: What are you building? Who is it for? What problem does it solve? How is it different from existing solutions?

**Example:**

```
Taskly is a minimalist task management app designed for freelancers and remote workers who need to stay organized without complexity. It addresses the common problem of task management tools being either too simple or too complex. Taskly strikes the perfect balance with an intuitive interface that includes smart task categorization, deadline tracking, and priority management.
```

### Core Purpose

The fundamental problem your product solves, distilled into one clear sentence. 

**Example:**

```
Help users stay organized with minimal friction.
```

## 2. Design Language

Establish the visual and emotional foundation that shapes how users perceive and experience your product.

### Design Style

The overarching visual approach that guides all design decisions and creates consistency across your product. See [design style options](options/design-styles.md) for common styles and their characteristics.

**Example:**

```
Brutalism
```

### Design Tone

The emotional qualities users should feel when interacting with your product. Choose up to 4 adjectives. See [design tone options](options/design-tones.md) for common tones and their characteristics.

**Example:**

```
Clean, Professional, Modern, Trustworthy, Friendly, Bold, Calm
```

### Design References

Real-world examples that embody aspects of your desired design direction. For each reference, specify what specific elements inspire you. See [design references](options/design-references.md) for curated examples to study.

```
1. (https://linear.app): Clean, minimal interface with excellent use of typography and subtle animations. Great example of purposeful whitespace and clear visual hierarchy.

2. (https://stripe.com): Professional colors with strong contrast. Documentation-style layouts that balance technical content with visual appeal.
```

### Additional Notes

Any additional context about your design principles, brand constraints, or accessibility considerations.

## 3. Colors

Define your color system including primary, secondary, and optional tertiary colors. Specify hex codes for each or provide a complete shade system. Use https://uicolors.app/ to generate comprehensive color palettes.

**Example:**

```
Simple format:

- Primary: #3B82F6
- Secondary: #8B5CF6
- Tertiary: #EC4899

or JSON format with tints and shades:

{
  "primary": {
    "50": "#f4f7f7",
    "100": "#e2ebeb",
    "200": "#c8d9d9",
    "300": "#a1bdbf",
    "400": "#739b9d",
    "500": "#588082",
    "600": "#4c6b6e",
    "700": "#42595c",
    "800": "#3b4c4f",
    "900": "#354144",
    "950": "#1a2224"
  }
}
```

### Dark Mode Support

Choose your theming strategy based on user needs and brand requirements. **Options:** Both Light and Dark Mode, Dark Mode Only, or Light Mode Only.

**Example:**

```
Dark mode only.
```

## 4. Typography

Define your typography system. Typography affects readability, hierarchy, and the overall personality of your product. See [typography options](options/typography.md) for font combinations and systems.

### Display Font

Typography for headings, titles, and high-impact text. Choose a font that captures your brand's voice.

**Example:**

```
Work Sans
```

### Body Font

The primary typeface for all readable content. Prioritize clarity and legibility across screen sizes.

**Example:**

```
Inter
```

### Monospace Font

Fixed-width font for code snippets, technical data, or numeric displays. Optional unless your product involves code or structured data.

**Example:**

```
Fira Code
```

### Typescale

Define your typescale ratio. A typescale is a mathematical system that creates harmonious font sizes by multiplying a base size by a consistent ratio. Use https://typescale.com/ to preview different ratios and generate your scale. See [type scale options](options/type-scale.md) for common ratios and implementation guidelines.

**Example:**

```
Major Third (1.25)
```

## 5. Icons

Establish a consistent icon system that improves navigation, clarifies actions, and reinforces your visual language. See [icon options](options/icons.md) for popular libraries and their characteristics.

### Icon Library

Choose a comprehensive icon library that matches your design aesthetic and offers the symbols you need.

**Example:**

```
Lucide Icons
```

### Icon Style

The visual treatment applied to all icons. Consistency here creates a cohesive, professional appearance.

**Example:**

```
Outlined
```

## 6. Layout

Define your layout structure and responsive behavior. Layout determines how content is organized and how your product adapts to different screen sizes. See [layout options](options/layout.md) for patterns and responsive strategies.

### Responsive Strategy

Your foundational approach to building layouts that work seamlessly from mobile to desktop.

**Example:**

```
Desktop-First: Start large, simplify downward.
```

### Additional Notes

Document specific layout patterns, accessibility requirements, or technical constraints that shape your structure.

## 7. Inspirations

Curate 3-5 examples that demonstrate specific aspects of great design, functionality, or user experience. For each, describe what specific elements inspire you. See [design references](options/design-references.md) for inspiration.

**Example:**

```
1. (https://notion.so): Flexible workspace with intuitive drag-and-drop interactions. Great example of progressive disclosure and nested content organization.

2. (https://airbnb.com): Beautiful imagery with strong visual hierarchy. Excellent search experience and responsive grid layouts that adapt seamlessly.

3. (https://github.com): Clean code-focused interface with excellent dark mode implementation. Smart use of tabs and clear information architecture.
```

### Additional Notes

Capture the overall mood, feeling, or design philosophy these inspirations represent. Example: "Aim for the simplicity of Apple, the playfulness of Duolingo, and the clarity of Linear."

## 8. User Stories

Write 5-10 stories using the format: "As a **[user type]**, I want to **[action]**, so that **[benefit]**".

**Example:**

```
- As a freelance designer, I want to quickly capture task ideas on my phone when inspiration strikes, so that I don't forget important to-dos when I'm away from my desk.

- As a remote worker, I want to see my tasks organized by priority at a glance, so that I can focus on what matters most without feeling overwhelmed.

- As a busy freelancer, I want to set deadline reminders for my tasks, so that I never miss a client deliverable and maintain my professional reputation.
```

## 9. Functional Requirements

Define your product's capabilities using MoSCoW prioritization to ensure focus on what truly matters for launch.

### Must Have Features

Core functionality required for your product to deliver value. Without these, the product doesn't work.

**Example:**

```
- User registration with email/password
- Create and edit tasks
- Real-time notifications
```

### Should Have Features

Important features that significantly enhance the experience but aren't launch-blockers.

**Example:**

```
- Task filtering by status
- Email reminders
- Profile customization
```

### Could Have Features

Nice-to-have features that add polish or convenience. Consider for post-MVP iterations.

**Example:**

```
- Dark mode toggle
- Keyboard shortcuts
- Export to CSV
```

### Won't Have Features

Features explicitly excluded from this version to maintain focus and manage scope.

**Example:**

```
- Advanced analytics dashboard
- Team collaboration
- Mobile app
```

## 10. Page Map

Document every page and route in your product to establish the complete information architecture and user navigation paths. List all pages including public pages, authenticated areas, settings, admin sections, and utility pages (404, 500, loading). See [page map options](options/page-map.md) for common structures and navigation patterns.

**Example:**

```
- Home (/): Landing page with hero section and key features
- Dashboard (/dashboard): Main dashboard view for authenticated users
- Profile Settings (/settings/profile): User profile editing page
- Not Found (/404): Error page for invalid routes
```

## 11. Content Structure

Define the data models and content types that power your product, establishing how information is organized and related.

### Common Content Types

Select standard content types that apply to your product. These come with predefined fields and relationships. See [content types](options/content-types.md) for detailed structures and field definitions.

**Example:**

```
- Product
- Task
- Event
- Category
```

### Add Custom Content Types

Define custom content types unique to your product's domain, listing all necessary fields and their types.

**Example:**

```
Recipe
- recipeName (text, required)
- description (rich text)
- ingredients (array)
- prepTime (number, minutes)
- difficulty (select: easy/medium/hard)
- author (reference: User)
- images (array: Media)
```

## 12. Tech Stack

Define your complete technical stack: frontend framework, UI library, backend infrastructure, database, authentication, and hosting.

### Framework

Your core frontend framework shapes the entire development experience. Choose based on team expertise, project requirements, and ecosystem.

**Example:**

```
Vite + React
```

### UI Library

Pre-built components that accelerate development and ensure consistency. Consider design flexibility vs speed of implementation.

**Example:**

```
Shadcn UI
```

### State Management

How application data flows and updates across components. Simple apps may not need dedicated state management.

**Example:**

```
Zustand
```

### Database

Choose your data persistence layer. Match the database type (SQL vs NoSQL) to your data structure and query patterns.

**Example:**

```
Supabase
```

### Authentication

Select your user authentication and identity management strategy based on security needs and user experience goals.

**Example:**

```
Firebase Auth
```

### Content Management System

Choose how content will be created, edited, and published. Consider team size, technical expertise, and content update frequency.

**Example:**

```
Markdown Files
```

### Hosting

Determine where your application will be deployed and served to users. Consider performance, cost, and deployment workflow.

**Example:**

```
Netlify
```

### Additional Notes

Document other tech stack choices like styling methodology, build tools, or specific libraries.

**Example:**

```
- Using CSS Modules for component styles
- Vite for fast development
- React Query for server state
- Framer Motion for animations
```

## 13. Core Components

Identify the UI building blocks your product requires. This inventory guides implementation and ensures nothing is overlooked.

**Example:**

```
Accordion, Alert, Avatar, Badge, Breadcrumb, Button, Button Group, Calendar, Card, Carousel, Chart, Pagination, Scroll Area, Textarea, Toast Message, Toggle, Tooltip
```

### Additional Components

Specialized or custom components not covered by standard libraries. These may require custom development.

**Example:**

```
- Rich Text Editor (TipTap)
- Interactive Map (Mapbox)
- Video Player (VideoJS), 
- Kanban Board, 
- Color Picker
```

## 14. Additional Notes

Document important context that doesn't fit other sections: constraints, standards, goals, or questions that need resolution. Capture technical constraints, success metrics, accessibility standards, future considerations, or anything else relevant to development.

**Example:**

```
- Must achieve WCAG AA compliance
- Target < 2s page load time
```