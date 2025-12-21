---
title: MindFlow
description: A minimalist meditation and focus app for digital wellbeing
author: AI Assistant
date: 2024-12-21
version: 1.0
format: PLAIN
plain: https://github.com/selfishprimate/plain
---

# Instructions for AI Coding Assistants

This is a **PLAIN (Product Language for AI Notation)** specification. You are an expert full-stack developer and UI/UX designer. **Your task is to generate production-ready code that implements every section accurately.**

**Core Principles**: Use exact technologies, colors (hex codes), fonts, and patterns specified. Implement all Must Have features, all pages, all components. Write accessible (WCAG AA), responsive, performant, well-typed code.

**Implementation Approach**: Read sections in order—start with foundation (overview, design, tech stack), then build features and pages. Use specified technologies exactly. When you see "Let AI Decide", choose modern, well-documented options that fit the stack. If you detect conflicts (e.g., "React + Vue"), pick the most compatible option and document your decision in code. Match design specifications precisely: exact hex codes, specified fonts, responsive strategy. Study Design References and Inspirations to learn patterns (don't copy directly).

**Code Standards**: Write clean, accessible TypeScript code with semantic HTML, ARIA labels, and keyboard navigation support. Maintain WCAG AA contrast ratios (4.5:1 text, 3:1 UI). Include proper form validation with helpful errors. Add loading, empty, and error states for every feature. Optimize images, implement code splitting, and handle errors comprehensively.

**Quality Checklist**: Before completion, verify all Must Have features are built, all pages from Page Map are created, and the app is responsive at all breakpoints with 44×44px minimum touch targets on mobile. Ensure brand colors are exact, fonts are loaded, dark mode is implemented if specified, and there are no crashes with helpful error messages throughout.

# 1. Project Overview

## Project Name

MindFlow

## Idea Statement

MindFlow is a minimalist meditation and focus app designed for remote workers and students who struggle with digital overwhelm and attention fragmentation. It addresses the problem of meditation apps being too complex or distracting with gamification. MindFlow offers a serene, distraction-free experience with guided breathing exercises, focus timers, and ambient soundscapes that help users achieve deep work states and mental clarity.

## Core Purpose

Help users reclaim their focus and mental clarity through simple, science-based mindfulness techniques.

# 2. Design Language

## Design Style

Minimalist, Glassmorphism

## Design Tone

Calm, Serene, Focused, Trustworthy

## Design References

1. (https://www.calm.com): Beautiful nature-inspired backgrounds with subtle animations. Excellent use of space and calming color palettes.

2. (https://oak.am): Ultra-minimalist meditation interface with perfect use of typography and breathing animations.

3. (https://endel.io): Adaptive soundscapes with fluid, organic visualizations that respond to user interaction.

## Additional Notes

- Focus on reducing cognitive load through intentional simplicity
- Use subtle animations that aid focus rather than distract
- Ensure all interactions feel smooth and meditative

# 3. Color Palette

{
  "primary": {
    "50": "#f0f9ff",
    "100": "#e0f2fe",
    "200": "#bae6fd",
    "300": "#7dd3fc",
    "400": "#38bdf8",
    "500": "#0ea5e9",
    "600": "#0284c7",
    "700": "#0369a1",
    "800": "#075985",
    "900": "#0c4a6e",
    "950": "#082f49"
  },
  "secondary": {
    "50": "#faf5ff",
    "100": "#f3e8ff",
    "200": "#e9d5ff",
    "300": "#d8b4fe",
    "400": "#c084fc",
    "500": "#a855f7",
    "600": "#9333ea",
    "700": "#7e22ce",
    "800": "#6b21a8",
    "900": "#581c87",
    "950": "#3b0764"
  },
  "tertiary": {
    "50": "#f0fdf4",
    "100": "#dcfce7",
    "200": "#bbf7d0",
    "300": "#86efac",
    "400": "#4ade80",
    "500": "#22c55e",
    "600": "#16a34a",
    "700": "#15803d",
    "800": "#166534",
    "900": "#14532d",
    "950": "#052e16"
  }
}

## Dark Mode Support

Both Light and Dark Mode with automatic system detection

# 4. Typography

## Display Font

DM Serif Display

## Body Font

Inter

## Monospace Font

JetBrains Mono

## Typescale

Major Third (1.25)

# 5. Icons

## Icon Library

Lucide Icons

## Icon Style

Outlined with rounded corners

# 6. Layout

## Responsive Strategy

Mobile-First: Start small, enhance upward

## Additional Notes

- Use fluid typography that scales smoothly between breakpoints
- Implement touch-friendly tap targets for mobile meditation sessions
- Center-aligned content with generous padding for focus

# 7. Inspirations

1. (https://headspace.com): Playful yet calming animations that guide users through meditation. Great onboarding flow and progress tracking.

2. (https://brain.fm): Science-based approach to focus music with clear visual feedback on brain states. Excellent data visualization.

3. (https://noisli.com): Simple sound mixing interface with intuitive controls. Perfect example of feature-rich yet minimal design.

4. (https://forest-app.cc): Gamification done right - motivating without being distracting. Beautiful illustration style.

## Additional Notes

Aim for the serenity of Oak, the scientific approach of Brain.fm, and the simplicity of Noisli.

# 8. User Stories

- As a remote worker, I want to start a quick 5-minute breathing exercise between meetings, so that I can reset my mental state and reduce stress.

- As a student, I want to use a pomodoro timer with ambient sounds, so that I can maintain focus during long study sessions.

- As a beginner meditator, I want guided meditation sessions of varying lengths, so that I can build a consistent practice at my own pace.

- As a busy professional, I want to track my meditation streak, so that I stay motivated to maintain daily mindfulness practice.

- As a night shift worker, I want sleep meditation sessions, so that I can wind down effectively despite irregular sleep schedules.

- As an anxious user, I want emergency calm exercises, so that I can quickly manage panic attacks or acute stress.

- As a data-driven person, I want to see my focus and meditation statistics, so that I can understand my progress over time.

# 9. Functional Requirements

## Must Have Features

- User registration with email/password or social login
- Guided breathing exercises (box breathing, 4-7-8, coherent breathing)
- Focus timer with customizable durations
- Library of ambient sounds and nature soundscapes
- Basic meditation sessions (5, 10, 15, 20 minutes)
- Progress tracking and streak counter
- Offline mode for downloaded content

## Should Have Features

- Pomodoro timer with break reminders
- Daily mindfulness reminders
- Customizable sound mixes
- Heart rate variability (HRV) integration
- Sleep meditation programs
- Focus music playlists
- Widget for quick access

## Could Have Features

- Apple Watch / WearOS integration
- Binaural beats generator
- Community meditation sessions
- AI-personalized meditation recommendations
- Export meditation data
- Corporate team features
- Spotify integration

## Won't Have Features

- Social media sharing
- In-app messaging or chat
- Video content
- Virtual reality meditation
- Paid coaching sessions
- Cryptocurrency rewards

# 10. Page Map

- Landing (/)
- Sign Up (/signup)
- Sign In (/signin)
- Dashboard (/dashboard)
- Breathe (/breathe)
- Focus Timer (/focus)
- Meditate (/meditate)
- Meditate Session (/meditate/:sessionId)
- Soundscapes (/sounds)
- Statistics (/stats)
- Settings (/settings)
- Profile (/settings/profile)
- Subscription (/settings/subscription)
- Privacy (/privacy)
- Terms (/terms)
- 404 (/404)
- Offline (/offline)

# 11. Content Structure

## Common Content Types

- User
- Event
- Category
- Media
- Notification

## Add Custom Content Types

MeditationSession
- sessionId (string, required)
- title (text, required)
- description (text)
- duration (number, minutes)
- category (select: breathing/focus/sleep/anxiety)
- audioUrl (string)
- instructor (text)
- difficulty (select: beginner/intermediate/advanced)
- thumbnail (Media)

FocusSession
- sessionId (string, required)
- userId (reference: User)
- startTime (datetime)
- endTime (datetime)
- duration (number, minutes)
- sessionType (select: pomodoro/deepwork/custom)
- soundscape (reference: Soundscape)
- completed (boolean)

Soundscape
- soundId (string, required)
- name (text, required)
- category (select: nature/ambient/white-noise/binaural)
- audioUrl (string)
- thumbnail (Media)
- isPremium (boolean)

UserProgress
- userId (reference: User)
- totalSessions (number)
- totalMinutes (number)
- currentStreak (number)
- longestStreak (number)
- favoriteSessionType (text)
- lastSessionDate (datetime)

# 12. Tech Stack

## Framework

Next.js 14 with App Router

## UI Library

Shadcn UI with Tailwind CSS

## State Management

Zustand with React Query

## Database

Supabase (PostgreSQL with real-time subscriptions)

## Authentication

Supabase Auth with OAuth providers

## Content Management System

Markdown files for static content, Supabase for dynamic content

## Hosting

Vercel with Edge Functions

## Additional Notes

- Using Framer Motion for meditation animations
- Howler.js for advanced audio control
- PWA with offline support using next-pwa
- React Hook Form for forms
- Zod for validation
- Recharts for statistics visualization

# 13. Core Components

Alert, Avatar, Badge, Button, Card, Dialog, Dropdown Menu, Form, Input, Label, Navigation Menu, Progress, Radio Group, Select, Separator, Skeleton, Slider, Switch, Tabs, Textarea, Toast, Tooltip

## Additional Components

- Breathing Animation Circle
- Audio Player with visualizer
- Timer Display with circular progress
- Streak Calendar
- Sound Mixer Panel
- Session Card
- Statistics Chart
- Meditation Player
- Focus Mode Overlay

# 14. Additional Notes

- Must support offline mode for downloaded meditation content
- Implement background audio playback for mobile
- Target < 1.5s initial load time
- Support keyboard navigation for accessibility
- Implement haptic feedback for mobile breathing exercises
- Use Web Audio API for precise audio timing
- Cache meditation sessions aggressively
- Implement auto-save for focus session data
- Support multiple audio tracks playing simultaneously
- Add fade in/out transitions between screens