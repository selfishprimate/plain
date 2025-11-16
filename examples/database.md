# Database: Options & Examples

This guide helps you choose the right database for your product.

---

## Option 1: None (Fully Static)

**Best for:** Static sites, no dynamic data

**Description:**
No database needed. All content is static (JSON files, Markdown) and bundled at build time.

**Pros:**
- Simplest option
- No infrastructure costs
- Fastest performance
- No security concerns
- Easy to host

**Cons:**
- No user-generated content
- No real-time updates (requires rebuild)
- No personalization
- Limited to static data

**Best Use Cases:**
- Landing pages
- Portfolios
- Blogs (with static files)
- Documentation

**Tech Stack:**
- JSON files or Markdown
- Static site generators (Hugo, Astro, 11ty)

---

## Option 2: Firestore (Firebase)

**Best for:** Real-time apps, rapid prototyping, NoSQL

**Description:**
Firestore is a NoSQL cloud database from Google Firebase. It's document-based, real-time, and scales automatically.

**Type:** NoSQL (Document-based)

**Pros:**
- Real-time synchronization
- Easy to set up (no backend needed)
- Generous free tier
- Automatic scaling
- Offline support
- SDKs for web, mobile, backend
- Built-in security rules

**Cons:**
- Limited querying capabilities
- Can get expensive at scale
- Vendor lock-in
- Not ideal for complex relational data
- Costs based on reads/writes

**Pricing:**
- **Free (Spark):** 1GB storage, 50K reads/day
- **Blaze (Pay-as-you-go):** $0.06 per 100K reads

**Best Use Cases:**
- Real-time chat apps
- Collaborative tools
- User profiles and preferences
- Bookmarks and favorites
- Activity feeds
- Mobile apps

**Example Schema:**
```javascript
// Collection: users
{
  uid: "user123",
  name: "John Doe",
  email: "john@example.com",
  bookmarks: ["tool1", "tool2"]
}

// Collection: tools
{
  id: "chatgpt",
  name: "ChatGPT",
  category: "ai-writing",
  upvotes: 245
}
```

**Example Code:**
```javascript
import { collection, addDoc } from "firebase/firestore";

// Add a document
await addDoc(collection(db, "tools"), {
  name: "ChatGPT",
  category: "ai-writing"
});
```

**Learn More:** https://firebase.google.com/docs/firestore

---

## Option 3: Supabase (PostgreSQL)

**Best for:** Relational data, open-source, SQL power

**Description:**
Supabase is an open-source Firebase alternative built on PostgreSQL. It offers a SQL database with real-time capabilities, authentication, and storage.

**Type:** SQL (PostgreSQL)

**Pros:**
- Open-source
- Full SQL power (joins, views, functions)
- Real-time subscriptions
- Row-level security
- Self-hostable
- Generous free tier
- Great developer experience
- Auth and storage included

**Cons:**
- More complex than Firestore
- Requires SQL knowledge
- Setup can be overwhelming for beginners

**Pricing:**
- **Free:** 500MB database, 1GB file storage
- **Pro:** $25/month (8GB database)
- **Self-hosted:** Free (you manage)

**Best Use Cases:**
- Apps requiring complex queries
- Relational data (users, posts, comments)
- Apps that may need to migrate later
- Open-source projects
- Startups wanting SQL power

**Example Schema:**
```sql
-- Users table
CREATE TABLE users (
  id UUID PRIMARY KEY,
  name TEXT,
  email TEXT UNIQUE,
  created_at TIMESTAMP DEFAULT NOW()
);

-- Tools table
CREATE TABLE tools (
  id UUID PRIMARY KEY,
  name TEXT,
  category TEXT,
  user_id UUID REFERENCES users(id)
);

-- Bookmarks table (many-to-many)
CREATE TABLE bookmarks (
  user_id UUID REFERENCES users(id),
  tool_id UUID REFERENCES tools(id),
  created_at TIMESTAMP DEFAULT NOW(),
  PRIMARY KEY (user_id, tool_id)
);
```

**Example Code:**
```javascript
import { createClient } from '@supabase/supabase-js'

const supabase = createClient(URL, KEY)

// Query with joins
const { data } = await supabase
  .from('tools')
  .select('*, users(name)')
  .eq('category', 'ai-writing')
```

**Learn More:** https://supabase.com

---

## Option 4: PostgreSQL (Self-Hosted or Managed)

**Best for:** Full control, complex queries, production apps

**Description:**
PostgreSQL is the most popular open-source relational database. It's powerful, standards-compliant, and battle-tested.

**Type:** SQL (Relational)

**Hosting Options:**

### Managed PostgreSQL:
- **Supabase** — Postgres + extras
- **Railway** — Simple PaaS with Postgres
- **Neon** — Serverless Postgres with branching
- **AWS RDS** — Enterprise-grade
- **DigitalOcean Managed DB** — Affordable

### Self-Hosted:
- VPS (DigitalOcean, Hetzner)
- Docker container

**Pros:**
- Industry standard
- Full SQL power
- ACID transactions
- Complex queries, joins, views
- Mature ecosystem
- Great for relational data
- Extensions (PostGIS, full-text search)

**Cons:**
- Requires backend (can't access directly from frontend)
- More setup than Firestore
- Scaling requires management
- SQL knowledge needed

**Pricing:**
- **Self-hosted:** VPS costs (~$5-20/month)
- **Managed:** From $7/month (Neon, Railway) to $15+ (RDS)

**Best Use Cases:**
- Production applications
- Complex relational data
- E-commerce platforms
- Multi-tenant SaaS
- Apps requiring transactions

**Example with Prisma ORM:**
```prisma
// schema.prisma
model User {
  id        String   @id @default(uuid())
  email     String   @unique
  tools     Tool[]
}

model Tool {
  id        String   @id @default(uuid())
  name      String
  userId    String
  user      User     @relation(fields: [userId], references: [id])
}
```

**Learn More:** https://postgresql.org

---

## Option 5: MongoDB

**Best for:** Flexible schemas, rapid iteration, unstructured data

**Description:**
MongoDB is a popular NoSQL document database. It stores data as JSON-like documents with flexible schemas.

**Type:** NoSQL (Document-based)

**Hosting Options:**
- **MongoDB Atlas** — official managed service
- **Self-hosted** — on VPS

**Pros:**
- Flexible schema (no migrations)
- Great for rapidly changing data
- Easy to scale horizontally
- JSON-like documents
- Good query language
- Works well with Node.js

**Cons:**
- Can lead to data inconsistency
- Not ideal for relational data
- Requires careful planning
- Atlas can get expensive

**Pricing:**
- **Atlas Free (M0):** 512MB storage
- **Atlas Shared:** From $9/month
- **Self-hosted:** VPS costs

**Best Use Cases:**
- Content management systems
- Catalogs with varying attributes
- Logging and analytics
- Rapid prototyping
- Apps with frequently changing schemas

**Example Schema:**
```javascript
// User document
{
  _id: ObjectId("..."),
  name: "John Doe",
  email: "john@example.com",
  bookmarks: [
    { toolId: "1", addedAt: ISODate("...") },
    { toolId: "2", addedAt: ISODate("...") }
  ]
}
```

**Example with Mongoose:**
```javascript
const userSchema = new mongoose.Schema({
  name: String,
  email: { type: String, unique: true },
  bookmarks: [{ toolId: String, addedAt: Date }]
});
```

**Learn More:** https://mongodb.com

---

## Option 6: Local Storage / IndexedDB

**Best for:** Client-side only, offline-first apps

**Description:**
Store data directly in the user's browser. No backend or database server needed.

**Options:**

### localStorage
- **Limit:** ~5-10MB
- **Type:** Key-value (strings only)
- **Best for:** Small settings, preferences

### IndexedDB
- **Limit:** ~50MB+ (varies by browser)
- **Type:** Object store (structured data)
- **Best for:** Offline data, caching

**Pros:**
- No backend needed
- Free
- Fast (local access)
- Works offline
- Simple to implement

**Cons:**
- Data only on user's device
- No sync across devices
- Limited storage
- User can clear data
- No server-side access

**Best Use Cases:**
- User preferences and settings
- Offline-first apps
- Drafts and temporary data
- Client-side caching

**Example (localStorage):**
```javascript
// Save
localStorage.setItem('theme', 'dark');

// Retrieve
const theme = localStorage.getItem('theme');
```

**Example (IndexedDB with Dexie):**
```javascript
import Dexie from 'dexie';

const db = new Dexie('MyDatabase');
db.version(1).stores({
  tools: '++id, name, category'
});

// Add data
await db.tools.add({ name: 'ChatGPT', category: 'AI' });
```

---

## Option 7: Serverless Databases

**Best for:** Auto-scaling, pay-per-use, edge performance

### PlanetScale
- **Type:** MySQL (serverless)
- **Pros:** Branching, auto-scaling, generous free tier
- **Cons:** MySQL only
- **Learn More:** https://planetscale.com

### Neon
- **Type:** Postgres (serverless)
- **Pros:** Branching, scale-to-zero, affordable
- **Learn More:** https://neon.tech

### Turso (libSQL)
- **Type:** SQLite-compatible (edge)
- **Pros:** Embedded, replicated, fast
- **Learn More:** https://turso.tech

### Upstash Redis
- **Type:** Redis (serverless)
- **Pros:** Low-latency, key-value, free tier
- **Learn More:** https://upstash.com

**Best Use Cases:**
- Variable traffic apps
- Edge functions
- Global low-latency needs
- Cost-sensitive projects

---

## Decision Guide

| **Your Need** | **Recommended Database** |
|---|---|
| No user data, static content | None (JSON files) |
| Real-time sync, rapid prototype | Firestore |
| Relational data, SQL power | Supabase or PostgreSQL |
| Flexible schema, rapid changes | MongoDB |
| Client-side only, offline | localStorage / IndexedDB |
| Complex queries, production | PostgreSQL |
| Serverless, auto-scale | Neon, PlanetScale, Turso |
| Simple key-value caching | Upstash Redis |

---

## Comparison Table

| **Database** | **Type** | **Ease of Use** | **Scalability** | **Cost** | **Best For** |
|---|---|---|---|---|---|
| None | N/A | Easiest | N/A | Free | Static sites |
| Firestore | NoSQL | Easy | Auto | Low-Medium | Real-time apps |
| Supabase | SQL | Medium | Good | Low | SQL power + ease |
| PostgreSQL | SQL | Medium | Manual | Low-Medium | Production apps |
| MongoDB | NoSQL | Easy | Good | Medium | Flexible data |
| localStorage | Client | Easy | N/A | Free | Client-side only |
| Neon/PlanetScale | SQL | Easy | Auto | Low | Serverless SQL |

---

## Example Tech Stacks

**Real-Time Chat App**
- Frontend: React + Vite
- Database: Firestore
- Auth: Firebase Auth

**SaaS Dashboard**
- Frontend: Next.js
- Database: Supabase (PostgreSQL)
- ORM: Prisma
- Auth: Supabase Auth

**E-commerce Platform**
- Frontend: Next.js
- Database: PostgreSQL (managed on Railway)
- ORM: Drizzle or Prisma
- Payments: Stripe

**Content Site with User Accounts**
- Frontend: Astro
- CMS: Sanity
- Database: Firestore (for user bookmarks)
- Auth: Firebase Auth

**Offline-First PWA**
- Frontend: React
- Storage: IndexedDB
- Sync: PouchDB + CouchDB
