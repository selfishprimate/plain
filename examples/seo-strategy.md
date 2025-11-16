# SEO Strategy: Best Practices & Implementation

This guide helps you optimize your product for search engines and social media sharing.

---

## SEO Fundamentals

### What is SEO?

Search Engine Optimization (SEO) makes your website discoverable and ranks it higher in search results.

**Key Benefits:**
- Organic traffic (free, long-term)
- Higher visibility
- Credibility and trust
- Better user experience

**Core Pillars:**
1. **Technical SEO** — site structure, performance
2. **On-Page SEO** — content, meta tags, headings
3. **Off-Page SEO** — backlinks, social signals

---

## Meta Tags

### Title Tags

**Most important SEO element.** Shows in search results and browser tabs.

**Best Practices:**
- 50-60 characters
- Include primary keyword
- Unique for each page
- Brand name at end (optional)

**Example:**
```html
<title>Affordable Task Manager for Freelancers | Taskly</title>
```

**Dynamic (React/Next.js):**
```jsx
// Next.js
import Head from 'next/head';

export default function Page() {
  return (
    <Head>
      <title>Affordable Task Manager for Freelancers | Taskly</title>
    </Head>
  );
}
```

---

### Meta Descriptions

**Shown in search results below title.** Influences click-through rate.

**Best Practices:**
- 150-160 characters
- Include target keyword
- Call to action
- Unique for each page

**Example:**
```html
<meta
  name="description"
  content="Organize your workday with Taskly. Fast task capture, deadline reminders, and offline sync. Built for freelancers and remote teams."
/>
```

---

### Open Graph (Social Sharing)

**Controls how links appear on social media (Facebook, LinkedIn, etc.).**

**Required Tags:**
```html
<meta property="og:title" content="Taskly - Task Manager for Freelancers" />
<meta property="og:description" content="Fast, simple task management for freelancers." />
<meta property="og:image" content="https://taskly.com/og-image.png" />
<meta property="og:url" content="https://taskly.com" />
<meta property="og:type" content="website" />
```

**Image Recommendations:**
- Size: 1200x630px (Facebook/LinkedIn)
- Format: PNG or JPG
- Max file size: 8MB
- Avoid text-heavy images

---

### Twitter Cards

**Controls Twitter sharing appearance.**

```html
<meta name="twitter:card" content="summary_large_image" />
<meta name="twitter:title" content="Taskly - Task Manager for Freelancers" />
<meta name="twitter:description" content="Fast, simple task management." />
<meta name="twitter:image" content="https://taskly.com/twitter-image.png" />
<meta name="twitter:site" content="@taskly" />
```

**Card Types:**
- `summary` — small image
- `summary_large_image` — large image (recommended)
- `player` — video/audio
- `app` — mobile app

---

### Canonical URLs

**Tells search engines which version of a page is the primary one.**

Prevents duplicate content issues.

**Example:**
```html
<link rel="canonical" href="https://taskly.com/features" />
```

**When to Use:**
- Multiple URLs for same content
- URL parameters (`?ref=twitter`)
- Pagination
- HTTP vs HTTPS

---

## Structured Data (Schema.org)

### What is Structured Data?

JSON-LD code that helps search engines understand your content. Enables **rich snippets** in search results.

**Common Types:**
- Organization
- Product
- Article
- FAQ
- Breadcrumb
- Review/Rating

---

### Organization Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Taskly",
  "url": "https://taskly.com",
  "logo": "https://taskly.com/logo.png",
  "sameAs": [
    "https://twitter.com/taskly",
    "https://facebook.com/taskly"
  ]
}
</script>
```

---

### Product Schema (E-commerce)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Taskly Pro",
  "image": "https://taskly.com/product.png",
  "description": "Premium task management tool",
  "brand": {
    "@type": "Brand",
    "name": "Taskly"
  },
  "offers": {
    "@type": "Offer",
    "price": "9.99",
    "priceCurrency": "USD"
  },
  "aggregateRating": {
    "@type": "AggregateRating",
    "ratingValue": "4.8",
    "reviewCount": "342"
  }
}
</script>
```

---

### Article Schema (Blog Posts)

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "10 Productivity Tips for Freelancers",
  "image": "https://taskly.com/blog/image.png",
  "author": {
    "@type": "Person",
    "name": "Jane Doe"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Taskly Blog",
    "logo": {
      "@type": "ImageObject",
      "url": "https://taskly.com/logo.png"
    }
  },
  "datePublished": "2024-01-15"
}
</script>
```

---

### FAQ Schema

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "How much does Taskly cost?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Taskly is free for personal use. Pro plans start at $9.99/month."
      }
    }
  ]
}
</script>
```

---

## URL Structure

### SEO-Friendly URLs

**Good:**
```
https://taskly.com/features
https://taskly.com/blog/productivity-tips
https://taskly.com/pricing
```

**Bad:**
```
https://taskly.com/page?id=123
https://taskly.com/p/547abc
https://taskly.com/index.php?page=features
```

**Best Practices:**
- Use hyphens (not underscores)
- Lowercase only
- Include keywords
- Keep short and descriptive
- Avoid parameters when possible

---

## Content Optimization

### Headings (H1-H6)

**Proper heading hierarchy helps SEO.**

**Rules:**
- One `<h1>` per page (page title)
- Use `<h2>` for main sections
- Use `<h3>-<h6>` for subsections
- Include keywords naturally

**Example:**
```html
<h1>Taskly: Task Manager for Freelancers</h1>
<h2>Features</h2>
<h3>Smart Task Capture</h3>
<h3>Deadline Reminders</h3>
<h2>Pricing</h2>
```

---

### Keyword Optimization

**Don't keyword stuff. Write naturally.**

**Best Practices:**
- Primary keyword in title, H1, first paragraph
- Use variations and synonyms
- Focus on user intent
- Long-tail keywords (specific phrases)

**Example:**
- **Broad:** "task manager"
- **Long-tail:** "simple task manager for freelancers"

---

### Internal Linking

**Link to other pages on your site.**

**Benefits:**
- Distributes page authority
- Helps search engines discover pages
- Improves user navigation

**Best Practices:**
- Use descriptive anchor text
- Link to relevant pages
- Avoid "click here"

**Example:**
```html
<!-- Bad -->
<a href="/features">Click here</a> to learn more.

<!-- Good -->
Learn more about our <a href="/features">task management features</a>.
```

---

## Technical SEO

### Sitemap

**XML file listing all pages.**

**Example (sitemap.xml):**
```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://taskly.com/</loc>
    <lastmod>2024-01-15</lastmod>
    <priority>1.0</priority>
  </url>
  <url>
    <loc>https://taskly.com/features</loc>
    <lastmod>2024-01-10</lastmod>
    <priority>0.8</priority>
  </url>
</urlset>
```

**Tools:**
- **Next.js:** `next-sitemap` package
- **Manual:** https://www.xml-sitemaps.com

**Submit to:**
- Google Search Console
- Bing Webmaster Tools

---

### Robots.txt

**Controls which pages search engines can crawl.**

**Example:**
```
User-agent: *
Allow: /
Disallow: /admin/
Disallow: /api/

Sitemap: https://taskly.com/sitemap.xml
```

**Location:** `/public/robots.txt`

---

### Performance (Core Web Vitals)

**Google uses page speed as a ranking factor.**

**Core Web Vitals:**
1. **LCP (Largest Contentful Paint)** — < 2.5s
2. **FID (First Input Delay)** — < 100ms
3. **CLS (Cumulative Layout Shift)** — < 0.1

**How to Improve:**
- Optimize images (WebP, lazy loading)
- Minimize JavaScript
- Use CDN
- Enable caching
- Preload critical resources

**Tools:**
- Lighthouse (Chrome DevTools)
- PageSpeed Insights: https://pagespeed.web.dev
- WebPageTest: https://webpagetest.org

---

### Mobile-Friendliness

**Google uses mobile-first indexing.**

**Requirements:**
- Responsive design
- No horizontal scrolling
- Readable text without zooming
- Touch-friendly buttons (min 48x48px)

**Test:**
- Google Mobile-Friendly Test: https://search.google.com/test/mobile-friendly

---

### HTTPS

**Required for SEO and security.**

**How:**
- Get SSL certificate (free via Let's Encrypt)
- Redirect HTTP → HTTPS
- Update internal links

---

## Image SEO

### Alt Text

**Describes image for search engines and screen readers.**

**Best Practices:**
- Descriptive and concise
- Include keywords naturally
- Don't start with "image of"

**Example:**
```html
<!-- Bad -->
<img src="screenshot.png" alt="screenshot" />

<!-- Good -->
<img src="taskly-dashboard.png" alt="Taskly dashboard showing task list and calendar" />
```

---

### File Names

**Use descriptive file names.**

**Good:**
```
taskly-mobile-app-screenshot.png
team-collaboration-feature.jpg
```

**Bad:**
```
IMG_1234.png
screenshot-final-v2.jpg
```

---

### Image Optimization

**Compress images for faster loading.**

**Tools:**
- TinyPNG: https://tinypng.com
- Squoosh: https://squoosh.app
- ImageOptim (Mac)

**Formats:**
- WebP (modern, best compression)
- JPEG (photos)
- PNG (transparency)
- SVG (icons, logos)

---

## Local SEO (If Applicable)

### Google Business Profile

**For local businesses.**

**Steps:**
1. Claim your Google Business Profile
2. Add accurate info (address, hours)
3. Upload photos
4. Collect reviews

**Schema:**
```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Taskly Office",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Main St",
    "addressLocality": "San Francisco",
    "addressRegion": "CA",
    "postalCode": "94102"
  },
  "telephone": "+1-415-555-1234"
}
</script>
```

---

## Analytics & Monitoring

### Google Search Console

**Monitor search performance.**

**Setup:**
1. Add property: https://search.google.com/search-console
2. Verify ownership (DNS or HTML file)
3. Submit sitemap

**Features:**
- Track search rankings
- Monitor errors
- Submit sitemaps
- Request indexing

---

### Google Analytics 4 (GA4)

**Track user behavior.**

**Setup:**
```html
<!-- Add to <head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

---

## SEO Checklist

### On-Page SEO
- [ ] Unique title tag (50-60 chars)
- [ ] Meta description (150-160 chars)
- [ ] H1 tag with primary keyword
- [ ] Proper heading hierarchy (H1-H6)
- [ ] Alt text for all images
- [ ] Internal links with descriptive anchors
- [ ] SEO-friendly URLs
- [ ] Canonical tags

### Technical SEO
- [ ] HTTPS enabled
- [ ] Mobile-friendly design
- [ ] Fast page speed (< 3s)
- [ ] XML sitemap created and submitted
- [ ] robots.txt configured
- [ ] Core Web Vitals optimized
- [ ] Structured data (Schema.org)
- [ ] No broken links

### Social & Sharing
- [ ] Open Graph tags
- [ ] Twitter Card tags
- [ ] Social share images (1200x630px)

### Content
- [ ] Keyword research done
- [ ] Content matches search intent
- [ ] Natural keyword usage
- [ ] High-quality, original content

---

## Tools & Resources

**SEO Tools:**
- Google Search Console: https://search.google.com/search-console
- Google Analytics: https://analytics.google.com
- Ahrefs: https://ahrefs.com (paid)
- SEMrush: https://semrush.com (paid)
- Moz: https://moz.com (paid)

**Free Tools:**
- Google PageSpeed Insights: https://pagespeed.web.dev
- Schema Markup Validator: https://validator.schema.org
- Structured Data Testing Tool: https://search.google.com/test/rich-results
- Mobile-Friendly Test: https://search.google.com/test/mobile-friendly

**Learning:**
- Google SEO Starter Guide: https://developers.google.com/search/docs/beginner/seo-starter-guide
- Moz Beginner's Guide: https://moz.com/beginners-guide-to-seo
