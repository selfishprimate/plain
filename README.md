# PLAIN: Product Language for AI Notation 📃

**PLAIN** is a structured markdown format that turns product ideas into machine-readable specs. It bridges the gap between product teams and AI tools like [Claude](https://claude.ai), [Gemini](https://gemini.google.com), [Cursor](https://cursor.sh), [v0](https://v0.dev/), [Figma Make](https://www.figma.com/), [Bolt](https://bolt.new/), and [Lovable](https://lovable.dev/), enabling them to generate UI, code, and documentation directly from your vision.

Unlike traditional specs scattered across tools and documents, a PLAIN file consolidates your product's design vision, technical foundation, and user experience into a single, AI-friendly document.

- **Structures your product vision:** Define your idea, core purpose, and target audience, giving both humans and AI a shared understanding of what you're building.
- **Captures your design direction:** Specify your color palette, typography, icons, and layout preferences so AI generates UIs that match your vision.
- **Documents requirements systematically:** Prioritize features using MoSCoW (Must/Should/Could/Won't) while User Stories capture the human context behind each requirement.
- **Specifies technical architecture:** Define your tech stack, data models, page routes, and component inventory in dedicated sections.
- **Empowers AI-assisted decisions:** Write "Let AI decide for me" in any section you're unsure about and AI will choose modern, compatible options that fit your stack.
- **Serves as living documentation:** Keep your spec in version control alongside your code. Update it as your product evolves, fork it for new features.

## Who is it for? 👩🏿‍💻

PLAIN is for **Product Managers** who want to quickly test whether their ideas actually work, **Designers** who want to bring creative ideas to life faster, and **Developers** who want to build great-looking apps without getting lost in design decisions.

It's also for **Solo Founders and Small Teams** who lack expertise in certain areas and can use "**Let AI decide for me!**" to get intelligent recommendations. And for **AI tools** like **Claude**, **Cursor**, **v0**, **Bolt**, and **Lovable** that need structured input to generate production-ready code and components.

In short, PLAIN is for anyone who loves to design and code.

## How to Use 💪

Follow these three steps to turn your product idea into a working application.

### Step 1: Get the PLAIN Template

Download the [PLAIN.md](PLAIN.md) and add it to the root level of your project folder. Rename it to `{project-name}-plain.md` to avoid confusion as your project grows.

### Step 2: Fill Out Your PLAIN File

Start with the **project metadata** in the HTML comment at the top (title, description, author, date, etc.). Then review the **"Instructions for AI Coding Assistants"** section and customize it if needed.

Work through each section from Project Overview to Additional Notes. The template includes examples and explanations for guidance. **Once you've filled in your content, delete the examples and explanations to keep your spec clean.**

**Tip:** For any section where you're unsure, simply write `Let AI decide for me`.

### Step 3: Feed Your PLAIN File to AI

Your spec is ready. Feed it to your favorite AI tool with the following command and let it build your application.

**Example Prompt:**

> Read the `{project-name}-plain.md` file in my project. Start with the "Instructions for AI Coding Assistants" section to understand the core principles, then work through each section from Project Overview to Additional Notes. Generate a complete application that follows every specification precisely.

**Bonus Tip:** Keep your PLAIN document in version control alongside your code. It serves as living documentation that evolves with your product.

## Plainify 🛠️

[Plainify](https://plainify.app) is a guided web application designed to help you create PLAIN specifications without staring at a blank page. Instead of manually filling out the template from scratch, Plainify provides a structured, section-by-section workflow that shows you relevant options and examples for each part of your specification.

**How it works:**

1. **Guided Section-by-Section Interface**: Work through each PLAIN section with curated options and examples, eliminating the blank page problem
2. **Context-Aware Options**: See relevant choices for Design Style, Color Palettes, Tech Stack, UI Libraries, and more
3. **AI-Enhanced Generation**: When you click Generate, Claude LLM processes your selections and creates a `{project-name}-plain.md` file
4. **Intelligent Context Layer**: The LLM interprets your choices and adds contextual details that help AI code assistants better understand your requirements
5. **Ready-to-Use Output**: Receive a complete, well-formed PLAIN markdown file ready to be added to your project repository

Plainify bridges the gap between knowing what a PLAIN specification should contain and actually creating one. It's perfect for teams who want to leverage PLAIN without spending hours learning the format's nuances.

## Why Markdown? 📂

AI tools can process various formats like PDF, DOCX, or images, but **Markdown stands out as the ideal choice** for PLAIN specifications. It's plain text that AI can easily read, parse, and regenerate without special processing. It's also **human-readable** in any text editor, no special tools required.

More importantly, Markdown files fit naturally into your **development workflow**. They integrate seamlessly with Git repositories, making it easy to **track changes** to your specs over time. They're lightweight, portable, and stay in sync with your codebase. In short, Markdown gives you **the best of both worlds**: effortless human collaboration and seamless AI integration.

## Contributing 🙌

Found a way to make PLAIN even plainer? We'd love to hear it! Every great tool starts as a simple idea. PLAIN started as one, and with your help, it'll grow into something even better.

Whether it's a typo fix, a new section idea, or a complete overhaul, we welcome it all. You can also **share your filled-out PLAIN files** with the community! If you've created a `{project-name}-plain.md` for your project, submit it with a live demo or design link in it to inspire others.

Read the [Contribution Guidelines](CONTRIBUTING.md) and join the crew!

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.