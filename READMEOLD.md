# PLAIN: Product Language for AI Notation

**PLAIN** is a structured documentation framework designed to help you define digital products in a format that’s both human-friendly and machine-readable. It helps you turn rough product ideas into clean, markdown-based specs that AI tools and product teams can immediately act on — generating UI, code, or documentation.

It bridges the gap between product managers, designers, and AI-powered tools such as [v0](https://v0.dev/), [Figma Make](https://www.figma.com/), [Bolt](https://bolt.new/), [Stitch](https://stitch.withgoogle.com/), [Uizard](https://uizard.io/), and [Lovable](https://lovable.dev/).

With PLAIN, product ideas become structured assets — ready to be translated into user interfaces, code, and documentation by generative AI.

## What is PLAIN? 🤔
**PLAIN (Product Language for AI Notation)** is more than just a documentation format — it is a shared interface between product teams and intelligent systems. It transforms raw ideas into structured, readable, and generative blueprints for digital product development. Unlike traditional specs scattered across tools and documents, a PLAIN file consolidates your product’s design vision, technical foundation, and user experience into a single, AI-friendly markdown document.

- **Defines product vision clearly:** Every PLAIN document starts with an “Idea Statement” — a short, focused summary of what the product is, who it’s for, and what problem it solves. This concise declaration becomes the compass for the entire product definition, guiding both human collaborators and AI tools with a shared understanding of purpose.

- **Describes visual and UX direction:** Through well-scoped sections like Design Language, Color, Typography, Layout, and Icons, PLAIN enables teams to codify a product’s look and feel. These visual and interaction principles are laid out in natural language but structured enough for design automation tools to interpret and act on.

- **Documents requirements systematically:** PLAIN splits requirements into two dedicated sections: Functional and Non-Functional. This separation ensures that product features, edge cases, performance expectations, accessibility needs, and localization goals are all defined clearly, avoiding ambiguity or duplication in downstream development.

- **Aligns on technical decisions from day one:** The format goes beyond UI and feature scope. With areas like State Management, Architecture Pattern, Route Design, and API Specification, developers gain clarity early — reducing back-and-forth and improving alignment between product, design, and engineering teams.

- **Serves as a single source of truth:** A PLAIN document evolves with your product — it’s not a static spec, but a living artifact. It can be updated as your product grows, forked for new features, or integrated into AI workflows for generating UI, component libraries, or even production code.

## Who is it for? 👩🏿‍💻

- AI tools that turn natural language into interfaces or code. PLAIN gives them the structure and semantics they need to generate relevant, high-quality output.
- Designers who need to translate product requirements into scalable systems, tokens, and layouts — while collaborating with both AI and humans.
- Developers who want clarity and consistency in technical handoffs, including routing, architecture patterns, and data flow structures.
- Product managers and teams who want to replace messy Google Docs and scattered tools with a clean, AI-first way of describing what to build and why.

## How to Use 💪
The PLAIN format is designed to be usable by both humans and AI. Below are the core steps for using it effectively in an AI-powered product development workflow.

### Step 1: Start with a Clear Idea Statement
Write a short but meaningful description of your product idea. This becomes your **Idea Statement**, **the first and most important section of the PLAIN file**. It explains the product’s **purpose**, **the problem it solves**, **the target audience**, and its **main value proposition** — all in 1–2 short paragraphs.

**What makes a good Idea Statement?**
- It focuses on the user problem, not just the features.
- It sets a clear vision for the product’s role.
- It is specific enough to guide design and development decisions.
 
_Example Idea Statement_
> Taskly is a lightweight task manager for freelancers, enabling fast capture of daily tasks, deadline reminders, and seamless syncing across devices. It helps independent workers stay organized without the clutter of enterprise tools.

### Step 2: Feed the Idea Statement to AI using plain.md
Ask an AI to generate the full PLAIN document based on your **Idea Statement**. Provide the model with your statement and point it to plain.md as a reference guide for structure, tone, and output expectations.

_Prompt Example_
> “You are an expert product designer and developer. Based on the following product idea, generate a complete product specification using the PLAIN format. Refer to plain.md for section structure and sample outputs.”
>
> Idea Statement:
“Taskly is a lightweight task manager for freelancers, enabling fast capture of daily tasks, deadline reminders, and seamless syncing across devices. It helps independent workers stay organized without the clutter of enterprise tools.”

### Step 3: Review and Refine the Filled-Out PLAIN Document
Once you’ve submitted your **Idea Statement** and the base **plain.md** structure to the AI, you’ll receive a **filled-out PLAIN document** — a fully populated version where each section has been generated based on your initial input.

**This filled-out document represents your product’s first structured draft.** It includes everything from design language and core components to user flows and technical architecture — written in natural language but formatted for both humans and machines.

**Your job now is to review and refine this draft:**

Improve any vague, generic, or misaligned content. Validate assumptions and correct terminology where necessary. Ensure consistency in tone, structure, and product vision. **Collaboration with your product, design, and engineering teams is highly recommended to finalize the document.**

During the review, pay special attention to sections such as:
- Core Components
- Page Map
- Technical Stack
- Accessibility
- Visual Tone
- User Flows

These areas tend to influence many downstream design and development decisions.

**Note:** Once refined, this filled-out PLAIN document (plain-{project-name}.md) becomes your AI-readable blueprint — ready for use in design generation, prototyping, or code scaffolding.

### Step 4: Feed the Final Document to Prompt-to-Code Tools
Use your filled plain.md as input to tools like **v0**, **Bolt**, **Figma Make**, **Lovely**, or **Cursor**. These tools can parse the structured content and generate design systems, page layouts, or component code based on what you’ve described.

_Prompt Example_
> “Use the following PLAIN document to generate the initial UI screens. Prioritize the onboarding and task creation flows. Use Shadcn components and Tailwind utility classes.”
>
> (Paste completed plain-{project-name}.md content)

### Step 5: Iterate, Export, and Build

Refine the AI-generated outputs and continue development. You can adjust designs, regenerate sections, or fork versions of the document to match feature growth. PLAIN is a living artifact — update it as your product evolves.

**Bonus:** Link your PLAIN files to design systems, CMS schemas, or build pipelines to make them part of your team’s workflow.

## Why Markdown? 📂

While AI tools can technically process a variety of formats — such as PDF, DOCX, or even images — Markdown (.md) offers unique advantages that make it the ideal format for PLAIN documents:

- **Easily Integrated into Codebases:** Markdown files fit naturally into Git repositories, documentation folders, and version-controlled environments.
- **AI-Friendly:** Unlike PDFs or image files, Markdown is a plain-text format that can be easily read, parsed, edited, and regenerated by AI tools.
- **Human-Readable:** It’s clean and simple to read in any text editor or code viewer — no special tools required.
- **Lightweight & Portable:** Markdown files are small, portable, and cross-platform, making collaboration and backups effortless.

By using .md files for your PLAIN documents, you get the best of both worlds — effortless human collaboration and seamless AI integration.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## Contributing 🙌

Want to improve PLAIN? Read the [Contribution Guidelines](./CONTRIBUTING.md) and submit a PR!