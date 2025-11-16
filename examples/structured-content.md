# Structured Content: Content Types & Schema Design

This guide helps you define and organize content types for your product.

---

## What is Structured Content?

Structured content means breaking content into reusable, well-defined components (content types) rather than treating it as unstructured text. Each content type has a schema defining its fields.

**Purpose:**
- Organize content systematically
- Enable content reuse
- Support multi-channel publishing (web, mobile, API)
- Facilitate search and filtering
- Guide content creation
- Enable better content management

**Examples:** Blog posts, products, user profiles, events, documentation

---

## Content Type Components

### Every content type should define:

1. **Name** — What is this content type? (e.g., "Blog Post")
2. **Fields** — What data does it contain? (e.g., title, body, author)
3. **Field Types** — What type of data? (text, rich text, number, date, image, relation)
4. **Validation** — What's required? What are the limits?
5. **Relationships** — How does it relate to other content types?

---

## Example 1: Blog / Content Site

### Content Type: Blog Post

**Schema:**
```yaml
type: BlogPost
fields:
  - name: title
    type: text
    required: true
    maxLength: 100
    description: "Post title (SEO: 50-60 chars)"

  - name: slug
    type: slug
    required: true
    unique: true
    generatedFrom: title
    description: "URL-friendly version of title"

  - name: excerpt
    type: text
    required: true
    maxLength: 160
    description: "Short summary for meta description"

  - name: body
    type: richText
    required: true
    description: "Main post content (Markdown or rich text)"

  - name: featuredImage
    type: image
    required: false
    description: "Main post image (1200x630px recommended)"

  - name: author
    type: relation
    relatedTo: Author
    required: true

  - name: category
    type: relation
    relatedTo: Category
    required: true

  - name: tags
    type: relation
    relatedTo: Tag
    multiple: true
    required: false

  - name: publishedAt
    type: dateTime
    required: true
    description: "Publication date"

  - name: status
    type: select
    options: [draft, published, archived]
    default: draft

  - name: seo
    type: object
    fields:
      - name: metaTitle
        type: text
        maxLength: 60
      - name: metaDescription
        type: text
        maxLength: 160
      - name: ogImage
        type: image
```

---

### Content Type: Author

**Schema:**
```yaml
type: Author
fields:
  - name: name
    type: text
    required: true

  - name: slug
    type: slug
    required: true
    unique: true

  - name: bio
    type: text
    maxLength: 500

  - name: avatar
    type: image

  - name: socialLinks
    type: object
    fields:
      - name: twitter
        type: url
      - name: github
        type: url
      - name: website
        type: url
```

---

### Content Type: Category

**Schema:**
```yaml
type: Category
fields:
  - name: name
    type: text
    required: true

  - name: slug
    type: slug
    required: true
    unique: true

  - name: description
    type: text
    maxLength: 300

  - name: color
    type: color
    description: "Hex color for category badge"
```

---

## Example 2: E-commerce Platform

### Content Type: Product

**Schema:**
```yaml
type: Product
fields:
  - name: name
    type: text
    required: true
    maxLength: 100

  - name: slug
    type: slug
    required: true
    unique: true

  - name: description
    type: richText
    required: true

  - name: shortDescription
    type: text
    maxLength: 300
    description: "For product cards"

  - name: price
    type: number
    required: true
    min: 0

  - name: compareAtPrice
    type: number
    description: "Original price (for discounts)"

  - name: sku
    type: text
    unique: true
    description: "Stock Keeping Unit"

  - name: inventory
    type: object
    fields:
      - name: quantity
        type: number
        default: 0
      - name: trackInventory
        type: boolean
        default: true
      - name: allowBackorder
        type: boolean
        default: false

  - name: images
    type: image
    multiple: true
    required: true
    max: 10
    description: "Product images (first is featured)"

  - name: category
    type: relation
    relatedTo: Category
    required: true

  - name: brand
    type: relation
    relatedTo: Brand
    required: false

  - name: tags
    type: relation
    relatedTo: Tag
    multiple: true

  - name: variants
    type: object
    multiple: true
    description: "Size, color, etc."
    fields:
      - name: name
        type: text
        description: "e.g., 'Small' or 'Red'"
      - name: sku
        type: text
      - name: price
        type: number
      - name: quantity
        type: number

  - name: specifications
    type: object
    fields:
      - name: dimensions
        type: text
      - name: weight
        type: text
      - name: material
        type: text

  - name: status
    type: select
    options: [draft, active, archived]
    default: draft

  - name: seo
    type: object
    fields:
      - name: metaTitle
        type: text
      - name: metaDescription
        type: text
```

---

### Content Type: Category (E-commerce)

**Schema:**
```yaml
type: Category
fields:
  - name: name
    type: text
    required: true

  - name: slug
    type: slug
    required: true
    unique: true

  - name: description
    type: text

  - name: image
    type: image
    description: "Category banner"

  - name: parentCategory
    type: relation
    relatedTo: Category
    description: "For nested categories"

  - name: sortOrder
    type: number
    description: "Display order in navigation"
```

---

## Example 3: Task Management App

### Content Type: Task

**Schema:**
```yaml
type: Task
fields:
  - name: title
    type: text
    required: true
    maxLength: 200

  - name: description
    type: richText
    required: false

  - name: status
    type: select
    options: [todo, in_progress, completed, archived]
    default: todo
    required: true

  - name: priority
    type: select
    options: [low, medium, high, urgent]
    default: medium

  - name: dueDate
    type: date
    required: false

  - name: assignee
    type: relation
    relatedTo: User
    required: false

  - name: project
    type: relation
    relatedTo: Project
    required: false

  - name: tags
    type: relation
    relatedTo: Tag
    multiple: true

  - name: attachments
    type: file
    multiple: true
    max: 10

  - name: createdBy
    type: relation
    relatedTo: User
    required: true

  - name: createdAt
    type: dateTime
    required: true

  - name: updatedAt
    type: dateTime
    required: true
```

---

### Content Type: Project

**Schema:**
```yaml
type: Project
fields:
  - name: name
    type: text
    required: true

  - name: description
    type: text
    maxLength: 500

  - name: color
    type: color
    description: "Project identifier color"

  - name: startDate
    type: date

  - name: endDate
    type: date

  - name: status
    type: select
    options: [planning, active, on_hold, completed, archived]
    default: planning

  - name: owner
    type: relation
    relatedTo: User
    required: true

  - name: members
    type: relation
    relatedTo: User
    multiple: true
```

---

## Example 4: Event Platform

### Content Type: Event

**Schema:**
```yaml
type: Event
fields:
  - name: title
    type: text
    required: true

  - name: slug
    type: slug
    required: true
    unique: true

  - name: description
    type: richText
    required: true

  - name: coverImage
    type: image
    required: true

  - name: startDateTime
    type: dateTime
    required: true

  - name: endDateTime
    type: dateTime
    required: true

  - name: location
    type: object
    fields:
      - name: type
        type: select
        options: [in_person, virtual, hybrid]
      - name: venueName
        type: text
      - name: address
        type: text
      - name: city
        type: text
      - name: country
        type: text
      - name: virtualUrl
        type: url

  - name: organizer
    type: relation
    relatedTo: Organizer
    required: true

  - name: category
    type: relation
    relatedTo: EventCategory
    required: true

  - name: capacity
    type: number
    description: "Max attendees"

  - name: ticketPrice
    type: number
    min: 0
    description: "0 for free events"

  - name: registrationDeadline
    type: dateTime

  - name: status
    type: select
    options: [draft, published, soldOut, completed, cancelled]
    default: draft
```

---

## Example 5: Documentation Site

### Content Type: Doc Page

**Schema:**
```yaml
type: DocPage
fields:
  - name: title
    type: text
    required: true

  - name: slug
    type: slug
    required: true
    unique: true

  - name: content
    type: markdown
    required: true

  - name: category
    type: relation
    relatedTo: DocCategory
    required: true

  - name: order
    type: number
    description: "Display order within category"

  - name: tocDepth
    type: number
    default: 3
    description: "Table of contents heading depth"

  - name: relatedPages
    type: relation
    relatedTo: DocPage
    multiple: true

  - name: lastUpdated
    type: dateTime
    required: true
```

---

## Field Types Reference

| Field Type | Description | Example |
|---|---|---|
| **text** | Short text (single line) | Title, name, email |
| **richText** | Formatted text (Markdown/HTML) | Blog post body, description |
| **number** | Integer or decimal | Price, quantity, rating |
| **boolean** | True/false | Published, featured, active |
| **date** | Date only | Birth date, due date |
| **dateTime** | Date + time | Published at, event start |
| **url** | Web address | Website, social links |
| **email** | Email address | Contact email |
| **image** | Image upload | Featured image, avatar |
| **file** | File upload | PDF, attachments |
| **color** | Hex color code | Brand color, category color |
| **select** | Dropdown options | Status, priority, category |
| **slug** | URL-friendly string | blog-post-title |
| **relation** | Link to other content | Author, category, tags |
| **object** | Nested fields | Address, SEO settings |
| **array** | List of items | Images, tags, variants |

---

## Validation Rules

### Common Validations

**Required:**
```yaml
required: true
```

**Max Length:**
```yaml
maxLength: 100
```

**Min/Max (Numbers):**
```yaml
min: 0
max: 100
```

**Unique:**
```yaml
unique: true
```

**Pattern (Regex):**
```yaml
pattern: "^[a-z0-9-]+$"
```

**Allowed Values:**
```yaml
options: [draft, published, archived]
```

---

## Content Relationships

### One-to-One
```yaml
# Blog Post → Featured Image
featuredImage:
  type: relation
  relatedTo: Image
  multiple: false
```

### One-to-Many
```yaml
# Author → Blog Posts
posts:
  type: relation
  relatedTo: BlogPost
  multiple: true
```

### Many-to-Many
```yaml
# Blog Post ↔ Tags
tags:
  type: relation
  relatedTo: Tag
  multiple: true
```

---

## Content Modeling Best Practices

### 1. Start with User Needs
```
❌ "We need a content management system"
✅ "Users need to find blog posts by topic"
```

### 2. Keep It Simple
```
❌ 20 fields per content type
✅ 5-10 essential fields
```

### 3. Normalize Reusable Content
```
✅ Separate Author content type (reuse across posts)
❌ Author fields in each blog post
```

### 4. Use Consistent Naming
```
✅ publishedAt, createdAt, updatedAt
❌ pubDate, date_created, modified
```

### 5. Plan for Localization
```yaml
title:
  type: text
  localized: true  # Enable translations
```

---

## Content Type Examples by Product

### SaaS Dashboard
- User
- Workspace
- Project
- Team Member
- Notification
- Integration

### E-learning Platform
- Course
- Lesson
- Quiz
- Student
- Instructor
- Certificate

### Recipe Site
- Recipe
- Ingredient
- Chef
- Cuisine
- Dietary Tag (vegan, gluten-free)

### Job Board
- Job Posting
- Company
- Location
- Job Category
- Application

---

## Headless CMS Examples

### Sanity Schema (TypeScript)
```typescript
export default {
  name: 'blogPost',
  title: 'Blog Post',
  type: 'document',
  fields: [
    {
      name: 'title',
      title: 'Title',
      type: 'string',
      validation: Rule => Rule.required().max(100)
    },
    {
      name: 'slug',
      title: 'Slug',
      type: 'slug',
      options: { source: 'title' }
    },
    {
      name: 'body',
      title: 'Body',
      type: 'blockContent'
    },
    {
      name: 'author',
      title: 'Author',
      type: 'reference',
      to: [{ type: 'author' }]
    }
  ]
}
```

---

### Contentful Content Model (JSON)
```json
{
  "name": "Blog Post",
  "fields": [
    {
      "id": "title",
      "name": "Title",
      "type": "Text",
      "required": true,
      "validations": [{ "size": { "max": 100 } }]
    },
    {
      "id": "body",
      "name": "Body",
      "type": "RichText",
      "required": true
    },
    {
      "id": "author",
      "name": "Author",
      "type": "Link",
      "linkType": "Entry",
      "validations": [{ "linkContentType": ["author"] }]
    }
  ]
}
```

---

### Strapi Content Type (JSON)
```json
{
  "kind": "collectionType",
  "collectionName": "blog_posts",
  "info": {
    "singularName": "blog-post",
    "pluralName": "blog-posts",
    "displayName": "Blog Post"
  },
  "attributes": {
    "title": {
      "type": "string",
      "required": true,
      "maxLength": 100
    },
    "slug": {
      "type": "uid",
      "targetField": "title"
    },
    "body": {
      "type": "richtext",
      "required": true
    },
    "author": {
      "type": "relation",
      "relation": "manyToOne",
      "target": "api::author.author"
    }
  }
}
```

---

## Static Content (JSON/Markdown)

### Option 1: JSON Files
```json
{
  "id": "post-1",
  "title": "Getting Started with Next.js",
  "slug": "getting-started-nextjs",
  "excerpt": "Learn the basics of Next.js",
  "body": "...",
  "author": "John Doe",
  "publishedAt": "2024-01-15",
  "tags": ["nextjs", "react", "tutorial"]
}
```

### Option 2: Markdown with Frontmatter
```markdown
---
title: Getting Started with Next.js
slug: getting-started-nextjs
author: John Doe
publishedAt: 2024-01-15
tags:
  - nextjs
  - react
  - tutorial
---

Blog post content here in Markdown...
```

---

## Checklist

- [ ] Content types identified
- [ ] Fields defined for each type
- [ ] Field types specified
- [ ] Validation rules set
- [ ] Relationships mapped
- [ ] Unique constraints identified
- [ ] Required fields marked
- [ ] SEO fields included
- [ ] Schema documented

---

## Resources

- **Sanity Content Modeling:** https://www.sanity.io/docs/content-modelling
- **Contentful Content Model:** https://www.contentful.com/developers/docs/concepts/data-model/
- **Strapi Content Types:** https://docs.strapi.io/dev-docs/backend-customization/models
- **Content Modeling Guide:** https://www.nngroup.com/articles/content-management-systems/
