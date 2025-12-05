# PLAIN: Product Language for AI Notation

**PLAIN** is a structured, markdown-based specification format designed to transform product ideas into AI-ready documentation. It provides 16 well-defined sections that cover design language, requirements, architecture, and implementation details — bridging the gap between product teams and AI development tools.

PLAIN serves as a universal product definition language that both humans and AI tools can understand and act on.

## What is PLAIN? 🤔

**PLAIN (Product Language for AI Notation)** is a standardized documentation framework that turns rough product ideas into structured, actionable blueprints. Unlike traditional specs scattered across tools and documents, a PLAIN file consolidates your product's design vision, technical foundation, and user experience into a single, AI-friendly markdown document.

- **Defines product vision clearly:** Every PLAIN document starts with an "Idea Statement" — a short, focused summary of what the product is, who it's for, and what problem it solves.

- **Describes visual and UX direction:** Through sections like Design Language, Color, Typography, Layout, and Icons, PLAIN enables teams to codify a product's look and feel in structured natural language.

- **Documents requirements systematically:** PLAIN splits requirements into Functional and Non-Functional sections, ensuring features, edge cases, performance expectations, accessibility needs, and localization goals are all defined clearly.

- **Aligns on technical decisions from day one:** With sections covering State Management, Architecture Pattern, Route Design, and API Specification, developers gain clarity early — reducing back-and-forth between teams.

- **Serves as a single source of truth:** A PLAIN document evolves with your product — it's a living artifact that can be updated, forked for new features, or integrated into AI workflows.

## Who is it for? 👩🏿‍💻

- **AI tools** like [v0](https://v0.dev/), [Bolt](https://bolt.new/), [Lovable](https://lovable.dev/), [Figma Make](https://www.figma.com/), and [Stitch](https://stitch.withgoogle.com/) that turn natural language into interfaces or code
- **Designers** who need to translate product requirements into scalable systems, tokens, and layouts
- **Developers** who want clarity and consistency in technical handoffs, including routing, architecture patterns, and data flow
- **Product managers** who want to replace messy Google Docs with a clean, AI-first way of describing what to build and why

## The 16 Sections of PLAIN 📋

Each PLAIN document is organized into 16 structured sections:

1. **Idea Statement** — The product's purpose, problem, audience, and value proposition
2. **Design Language** — Visual tone, style references, and overall aesthetic direction
3. **Color Palette** — Primary, secondary, and semantic color definitions
4. **Typography** — Font families, scales, weights, and text hierarchy
5. **Layout** — Grid systems, spacing, breakpoints, and responsive behavior
6. **Icons** — Icon style, library choice, and usage guidelines
7. **Core Components** — Reusable UI elements and their variants
8. **Page Map** — High-level structure of pages, routes, and navigation
9. **User Stories** — Key user flows and scenarios written from the user's perspective
10. **Functional Requirements** — Features, interactions, and behaviors the product must support
11. **Non-Functional Requirements** — Performance, accessibility, security, and localization needs
12. **Content Management** — How content is created, stored, and updated
13. **State Management** — Data flow, local vs global state, and state libraries
14. **Architecture Pattern** — Overall system structure and technical approach
15. **Frontend Technology** — Languages, frameworks, and libraries to be used
16. **API Specification** — Endpoint design, authentication, and data contracts

## How to Use PLAIN 💪

### Step 1: Write an Idea Statement
Start with a clear, 1–2 paragraph description of your product. Explain the problem it solves, who it's for, and its main value proposition.

**Example:**
> Taskly is a lightweight task manager for freelancers, enabling fast capture of daily tasks, deadline reminders, and seamless syncing across devices. It helps independent workers stay organized without the clutter of enterprise tools.

### Step 2: Generate the Full Document with AI
Feed your Idea Statement to an AI tool and ask it to generate a complete PLAIN document based on the 16-section structure.

**Prompt Example:**
> "You are an expert product designer and developer. Based on the following product idea, generate a complete product specification using the PLAIN format. Follow the 16-section structure defined in plain.md."
>
> Idea Statement: [Your statement here]

### Step 3: Review and Refine
Review the generated document with your team. Improve vague or misaligned content, validate assumptions, and ensure consistency across sections.

### Step 4: Feed to AI Development Tools
Use the finalized PLAIN document as input to tools like **v0**, **Bolt**, **Lovable**, or **Cursor** to generate UI screens, component libraries, or even production code.

**Prompt Example:**
> "Use the following PLAIN document to generate the initial UI screens. Prioritize the onboarding and task creation flows. Use Shadcn components and Tailwind utility classes."
>
> [Paste your PLAIN document]

### Step 5: Iterate and Evolve
Update your PLAIN document as your product grows. Fork it for new features, link it to design systems, or integrate it into build pipelines.

## Why Markdown? 📂

Markdown offers unique advantages for structured product documentation:

- **Easily integrated into codebases** — Fits naturally into Git repositories and version-controlled environments
- **AI-friendly** — Plain text format that can be easily read, parsed, edited, and regenerated by AI
- **Human-readable** — Clean and simple to read in any text editor
- **Lightweight & portable** — Small file size, cross-platform, easy to back up and share

By using `.md` files, PLAIN documents offer effortless human collaboration and seamless AI integration.

## Getting Started 🚀

1. Check out the `/demos/` folder for real-world examples
2. Read `plain.md` for the complete format specification
3. Review `plain-explained.md` for detailed section guidance
4. Use the `/prompts/` folder for effective AI prompt templates

## Related Projects 🔗

- **[Plainify](https://github.com/selfishprimate/plainify)** — A visual editor and form-based tool for generating PLAIN documents

## License 📄

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Contributing 🙌

Want to improve PLAIN? Read the [Contribution Guidelines](./CONTRIBUTING.md) and submit a PR!

## Community & Support 💬

- Open an issue for bugs or feature requests
- Share your PLAIN documents in the discussions section
- Follow updates and best practices in the wiki

---

**PLAIN** is an open-source project maintained by [Halil İbrahim Çakıroğlu](https://github.com/selfishprimate).
