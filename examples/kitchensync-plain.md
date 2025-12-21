---
title: KitchenSync
description: A smart recipe management and meal planning app for home cooks
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

Born from the frustration of juggling cookbooks, screenshots, and handwritten notes while trying to cook dinner. This is the command center for home cooking.

## Project Name

KitchenSync

## Idea Statement

KitchenSync is a smart recipe management and meal planning app designed for home cooks and food enthusiasts who want to organize their culinary life. It solves the problem of scattered recipes across books, websites, and handwritten notes by providing a unified platform with intelligent features. KitchenSync stands out with its recipe import from any source, smart grocery list generation, and adaptive meal planning based on dietary preferences and what's in your pantry.

## Core Purpose

Transform chaotic recipe collection into organized, actionable meal plans with automated shopping lists.

# 2. Design Language

The kitchen is the heart of the home - our design reflects warmth, organization, and the joy of cooking. Clean enough for efficiency, warm enough for comfort.

## Design Style

Material Design 3, Flat Design

## Design Tone

Warm, Inviting, Organized, Fresh

## Design References

1. (https://www.paprika.app): Clean recipe card layouts with excellent information hierarchy. Great example of recipe organization.

2. (https://www.yummly.com): Beautiful food photography integration with smart recipe recommendations. Excellent search and filter UI.

3. (https://cooking.nytimes.com): Editorial-quality design with perfect typography for recipe instructions. Great use of white space.

## Additional Notes

- Use food-inspired warm colors and organic shapes
- Prioritize readability for recipe instructions
- Make cooking mode distraction-free and splash-proof friendly

# 3. Color Palette

A palette inspired by fresh ingredients and warm kitchens - tomato reds, herb greens, and golden yellows that make you hungry just looking at them.

{
  "primary": {
    "50": "#fef2f2",
    "100": "#fee2e2",
    "200": "#fecaca",
    "300": "#fca5a5",
    "400": "#f87171",
    "500": "#ef4444",
    "600": "#dc2626",
    "700": "#b91c1c",
    "800": "#991b1b",
    "900": "#7f1d1d",
    "950": "#450a0a"
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

Light Mode Only (optimized for kitchen use with bright lighting)

# 4. Typography

Typography that's readable even with flour-covered fingers and steam-fogged glasses. Clear hierarchy helps cooks follow recipes without losing their place.

## Display Font

Playfair Display

## Body Font

Source Sans Pro

## Monospace Font

Roboto Mono

## Typescale

Perfect Fourth (1.333)

# 5. Icons

Icons that are instantly recognizable even when you're multitasking between stirring, chopping, and checking the timer.

## Icon Library

Tabler Icons

## Icon Style

Filled with rounded corners

# 6. Layout

Desktop-first because serious meal planning happens on bigger screens, but fully responsive for checking recipes while shopping or cooking.

## Responsive Strategy

Desktop-First: Start large, simplify downward

## Additional Notes

- Recipe cards should be responsive grid that adapts from 4 columns to 1
- Cooking mode should be full-screen with large touch targets
- Implement swipe gestures for recipe steps on mobile

# 7. Inspirations

We studied how professional chefs organize their recipes and how home cooks actually use recipe apps in real kitchens.

1. (https://www.epicurious.com): Excellent recipe discovery with powerful filtering. Great combination of editorial content and functionality.

2. (https://www.bonappetit.com): Beautiful food photography and typography. Perfect balance of content and white space.

3. (https://www.allrecipes.com): Strong community features with ratings and reviews. Excellent recipe scaling calculator.

4. (https://www.seriouseats.com): Science-based cooking with detailed instructions. Great use of process photos and technique videos.

## Additional Notes

Aim for the organization of Paprika, the beauty of Bon Appétit, and the functionality of Yummly.

# 8. User Stories

Real stories from home cooks tired of the recipe chaos - from busy parents planning weekly meals to ambitious cooks building their repertoire.

- As a home cook, I want to import recipes from any website with one click, so that I can quickly build my recipe collection.

- As a meal planner, I want to drag and drop recipes into a weekly calendar, so that I can organize meals for my family efficiently.

- As a busy parent, I want automatic grocery lists from my meal plan, so that I never forget ingredients at the store.

- As a health-conscious eater, I want to filter recipes by dietary restrictions, so that I only see meals I can actually eat.

- As a budget shopper, I want to see recipe costs based on local prices, so that I can plan meals within my budget.

- As a cooking beginner, I want step-by-step photo guides, so that I can follow along without confusion.

- As a recipe collector, I want to organize recipes with tags and collections, so that I can find the perfect dish quickly.

- As a social cook, I want to share recipe collections with friends, so that we can exchange favorite meals.

# 9. Functional Requirements

Features built from observing real cooking workflows - from discovering recipes to cleaning up after dinner. Every feature solves a real kitchen problem.

## Must Have Features

- User registration and profile creation
- Recipe creation, editing, and deletion
- Recipe import from URLs
- Recipe search and filtering
- Ingredient list management
- Cooking instructions with timer integration
- Recipe collections/folders
- Shopping list generation
- Recipe scaling (adjust servings)
- Print-friendly recipe view

## Should Have Features

- Meal planning calendar
- Nutritional information calculation
- Recipe rating and notes
- Pantry inventory tracking
- Unit conversion calculator
- Recipe sharing via link
- Cooking mode (hands-free, screen stays on)
- Recipe duplication
- Multi-language support

## Could Have Features

- Barcode scanning for pantry items
- Voice commands for hands-free cooking
- Recipe video upload
- Social features (follow other cooks)
- Restaurant menu inspiration
- Wine pairing suggestions
- Seasonal recipe recommendations
- Kitchen timer widgets

## Won't Have Features

- Food delivery integration
- Live cooking classes
- Professional chef consultations
- Recipe monetization
- Grocery delivery ordering
- Kitchen appliance IoT control

# 10. Page Map

Navigation designed around the cooking workflow - from inspiration to preparation to cooking to sharing.

- Home (/)
- Sign Up (/signup)
- Sign In (/signin)
- Dashboard (/dashboard)
- Recipe Browse (/recipes)
- Recipe Detail (/recipe/:id)
- Recipe Edit (/recipe/:id/edit)
- Add Recipe (/recipe/new)
- Import Recipe (/import)
- Meal Planner (/planner)
- Shopping List (/shopping)
- Pantry (/pantry)
- Collections (/collections)
- Collection View (/collection/:id)
- Search Results (/search)
- Settings (/settings)
- Profile (/profile)
- Cooking Mode (/cook/:id)
- Print View (/print/:id)
- 404 (/404)

# 11. Content Structure

Data models that capture recipes in all their complexity while keeping things simple for the user. Flexible enough for grandma's vague instructions and precise enough for baking.

## Common Content Types

- User
- Category
- Tag
- Media
- Comment
- Review

## Add Custom Content Types

Recipe
- recipeId (string, required)
- title (text, required)
- description (text)
- prepTime (number, minutes)
- cookTime (number, minutes)
- totalTime (number, computed)
- servings (number)
- difficulty (select: easy/medium/hard)
- cuisine (text)
- course (select: appetizer/main/dessert/snack/breakfast)
- author (reference: User)
- images (array: Media)
- sourceUrl (text)
- dateCreated (datetime)
- lastModified (datetime)

Ingredient
- ingredientId (string, required)
- recipeId (reference: Recipe)
- name (text, required)
- quantity (number)
- unit (text)
- notes (text)
- isOptional (boolean)
- category (select: produce/protein/dairy/grain/spice/other)

Instruction
- instructionId (string, required)
- recipeId (reference: Recipe)
- stepNumber (number)
- text (text, required)
- duration (number, minutes)
- temperature (text)
- image (Media)
- tips (text)

MealPlan
- planId (string, required)
- userId (reference: User)
- date (date)
- mealType (select: breakfast/lunch/dinner/snack)
- recipe (reference: Recipe)
- servingsPlanned (number)
- notes (text)

ShoppingItem
- itemId (string, required)
- userId (reference: User)
- ingredientName (text)
- quantity (number)
- unit (text)
- recipeSource (reference: Recipe)
- isPurchased (boolean)
- category (text)
- addedDate (datetime)

Collection
- collectionId (string, required)
- userId (reference: User)
- name (text, required)
- description (text)
- isPublic (boolean)
- recipes (array: Recipe)
- coverImage (Media)

# 12. Tech Stack

Reliable, modern technologies that won't let you down when you're halfway through cooking dinner for eight.

## Framework

Next.js 14 with TypeScript

## UI Library

Mantine UI

## State Management

Redux Toolkit with RTK Query

## Database

PostgreSQL with Prisma ORM

## Authentication

NextAuth.js with JWT

## Content Management System

Custom admin panel

## Hosting

Vercel with Vercel Postgres

## Additional Notes

- Using React Hook Form for complex recipe forms
- Fuse.js for client-side fuzzy search
- Sharp for image optimization
- React Beautiful DnD for meal planning drag-drop
- DayJS for date handling
- Recharts for nutritional data visualization
- React-to-print for print views

# 13. Core Components

Components designed for the kitchen environment - large touch targets for messy fingers, clear visual hierarchy for quick scanning, and smooth interactions even on older devices.

Accordion, Alert, Autocomplete, Avatar, Badge, Button, Card, Carousel, Checkbox, Date Picker, Dialog, Drawer, Dropdown, File Upload, Grid, Input, List, Loading Spinner, Modal, Navigation, Pagination, Progress Bar, Radio Group, Rating, Search Bar, Select, Skeleton, Slider, Switch, Tabs, Tag, Textarea, Timeline, Toast, Tooltip

## Additional Components

- Recipe Card with hover effects
- Ingredient List with checkboxes
- Nutrition Label
- Timer Component
- Serving Size Adjuster
- Recipe Import Modal
- Meal Calendar Grid
- Shopping List Item
- Recipe Step Carousel
- Cooking Mode Interface
- Filter Sidebar
- Recipe Quick View

# 14. Additional Notes

Essential features based on real kitchen testing - these details make the difference between an app that gets used and one that gets deleted.

- Implement recipe web scraping with schema.org/Recipe support
- Support imperial and metric unit systems with conversion
- Add keyboard shortcuts for common actions (Cmd+N for new recipe)
- Implement auto-save for recipe editing
- Support bulk actions (delete multiple recipes)
- Add recipe versioning/history
- Implement smart grocery categorization
- Cache recipes for offline viewing
- Support recipe export to PDF and JSON
- Add OpenGraph tags for recipe sharing
- Implement recipe duplicate detection
- Target 95+ Lighthouse performance score
- Support high-resolution food photography (WebP format)