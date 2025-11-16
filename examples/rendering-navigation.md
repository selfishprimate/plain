# Rendering & Navigation: SSR, SSG, SPA & More

This guide helps you choose the right rendering strategy and navigation approach for your product.

---

## Rendering Strategies

### Option 1: SPA (Single-Page Application)

**Description:**
JavaScript renders everything in the browser. Initial HTML is minimal, then JS takes over.

**How it works:**
1. Server sends minimal HTML + JavaScript bundle
2. JavaScript loads in browser
3. JavaScript renders entire UI
4. Navigation happens client-side (no page reloads)

**Frameworks:**
- React (with Vite or Create React App)
- Vue (with Vite)
- Svelte (with Vite)
- Angular

**Pros:**
- Fast navigation after initial load
- Rich, interactive UI
- No page reloads
- Great for apps (dashboards, tools)
- Works offline (with service workers)

**Cons:**
- Slow initial load (large JS bundle)
- Poor SEO (unless pre-rendered)
- Blank screen while JS loads
- Not great for content-heavy sites

**Best For:**
- Web apps and dashboards
- Admin panels
- Interactive tools
- Apps behind login

**Example:**
```jsx
// React SPA (Vite)
import { BrowserRouter, Routes, Route } from 'react-router-dom';

function App() {
  return (
    <BrowserRouter>
      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}
```

---

### Option 2: SSR (Server-Side Rendering)

**Description:**
Server generates full HTML for each request. Page is interactive after hydration.

**How it works:**
1. User requests page
2. Server fetches data and renders HTML
3. Server sends complete HTML to browser
4. Browser displays HTML immediately
5. JavaScript "hydrates" to make interactive

**Frameworks:**
- Next.js (React)
- Nuxt (Vue)
- SvelteKit
- Remix

**Pros:**
- Fast initial page load
- Great SEO (search engines see HTML)
- Works without JavaScript
- Good for dynamic, personalized content

**Cons:**
- Slower navigation (server request per page)
- More server resources needed
- More complex to deploy
- TTFB (Time to First Byte) can be slow

**Best For:**
- E-commerce sites
- News/media sites
- Personalized dashboards
- Apps with dynamic data

**Example (Next.js):**
```jsx
// pages/index.js
export async function getServerSideProps() {
  const data = await fetch('https://api.example.com/data');
  return { props: { data } };
}

export default function Home({ data }) {
  return <div>{data.title}</div>;
}
```

---

### Option 3: SSG (Static Site Generation)

**Description:**
HTML is generated at build time. Same HTML served to all users.

**How it works:**
1. Build process generates HTML for all pages
2. HTML files are deployed to CDN
3. User requests page → instant HTML response
4. Optional: JavaScript hydrates for interactivity

**Frameworks:**
- Next.js (React)
- Gatsby (React)
- Nuxt (Vue)
- Astro
- Hugo, 11ty (no JS)

**Pros:**
- Fastest load times (pre-built HTML)
- Cheapest hosting (static files)
- Best SEO
- Great security (no server)
- Works offline

**Cons:**
- Build time increases with page count
- Can't handle user-specific content easily
- Stale data (until rebuild)
- Not for highly dynamic content

**Best For:**
- Blogs and documentation
- Marketing sites
- Portfolios
- Landing pages
- Product catalogs (with ISR)

**Example (Next.js):**
```jsx
// pages/index.js
export async function getStaticProps() {
  const data = await fetch('https://api.example.com/data');
  return { props: { data }, revalidate: 60 };
}

export default function Home({ data }) {
  return <div>{data.title}</div>;
}
```

---

### Option 4: ISR (Incremental Static Regeneration)

**Description:**
Hybrid of SSG + SSR. Pages are static but regenerate in background.

**How it works:**
1. Page is statically generated at build time
2. User requests page → instant HTML (cached)
3. After revalidation time, next request triggers rebuild
4. New version generated in background
5. Subsequent requests get fresh version

**Frameworks:**
- Next.js (React)
- Astro (experimental)

**Pros:**
- Fast like SSG
- Fresh data without full rebuild
- Best of both worlds
- Scales well

**Cons:**
- Next.js specific (mostly)
- Caching complexity
- Stale data possible

**Best For:**
- E-commerce product pages
- Blog posts with comments
- News sites
- Large sites with frequent updates

**Example (Next.js):**
```jsx
export async function getStaticProps() {
  const data = await fetch('https://api.example.com/data');
  return {
    props: { data },
    revalidate: 300 // Regenerate every 5 minutes
  };
}
```

---

### Option 5: Hybrid Rendering

**Description:**
Mix multiple strategies in one app. Different pages use different methods.

**Example (Next.js):**
```
/ → SSG (static homepage)
/blog → SSG (static blog listing)
/blog/[slug] → ISR (regenerate blog posts)
/dashboard → SSR (personalized, dynamic)
/app/* → SPA (client-side only)
```

**Best For:**
- Large, complex sites
- Apps with varied content types
- Optimizing for performance

---

## Comparison Table

| **Strategy** | **Load Speed** | **SEO** | **Server Cost** | **Fresh Data** | **Best For** |
|---|---|---|---|---|---|
| **SPA** | Slow initial | Poor | Low | Real-time | Web apps |
| **SSR** | Medium | Excellent | High | Real-time | Dynamic sites |
| **SSG** | Fastest | Excellent | Lowest | Stale | Blogs, marketing |
| **ISR** | Fast | Excellent | Low-Med | Near real-time | E-commerce |
| **Hybrid** | Varies | Excellent | Varies | Varies | Complex apps |

---

## Navigation Patterns

### Client-Side Navigation (SPA)

**How it works:**
- JavaScript intercepts link clicks
- Fetches data via API
- Updates UI without page reload

**Example (React Router):**
```jsx
import { Link } from 'react-router-dom';

<Link to="/about">About</Link>
```

**Pros:**
- Instant navigation
- Smooth transitions
- Maintains app state

**Cons:**
- Requires JavaScript
- Accessibility concerns if done wrong

---

### Server-Side Navigation (MPA)

**How it works:**
- Each link is a full page reload
- Server generates new HTML

**Example:**
```html
<a href="/about">About</a>
```

**Pros:**
- Works without JavaScript
- Simple
- Browser handles everything

**Cons:**
- Slower (full reload)
- Loses app state

---

### Hybrid Navigation (Next.js)

**How it works:**
- Uses `<Link>` for client-side navigation
- Prefetches pages in background
- Falls back to server navigation if JS disabled

**Example (Next.js):**
```jsx
import Link from 'next/link';

<Link href="/about">About</Link>
```

**Features:**
- Automatic prefetching
- Client-side navigation
- Scroll restoration
- Focus management

---

## Advanced Navigation Patterns

### Prefetching

**Load pages before user clicks.**

**Strategies:**
- On hover
- On viewport enter
- On idle time

**Example (Next.js):**
```jsx
<Link href="/about" prefetch={true}>
  About
</Link>
```

---

### Route Transitions

**Animate between pages.**

**Example (Framer Motion + React Router):**
```jsx
<AnimatePresence mode="wait">
  <motion.div
    key={location.pathname}
    initial={{ opacity: 0 }}
    animate={{ opacity: 1 }}
    exit={{ opacity: 0 }}
  >
    <Routes location={location}>
      <Route path="/" element={<Home />} />
    </Routes>
  </motion.div>
</AnimatePresence>
```

---

### Scroll Restoration

**Restore scroll position on back/forward.**

**Options:**
- Auto (browser default)
- Manual (custom logic)

**Example (React Router):**
```jsx
<ScrollRestoration />
```

---

### Loading States

**Show feedback during navigation.**

**Example (Next.js 13+ App Router):**
```jsx
// app/loading.js
export default function Loading() {
  return <div>Loading...</div>;
}
```

---

## Progressive Enhancement

**Strategy:** Build for HTML first, enhance with JavaScript.

**Approach:**
1. HTML works without JS
2. CSS enhances visuals
3. JavaScript adds interactivity

**Example:**
```html
<!-- Works without JS -->
<form action="/search" method="GET">
  <input name="q" />
  <button>Search</button>
</form>

<!-- Enhanced with JS -->
<script>
  form.addEventListener('submit', async (e) => {
    e.preventDefault();
    // Client-side search
  });
</script>
```

**Benefits:**
- Accessible
- Resilient
- SEO-friendly
- Faster perceived performance

---

## Route Design Patterns

### Flat Routes
```
/
/about
/contact
/blog
/blog/post-1
```

**Pros:** Simple
**Cons:** Can get messy with many pages

---

### Nested Routes
```
/
/app
/app/dashboard
/app/dashboard/settings
```

**Pros:** Organized, shared layouts
**Cons:** Deep nesting can be confusing

---

### Dynamic Routes
```
/blog/[slug]
/user/[id]
/product/[id]/reviews
```

**Enables:**
- Content-driven pages
- User profiles
- Product pages

---

## Rendering Decision Guide

| **Your Goal** | **Recommended Strategy** |
|---|---|
| Blog or documentation | SSG (Astro, Hugo, Next.js) |
| Marketing site | SSG or ISR |
| E-commerce | ISR or SSR |
| SaaS dashboard | SPA or SSR |
| News site | SSR or ISR |
| Personalized app | SSR |
| Static portfolio | SSG |
| Large catalog | ISR |

---

## Performance Optimization

### Code Splitting

**Load only code needed for current page.**

**Automatic (Next.js, Nuxt):**
```jsx
// Automatically code-split per page
```

**Manual (React):**
```jsx
import { lazy, Suspense } from 'react';

const About = lazy(() => import('./About'));

<Suspense fallback={<div>Loading...</div>}>
  <About />
</Suspense>
```

---

### Image Optimization

**Use next/image or similar:**
```jsx
import Image from 'next/image';

<Image
  src="/hero.jpg"
  alt="Hero"
  width={1200}
  height={600}
  priority
/>
```

**Features:**
- Lazy loading
- Responsive images
- Format optimization (WebP)
- Blur placeholders

---

## Resources

- **Next.js Docs:** https://nextjs.org/docs
- **Nuxt Docs:** https://nuxt.com
- **Astro Docs:** https://astro.build
- **Web.dev Rendering:** https://web.dev/rendering-on-the-web/
- **React Router:** https://reactrouter.com
