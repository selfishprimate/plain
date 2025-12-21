---
title: StudyBuddy
description: A collaborative learning platform for students and study groups
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

StudyBuddy

## Idea Statement

StudyBuddy is a collaborative learning platform designed for high school and college students who learn better together. It addresses the isolation and inefficiency of solo studying by creating virtual study rooms where students can share notes, work through problems together, and keep each other accountable. StudyBuddy stands out with its Pomodoro-based study sessions, AI-powered flashcard generation, and peer explanation features that turn studying into an engaging social experience.

## Core Purpose

Transform solitary studying into collaborative learning experiences that boost retention and motivation.

# 2. Design Language

## Design Style

Material Design, Glassmorphism

## Design Tone

Energetic, Modern, Academic, Collaborative

## Design References

1. (https://www.notion.so): Clean workspace organization with excellent note-taking capabilities. Great collaborative features.

2. (https://discord.com): Excellent room-based communication with voice and screen sharing. Strong community feel.

3. (https://quizlet.com): Engaging study tools with gamification. Great flashcard and quiz interfaces.

## Additional Notes

- Use vibrant but not distracting colors
- Incorporate achievement badges and progress indicators
- Ensure readability for long study sessions
- Make collaboration features prominent and intuitive

# 3. Color Palette

{
  "primary": {
    "50": "#eff6ff",
    "100": "#dbeafe",
    "200": "#bfdbfe",
    "300": "#93c5fd",
    "400": "#60a5fa",
    "500": "#3b82f6",
    "600": "#2563eb",
    "700": "#1d4ed8",
    "800": "#1e40af",
    "900": "#1e3a8a",
    "950": "#172554"
  },
  "secondary": {
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
  },
  "tertiary": {
    "50": "#fef3c7",
    "100": "#fde68a",
    "200": "#fcd34d",
    "300": "#fbbf24",
    "400": "#f59e0b",
    "500": "#d97706",
    "600": "#b45309",
    "700": "#92400e",
    "800": "#78350f",
    "900": "#451a03",
    "950": "#281002"
  }
}

## Dark Mode Support

Both Light and Dark Mode with system preference detection

# 4. Typography

## Display Font

Poppins

## Body Font

Inter

## Monospace Font

JetBrains Mono

## Typescale

Minor Third (1.2)

# 5. Icons

## Icon Library

Heroicons

## Icon Style

Solid with rounded corners

# 6. Layout

## Responsive Strategy

Desktop-First: Start large, simplify downward

## Additional Notes

- Split-screen layout for video chat and shared workspace
- Collapsible sidebars for maximum study space
- Floating video bubbles for study room participants
- Responsive grid for study materials and resources

# 7. Inspirations

1. (https://www.figma.com): Real-time collaboration with cursor tracking. Excellent multiplayer editing experience.

2. (https://www.miro.com): Infinite canvas for visual collaboration. Great whiteboard and sticky note features.

3. (https://www.kahoot.com): Gamified learning with competitive elements. Engaging quiz interfaces.

4. (https://www.focusmate.com): Virtual co-working with accountability partners. Simple but effective video presence.

5. (https://www.remnote.com): Spaced repetition integrated with note-taking. Smart learning algorithms.

## Additional Notes

Aim for the collaboration of Figma, the engagement of Kahoot, and the focus features of Focusmate.

# 8. User Stories

- As a college student, I want to create study rooms for specific courses, so that I can collaborate with classmates on assignments and exam prep.

- As a study group member, I want to share my screen and annotate documents, so that I can explain concepts to my peers effectively.

- As a visual learner, I want to use a shared whiteboard, so that I can draw diagrams and work through problems collaboratively.

- As a procrastinator, I want Pomodoro timers with group accountability, so that I stay focused during study sessions.

- As a note-taker, I want to collaboratively create and share study guides, so that we can combine our knowledge efficiently.

- As an exam prepper, I want AI-generated flashcards from my notes, so that I can review material quickly and effectively.

- As a night owl, I want to find study partners in my timezone, so that I'm not studying alone at odd hours.

- As a competitive learner, I want study streaks and leaderboards, so that I stay motivated through gamification.

# 9. Functional Requirements

## Must Have Features

- User registration and profiles
- Create and join study rooms
- Real-time text chat
- Video/audio calling
- Screen sharing
- Shared document editing
- Flashcard creation and review
- Pomodoro timer with breaks
- File upload and sharing
- Study session history
- Basic note-taking

## Should Have Features

- Collaborative whiteboard
- AI flashcard generation from notes
- Study streak tracking
- Calendar integration
- Quiz creation and sharing
- Study group management
- Progress analytics
- Mobile app
- Notification system
- Study room scheduling
- Subject categorization

## Could Have Features

- AI study buddy (chatbot tutor)
- Handwriting recognition
- Voice notes transcription
- Integration with learning platforms
- Study music/ambient sounds
- Virtual backgrounds
- Emoji reactions
- Study session recording
- Peer tutoring marketplace
- Achievement badges
- Study challenges

## Won't Have Features

- Proctored exams
- Official academic credits
- Professional tutoring services
- Homework solutions database
- Plagiarism checking
- Grade tracking from schools
- Parent monitoring features

# 10. Page Map

- Landing (/)
- Sign Up (/signup)
- Sign In (/signin)
- Dashboard (/dashboard)
- Study Rooms (/rooms)
- Create Room (/room/new)
- Study Room (/room/:id)
- My Notes (/notes)
- Note Editor (/note/:id)
- Flashcards (/flashcards)
- Flashcard Set (/flashcards/:setId)
- Study Session (/study/:roomId)
- Whiteboard (/whiteboard/:roomId)
- Calendar (/calendar)
- Study Groups (/groups)
- Group Detail (/group/:id)
- Profile (/profile/:userId)
- Settings (/settings)
- Analytics (/analytics)
- Search (/search)
- Help (/help)
- 404 (/404)

# 11. Content Structure

## Common Content Types

- User
- Event
- Comment
- Tag
- Media
- Notification
- Message
- Document

## Add Custom Content Types

StudyRoom
- roomId (string, required)
- name (text, required)
- subject (text)
- description (text)
- creatorId (reference: User)
- participants (array: User)
- maxParticipants (number)
- isPublic (boolean)
- password (text)
- startTime (datetime)
- endTime (datetime)
- resources (array: Document)
- tags (array: Tag)

StudySession
- sessionId (string, required)
- roomId (reference: StudyRoom)
- participants (array: User)
- startTime (datetime)
- endTime (datetime)
- pomodoroCount (number)
- notes (array: Note)
- recordings (array: Media)

Note
- noteId (string, required)
- authorId (reference: User)
- title (text, required)
- content (rich text)
- subject (text)
- isPublic (boolean)
- collaborators (array: User)
- lastModified (datetime)
- tags (array: Tag)
- attachments (array: Media)

FlashcardSet
- setId (string, required)
- creatorId (reference: User)
- title (text, required)
- description (text)
- subject (text)
- cards (array: Flashcard)
- isPublic (boolean)
- difficulty (select: easy/medium/hard)
- studyCount (number)

Flashcard
- cardId (string, required)
- setId (reference: FlashcardSet)
- front (text, required)
- back (text, required)
- image (Media)
- hint (text)
- lastReviewed (datetime)
- correctCount (number)
- incorrectCount (number)

StudyGroup
- groupId (string, required)
- name (text, required)
- description (text)
- subject (text)
- adminId (reference: User)
- members (array: User)
- isPublic (boolean)
- joinCode (text)
- schedule (array: Event)
- resources (array: Document)

UserProgress
- userId (reference: User)
- studyStreak (number)
- totalStudyMinutes (number)
- flashcardsReviewed (number)
- pomodorosCompleted (number)
- points (number)
- level (number)
- achievements (array: Achievement)

# 12. Tech Stack

## Framework

Next.js 14 with TypeScript

## UI Library

Chakra UI

## State Management

Valtio with React Query

## Database

MongoDB with Prisma

## Authentication

Auth0

## Content Management System

Sanity for study resources

## Hosting

Vercel

## Additional Notes

- Socket.io for real-time collaboration
- WebRTC for video/audio calls
- Agora for screen sharing
- Excalidraw for whiteboard
- Monaco Editor for code collaboration
- React DnD for drag-and-drop
- FullCalendar for scheduling
- Chart.js for analytics
- react-markdown for note rendering
- Workbox for PWA features
- Algolia for search

# 13. Core Components

Accordion, Alert, Avatar, Avatar Group, Badge, Breadcrumb, Button, Card, Checkbox, Counter, Date Picker, Drawer, Dropdown, Form, Grid, Icon Button, Input, List, Loading, Menu, Modal, Navigation, Pagination, Popover, Progress Bar, Radio Group, Search Bar, Select, Skeleton, Slider, Spinner, Stat, Switch, Table, Tabs, Tag, Text Editor, Time Picker, Toast, Tooltip, Upload

## Additional Components

- Video Grid Layout
- Pomodoro Timer Display
- Flashcard Flip Animation
- Study Room Card
- Whiteboard Canvas
- Chat Message Bubble
- Study Streak Calendar
- Achievement Badge
- Screen Share Viewer
- Note Card with Preview
- Quiz Question Card
- Study Analytics Chart
- Participant Status Indicator
- Resource Library Grid

# 14. Additional Notes

- Implement WebRTC fallback for poor connections
- Add offline mode for flashcard review
- Support latex/math equation rendering
- Implement auto-save for all documents
- Add keyboard shortcuts for power users
- Support multiple language study tools
- Implement anti-cheating for quizzes
- Add bandwidth optimization for video
- Support file formats: PDF, DOCX, PPTX
- Implement smart notification batching
- Add study session analytics export
- Support SSO for educational institutions
- Implement FERPA compliance
- Add accessibility features for diverse learners
- Target Core Web Vitals scores: LCP < 2.5s, FID < 100ms, CLS < 0.1