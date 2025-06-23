# PLAIN: Product Language for AI Notation

**PLAIN** is a structured documentation framework designed to help you define digital products in a format that's both human-friendly and machine-readable. It bridges the gap between product managers, designers, and AI-powered tools such as [v0](https://v0.dev/), [Figma Make](https://www.figma.com/), [Bolt](https://bolt.new/), [Stitch](https://stitch.withgoogle.com/), [Uizard](https://uizard.io/), and [Lovable](https://lovable.dev/).

With PLAIN, product ideas become structured assets — ready to be translated into user interfaces, code, and documentation by generative AI.

## What is PLAIN? 🤔

PLAIN is more than just a static spec — it’s a bridge between creative thinking and technical execution, formatted in a way that AI systems can parse, and product teams can understand.

- Clearly defines product vision and value in the “Idea Statement,” giving a concise foundation for all subsequent work.
- Breaks down visual and UX direction through dedicated sections on Design Language, Typography, Color, and more, enabling design consistency and AI interpretability.
- Details functional and non-functional requirements in structured, human-readable sections that guide both implementation and testing.
- Specifies technical implementation patterns such as state management, API design, and rendering methods, helping align developers and tools from day one.
- Creates a single source of truth that can be used to guide AI-generated UI code, component libraries, and workflows.

## Who is it for? 👩🏿‍💻

- AI tools that turn natural language into interfaces or code. PLAIN gives them the structure and semantics they need to generate relevant, high-quality output.
- Designers who need to translate product requirements into scalable systems, tokens, and layouts — while collaborating with both AI and humans.
- Developers who want clarity and consistency in technical handoffs, including routing, architecture patterns, and data flow structures.
- Product managers and teams who want to replace messy Google Docs and scattered tools with a clean, AI-first way of describing what to build and why.

## How to Use
The PLAIN format is designed to be usable by both humans and AI. Below are the core steps for using it effectively in an AI-powered product development workflow.

### Step 1: Start with a Clear Idea Statement
Write a short but meaningful description of your product idea. This becomes your Idea Statement, the first and most important section of the PLAIN file. It explains the product’s purpose, the problem it solves, the target audience, and its main value proposition — all in 1–2 short paragraphs.

What makes a good Idea Statement?
- It focuses on the user problem, not just the features
- It sets a clear vision for the product’s role
- It is specific enough to guide design and development decisions
 
_Example Idea Statement_
> Taskly is a lightweight task manager for freelancers, enabling fast capture of daily tasks, deadline reminders, and seamless syncing across devices. It helps independent workers stay organized without the clutter of enterprise tools.

### Step 2: Feed the Idea Statement to AI using plain-explained.md
Ask an AI to generate the full PLAIN document based on your **Idea Statement**. Provide the model with your statement and point it to plain-explained.md as a reference guide for structure, tone, and output expectations.

_Prompt Example_
> “You are an expert product designer and developer. Based on the following product idea, generate a complete product specification using the PLAIN format. Refer to plain-explained.md for section structure and sample outputs.”
>
> Idea Statement:
“Taskly is a lightweight task manager for freelancers, enabling fast capture of daily tasks, deadline reminders, and seamless syncing across devices. It helps independent workers stay organized without the clutter of enterprise tools.”

### Step 3: Review and Refine the Output
Evaluate the AI-generated content. Edit and improve sections that feel generic or unclear. Validate assumptions, correct terminology, and ensure coherence across the document. Collaboration with product, design, and engineering stakeholders is recommended here.
Focus Areas:
- Core Components
- Page Map
- Technical Stack
- Accessibility and Visual Tone

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
- Easily Integrated into Codebases: Markdown files fit naturally into Git repositories, documentation folders, and version-controlled environments.
- AI-Friendly: Unlike PDFs or image files, Markdown is a plain-text format that can be easily read, parsed, edited, and regenerated by AI tools.
- Human-Readable: It’s clean and simple to read in any text editor or code viewer — no special tools required.
- Lightweight & Portable: Markdown files are small, portable, and cross-platform, making collaboration and backups effortless.

By using .md files for your PLAIN documents, you get the best of both worlds — effortless human collaboration and seamless AI integration.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

## 🙌 Contributing

Want to improve PLAIN? Read the [contribution guide](./docs/contribution-guide.md) and submit a PR!
