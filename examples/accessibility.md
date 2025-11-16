# Accessibility: Guidelines & Best Practices

This guide helps you make your product accessible to everyone, including people with disabilities.

---

## Why Accessibility Matters

**Statistics:**
- 15% of the world's population lives with some form of disability
- 1 in 4 adults in the US has a disability
- Accessibility benefits everyone (keyboard users, mobile users, etc.)

**Legal Requirements:**
- ADA (Americans with Disabilities Act)
- Section 508 (US federal agencies)
- WCAG (Web Content Accessibility Guidelines)

**Business Benefits:**
- Larger audience
- Better SEO
- Improved usability for all
- Legal compliance

---

## WCAG Levels

### Level A (Minimum)
Basic accessibility features. Required by law in many countries.

### Level AA (Recommended)
Industry standard. Addresses major barriers.

### Level AAA (Enhanced)
Highest level. Difficult to achieve for all content.

**Recommendation:** Aim for **WCAG 2.1 Level AA** compliance.

---

## Color & Contrast

### Contrast Ratios

**WCAG AA Requirements:**
- **Normal text:** 4.5:1 minimum contrast ratio
- **Large text (18pt+ or 14pt+ bold):** 3:1 minimum
- **UI components and graphics:** 3:1 minimum

**WCAG AAA Requirements:**
- **Normal text:** 7:1 minimum
- **Large text:** 4.5:1 minimum

**Tools:**
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- Coolors Contrast Checker: https://coolors.co/contrast-checker
- Chrome DevTools: Built-in contrast ratio checker

**Example:**
```css
/* Good: White text on dark blue (7.2:1) */
.button {
  background: #003366;
  color: #ffffff;
}

/* Bad: Light gray on white (2.1:1) */
.text {
  background: #ffffff;
  color: #cccccc; /* Fails WCAG AA */
}
```

---

### Color Blindness

**Never rely on color alone** to convey information.

**Types:**
- **Deuteranopia** — red-green (most common)
- **Protanopia** — red-green
- **Tritanopia** — blue-yellow
- **Achromatopsia** — total color blindness

**Best Practices:**
- Use icons + color (not just color)
- Add patterns or labels
- Test with simulators

**Example:**
```jsx
// Bad: Color only
<span style={{ color: 'red' }}>Error</span>

// Good: Icon + color + text
<span className="text-red-600">
  <ErrorIcon /> Error: Invalid email
</span>
```

**Tools:**
- Chromatic Vision Simulator (browser extension)
- Color Oracle (desktop app)

---

## Keyboard Navigation

**All interactive elements must be keyboard accessible.**

### Tab Order

**Requirements:**
- Logical tab order (top to bottom, left to right)
- All interactive elements focusable
- Skip links for navigation
- No keyboard traps

**Implementation:**
```html
<!-- Good: Proper tabindex -->
<button tabindex="0">Click Me</button>

<!-- Bad: tabindex > 0 -->
<button tabindex="5">Don't do this</button>

<!-- Skip link -->
<a href="#main-content" class="skip-link">
  Skip to main content
</a>
```

---

### Focus Indicators

**Always show visible focus states.**

**Requirements:**
- Visible focus indicator (outline or border)
- Minimum 3:1 contrast ratio with background
- Never `outline: none` without replacement

**Example:**
```css
/* Good: Clear focus state */
button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}

/* Bad: No focus indicator */
button:focus {
  outline: none; /* Never do this alone */
}

/* Good alternative: Custom focus ring */
button:focus-visible {
  box-shadow: 0 0 0 3px rgba(0, 102, 204, 0.5);
  outline: none;
}
```

---

### Keyboard Shortcuts

**Common Shortcuts:**
- `Tab` — Next focusable element
- `Shift + Tab` — Previous focusable element
- `Enter / Space` — Activate button/link
- `Esc` — Close modal/dialog
- `Arrow keys` — Navigate lists, tabs

**Custom Shortcuts:**
```jsx
function SearchBar() {
  useEffect(() => {
    const handleKeyPress = (e) => {
      if (e.key === '/' && !e.ctrlKey) {
        e.preventDefault();
        document.getElementById('search').focus();
      }
    };
    window.addEventListener('keydown', handleKeyPress);
    return () => window.removeEventListener('keydown', handleKeyPress);
  }, []);

  return <input id="search" placeholder="Press / to search" />;
}
```

---

## Screen Readers

### Semantic HTML

**Use proper HTML elements.**

**Good:**
```html
<nav>
  <ul>
    <li><a href="/">Home</a></li>
  </ul>
</nav>

<main>
  <article>
    <h1>Page Title</h1>
    <p>Content...</p>
  </article>
</main>

<button>Submit</button>
```

**Bad:**
```html
<div class="nav">
  <div class="link" onclick="...">Home</div>
</div>

<div class="main">
  <div class="title">Page Title</div>
  <div>Content...</div>
</div>

<div onclick="submit()">Submit</div> <!-- Use <button> -->
```

---

### ARIA (Accessible Rich Internet Applications)

**Use ARIA when semantic HTML isn't enough.**

**Common ARIA Attributes:**

#### `aria-label`
Provides label when visible text isn't available.
```jsx
<button aria-label="Close modal">
  <XIcon />
</button>
```

#### `aria-labelledby`
References an element ID for the label.
```html
<h2 id="dialog-title">Confirm Delete</h2>
<div role="dialog" aria-labelledby="dialog-title">
  ...
</div>
```

#### `aria-describedby`
Additional description.
```html
<input
  id="email"
  aria-describedby="email-help"
/>
<span id="email-help">We'll never share your email.</span>
```

#### `aria-live`
Announces dynamic content changes.
```jsx
<div aria-live="polite" aria-atomic="true">
  {message} <!-- Screen reader announces changes -->
</div>
```

#### `aria-hidden`
Hides decorative elements from screen readers.
```jsx
<span aria-hidden="true">🎉</span> Success!
```

---

### Landmark Roles

**Help screen readers navigate sections.**

**Semantic HTML (Preferred):**
```html
<header> <!-- role="banner" -->
<nav>    <!-- role="navigation" -->
<main>   <!-- role="main" -->
<aside>  <!-- role="complementary" -->
<footer> <!-- role="contentinfo" -->
```

**ARIA Roles (when semantic HTML isn't possible):**
```html
<div role="navigation">...</div>
<div role="main">...</div>
```

---

## Forms

### Labels

**Every input needs a label.**

**Good:**
```html
<label for="email">Email</label>
<input id="email" type="email" />

<!-- Or wrapping -->
<label>
  Email
  <input type="email" />
</label>
```

**Bad:**
```html
<input type="email" placeholder="Email" /> <!-- Placeholder is not a label -->
```

---

### Error Messages

**Clear, helpful, accessible errors.**

**Good:**
```jsx
<div>
  <label htmlFor="email">Email</label>
  <input
    id="email"
    type="email"
    aria-invalid={hasError}
    aria-describedby="email-error"
  />
  {hasError && (
    <span id="email-error" role="alert">
      Please enter a valid email address
    </span>
  )}
</div>
```

---

### Required Fields

**Indicate required fields clearly.**

```html
<label for="name">
  Name <span aria-label="required">*</span>
</label>
<input id="name" required aria-required="true" />
```

---

## Images

### Alt Text

**Every image needs alternative text.**

**Decorative Images:**
```html
<img src="border.png" alt="" /> <!-- Empty alt for decorative -->
<!-- Or -->
<img src="border.png" role="presentation" />
```

**Informative Images:**
```html
<img src="chart.png" alt="Sales increased 25% in Q4 2024" />
```

**Links/Buttons with Images:**
```html
<a href="/profile">
  <img src="avatar.png" alt="Go to profile" />
</a>
```

---

### SVG Icons

**Make SVG icons accessible.**

```jsx
// Decorative (hidden from screen readers)
<svg aria-hidden="true" focusable="false">
  <path d="..." />
</svg>

// Informative
<svg role="img" aria-labelledby="heart-icon">
  <title id="heart-icon">Favorite</title>
  <path d="..." />
</svg>
```

---

## Interactive Components

### Modals/Dialogs

**Requirements:**
- Focus trap (tab stays inside modal)
- Close on `Esc` key
- Return focus on close
- `role="dialog"` or `role="alertdialog"`
- `aria-modal="true"`
- `aria-labelledby` for title

**Example:**
```jsx
<div
  role="dialog"
  aria-modal="true"
  aria-labelledby="modal-title"
>
  <h2 id="modal-title">Confirm Action</h2>
  <p>Are you sure?</p>
  <button onClick={confirm}>Yes</button>
  <button onClick={cancel}>No</button>
</div>
```

---

### Dropdowns/Menus

**Use proper ARIA patterns.**

```html
<button
  aria-haspopup="true"
  aria-expanded="false"
  aria-controls="menu"
>
  Menu
</button>
<ul id="menu" role="menu" hidden>
  <li role="menuitem">Item 1</li>
  <li role="menuitem">Item 2</li>
</ul>
```

---

### Tooltips

**Ensure tooltips are accessible.**

```html
<button aria-describedby="tooltip">
  Help
</button>
<div id="tooltip" role="tooltip">
  Click for more information
</div>
```

---

## Motion & Animation

### Reduced Motion

**Respect `prefers-reduced-motion`.**

```css
/* Animations by default */
.element {
  transition: transform 0.3s ease;
}

/* Disable for reduced motion users */
@media (prefers-reduced-motion: reduce) {
  .element {
    transition: none;
  }
}
```

**JavaScript:**
```js
const prefersReducedMotion = window.matchMedia(
  '(prefers-reduced-motion: reduce)'
).matches;

if (!prefersReducedMotion) {
  // Apply animations
}
```

---

## Testing Checklist

### Manual Testing

- [ ] Navigate entire site using keyboard only
- [ ] Test with screen reader (NVDA, JAWS, VoiceOver)
- [ ] Check color contrast (all text and UI)
- [ ] Test with browser zoom (200%)
- [ ] Disable JavaScript (graceful degradation)
- [ ] Test with color blindness simulator
- [ ] Check all form labels and errors
- [ ] Verify focus indicators on all interactive elements

---

### Automated Testing

**Tools:**
- **axe DevTools** (browser extension)
- **Lighthouse** (Chrome DevTools)
- **WAVE** (web accessibility evaluator)
- **Pa11y** (automated testing)

**Example (Pa11y):**
```bash
npm install -g pa11y
pa11y https://your-site.com
```

---

## Common Mistakes to Avoid

❌ `outline: none` without replacement
❌ Color-only indicators
❌ Missing alt text
❌ Non-semantic HTML (`<div>` for buttons)
❌ Empty links or buttons
❌ Automatic video/audio playback
❌ Inaccessible modals (no focus trap)
❌ Poor color contrast
❌ Missing form labels
❌ Keyboard traps

---

## Resources

**Guidelines:**
- WCAG 2.1: https://www.w3.org/WAI/WCAG21/quickref/
- ARIA Authoring Practices: https://www.w3.org/WAI/ARIA/apg/

**Tools:**
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/
- axe DevTools: https://www.deque.com/axe/devtools/
- WAVE: https://wave.webaim.org/
- Pa11y: https://pa11y.org/

**Screen Readers:**
- NVDA (Windows, free): https://www.nvaccess.org/
- JAWS (Windows, paid)
- VoiceOver (Mac/iOS, built-in)
- TalkBack (Android, built-in)

**Learning:**
- WebAIM: https://webaim.org/
- A11y Project: https://www.a11yproject.com/
- MDN Accessibility: https://developer.mozilla.org/en-US/docs/Web/Accessibility
