---
title: GreenThumb
description: An intelligent plant care assistant for indoor gardeners
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

Every plant parent's journey starts with love and ends with dead plants. We're here to change that story, one thriving plant at a time.

## Project Name

GreenThumb

## Idea Statement

GreenThumb is an intelligent plant care assistant designed for urban dwellers and houseplant enthusiasts who want to keep their indoor gardens thriving. It addresses the common problem of plant parents killing their plants due to improper care by providing personalized care schedules, plant identification, and troubleshooting guidance. GreenThumb stands out with its AI-powered plant health diagnostics, community plant swapping features, and integration with smart home watering systems.

## Core Purpose

Help plant parents nurture thriving indoor gardens through intelligent care guidance and community support.

# 2. Design Language

Nature doesn't need embellishment - our design embraces organic beauty, natural textures, and the calming presence of greenery in digital form.

## Design Style

Organic Design, Neumorphism

## Design Tone

Natural, Fresh, Nurturing, Peaceful

## Design References

1. (https://www.plantnet.org): Excellent plant identification interface with clear photo capture guidance. Great species database presentation.

2. (https://www.gardenize.com): Beautiful garden journal with photo-centric design. Excellent plant progress tracking.

3. (https://www.florish.app): Clean plant care interface with intuitive watering schedules. Great use of plant illustrations.

## Additional Notes

- Use nature-inspired organic shapes and patterns
- Incorporate plant illustrations and botanical elements
- Ensure high contrast for outdoor use
- Make care actions prominent with large touch targets

# 3. Color Palette

A palette drawn from nature's own canvas - the deep greens of healthy foliage, sunny yellows of growth, and soft purples of blooming flowers.

{
  "primary": {
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
  "secondary": {
    "50": "#fefce8",
    "100": "#fef9c3",
    "200": "#fef08a",
    "300": "#fde047",
    "400": "#facc15",
    "500": "#eab308",
    "600": "#ca8a04",
    "700": "#a16207",
    "800": "#854d0e",
    "900": "#713f12",
    "950": "#422006"
  },
  "tertiary": {
    "50": "#fdf4ff",
    "100": "#fae8ff",
    "200": "#f5d0fe",
    "300": "#f0abfc",
    "400": "#e879f9",
    "500": "#d946ef",
    "600": "#c026d3",
    "700": "#a21caf",
    "800": "#86198f",
    "900": "#701a75",
    "950": "#4a044e"
  }
}

## Dark Mode Support

Light Mode Only (optimized for plant photography)

# 4. Typography

Typography that feels as organic as the plants themselves - elegant serifs for headers like botanical labels, clean sans for care instructions.

## Display Font

Playfair Display

## Body Font

Lato

## Monospace Font

Cousine

## Typescale

Perfect Fourth (1.333)

# 5. Icons

Icons inspired by botanical illustrations - delicate, detailed, and instantly recognizable even to novice plant parents.

## Icon Library

Remix Icons

## Icon Style

Line style with organic curves

# 6. Layout

Mobile-first because plant care happens on the go - checking your plants while at the nursery, getting care tips while repotting, or identifying that mystery plant at a friend's house.

## Responsive Strategy

Mobile-First: Start small, enhance upward

## Additional Notes

- Card-based layout for plant profiles
- Masonry grid for plant gallery
- Bottom sheet for quick actions
- Horizontal scrolling for plant collections

# 7. Inspirations

We studied how botanists catalog plants, how gardeners track growth, and how plant lovers share their passion - then made it accessible to everyone.

1. (https://www.picturethisai.com): AI-powered plant identification with disease diagnosis. Excellent camera interface and results presentation.

2. (https://www.planta.app): Beautiful plant care reminders with weather integration. Great notification system and care tracking.

3. (https://www.smartplantapp.com): IoT sensor integration for plant monitoring. Excellent data visualization for plant health metrics.

4. (https://www.inaturalist.org): Community-driven species identification. Great social features and expert validation.

5. (https://www.leafsnap.com): Visual plant recognition with detailed species information. Beautiful leaf photography guides.

## Additional Notes

Aim for the AI capabilities of PictureThis, the care features of Planta, and the community aspects of iNaturalist.

# 8. User Stories

Real struggles from real plant parents - from serial plant killers trying to keep just one plant alive to collectors managing hundreds of rare species.

- As a plant beginner, I want to identify plants by taking a photo, so that I know exactly what care they need.

- As a busy professional, I want customized watering reminders, so that I never forget to care for my plants.

- As a plant enthusiast, I want to track my plants' growth with photos, so that I can see their progress over time.

- As a struggling plant parent, I want to diagnose plant problems from photos, so that I can save dying plants.

- As a collector, I want to organize my plants by room and care needs, so that I can efficiently manage my collection.

- As a social gardener, I want to share and swap plant cuttings locally, so that I can expand my collection affordably.

- As a data lover, I want to see care statistics and success rates, so that I can improve my plant care skills.

- As a forgetful person, I want location-based reminders, so that I water plants when I'm actually near them.

# 9. Functional Requirements

Features born from watching plant parents struggle - and succeed. Every feature addresses a real problem that leads to plant death or disappointment.

## Must Have Features

- User registration and profile
- Plant identification from photos
- Add plants to personal collection
- Care schedule with reminders (water, fertilize, repot)
- Plant care guides database
- Photo journal for each plant
- Basic problem diagnosis
- Search plants by name or characteristics
- Care history tracking
- Push notifications for care tasks

## Should Have Features

- Weather-based care adjustments
- Community plant swap board
- Plant health scoring
- Barcode scanning for store plants
- Multiple homes/rooms organization
- Care streak gamification
- Export plant collection
- Wish list for future plants
- Local nursery finder
- Seasonal care tips

## Could Have Features

- AR plant placement preview
- IoT sensor integration
- AI chatbot for plant questions
- Time-lapse photo creation
- Plant sitting coordination
- Marketplace for rare plants
- Virtual plant consultations
- Pest identification
- Soil testing integration
- Plant care expense tracking

## Won't Have Features

- E-commerce plant sales
- Professional landscaping services
- Outdoor garden planning
- Agricultural/farming features
- Plant breeding tools
- Pesticide recommendations

# 10. Page Map

Navigation that mirrors the plant care journey - from bringing a new plant home to celebrating years of growth together.

- Landing (/)
- Sign Up (/signup)
- Sign In (/signin)
- Dashboard (/dashboard)
- My Plants (/plants)
- Plant Profile (/plant/:id)
- Add Plant (/plant/new)
- Plant Identifier (/identify)
- Care Calendar (/calendar)
- Plant Health Check (/diagnose)
- Plant Library (/library)
- Plant Detail (/library/:plantId)
- Community Swap (/swap)
- Swap Listing (/swap/:id)
- Photo Journal (/plant/:id/journal)
- Care Guide (/guide/:plantId)
- Notifications (/notifications)
- Settings (/settings)
- Profile (/profile)
- Statistics (/stats)
- Search (/search)
- Help (/help)
- 404 (/404)

# 11. Content Structure

Data models that capture the full lifecycle of plant parenthood - from adoption to propagation, with all the struggles and successes in between.

## Common Content Types

- User
- Media
- Notification
- Comment
- Tag
- Event

## Add Custom Content Types

Plant
- plantId (string, required)
- userId (reference: User)
- nickname (text)
- scientificName (text, required)
- commonName (text)
- location (select: living-room/bedroom/kitchen/bathroom/balcony/office)
- dateAdded (date)
- acquisitionType (select: purchased/propagated/gifted/rescued)
- potSize (text)
- soilType (text)
- sunlightReceived (select: direct/indirect/shade)
- healthScore (number, 0-100)
- lastWatered (datetime)
- lastFertilized (datetime)
- photos (array: Media)
- notes (text)

PlantSpecies
- speciesId (string, required)
- scientificName (text, required)
- commonNames (array: text)
- family (text)
- nativeRegion (text)
- sunlight (select: full/partial/shade)
- waterFrequency (select: daily/weekly/biweekly/monthly)
- humidity (select: low/medium/high)
- temperature (text)
- toxicity (select: safe/toxic-pets/toxic-humans)
- difficulty (select: easy/moderate/hard)
- description (text)
- careGuide (rich text)

CareTask
- taskId (string, required)
- plantId (reference: Plant)
- taskType (select: water/fertilize/repot/prune/rotate/mist)
- dueDate (datetime)
- completed (boolean)
- completedDate (datetime)
- notes (text)
- photoProof (Media)
- frequency (text)

PlantProblem
- problemId (string, required)
- plantId (reference: Plant)
- problemType (select: pest/disease/nutrient/watering/light/other)
- severity (select: mild/moderate/severe)
- identifiedDate (date)
- description (text)
- photos (array: Media)
- treatment (text)
- resolved (boolean)
- resolvedDate (date)

SwapListing
- listingId (string, required)
- userId (reference: User)
- plantSpecies (text)
- listingType (select: offer/wanted)
- description (text)
- photos (array: Media)
- location (text)
- availableUntil (date)
- status (select: active/claimed/completed)

JournalEntry
- entryId (string, required)
- plantId (reference: Plant)
- date (datetime)
- photo (Media, required)
- height (number, cm)
- newGrowth (boolean)
- flowering (boolean)
- notes (text)
- milestones (array: text)

# 12. Tech Stack

Technology choices optimized for handling millions of plant photos, real-time care reminders, and a community of passionate plant parents.

## Framework

React Native with Expo

## UI Library

React Native Elements

## State Management

Redux Toolkit

## Database

Firebase Firestore

## Authentication

Firebase Auth

## Content Management System

Contentful for plant species data

## Hosting

Expo Application Services

## Additional Notes

- TensorFlow Lite for plant identification
- React Native Camera for photo capture
- React Native Push Notifications
- React Native Reanimated for animations
- React Native Image Picker
- React Native Calendars
- Victory Native for charts
- React Native Maps for nursery finder
- AsyncStorage for offline data
- React Native Share for plant sharing
- Expo Sensors for light meter
- React Native Background Fetch for reminders

# 13. Core Components

Components that feel as natural as tending to your plants - smooth interactions, delightful animations, and clear visual feedback for every action.

Action Button, Alert, Avatar, Badge, Bottom Sheet, Button, Calendar, Camera View, Card, Carousel, Chart, Checkbox, Date Picker, Divider, FAB, Filter Pills, Form, Gallery Grid, Header, Icon, Image, Input, List Item, Loading, Map View, Modal, Navigation Tab Bar, Overlay, Progress Circle, Radio, Rating, Search Bar, Segment Control, Select, Slider, Snackbar, Stat Card, Switch, Tag, Text Area, Time Picker, Tooltip

## Additional Components

- Plant Card with Health Indicator
- Care Task Card
- Plant Identification Result Card
- Watering Schedule Timeline
- Plant Growth Chart
- Problem Diagnosis Card
- Swap Listing Card
- Weather Widget
- Plant Gallery Masonry
- Care Streak Badge
- Quick Care Actions Menu
- Species Information Panel
- Photo Comparison Slider
- Plant Collection Stats

# 14. Additional Notes

Critical details that make the difference between a plant thriving and dying - these features were tested with real plant parents in real homes.

- Implement offline mode for core features
- Cache plant database for offline identification
- Use ML Kit for on-device plant recognition
- Add widget support for care reminders
- Implement location-based notifications
- Support image compression for journal photos
- Add backup/restore for plant data
- Implement deep linking for plant sharing
- Support multiple photo angles for identification
- Add seasonal care adjustments
- Implement smart notification grouping
- Support metric and imperial measurements
- Add accessibility labels for plant images
- Optimize battery usage for background tasks
- Target app size under 60MB
- Support image EXIF data for light analysis