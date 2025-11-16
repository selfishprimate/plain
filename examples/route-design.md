# Route Design: URL Structure & Patterns

This guide helps you design clean, intuitive URL structures for your product.

---

## What is Route Design?

Route design defines your URL structure and how URLs map to pages and features. Good routes are predictable, SEO-friendly, and user-friendly.

**Purpose:**
- Create intuitive navigation
- Enable deep linking
- Improve SEO
- Support sharing
- Guide development
- Maintain consistency

**Principles:**
- Predictable and logical
- Human-readable
- RESTful (for APIs)
- Lowercase with hyphens
- Avoid unnecessary nesting

---

## Route Naming Conventions

### 1. Use Lowercase
```
✅ /about-us
❌ /About-Us
❌ /ABOUT-US
```

### 2. Use Hyphens, Not Underscores
```
✅ /blog/getting-started
❌ /blog/getting_started
```

### 3. Keep URLs Short
```
✅ /blog/seo-tips
❌ /blog/2024/01/15/the-ultimate-guide-to-seo-tips-for-beginners
```

### 4. Use Nouns, Not Verbs
```
✅ /tasks
✅ /tasks/new
❌ /create-task
❌ /get-tasks
```

### 5. Be Descriptive
```
✅ /products/wireless-headphones
❌ /products/12345
❌ /p/wh
```

### 6. Avoid File Extensions
```
✅ /about
❌ /about.html
❌ /about.php
```

---

## Pattern 1: Flat Routes (Simple Sites)

**Best for:** Blogs, portfolios, landing pages

```
/
/about
/contact
/blog
/pricing
```

**Pros:**
- Simple and clear
- Easy to remember
- SEO-friendly

**Cons:**
- Doesn't scale well
- No hierarchy

---

## Pattern 2: Hierarchical Routes (Nested Resources)

**Best for:** E-commerce, complex apps

```
/shop
/shop/clothing
/shop/clothing/mens
/shop/clothing/mens/shirts
```

**Pros:**
- Clear hierarchy
- Breadcrumb-friendly
- Logical organization

**Cons:**
- Can get too deep
- Long URLs

**Best Practice:** Limit nesting to 3-4 levels maximum

```
✅ /shop/clothing/mens
❌ /shop/clothing/mens/casual/shirts/long-sleeve
```

---

## Pattern 3: Dynamic Routes (Parameterized)

**Best for:** User-generated content, data-driven pages

### Slug-Based (SEO-Friendly)
```
/blog/how-to-write-clean-code
/products/wireless-headphones
/users/john-doe
```

### ID-Based
```
/tasks/task_123abc
/orders/order_456def
/posts/12345
```

### Hybrid (ID + Slug)
```
/blog/123-how-to-write-clean-code
/products/456-wireless-headphones
```
**Note:** ID ensures uniqueness, slug provides SEO benefit

---

## Pattern 4: Query Parameters (Filters & Search)

**Use for:** Filtering, sorting, searching, pagination

```
/products?category=electronics&sort=price&order=asc
/search?q=headphones&page=2
/tasks?status=completed&priority=high
```

**When to use query params:**
- Filtering and sorting
- Search queries
- Pagination
- Non-essential parameters
- Optional parameters

**When NOT to use:**
```
❌ /products?id=123
✅ /products/123

❌ /blog?slug=how-to-code
✅ /blog/how-to-code
```

---

## Route Structure Examples

### Example 1: Task Management App (Taskly)

#### Public Routes
```
/                          # Homepage
/features                  # Product features
/pricing                   # Pricing page
/about                     # About us
/blog                      # Blog listing
/blog/[slug]               # Blog post
/contact                   # Contact form
/login                     # Login page
/signup                    # Sign up page
/forgot-password           # Password reset request
/reset-password/[token]    # Password reset form
```

#### App Routes (Authenticated)
```
/app                       # Redirect to /app/dashboard
/app/dashboard             # Main dashboard
/app/tasks                 # All tasks
/app/tasks?status=done     # Filtered tasks
/app/tasks/new             # Create task
/app/tasks/[taskId]        # Task detail
/app/tasks/[taskId]/edit   # Edit task
/app/projects              # All projects
/app/projects/[projectId]  # Project detail
/app/team                  # Team members
/app/settings              # User settings
/app/settings/profile      # Profile settings
/app/settings/billing      # Billing settings
```

---

### Example 2: E-commerce (Shopnest)

#### Public Routes
```
/                          # Homepage
/shop                      # All products
/shop/[category]           # Category page (e.g., /shop/electronics)
/shop/[category]/[sub]     # Subcategory (e.g., /shop/electronics/phones)
/products/[slug]           # Product detail
/search?q=[query]          # Search results
/cart                      # Shopping cart
/checkout                  # Checkout flow
/checkout/shipping         # Shipping step
/checkout/payment          # Payment step
/checkout/confirmation     # Order confirmation
```

#### Account Routes
```
/account/login             # Login
/account/register          # Sign up
/account/profile           # User profile
/account/orders            # Order history
/account/orders/[orderId]  # Order detail
/account/wishlist          # Saved items
/account/addresses         # Saved addresses
```

---

### Example 3: Social Platform (Connectly)

```
/                          # Homepage or feed
/login                     # Login
/signup                    # Sign up
/[username]                # User profile
/[username]/posts          # User's posts
/[username]/followers      # Followers list
/[username]/following      # Following list
/post/[postId]             # Single post
/explore                   # Discover content
/notifications             # Notifications
/messages                  # Messages inbox
/messages/[conversationId] # Conversation thread
/search?q=[query]          # Search users/posts
/settings                  # Account settings
```

---

### Example 4: SaaS Dashboard (Shopmetrics)

#### Marketing Site
```
/                          # Homepage
/features                  # Features
/pricing                   # Pricing
/integrations              # Integrations list
/integrations/shopify      # Shopify integration
/customers                 # Case studies
/blog                      # Blog
/blog/[slug]               # Blog post
/login                     # Login
/signup                    # Sign up
```

#### App (Dashboard)
```
/app                       # Redirect to /app/overview
/app/overview              # Dashboard home
/app/analytics/revenue     # Revenue analytics
/app/analytics/products    # Product analytics
/app/reports               # Reports list
/app/reports/[reportId]    # Report detail
/app/integrations          # Connected integrations
/app/team                  # Team management
/app/settings              # Settings
/app/settings/billing      # Billing
```

---

## RESTful API Routes

**For APIs, use RESTful conventions:**

### Resource Collection
```
GET    /api/tasks         # List all tasks
POST   /api/tasks         # Create new task
```

### Single Resource
```
GET    /api/tasks/123     # Get task #123
PUT    /api/tasks/123     # Update task #123 (full)
PATCH  /api/tasks/123     # Update task #123 (partial)
DELETE /api/tasks/123     # Delete task #123
```

### Nested Resources
```
GET    /api/projects/456/tasks      # List tasks in project #456
POST   /api/projects/456/tasks      # Create task in project #456
GET    /api/tasks/123/comments      # List comments on task #123
POST   /api/tasks/123/comments      # Add comment to task #123
```

### Filters & Search
```
GET /api/tasks?status=completed
GET /api/tasks?sort=dueDate&order=asc
GET /api/products?category=electronics&price_max=100
```

---

## Route Versioning (APIs)

### Option 1: URL Versioning (Most Common)
```
/api/v1/tasks
/api/v2/tasks
```

**Pros:** Clear, easy to route
**Cons:** URL changes with version

---

### Option 2: Header Versioning
```
GET /api/tasks
Accept: application/vnd.taskly.v1+json
```

**Pros:** Clean URLs
**Cons:** Less visible

---

## Advanced Patterns

### Optional Segments
```
/blog/[[...slug]]          # Matches /blog, /blog/post, /blog/category/post
```

### Catch-All Routes
```
/docs/[...slug]            # Matches /docs/intro, /docs/guides/start, etc.
```

### Route Groups (Next.js App Router)
```
/(auth)/login              # Groups login/signup visually, doesn't affect URL
/(auth)/signup
/(app)/dashboard           # Groups app routes
```

---

## Locale/Language Routes

### Option 1: Subdirectory
```
/en/about
/es/about
/fr/about
```

### Option 2: Subdomain
```
en.example.com
es.example.com
```

### Option 3: Query Parameter
```
/about?lang=en
/about?lang=es
```

**Best Practice:** Use subdirectory for SEO

---

## Trailing Slashes

**Choose one and be consistent:**

```
Option 1 (No trailing slash):
/about
/contact

Option 2 (With trailing slash):
/about/
/contact/
```

**Recommendation:** No trailing slash (cleaner)

**Important:** Redirect one to the other to avoid duplicate content
```
/about/ → redirects to → /about
```

---

## Route Redirects

### Permanent Redirect (301)
```
/old-page → 301 → /new-page
```
Use when page moved permanently (SEO-friendly)

### Temporary Redirect (302)
```
/maintenance → 302 → /
```
Use for temporary changes

### Common Redirects
```
/app → /app/dashboard (convenience redirect)
/blog → /blog/page/1 (pagination)
/ → /app/dashboard (if logged in)
```

---

## SEO-Friendly Routes

### 1. Include Keywords
```
✅ /blog/seo-best-practices
❌ /blog/post-123
```

### 2. Use Categories
```
✅ /blog/web-development/react-tips
✅ /shop/electronics/headphones
```

### 3. Avoid Session IDs
```
❌ /products?sessionid=abc123
✅ /products/wireless-headphones
```

### 4. Use Canonical URLs
```html
<link rel="canonical" href="https://example.com/products/headphones" />
```

---

## Route Security

### Protected Routes
```
/app/*                    # Requires authentication
/admin/*                  # Requires admin role
/settings/billing         # Requires subscription
```

### Implementation (Next.js Middleware):
```typescript
export function middleware(request: NextRequest) {
  const token = request.cookies.get('token');

  if (!token && request.nextUrl.pathname.startsWith('/app')) {
    return NextResponse.redirect(new URL('/login', request.url));
  }
}
```

---

## Route Organization (File-Based Routing)

### Next.js App Router
```
/app
├── page.tsx                    # /
├── about/page.tsx              # /about
├── blog
│   ├── page.tsx                # /blog
│   └── [slug]/page.tsx         # /blog/[slug]
└── app
    ├── layout.tsx              # Layout for /app/*
    ├── dashboard/page.tsx      # /app/dashboard
    └── tasks/[id]/page.tsx     # /app/tasks/[id]
```

### SvelteKit
```
/routes
├── +page.svelte                # /
├── about/+page.svelte          # /about
├── blog
│   ├── +page.svelte            # /blog
│   └── [slug]/+page.svelte     # /blog/[slug]
└── app
    ├── +layout.svelte          # Layout
    └── dashboard/+page.svelte  # /app/dashboard
```

---

## Common Route Mistakes

### 1. Inconsistent Naming
```
❌ /products, /getUsers, /CreateTask
✅ /products, /users, /tasks/new
```

### 2. Too Deep Nesting
```
❌ /app/workspace/project/task/comment/reply
✅ /app/tasks/123/comments
```

### 3. Using Verbs for Pages
```
❌ /create-account
✅ /signup
```

### 4. Mixing Patterns
```
❌ /blog/post-123 and /products/wireless-headphones
✅ /blog/[slug] and /products/[slug] (consistent)
```

---

## Checklist

- [ ] Routes use lowercase with hyphens
- [ ] Dynamic routes use descriptive slugs
- [ ] Query params used for filters/search
- [ ] RESTful conventions for APIs
- [ ] No file extensions in URLs
- [ ] Trailing slash handled consistently
- [ ] Protected routes require authentication
- [ ] SEO-friendly structure
- [ ] Redirects in place for old URLs

---

## Resources

- **RESTful API Design:** https://restfulapi.net/
- **Next.js Routing:** https://nextjs.org/docs/app/building-your-application/routing
- **URL Best Practices:** https://developers.google.com/search/docs/crawling-indexing/url-structure
