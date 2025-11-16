# Hosting & Deployment: Options & Examples

This guide helps you choose the right hosting and deployment platform for your product.

---

## Option 1: Vercel

**Best for:** Next.js apps, serverless, instant deploys

**Description:**
Vercel is a cloud platform optimized for frontend frameworks, especially Next.js (which they created). It offers instant deployments, serverless functions, and edge network.

**Supported Frameworks:**
- Next.js (best support)
- React, Vue, Svelte, Astro
- Any static site

**Pros:**
- Fastest deployments
- Excellent Next.js support
- Automatic preview deploys for PRs
- Edge functions and middleware
- Built-in analytics
- Free SSL certificates
- Generous free tier

**Cons:**
- Can get expensive at scale
- Vendor lock-in (especially with Next.js)
- Limited backend capabilities (serverless only)
- Build time limits on free tier

**Pricing:**
- **Free:** Hobby projects, unlimited sites
- **Pro:** $20/month per user
- **Enterprise:** Custom pricing

**Best Use Cases:**
- Next.js applications
- Jamstack sites
- Serverless apps
- Landing pages and marketing sites

**Deployment:**
```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

**Learn More:** https://vercel.com

---

## Option 2: Netlify

**Best for:** Static sites, Jamstack, form handling

**Description:**
Netlify is a platform for deploying static sites and serverless functions. Great for Jamstack architecture with built-in forms, authentication, and edge functions.

**Supported Frameworks:**
- Any static site generator
- React, Vue, Svelte
- Astro, Hugo, 11ty
- Next.js (limited SSR support)

**Pros:**
- Simple deployment (git push)
- Built-in forms (no backend needed)
- Netlify Identity (authentication)
- Split testing and analytics
- Excellent documentation
- Generous free tier

**Cons:**
- Less optimized for Next.js than Vercel
- Build minutes limited on free tier
- Functions can be slow to cold start
- Less advanced than Vercel for modern frameworks

**Pricing:**
- **Free:** Personal projects
- **Pro:** $19/month
- **Business:** $99/month

**Best Use Cases:**
- Static sites and blogs
- Jamstack apps
- Hugo, 11ty, Astro sites
- Landing pages with forms

**Deployment:**
```bash
# Install Netlify CLI
npm install -g netlify-cli

# Deploy
netlify deploy --prod
```

**Learn More:** https://netlify.com

---

## Option 3: GitHub Pages

**Best for:** Free hosting, static sites, open-source projects

**Description:**
GitHub Pages is a free hosting service for static sites, directly from a GitHub repository. Perfect for documentation, portfolios, and simple sites.

**Supported:**
- Static HTML/CSS/JS
- Jekyll (built-in support)
- Any static site generator (with manual build)

**Pros:**
- Completely free
- Simple setup (just push to repo)
- Custom domains supported
- Free SSL
- Integrated with GitHub workflow

**Cons:**
- Static sites only (no serverless functions)
- Limited build options
- Slower than modern platforms
- No preview deploys
- 1GB storage limit

**Pricing:**
- **Free:** Forever

**Best Use Cases:**
- Documentation sites
- Personal portfolios
- Open-source project pages
- Simple landing pages

**Deployment:**
```bash
# Enable GitHub Pages in repository settings
# Push to gh-pages branch or docs folder
```

**Learn More:** https://pages.github.com

---

## Option 4: Cloudflare Pages

**Best for:** Global edge network, fast performance, affordable

**Description:**
Cloudflare Pages is a Jamstack platform built on Cloudflare's global network. Offers fast performance with edge functions and generous free tier.

**Supported Frameworks:**
- Next.js, React, Vue, Svelte
- Astro, Hugo, 11ty
- Any static site

**Pros:**
- Cloudflare's global CDN (fast everywhere)
- Unlimited bandwidth (even on free tier)
- Generous build minutes
- Workers (edge functions) included
- Free SSL
- Great performance

**Cons:**
- Less mature than Vercel/Netlify
- Fewer integrations
- More complex setup for some features
- Dashboard can be overwhelming

**Pricing:**
- **Free:** Unlimited sites, unlimited bandwidth
- **Pro:** $20/month (advanced features)

**Best Use Cases:**
- Global performance-critical sites
- High-traffic sites (free bandwidth)
- Edge-first applications
- Static sites and Jamstack

**Deployment:**
```bash
# Connect GitHub repo via dashboard
# Or use Wrangler CLI
npx wrangler pages publish dist
```

**Learn More:** https://pages.cloudflare.com

---

## Option 5: Firebase Hosting

**Best for:** Firebase ecosystem, simple static sites

**Description:**
Firebase Hosting is a fast and secure hosting service for static content. Works seamlessly with other Firebase services like Auth, Firestore, and Functions.

**Supported:**
- Static sites
- Single-page apps (React, Vue, etc.)
- Works with Firebase Functions for backend

**Pros:**
- Fast CDN
- Free SSL
- Integrates with Firebase ecosystem
- Simple CLI deployment
- Generous free tier
- Custom domains

**Cons:**
- Best for Firebase users
- Limited features compared to Vercel/Netlify
- No automatic git deploys
- Less optimized for modern frameworks

**Pricing:**
- **Spark (Free):** 10GB storage, 360MB/day transfer
- **Blaze (Pay as you go):** Affordable scaling

**Best Use Cases:**
- Firebase-based apps
- Static sites with Firebase backend
- Simple SPAs
- Projects already using Firebase

**Deployment:**
```bash
# Install Firebase CLI
npm install -g firebase-tools

# Deploy
firebase deploy
```

**Learn More:** https://firebase.google.com/docs/hosting

---

## Option 6: Custom Server (VPS / Cloud)

**Best for:** Full control, custom backends, complex needs

**Description:**
Self-host on a Virtual Private Server (VPS) or cloud provider. Requires server management but offers complete control.

**Providers:**

### DigitalOcean
- **Pros:** Simple, affordable, good docs
- **Pricing:** From $6/month
- **Learn More:** https://digitalocean.com

### AWS (EC2, Amplify)
- **Pros:** Scalable, enterprise-grade, many services
- **Cons:** Complex, expensive, steep learning curve
- **Learn More:** https://aws.amazon.com

### Google Cloud Platform
- **Pros:** Powerful, global network
- **Cons:** Complex pricing
- **Learn More:** https://cloud.google.com

### Linode (Akamai)
- **Pros:** Affordable, simple
- **Pricing:** From $5/month
- **Learn More:** https://linode.com

### Hetzner
- **Pros:** Cheapest, powerful
- **Cons:** EU-based (GDPR compliant)
- **Pricing:** From €4/month
- **Learn More:** https://hetzner.com

**Pros:**
- Full control
- No vendor lock-in
- Cheaper at scale
- Custom configurations
- Run any backend

**Cons:**
- Requires DevOps knowledge
- Server management and updates
- Security is your responsibility
- Manual deployment setup
- No automatic scaling

**Best Use Cases:**
- Custom backends
- Long-running services
- Complex applications
- Cost-sensitive large-scale apps

**Deployment:**
```bash
# Example with Docker on VPS
ssh user@your-server
git pull
docker-compose up -d
```

---

## Option 7: Platform-as-a-Service (PaaS)

**Best for:** Managed infrastructure, easy scaling

### Render
- **Description:** Modern PaaS, easy deploys
- **Pros:** Free tier, automatic SSL, easy setup
- **Cons:** Can be slow on free tier
- **Pricing:** Free tier, then from $7/month
- **Learn More:** https://render.com

### Railway
- **Description:** Developer-first PaaS
- **Pros:** Great DX, usage-based pricing
- **Cons:** No free tier anymore
- **Pricing:** Pay for what you use (~$5+/month)
- **Learn More:** https://railway.app

### Fly.io
- **Description:** Global app platform
- **Pros:** Deploy close to users, Docker-based
- **Cons:** Learning curve
- **Pricing:** Free allowance, then pay-as-you-go
- **Learn More:** https://fly.io

### Heroku
- **Description:** Original PaaS (declining)
- **Cons:** Expensive, removed free tier
- **Pricing:** From $5-7/month
- **Learn More:** https://heroku.com

**Best Use Cases:**
- Full-stack apps
- Apps with backends
- Database-driven apps
- Docker containers

---

## Decision Guide

| **Your Project** | **Recommended Hosting** |
|---|---|
| Next.js app | Vercel |
| Static site or blog | Netlify or Cloudflare Pages |
| Free personal site | GitHub Pages |
| Firebase app | Firebase Hosting |
| High traffic, free bandwidth | Cloudflare Pages |
| Full-stack app with backend | Render, Railway, or Fly.io |
| Custom backend needs | VPS (DigitalOcean, Hetzner) |
| Enterprise scale | AWS, GCP, or Vercel Enterprise |

---

## Comparison Table

| **Platform** | **Free Tier** | **Serverless** | **Backend Support** | **Best For** |
|---|---|---|---|---|
| Vercel | Yes | Yes | Limited | Next.js, Jamstack |
| Netlify | Yes | Yes | Limited | Static sites, forms |
| GitHub Pages | Yes | No | No | Simple static sites |
| Cloudflare Pages | Yes (generous) | Yes | Yes (Workers) | Global performance |
| Firebase Hosting | Yes | Via Functions | Yes (Functions) | Firebase ecosystem |
| Render | Yes | No | Yes (full) | Full-stack apps |
| Railway | No | No | Yes (full) | Full-stack apps |
| DigitalOcean | No | No | Yes (full) | Custom backends |

---

## CI/CD Integration

Most platforms support automatic deployment from Git:

**Vercel:**
- Connect GitHub repo
- Auto-deploy on push to `main`
- Preview deploys for PRs

**Netlify:**
- Connect GitHub/GitLab/Bitbucket
- Branch deploys
- Deploy previews

**Cloudflare Pages:**
- Connect GitHub/GitLab
- Branch deploys

**GitHub Pages:**
- GitHub Actions workflow
- Deploy on push

**Example GitHub Actions (Vercel):**
```yaml
name: Deploy to Vercel
on:
  push:
    branches: [main]
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - run: npm install
      - run: npm run build
      - uses: amondnet/vercel-action@v20
```

---

## Final Recommendations

**Beginners / MVPs:**
- Vercel (Next.js) or Netlify (static)

**Cost-conscious:**
- Cloudflare Pages or GitHub Pages

**Firebase users:**
- Firebase Hosting

**Full-stack apps:**
- Render or Railway

**Enterprise / Scale:**
- Vercel Enterprise or AWS
