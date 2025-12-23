# Hosting

Platform and infrastructure options for deploying your application. Choose based on your technical requirements, budget, scale, and team expertise.

## Static Site Hosts

Platforms optimized for hosting static files (HTML, CSS, JavaScript) with global CDN distribution. These services excel at serving pre-built sites with no server-side processing, offering instant deployments, automatic scaling, and built-in performance optimization. Choose static hosting when building JAMstack applications, documentation sites, marketing pages, or any site where content can be pre-rendered at build time for maximum performance and security.

### Vercel
Next.js creators' platform optimized for frontend frameworks.
- **Best for:** Next.js, React, Vue, Svelte apps
- **Features:** Edge functions, automatic HTTPS, preview deployments, analytics
- **Performance:** Global edge network, automatic optimization
- **Pricing:** Free hobby tier, Pro from $20/month
- **Deployment:** Git push, CLI, or drag-and-drop

### Netlify
Pioneer of JAMstack hosting with powerful features.
- **Best for:** Static sites, JAMstack applications
- **Features:** Forms, functions, identity, split testing, plugins
- **Performance:** Global CDN, instant cache invalidation
- **Pricing:** Free tier generous, Pro from $19/month
- **Deployment:** Git-based, CLI, drag-and-drop

### GitHub Pages
Free static hosting directly from GitHub repositories.
- **Best for:** Documentation, portfolios, open source projects
- **Features:** Custom domains, HTTPS, Jekyll support
- **Performance:** GitHub's CDN
- **Pricing:** Free for public repos
- **Deployment:** Git push to gh-pages branch

### Cloudflare Pages
Fast static hosting with Cloudflare's network.
- **Best for:** Static sites with advanced CDN needs
- **Features:** Workers integration, analytics, Web3 gateways
- **Performance:** Cloudflare's global network
- **Pricing:** Free tier unlimited, Pro from $20/month
- **Deployment:** Git integration, direct upload

### Surge.sh
Simple, single-command static hosting.
- **Best for:** Quick demos, prototypes
- **Features:** Custom domains, clean URLs, CORS
- **Performance:** Global CDN
- **Pricing:** Free tier, Pro from $30/month
- **Deployment:** CLI only

### GitLab Pages
Static hosting integrated with GitLab.
- **Best for:** GitLab users, documentation
- **Features:** CI/CD integration, access control
- **Performance:** GitLab's CDN
- **Pricing:** Free with GitLab
- **Deployment:** GitLab CI/CD

## Platform-as-a-Service (PaaS)

Managed platforms that handle infrastructure complexity while allowing you to deploy backend applications with minimal configuration. PaaS solutions manage servers, networking, storage, and runtime environments, letting you focus on code rather than operations. Choose PaaS when you need backend functionality, want automatic scaling and maintenance, prefer git-push deployments, or lack dedicated DevOps resources.

### Heroku
Developer-friendly platform with add-ons ecosystem.
- **Best for:** Rapid prototyping, small to medium apps
- **Features:** Add-ons marketplace, buildpacks, review apps
- **Languages:** Node.js, Ruby, Python, Java, PHP, Go
- **Pricing:** Free tier removed, Basic from $7/month
- **Deployment:** Git push, GitHub integration

### Railway
Modern platform for deploying any application.
- **Best for:** Full-stack applications
- **Features:** Databases, background jobs, preview environments
- **Languages:** Any via Dockerfile
- **Pricing:** Usage-based, $5 credit/month free
- **Deployment:** Git push, CLI

### Render
Unified platform for all your apps and services.
- **Best for:** Modern web apps, APIs, databases
- **Features:** Automatic deploys, preview environments, managed databases
- **Languages:** Node.js, Python, Ruby, Go, Rust, Elixir
- **Pricing:** Free tier available, paid from $7/month
- **Deployment:** Git-based automatic

### Fly.io
Run apps close to users worldwide.
- **Best for:** Globally distributed apps
- **Features:** Edge computing, persistent storage, private networking
- **Languages:** Any via Docker
- **Pricing:** Free tier available, usage-based
- **Deployment:** CLI, Docker

### DigitalOcean App Platform
Simple PaaS from DigitalOcean.
- **Best for:** Developers familiar with DigitalOcean
- **Features:** Managed databases, automatic scaling, CDN
- **Languages:** Node.js, Python, Go, PHP, Ruby
- **Pricing:** From $5/month
- **Deployment:** GitHub, GitLab integration

## Cloud Providers

Comprehensive cloud computing platforms offering the full spectrum of infrastructure services from virtual machines to managed databases and AI services. These providers give you complete control and flexibility but require more technical expertise to configure and manage. Choose cloud providers when building complex applications, needing specific regional presence, requiring enterprise compliance certifications, or when you need access to specialized services like machine learning or IoT platforms.

### AWS (Amazon Web Services)
Most comprehensive cloud platform.
- **Best for:** Enterprise, complex requirements
- **Services:** EC2, S3, Lambda, RDS, 200+ services
- **Performance:** Global infrastructure
- **Pricing:** Pay-as-you-go, free tier available
- **Complexity:** High, steep learning curve

### Google Cloud Platform
Google's infrastructure for everyone.
- **Best for:** Big data, machine learning, Kubernetes
- **Services:** Compute Engine, App Engine, Cloud Run, Firebase
- **Performance:** Google's network
- **Pricing:** Pay-as-you-go, free tier and credits
- **Complexity:** Medium-high

### Microsoft Azure
Enterprise-focused cloud platform.
- **Best for:** Enterprise, .NET applications, hybrid cloud
- **Services:** VMs, App Service, Functions, Cosmos DB
- **Performance:** Global data centers
- **Pricing:** Pay-as-you-go, free tier available
- **Complexity:** Medium-high

### Alibaba Cloud
Leading cloud provider in Asia.
- **Best for:** Asian market, Chinese regulations
- **Services:** Similar to AWS offerings
- **Performance:** Strong in Asia-Pacific
- **Pricing:** Competitive, free trial
- **Complexity:** Medium

## Serverless Platforms

Function-as-a-Service platforms that run code in response to events without managing servers. You write functions that execute on-demand, automatically scale to handle any load, and charge only for actual compute time used. Choose serverless when building event-driven architectures, handling variable or unpredictable traffic, wanting to minimize operational overhead, or when you need to run code at the edge closer to users.

### AWS Lambda
Event-driven serverless computing.
- **Best for:** Microservices, event processing
- **Features:** Auto-scaling, pay-per-execution
- **Languages:** Node.js, Python, Java, Go, .NET
- **Pricing:** 1M requests free/month
- **Integration:** Deep AWS ecosystem

### Cloudflare Workers
Serverless at the edge.
- **Best for:** Edge computing, API gateways
- **Features:** Global deployment, KV storage, Durable Objects
- **Languages:** JavaScript, TypeScript, Rust, C++
- **Pricing:** 100K requests/day free
- **Performance:** Runs at edge locations

### Netlify Functions
Serverless functions integrated with Netlify.
- **Best for:** JAMstack applications
- **Features:** Background functions, scheduled functions
- **Languages:** JavaScript, TypeScript, Go
- **Pricing:** 125K requests/month free
- **Integration:** Seamless with Netlify

### Vercel Edge Functions
Serverless at Vercel's edge network.
- **Best for:** Next.js applications
- **Features:** Edge runtime, streaming responses
- **Languages:** JavaScript, TypeScript
- **Pricing:** Included in Vercel plans
- **Performance:** Global edge network

## Container Platforms

Managed container hosting services that run Docker containers without the complexity of orchestration systems like Kubernetes. These platforms handle container scheduling, scaling, and networking while you provide container images. Choose container platforms when you have dockerized applications, need consistent environments across development and production, want portability between cloud providers, or require more control than PaaS but less complexity than managing Kubernetes.

### Google Cloud Run
Fully managed serverless containers.
- **Best for:** Containerized apps without Kubernetes complexity
- **Features:** Auto-scaling, pay-per-use, custom domains
- **Pricing:** Free tier generous
- **Deployment:** Container registry, GitHub

### AWS Fargate
Serverless containers on AWS.
- **Best for:** AWS users wanting serverless containers
- **Features:** Works with ECS and EKS
- **Pricing:** Pay for vCPU and memory
- **Integration:** AWS ecosystem

### Azure Container Instances
Fastest way to run containers in Azure.
- **Best for:** Simple container workloads
- **Features:** Fast startup, per-second billing
- **Pricing:** Pay-per-second
- **Integration:** Azure services

## Specialized Hosting

Platforms tailored for specific technologies or use cases, providing optimized environments and integrated tools for particular frameworks or applications. These services often include platform-specific features like visual editors, built-in e-commerce, or content management. Choose specialized hosting when using specific platforms like WordPress or Shopify, wanting integrated tools and workflows, needing platform-specific optimizations, or preferring all-in-one solutions over custom setups.

### WordPress.com
Managed WordPress hosting.
- **Best for:** WordPress sites
- **Features:** Automatic updates, backups, security
- **Pricing:** Free with ads, paid from $4/month
- **Management:** Fully managed

### Shopify
E-commerce platform with hosting.
- **Best for:** Online stores
- **Features:** Complete e-commerce solution
- **Pricing:** From $39/month
- **Management:** Fully managed

### Ghost(Pro)
Managed Ghost CMS hosting.
- **Best for:** Publications, newsletters
- **Features:** Built-in membership, newsletter
- **Pricing:** From $11/month
- **Management:** Fully managed

### Webflow
Visual web design with hosting.
- **Best for:** Design-focused sites
- **Features:** Visual editor, CMS
- **Pricing:** From $14/month
- **Management:** Fully managed

## VPS Providers

Virtual Private Server providers offering raw compute resources with full root access and complete control over the operating system. VPS gives you dedicated resources at a fraction of the cost of physical servers, with the flexibility to install any software and configure any environment. Choose VPS when you need full server control, want to run custom software stacks, require specific server configurations, or when managed solutions are too restrictive or expensive for your needs.

### DigitalOcean
Developer-friendly cloud infrastructure.
- **Best for:** Developers wanting simplicity
- **Products:** Droplets, Kubernetes, Spaces
- **Pricing:** From $4/month
- **Management:** Self-managed

### Linode (Akamai)
Reliable VPS with good performance.
- **Best for:** Traditional VPS needs
- **Products:** Compute, Kubernetes, Object Storage
- **Pricing:** From $5/month
- **Management:** Self-managed

### Vultr
High-performance SSD cloud.
- **Best for:** Global deployment needs
- **Products:** Cloud Compute, Bare Metal, Kubernetes
- **Pricing:** From $2.50/month
- **Management:** Self-managed

### Hetzner
European cloud provider with great value.
- **Best for:** European projects, budget-conscious
- **Products:** Cloud servers, dedicated servers
- **Pricing:** From €3.79/month
- **Management:** Self-managed

## Selection Criteria

Key factors to evaluate when choosing a hosting solution. These criteria help you match technical requirements with operational capabilities while considering cost, performance, and growth potential.

Consider these factors:

- **Application Type:** Static vs. dynamic, serverless vs. traditional
- **Technical Skills:** Managed services vs. self-managed infrastructure
- **Scale:** Current traffic and growth projections
- **Budget:** Fixed vs. usage-based pricing
- **Geographic Needs:** User location, data residency requirements
- **Performance:** CDN, edge computing needs
- **Developer Experience:** Deployment ease, debugging tools
- **Ecosystem:** Additional services needed (database, storage, etc.)
- **Support:** Community vs. paid support options
- **Compliance:** Industry regulations, certifications

---

*Choose hosting that aligns with your technical requirements and team capabilities. Start simple and scale up as needed—modern platforms make migration easier than ever.*