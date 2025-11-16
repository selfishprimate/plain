# Architecture Patterns: System Design & Structure

This guide helps you choose the right architectural pattern for your product.

---

## What are Architecture Patterns?

Architecture patterns define how your application is structured and how components interact. They provide proven solutions for organizing code and managing complexity.

**Purpose:**
- Organize codebase structure
- Separate concerns
- Enable scalability
- Facilitate testing
- Guide team development
- Support maintainability

---

## Pattern 1: Monolithic Architecture

**Description:**
All components of the application run in a single codebase and deployment unit.

**Structure:**
```
Application
├── Frontend (React/Vue)
├── Backend (Express/Django)
├── Database (PostgreSQL)
└── All deployed together
```

**Example Stack:**
- Next.js (Full-stack framework)
- Django (Python monolith)
- Ruby on Rails
- Laravel (PHP)

**Pros:**
- Simple to develop and deploy
- Easy to debug (everything in one place)
- No network latency between components
- Good for small to medium apps
- Lower infrastructure costs

**Cons:**
- Harder to scale (all or nothing)
- Tight coupling between components
- Deployment risk (one bug affects everything)
- Can become complex over time

**Best For:**
- MVPs and early-stage products
- Small teams (1-10 developers)
- Apps with straightforward requirements
- Internal tools and admin panels

**Example (Next.js Monolith):**
```
/app
├── /api (Backend API routes)
│   ├── /api/tasks
│   └── /api/users
├── /app (Frontend pages)
│   ├── /app/dashboard
│   └── /app/tasks
└── /lib (Shared utilities)
```

---

## Pattern 2: Microservices Architecture

**Description:**
Application split into independent services, each handling specific business capabilities.

**Structure:**
```
Frontend App
    ↓
API Gateway
    ↓
├── User Service (Auth, profiles)
├── Task Service (Tasks, projects)
├── Notification Service (Emails, push)
└── Analytics Service (Tracking, reports)
    ↓
Multiple Databases (each service owns its data)
```

**Technologies:**
- Docker / Kubernetes for orchestration
- Message queues (RabbitMQ, Kafka)
- API Gateway (Kong, AWS API Gateway)
- Service mesh (Istio, Linkerd)

**Pros:**
- Independent scaling (scale what you need)
- Technology flexibility (different languages per service)
- Fault isolation (one service failure doesn't kill all)
- Parallel development (teams work independently)
- Easier to understand (each service is small)

**Cons:**
- Complex deployment and orchestration
- Network latency between services
- Distributed system challenges (eventual consistency)
- Higher infrastructure costs
- Requires DevOps expertise

**Best For:**
- Large, complex applications
- High-traffic products (millions of users)
- Teams with multiple squads
- Products requiring independent scaling

---

## Pattern 3: Serverless Architecture

**Description:**
Application runs on managed cloud functions (FaaS - Function as a Service) without managing servers.

**Structure:**
```
Frontend (Static hosting)
    ↓
API (AWS Lambda / Vercel Functions / Netlify Functions)
    ↓
Database (Firestore, DynamoDB, Supabase)
    ↓
Third-party services (Auth0, Stripe, etc.)
```

**Technologies:**
- **AWS Lambda** (Node.js, Python, etc.)
- **Vercel Functions** (Next.js)
- **Netlify Functions**
- **Cloudflare Workers**
- **Google Cloud Functions**

**Pros:**
- No server management
- Auto-scaling (0 to infinity)
- Pay per use (cost-efficient for low traffic)
- Fast deployment
- Focus on code, not infrastructure

**Cons:**
- Cold start latency (first request slow)
- Vendor lock-in
- Execution time limits (e.g., 15 min max for Lambda)
- Difficult to debug
- Not ideal for long-running tasks

**Best For:**
- Event-driven applications
- APIs with variable traffic
- Prototypes and MVPs
- Serverless-first teams
- Low to medium traffic apps

**Example (Vercel + Serverless Functions):**
```
/app
├── /app/page.tsx (Frontend)
└── /api
    ├── /api/tasks.ts (Serverless function)
    └── /api/users.ts (Serverless function)
```

---

## Pattern 4: JAMstack (Static Site Generation)

**Description:**
JavaScript, APIs, and Markup. Pre-rendered static pages served from CDN, with dynamic features via APIs.

**Structure:**
```
Static Site (HTML, CSS, JS)
    ↓ (Deployed to CDN)
Vercel / Netlify / Cloudflare Pages
    ↓ (Calls APIs for dynamic data)
Headless CMS + Third-party APIs
```

**Technologies:**
- **Next.js** (SSG)
- **Gatsby**
- **Astro**
- **Hugo** (Go)
- **11ty** (JavaScript)

**Pros:**
- Blazing fast (pre-rendered HTML)
- SEO-friendly (static HTML)
- Highly scalable (CDN distribution)
- Secure (no server to hack)
- Low cost (static hosting is cheap)

**Cons:**
- Build time increases with page count
- Not ideal for highly dynamic content
- Requires rebuild for content changes (unless using ISR)
- Limited real-time features

**Best For:**
- Blogs and content sites
- Marketing websites
- Documentation sites
- Portfolios
- E-commerce (with ISR)

---

## Pattern 5: Client-Server (Traditional SPA)

**Description:**
React/Vue SPA (Single Page Application) communicating with a separate backend API.

**Structure:**
```
Frontend (React SPA)
    ↓ (HTTP/REST or GraphQL)
Backend API (Express, Django, Rails)
    ↓
Database (PostgreSQL, MongoDB)
```

**Technologies:**
- **Frontend:** React, Vue, Angular
- **Backend:** Express, FastAPI, Django, Rails
- **Communication:** REST, GraphQL, tRPC

**Pros:**
- Clear separation of concerns
- Independent frontend/backend deployments
- Technology flexibility
- Good for teams with frontend/backend specialists

**Cons:**
- Requires managing two codebases
- SEO challenges (client-side rendering)
- Slower initial load (large JS bundle)
- CORS and authentication complexity

**Best For:**
- Web applications (dashboards, tools)
- Apps behind authentication
- Mobile + web apps (shared backend)
- Teams with frontend/backend split

---

## Pattern 6: Event-Driven Architecture

**Description:**
Components communicate via events rather than direct calls. Decoupled, asynchronous system.

**Structure:**
```
Service A (Publishes event: "Order Placed")
    ↓
Message Queue / Event Bus (RabbitMQ, Kafka, AWS SNS)
    ↓
├── Service B (Sends confirmation email)
├── Service C (Updates inventory)
└── Service D (Records analytics)
```

**Technologies:**
- **Message Queues:** RabbitMQ, AWS SQS, Redis Pub/Sub
- **Event Streaming:** Apache Kafka, AWS Kinesis
- **Event Bus:** AWS EventBridge, Google Pub/Sub

**Pros:**
- Loose coupling (services don't know about each other)
- Asynchronous processing (non-blocking)
- Scalable (add consumers as needed)
- Resilient (failures isolated)

**Cons:**
- Complex debugging (event flow unclear)
- Eventual consistency challenges
- Requires message broker infrastructure
- Ordering and duplicate handling

**Best For:**
- E-commerce platforms (order processing)
- Real-time analytics
- IoT applications
- Systems with complex workflows

---

## Pattern 7: Layered (N-Tier) Architecture

**Description:**
Application organized into horizontal layers, each with specific responsibilities.

**Layers:**
```
Presentation Layer (UI)
    ↓
Business Logic Layer (Services)
    ↓
Data Access Layer (Repositories)
    ↓
Database Layer (PostgreSQL, etc.)
```

**Example (Express + TypeScript):**
```
/src
├── /controllers (Presentation - Handle HTTP)
├── /services (Business Logic)
├── /repositories (Data Access)
└── /models (Database Models)
```

**Pros:**
- Clear separation of concerns
- Easy to test (mock layers)
- Familiar to most developers
- Good for traditional apps

**Cons:**
- Can become rigid
- Layers can be too abstract
- Performance overhead (many layers)

**Best For:**
- Traditional web applications
- Enterprise software
- CRUD-heavy applications

---

## Pattern 8: Hexagonal (Ports & Adapters)

**Description:**
Business logic at the center, isolated from external concerns (UI, databases, APIs). Adapters connect core to external systems.

**Structure:**
```
      [UI Adapter]
           ↓
    [Core Business Logic]
      ↙          ↘
[Database Adapter] [API Adapter]
```

**Benefits:**
- Highly testable (mock adapters)
- Framework-independent
- Easy to swap implementations

**Best For:**
- Complex business logic
- Apps requiring multiple interfaces (web, mobile, CLI)
- Long-term maintainability

---

## Pattern 9: Modular Monolith

**Description:**
Monolithic deployment with modular code organization. Combines benefits of monoliths and microservices.

**Structure:**
```
/src
├── /modules
│   ├── /users (User module - self-contained)
│   │   ├── controllers
│   │   ├── services
│   │   └── models
│   ├── /tasks (Task module)
│   └── /billing (Billing module)
└── /shared (Shared utilities)
```

**Pros:**
- Modular code (like microservices)
- Simple deployment (like monolith)
- Easy to split into microservices later
- Good balance of simplicity and structure

**Cons:**
- Requires discipline (prevent module coupling)
- Still shares database (harder to scale independently)

**Best For:**
- Growing startups
- Teams transitioning from monolith to microservices
- Medium-sized applications

---

## Pattern 10: Backend-for-Frontend (BFF)

**Description:**
Separate backend for each frontend (web, mobile, etc.), tailored to specific client needs.

**Structure:**
```
Web App → BFF (Web) ↘
                      ↘
Mobile App → BFF (Mobile) → Shared Backend Services
                      ↗
Desktop App → BFF (Desktop) ↗
```

**Pros:**
- Optimized APIs for each client
- No over-fetching/under-fetching
- Independent evolution

**Cons:**
- Code duplication
- More backends to maintain

**Best For:**
- Multi-platform products (web + mobile + desktop)
- GraphQL for web, REST for mobile

---

## Decision Guide

| Your Need | Recommended Pattern |
|---|---|
| MVP, small team | **Monolithic** (Next.js, Rails) |
| Blog, content site | **JAMstack** (Astro, Hugo, Next.js SSG) |
| SaaS dashboard | **Client-Server** (React + Express) |
| High traffic, scaling | **Microservices** or **Serverless** |
| Event-driven workflows | **Event-Driven** (Kafka, RabbitMQ) |
| Multi-platform app | **BFF** (Backend-for-Frontend) |
| Variable traffic | **Serverless** (Lambda, Vercel) |
| Complex business logic | **Hexagonal** or **Layered** |

---

## Hybrid Example: Next.js with Microservices

**Marketing Site (JAMstack):**
```
/ → Static pages (Next.js SSG)
/blog → Static blog (Markdown)
```

**App (Monolithic Next.js):**
```
/app → Server-side rendered (Next.js SSR)
```

**Backend Services (Microservices):**
```
User Service → Handles auth
Task Service → Handles tasks
Notification Service → Sends emails
```

---

## Common Mistakes

### 1. Premature Microservices
```
❌ Starting with microservices for a small app
✅ Start monolithic, split later if needed
```

### 2. Overengineering
```
❌ Using event-driven architecture for simple CRUD
✅ Match complexity to requirements
```

### 3. Ignoring Team Size
```
❌ Microservices with a 2-person team
✅ Monolith is fine for small teams
```

---

## Resources

- **Microservices Guide:** https://microservices.io/
- **Serverless Patterns:** https://serverlessland.com/patterns
- **JAMstack:** https://jamstack.org/
- **Architecture Patterns:** https://martinfowler.com/architecture/
