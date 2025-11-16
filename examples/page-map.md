# Page Map: Site Structure & Navigation

This guide helps you plan and document your product's page structure and navigation hierarchy.

---

## What is a Page Map?

A page map (also called sitemap or IA - Information Architecture) shows all pages in your product and how they relate to each other.

**Purpose:**
- Plan navigation structure
- Identify all required pages
- Understand user journeys
- Guide development priorities
- Prevent missing pages
- Design navigation menus

**Format:** Hierarchical tree showing parent-child relationships

---

## Example 1: SaaS Task Management App (Taskly)

### Public Pages (Logged Out)

```
/ (Homepage)
├── /features
├── /pricing
├── /about
├── /blog
│   └── /blog/[slug]
├── /contact
├── /login
├── /signup
├── /forgot-password
└── /reset-password
```

### App Pages (Logged In)

```
/app
├── /app/dashboard (default after login)
├── /app/tasks
│   ├── /app/tasks/list
│   ├── /app/tasks/board
│   ├── /app/tasks/calendar
│   └── /app/tasks/[taskId]
├── /app/projects
│   ├── /app/projects/new
│   └── /app/projects/[projectId]
│       ├── /app/projects/[projectId]/tasks
│       └── /app/projects/[projectId]/settings
├── /app/team
│   ├── /app/team/members
│   └── /app/team/invite
├── /app/settings
│   ├── /app/settings/profile
│   ├── /app/settings/account
│   ├── /app/settings/notifications
│   ├── /app/settings/billing
│   └── /app/settings/integrations
└── /app/help
```

**Total Pages:** ~25-30

---

## Example 2: E-commerce Platform (Shopnest)

### Public Pages

```
/ (Homepage)
├── /shop
│   ├── /shop/[category]
│   └── /shop/[category]/[subcategory]
├── /products/[slug]
├── /search?q=[query]
├── /deals
├── /new-arrivals
├── /brands
│   └── /brands/[brandSlug]
├── /about
├── /contact
├── /faq
├── /shipping-returns
├── /privacy-policy
└── /terms-of-service
```

### Account Pages

```
/account
├── /account/login
├── /account/register
├── /account/forgot-password
├── /account/profile
├── /account/orders
│   └── /account/orders/[orderId]
├── /account/addresses
├── /account/payment-methods
├── /account/wishlist
└── /account/settings
```

### Checkout Flow

```
/cart
└── /checkout
    ├── /checkout/shipping
    ├── /checkout/payment
    └── /checkout/confirmation
```

**Total Pages:** ~40-50

---

## Example 3: Blog / Content Site (Devfolio)

### Public Pages

```
/ (Homepage - Recent posts)
├── /blog
│   ├── /blog/[slug]
│   ├── /blog/category/[categorySlug]
│   └── /blog/tag/[tagSlug]
├── /projects
│   └── /projects/[slug]
├── /about
├── /contact
├── /uses (Tools & setup)
├── /newsletter
│   ├── /newsletter/subscribe
│   └── /newsletter/confirm
└── /search?q=[query]
```

**Total Pages:** ~15-20

---

## Example 4: SaaS Analytics Dashboard (Shopmetrics)

### Marketing Site

```
/ (Homepage)
├── /features
├── /pricing
├── /integrations
│   └── /integrations/[platformName]
├── /customers
├── /resources
│   ├── /resources/blog
│   │   └── /resources/blog/[slug]
│   ├── /resources/guides
│   └── /resources/case-studies
├── /about
├── /contact
├── /login
└── /signup
```

### App (Dashboard)

```
/app
├── /app/overview (Dashboard home)
├── /app/analytics
│   ├── /app/analytics/revenue
│   ├── /app/analytics/products
│   ├── /app/analytics/customers
│   └── /app/analytics/traffic
├── /app/reports
│   ├── /app/reports/new
│   └── /app/reports/[reportId]
├── /app/alerts
│   └── /app/alerts/new
├── /app/integrations
│   └── /app/integrations/connect/[platform]
├── /app/team
│   ├── /app/team/members
│   └── /app/team/invite
└── /app/settings
    ├── /app/settings/profile
    ├── /app/settings/billing
    ├── /app/settings/notifications
    └── /app/settings/api-keys
```

**Total Pages:** ~35-40

---

## Example 5: Social Platform (Connectly)

### Public Pages

```
/ (Homepage or redirect to /login)
├── /login
├── /signup
├── /forgot-password
└── /about
```

### App Pages (Logged In)

```
/app
├── /app/feed (Home feed)
├── /app/explore
├── /app/notifications
├── /app/messages
│   └── /app/messages/[conversationId]
├── /app/profile/[username]
│   ├── /app/profile/[username]/posts
│   ├── /app/profile/[username]/followers
│   └── /app/profile/[username]/following
├── /app/post/[postId]
├── /app/search?q=[query]
└── /app/settings
    ├── /app/settings/profile
    ├── /app/settings/account
    ├── /app/settings/privacy
    └── /app/settings/notifications
```

**Total Pages:** ~20-25

---

## Page Map Template (Markdown)

```markdown
## Public Pages
- / — Homepage
- /features — Product features
- /pricing — Pricing plans
- /about — About us
- /contact — Contact form
- /login — User login
- /signup — User registration

## App Pages (Authenticated)
- /app/dashboard — Main dashboard
- /app/settings — User settings
- /app/[resource] — Resource list
- /app/[resource]/[id] — Resource detail

## Utility Pages
- /404 — Not found
- /500 — Server error
- /maintenance — Maintenance mode
```

---

## Page Map Template (Nested List)

```
Website Name
│
├── Marketing Site
│   ├── Homepage (/)
│   ├── Features (/features)
│   ├── Pricing (/pricing)
│   ├── About (/about)
│   └── Contact (/contact)
│
├── Authentication
│   ├── Login (/login)
│   ├── Sign Up (/signup)
│   ├── Forgot Password (/forgot-password)
│   └── Reset Password (/reset-password)
│
├── Application (requires auth)
│   ├── Dashboard (/app/dashboard)
│   ├── Settings (/app/settings)
│   └── [Feature Pages]
│
└── Legal
    ├── Privacy Policy (/privacy)
    └── Terms of Service (/terms)
```

---

## Navigation Patterns

### Pattern 1: Flat Structure (Simple Sites)

**Best for:** Blogs, portfolios, landing pages

```
/ (Home)
/about
/work
/blog
/contact
```

**Pros:** Simple, easy to navigate
**Cons:** Doesn't scale well

---

### Pattern 2: Hub & Spoke (App-like)

**Best for:** SaaS dashboards, admin panels

```
/app/dashboard (Hub)
  ├── /app/tasks
  ├── /app/projects
  ├── /app/team
  └── /app/settings
```

**Pros:** Clear primary page (dashboard), organized sections
**Cons:** Users must return to hub to switch sections

---

### Pattern 3: Hierarchical (Deep)

**Best for:** E-commerce, large content sites

```
/shop
  ├── /shop/clothing
  │   ├── /shop/clothing/mens
  │   └── /shop/clothing/womens
  └── /shop/electronics
      ├── /shop/electronics/phones
      └── /shop/electronics/laptops
```

**Pros:** Organized by category, scalable
**Cons:** Deep nesting can be confusing

---

### Pattern 4: Hybrid

**Best for:** Complex apps with multiple user types

```
/ (Marketing homepage)
/app (Logged-in app)
/admin (Admin panel)
/blog (Content marketing)
```

---

## Special Pages to Include

### Error Pages
- `/404` — Page not found
- `/500` — Internal server error
- `/503` — Service unavailable
- `/403` — Forbidden
- `/401` — Unauthorized

### Utility Pages
- `/maintenance` — Maintenance mode
- `/offline` — PWA offline page
- `/unsubscribe` — Email unsubscribe

### Legal Pages
- `/privacy` — Privacy policy
- `/terms` — Terms of service
- `/cookies` — Cookie policy
- `/accessibility` — Accessibility statement

### SEO Pages
- `/sitemap.xml` — XML sitemap
- `/robots.txt` — Robots file
- `/rss.xml` — RSS feed (blogs)

---

## Navigation Hierarchy Example

### Primary Navigation (Header)
```
Logo | Features | Pricing | About | Blog | [Login] [Sign Up]
```

### Logged-In Navigation
```
Logo | Dashboard | Tasks | Projects | Team | [Settings ▼] [Profile ▼]
```

### Sidebar Navigation (App)
```
├── Dashboard
├── Tasks
│   ├── My Tasks
│   ├── Assigned to Me
│   └── All Tasks
├── Projects
├── Team
└── Settings
    ├── Profile
    ├── Account
    ├── Billing
    └── Integrations
```

### Footer Navigation
```
Product        Company       Resources      Legal
Features       About         Blog           Privacy
Pricing        Careers       Docs           Terms
Integrations   Contact       Support        Cookies
```

---

## Mobile Navigation Considerations

### Hamburger Menu
- Collapsed by default on mobile
- Reveals full navigation when tapped
- Common for marketing sites

### Bottom Tab Bar
- 4-5 primary items
- Always visible
- Common for mobile apps
- Example: Home | Search | Notifications | Profile

### Drawer Navigation
- Slides in from left/right
- Good for hierarchical navigation
- Common for content apps

---

## URL Design Best Practices

### 1. Use Lowercase
```
✅ /about-us
❌ /About-Us
```

### 2. Use Hyphens, Not Underscores
```
✅ /blog/how-to-write-code
❌ /blog/how_to_write_code
```

### 3. Keep URLs Short
```
✅ /blog/seo-tips
❌ /blog/2024/01/15/seo-tips-for-beginners-complete-guide
```

### 4. Make URLs Descriptive
```
✅ /products/wireless-headphones
❌ /products/12345
```

### 5. Avoid Query Parameters for Content
```
✅ /blog/category/design
❌ /blog?category=design
```

### 6. Use Trailing Slashes Consistently
```
Choose one:
/about (no slash)
/about/ (with slash)
```

---

## Page Priority Matrix

| Page | Priority | Why |
|---|---|---|
| Homepage | Critical | First impression |
| Login/Signup | Critical | Conversion |
| Dashboard | Critical | Core app entry |
| Core features | High | Main value |
| Settings | Medium | User management |
| Help/Docs | Medium | Support |
| About | Low | Nice to have |
| Blog | Low | Marketing |

---

## Checklist

- [ ] All user flows have corresponding pages
- [ ] Error pages defined (404, 500)
- [ ] Legal pages included (privacy, terms)
- [ ] Navigation hierarchy makes sense
- [ ] URLs follow best practices
- [ ] Mobile navigation considered
- [ ] Pages organized by priority
- [ ] Sitemap.xml planned for SEO

---

## Tools for Page Mapping

**Visual Tools:**
- **Figma / FigJam** — Visual sitemap diagrams
- **Whimsical** — Quick sitemaps
- **Miro** — Collaborative boards
- **Octopus.do** — Sitemap generator
- **Slickplan** — Professional sitemaps

**Code-Based:**
- Markdown nested lists
- YAML structure files
- Spreadsheets (Excel, Google Sheets)

---

## Example: Complete Page List (CSV Format)

```csv
Path,Title,Access,Priority
/,Homepage,Public,Critical
/features,Features,Public,High
/pricing,Pricing,Public,Critical
/about,About Us,Public,Low
/login,Login,Public,Critical
/signup,Sign Up,Public,Critical
/app/dashboard,Dashboard,Auth Required,Critical
/app/tasks,Tasks,Auth Required,Critical
/app/settings,Settings,Auth Required,Medium
/404,Not Found,Public,Medium
/privacy,Privacy Policy,Public,Low
```

---

## Resources

- **IA Best Practices:** https://www.nngroup.com/articles/ia-vs-navigation/
- **Sitemap Examples:** https://www.sitemap.org/
- **Navigation Patterns:** https://ui-patterns.com/patterns/navigation
