---
title: PetPal
description: A comprehensive pet care tracker for devoted pet parents
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

This section defines the foundation of what we're building and why it matters.

## Project Name

PetPal

## Idea Statement

PetPal is a comprehensive pet care management app designed for devoted pet parents who want to provide the best care for their furry family members. It addresses the challenge of tracking multiple aspects of pet care across veterinary visits, medications, grooming, and daily activities. PetPal stands out with its family sharing features, emergency vet locator, and intelligent reminders that adapt to each pet's unique needs and schedule.

## Core Purpose

Simplify pet care management while ensuring no important health task or appointment is ever missed.

# 2. Design Language

The visual and emotional framework that will shape every pixel of our app. These choices will create the personality users connect with.

## Design Style

Neumorphism, Flat Design

## Design Tone

Playful, Caring, Reliable, Friendly

## Design References

1. (https://www.rover.com): Friendly and approachable pet care interface with great use of pet photography. Excellent trust signals.

2. (https://www.pawtrack.com): Clean tracking interface with clear data visualization. Great mobile experience.

3. (https://www.petcoach.co): Professional yet warm design for pet health information. Good balance of medical and friendly.

## Additional Notes

- Use soft, rounded corners throughout for a friendly feel
- Incorporate playful micro-interactions (paw prints, tail wags)
- Ensure high contrast for outdoor mobile use
- Make emergency features instantly accessible

# 3. Color Palette

Our color system needs to be warm and inviting while maintaining professionalism for health-related features. These colors will create emotional connections with pet parents.

{
  "primary": {
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
  },
  "secondary": {
    "50": "#ede9fe",
    "100": "#ddd6fe",
    "200": "#c4b5fd",
    "300": "#a78bfa",
    "400": "#8b5cf6",
    "500": "#7c3aed",
    "600": "#6d28d9",
    "700": "#5b21b6",
    "800": "#4c1d95",
    "900": "#3b167f",
    "950": "#2e115f"
  },
  "tertiary": {
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
  }
}

## Dark Mode Support

Both Light and Dark Mode

# 4. Typography

Font choices that balance playfulness with readability, especially important for medication dosages and medical records where clarity is critical.

## Display Font

Fredoka One

## Body Font

Nunito

## Monospace Font

Space Mono

## Typescale

Major Second (1.125)

# 5. Icons

Icons need to be instantly recognizable at small sizes, especially for quick actions like marking medications as given or logging activities.

## Icon Library

Phosphor Icons

## Icon Style

Duotone with playful colors

# 6. Layout

Mobile-first is essential since pet parents often need to access the app while at the vet, during walks, or with hands full managing their pets.

## Responsive Strategy

Mobile-First: Start small, enhance upward

## Additional Notes

- Bottom navigation bar for mobile with 5 main sections
- Floating action button for quick task addition
- Card-based layout for pet profiles
- Swipeable cards for multiple pets

# 7. Inspirations

Learning from the best in pet care and health tracking to create something even better for our users.

1. (https://www.11pets.com): Comprehensive pet care tracking with excellent calendar integration. Great reminder system.

2. (https://www.buddyapp.com): Beautiful pet profiles with timeline-based activity tracking. Excellent photo management.

3. (https://www.fitbark.com): Activity tracking with engaging data visualizations. Great gamification elements.

4. (https://www.petfirst.com): Clean insurance and health tracking interface. Professional medical record keeping.

## Additional Notes

Aim for the comprehensiveness of 11pets, the visual appeal of Buddy, and the data clarity of Fitbark.

# 8. User Stories

Real scenarios from pet parents that drive every feature decision. These aren't just features - they're solutions to real daily challenges.

- As a multi-pet owner, I want to manage all my pets' profiles in one place, so that I can track each pet's unique needs efficiently.

- As a concerned pet parent, I want medication reminders with dosage information, so that I never miss giving my pet their important medications.

- As a busy professional, I want to share pet care responsibilities with family members, so that everyone knows who's handling what tasks.

- As a new pet owner, I want vaccination and checkup schedules, so that I keep my pet healthy and up-to-date on preventive care.

- As an emergency responder, I want quick access to my pet's medical history and vet contacts, so that I can act fast in emergencies.

- As a pet parent, I want to track my pet's weight and diet changes, so that I can maintain their optimal health.

- As a traveling owner, I want to find nearby emergency vets and pet services, so that I'm prepared anywhere I go.

- As a responsible owner, I want expense tracking for pet care, so that I can budget effectively for my pet's needs.

# 9. Functional Requirements

Prioritized features based on extensive user research and feedback from pet parents. Must-haves address immediate pain points, while future features enhance the experience.

## Must Have Features

- User registration and authentication
- Multiple pet profiles with photos
- Vaccination record tracking
- Medication reminders and tracking
- Vet appointment scheduling and reminders
- Emergency vet contact storage
- Weight and growth tracking
- Medical history documentation
- Photo gallery for each pet
- Basic reminder notifications

## Should Have Features

- Family member sharing and permissions
- Expense tracking and budgeting
- Food and diet tracking
- Exercise and activity logging
- Grooming schedule management
- Document storage (insurance, records)
- Vet visit notes and summaries
- Symptom checker
- Pet birthday reminders
- Export medical records as PDF

## Could Have Features

- GPS pet tracking integration
- Social features (pet playdates)
- Breed-specific care tips
- Pet sitter mode
- Video storage for behaviors
- Integration with vet clinics
- Pet insurance management
- Training progress tracking
- QR code pet tags
- Weather-based activity suggestions

## Won't Have Features

- Veterinary telemedicine
- Pet breeding management
- Pet marketplace or adoption
- Real-time health monitoring devices
- Professional training courses
- Pet dating or mating services

# 10. Page Map

Every screen carefully planned to ensure smooth navigation and quick access to critical features, especially emergency information.

- Landing (/)
- Sign Up (/signup)
- Sign In (/signin)
- Dashboard (/dashboard)
- Pet List (/pets)
- Pet Profile (/pet/:id)
- Add Pet (/pet/new)
- Edit Pet (/pet/:id/edit)
- Health Records (/pet/:id/health)
- Medications (/pet/:id/medications)
- Appointments (/appointments)
- Add Appointment (/appointment/new)
- Reminders (/reminders)
- Emergency Contacts (/emergency)
- Find Vet (/find-vet)
- Photo Gallery (/pet/:id/photos)
- Family Members (/family)
- Expenses (/expenses)
- Settings (/settings)
- Profile (/profile)
- Export Records (/export)
- Help (/help)
- 404 (/404)

# 11. Content Structure

Data models designed to capture everything important about your pet's health and care, with flexibility for different types of pets and care routines.

## Common Content Types

- User
- Event
- Media
- Notification
- Document

## Add Custom Content Types

Pet
- petId (string, required)
- ownerId (reference: User)
- name (text, required)
- species (select: dog/cat/bird/rabbit/other)
- breed (text)
- birthDate (date)
- gender (select: male/female)
- isNeutered (boolean)
- microchipId (text)
- weight (number, kg)
- color (text)
- profilePhoto (Media)
- notes (text)

HealthRecord
- recordId (string, required)
- petId (reference: Pet)
- recordType (select: vaccination/checkup/surgery/illness/injury)
- date (datetime)
- vetClinic (reference: VetClinic)
- veterinarian (text)
- diagnosis (text)
- treatment (text)
- followUpDate (date)
- documents (array: Document)
- cost (number)

Medication
- medicationId (string, required)
- petId (reference: Pet)
- name (text, required)
- dosage (text)
- frequency (text)
- startDate (date)
- endDate (date)
- prescribedBy (text)
- reason (text)
- reminders (array: Reminder)
- refillDate (date)

Appointment
- appointmentId (string, required)
- petId (reference: Pet)
- type (select: checkup/vaccination/grooming/surgery/other)
- date (datetime)
- vetClinic (reference: VetClinic)
- reason (text)
- notes (text)
- reminderSet (boolean)
- status (select: scheduled/completed/cancelled)

VetClinic
- clinicId (string, required)
- name (text, required)
- address (text)
- phone (text)
- email (text)
- emergencyPhone (text)
- hours (text)
- isEmergency (boolean)
- latitude (number)
- longitude (number)

FamilyMember
- memberId (string, required)
- userId (reference: User)
- petIds (array: Pet)
- permissions (select: view/edit/admin)
- relationship (text)

Expense
- expenseId (string, required)
- petId (reference: Pet)
- category (select: food/medical/grooming/toys/other)
- amount (number)
- date (date)
- vendor (text)
- description (text)
- receipt (Document)

# 12. Tech Stack

Technology choices optimized for mobile performance and offline reliability, because pet care doesn't stop when you lose signal.

## Framework

React Native with Expo

## UI Library

NativeBase

## State Management

MobX with MobX State Tree

## Database

Firebase Firestore

## Authentication

Firebase Auth

## Content Management System

Firebase Storage for media

## Hosting

Expo Application Services (EAS)

## Additional Notes

- React Native Reanimated for animations
- React Native Maps for vet locator
- React Native Push Notifications
- React Native Camera for photo capture
- React Native Calendar for scheduling
- React Native Share for record sharing
- AsyncStorage for offline data
- React Native PDF for document viewing
- Expo Location for GPS features

# 13. Core Components

Building blocks designed for quick interactions and clear information display, crucial when you're juggling a pet at the vet's office.

Action Sheet, Alert, Avatar, Badge, Button, Card, Checkbox, Date Picker, Drawer, FAB (Floating Action Button), Form, Icon Button, Image Gallery, Input, List, Loading, Modal, Navigation Bar, Progress, Radio, Search Bar, Select, Slider, Spinner, Switch, Tabs, Tag, Text Area, Time Picker, Toast

## Additional Components

- Pet Profile Card
- Health Timeline
- Medication Reminder Card
- Appointment Card
- Weight Chart
- Vaccine Schedule Grid
- Emergency Contact Card
- Photo Carousel
- Expense Summary Chart
- Pet Switcher (for multi-pet households)
- Quick Action Menu
- Pet Age Calculator
- Breed Information Panel

# 14. Additional Notes

Critical implementation details to ensure the app works reliably in real-world pet care situations, from vet visits to park adventures.

- Implement biometric authentication for quick access
- Support offline mode with data sync when connected
- Add haptic feedback for important actions
- Implement push notifications with custom sounds
- Support both imperial and metric units
- Add data backup and restore functionality
- Implement pet profile QR codes for emergency situations
- Cache vet locations for offline access
- Support voice notes for quick medical observations
- Add widget support for medication reminders
- Implement deep linking for appointment reminders
- Support multiple languages
- Ensure COPPA compliance for family sharing
- Add Apple Health / Google Fit integration for activity data
- Target app size under 50MB for quick downloads