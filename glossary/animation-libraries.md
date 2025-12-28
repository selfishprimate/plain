# Animation Libraries

Choose the right animation library based on your project's complexity, performance requirements, and design needs. From micro-interactions to complex animations, these libraries help bring your interface to life.

## Framer Motion

A production-ready motion library for React that makes creating animations simple and declarative. It provides a powerful yet easy-to-use API for animations, gestures, and layout transitions.

**Best for:** React projects needing production-ready animations with minimal setup
- Declarative animations with simple syntax
- Gesture support (drag, tap, hover, pan)
- Layout animations and shared element transitions
- Server-side rendering support
- Excellent TypeScript support
- Bundle size: ~50KB gzipped

## GSAP (GreenSock)

The industry-standard JavaScript animation library trusted by major brands and agencies worldwide. GSAP provides unmatched performance and control for complex animations and timeline sequencing.

**Best for:** Complex, high-performance animations and timeline control
- Industry-standard animation library
- Powerful timeline and sequencing features
- Cross-browser compatibility
- Plugin ecosystem (ScrollTrigger, TextPlugin, etc.)
- Works with any framework or vanilla JS
- Bundle size: ~25KB core (additional for plugins)

## Lottie

A library that renders After Effects animations in real-time, allowing designers to create complex animations that developers can easily integrate without recreating them in code.

**Best for:** Complex animations designed in After Effects
- Render After Effects animations natively
- JSON-based animations
- Supports web, iOS, Android, React Native
- Perfect for illustrations and micro-animations
- Designer-developer workflow
- Bundle size: ~150KB (lottie-web)

## React Spring

A spring-physics based animation library that brings fluid, natural motion to React applications. It focuses on physics-based animations rather than duration-based ones for more realistic movement.

**Best for:** Spring-physics based animations in React
- Physics-based animation library
- Hooks-based API
- Support for gestures and scrolling
- Smaller bundle than Framer Motion
- Good for natural-feeling animations
- Bundle size: ~20KB gzipped

## Anime.js

A lightweight JavaScript animation library with a simple, yet powerful API. It works with CSS properties, SVG, DOM attributes and JavaScript objects, making it versatile for various animation needs.

**Best for:** Lightweight animations with simple API
- Lightweight JavaScript animation library
- Works with CSS, SVG, DOM attributes
- Timeline feature for complex sequences
- No dependencies
- Simple, clean API
- Bundle size: ~17KB minified

## Three.js

A cross-browser JavaScript library that uses WebGL to create and display animated 3D computer graphics in web browsers. It's the go-to solution for 3D visualizations and interactive experiences.

**Best for:** 3D graphics and WebGL animations
- Create 3D animations and visualizations
- WebGL wrapper with fallbacks
- Extensive examples and community
- Physics engines integration
- VR/AR support
- Bundle size: ~140KB gzipped (core)

## Motion One

A modern animation library built on the Web Animations API, designed to be incredibly small while maintaining powerful features. It delivers high-performance animations with minimal JavaScript.

**Best for:** Modern, performant web animations with minimal size
- Built on Web Animations API
- Tiny bundle size
- Spring animations
- Timeline support
- TypeScript first
- Bundle size: ~3KB gzipped

## Auto-Animate

A zero-config animation utility that automatically adds smooth transitions to your web app. Just add one line of code to get automatic animations whenever the DOM changes.

**Best for:** Zero-config layout animations
- One-line animation library
- Automatic animations on DOM changes
- Works with any framework
- No configuration needed
- Perfect for lists and layouts
- Bundle size: ~2KB gzipped

## Rive

A real-time interactive animation tool that allows designers to create animations with state machines and developers to control them programmatically. It bridges the gap between design and development.

**Best for:** Interactive animations and state machines
- Design tool + runtime
- Interactive animations with state machines
- Cross-platform (web, mobile, desktop)
- Vector-based animations
- Real-time manipulation
- Bundle size: ~200KB

## CSS Only

Pure CSS animations using transitions, transforms, and keyframes without any JavaScript. This approach offers the best performance for simple animations and requires no additional libraries.

**Best for:** Simple animations without JavaScript dependencies
- No JavaScript required
- Best performance for simple animations
- Native browser support
- CSS transitions and keyframes
- CSS animation libraries (Animate.css, etc.)
- Bundle size: 0KB JavaScript

## Popmotion

A functional, reactive animation library that provides low-level animation tools and utilities. It's designed to be the foundation for building more complex animation systems.

**Best for:** Low-level animation toolbox
- Functional animation library
- Framework agnostic
- Composable animations
- Physics simulations
- Gesture recognition
- Bundle size: ~15KB gzipped

## Remotion

A framework for creating videos programmatically using React. It allows developers to use their React skills to create animated videos, making video creation as easy as building web applications.

**Best for:** Creating videos programmatically with React
- Create videos using React
- Export as MP4, GIF, or image sequence
- Programmatic video generation
- Perfect for social media content
- Audio support
- Bundle size: N/A (build-time tool)

## Decision Factors

### Performance Requirements
- **High Performance Needed:** GSAP, Motion One, CSS Only
- **Standard Performance:** Framer Motion, React Spring, Anime.js
- **Complex Graphics:** Three.js, Rive

### Bundle Size Priority
- **Smallest:** Motion One (~3KB), Auto-Animate (~2KB), CSS Only (0KB)
- **Small:** Anime.js (~17KB), React Spring (~20KB)
- **Medium:** GSAP Core (~25KB), Framer Motion (~50KB)
- **Large:** Lottie (~150KB), Three.js (~140KB), Rive (~200KB)

### Framework Compatibility
- **React Specific:** Framer Motion, React Spring, Remotion
- **Framework Agnostic:** GSAP, Anime.js, Lottie, Motion One, Three.js
- **Any Framework:** Auto-Animate, CSS Only

### Animation Complexity
- **Simple Transitions:** CSS Only, Auto-Animate, Motion One
- **Standard Animations:** Framer Motion, Anime.js, React Spring
- **Complex Sequences:** GSAP, Lottie, Rive
- **3D Graphics:** Three.js

### Designer Collaboration
- **Designer-Friendly:** Lottie (After Effects), Rive (Rive Editor)
- **Code-Based:** All others

## Common Patterns

### Micro-interactions
Best libraries: Framer Motion, Motion One, CSS Only
- Button hover effects
- Form field animations
- Loading states
- Tooltips

### Page Transitions
Best libraries: Framer Motion, GSAP, Anime.js
- Route transitions
- Shared element animations
- Parallax scrolling
- Reveal animations

### Data Visualizations
Best libraries: Three.js (3D), GSAP, Framer Motion
- Charts and graphs
- Interactive dashboards
- Real-time data updates

### Illustrations
Best libraries: Lottie, Rive, GSAP
- Animated illustrations
- Onboarding flows
- Empty states
- Success animations

## Quick Selection Guide

```
Need After Effects animations? → Lottie
Building with React? → Framer Motion
Need maximum performance? → GSAP or CSS Only
Want 3D graphics? → Three.js
Need tiny bundle? → Motion One or Auto-Animate
Want interactive animations? → Rive
Creating videos? → Remotion
Need physics? → React Spring or Popmotion
Want simplicity? → Anime.js
Zero configuration? → Auto-Animate
```

## Letting AI Decide

If you specify "Let AI decide for me", the choice will be based on:
1. Your chosen framework (React → Framer Motion, Vue → GSAP, etc.)
2. Performance requirements from your project description
3. Complexity of animations needed
4. Bundle size constraints
5. Team expertise level

The AI will typically choose Framer Motion for React projects, GSAP for complex requirements, or CSS-only solutions for simple needs.