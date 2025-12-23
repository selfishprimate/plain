# Content Types

Common content structures and their implementation patterns. Each type represents a specific way of organizing and presenting information to users.

Choose content types that match your application's purpose and user needs:

## Primary Content Types

### Articles/Blog Posts
Long-form written content with rich formatting.
```
Article
- title (text, required)
- slug (text, unique)
- author (reference: User)
- publishedAt (datetime)
- status (select: draft/published/archived)
- category (reference: Category)
- tags (array: Tag)
- excerpt (text, max: 160)
- body (rich text)
- featuredImage (reference: Media)
- readTime (number, calculated)
- views (number, auto-increment)
```
- **Features:** Comments, sharing, bookmarks, related posts
- **Best for:** Blogs, news sites, documentation
- **Examples:** Medium, Dev.to, Substack

### Products
Items for sale or showcase with detailed information.
```
Product
- name (text, required)
- slug (text, unique)
- sku (text, unique)
- price (decimal, required)
- compareAtPrice (decimal)
- cost (decimal)
- description (rich text)
- category (reference: Category)
- brand (reference: Brand)
- images (array: Media, min: 1)
- variants (array: ProductVariant)
- inventory (number, default: 0)
- trackInventory (boolean)
- weight (number, grams)
- dimensions (object: length, width, height)
- tags (array: Tag)
- status (select: active/draft/archived)
- featured (boolean)
- reviews (array: Review)
```
- **Features:** Gallery, variants, reviews, specifications
- **Best for:** E-commerce, catalogs, marketplaces
- **Examples:** Amazon, Shopify stores, Etsy

### User Profiles
Information about users or members.
```
User
- id (uuid, auto)
- email (email, required, unique)
- username (text, unique)
- firstName (text)
- lastName (text)
- avatar (reference: Media)
- coverImage (reference: Media)
- bio (text, max: 500)
- location (text)
- website (url)
- socialLinks (object: twitter, linkedin, github)
- joinedAt (datetime, auto)
- lastActive (datetime, auto)
- role (select: user/admin/moderator)
- followers (array: User)
- following (array: User)
- verified (boolean)
```
- **Features:** Follow/connect, activity feed, achievements
- **Best for:** Social platforms, communities, teams
- **Examples:** Twitter, LinkedIn, GitHub

### Events
Time-based occurrences with registration or attendance.
```
Event
- title (text, required)
- slug (text, unique)
- description (rich text)
- startDate (datetime, required)
- endDate (datetime, required)
- timezone (text, required)
- location (object: venue, address, city, country)
- isOnline (boolean)
- meetingUrl (url)
- capacity (number)
- price (decimal)
- currency (select: USD/EUR/GBP)
- organizer (reference: User)
- attendees (array: User)
- waitlist (array: User)
- coverImage (reference: Media)
- status (select: upcoming/ongoing/completed/cancelled)
- tags (array: Tag)
```
- **Features:** RSVP, calendar sync, reminders, attendees
- **Best for:** Event platforms, calendars, ticketing
- **Examples:** Eventbrite, Meetup, Facebook Events

### Courses/Lessons
Educational content with structured learning paths.
```
Course
- title (text, required)
- slug (text, unique)
- description (rich text)
- instructor (reference: User)
- duration (number, hours)
- level (select: beginner/intermediate/advanced)
- language (select: en/es/fr/de)
- price (decimal)
- curriculum (array: Module)
- prerequisites (array: text)
- learningOutcomes (array: text)
- thumbnail (reference: Media)
- previewVideo (reference: Media)
- enrolledStudents (array: User)
- rating (decimal, 0-5)
- reviews (array: Review)
- certificate (boolean)
- publishedAt (datetime)
```
- **Features:** Progress tracking, quizzes, certificates, discussions
- **Best for:** E-learning, tutorials, training
- **Examples:** Coursera, Udemy, Khan Academy

### Projects/Portfolio
Showcase of work with process and outcomes.
```
Project
- title (text, required)
- slug (text, unique)
- client (text)
- date (date)
- duration (text)
- role (text)
- team (array: text)
- description (rich text)
- challenge (text)
- solution (text)
- results (text)
- technologies (array: text)
- deliverables (array: text)
- images (array: Media, min: 1)
- videoUrl (url)
- liveUrl (url)
- caseStudyUrl (url)
- testimonial (object: text, author, company)
- featured (boolean)
- category (reference: Category)
```
- **Features:** Gallery, case study, testimonials, links
- **Best for:** Portfolios, agencies, freelancers
- **Examples:** Behance, Dribbble, personal portfolios

### Documentation/Help
Technical or support content with clear structure.
```
Documentation
- title (text, required)
- slug (text, unique)
- content (markdown, required)
- category (reference: DocCategory)
- version (text, default: "latest")
- lastUpdated (datetime, auto)
- author (reference: User)
- relatedDocs (array: Documentation)
- tableOfContents (array: auto-generated)
- searchKeywords (array: text)
- helpfulness (object: yes, no)
- pageViews (number)
- deprecated (boolean)
- redirectTo (reference: Documentation)
```
- **Features:** Search, navigation tree, copy code, feedback
- **Best for:** Software docs, knowledge bases, FAQs
- **Examples:** MDN, Stripe Docs, Notion Help

### Messages/Comments
User-generated conversational content.
```
Message
- id (uuid, auto)
- author (reference: User, required)
- content (text, required, max: 5000)
- timestamp (datetime, auto)
- editedAt (datetime)
- parentMessage (reference: Message)
- thread (reference: Thread)
- mentions (array: User)
- reactions (array: Reaction)
- attachments (array: Media)
- isPinned (boolean)
- isDeleted (boolean)
- deletedAt (datetime)
- readBy (array: User)
```
- **Features:** Reply, edit, delete, mention, formatting
- **Best for:** Forums, chat, comments, discussions
- **Examples:** Slack, Discord, Reddit

### Tasks/Todos
Actionable items with status tracking.
```
Task
- title (text, required)
- description (text)
- status (select: todo/in-progress/review/done/cancelled)
- priority (select: low/medium/high/urgent)
- assignee (reference: User)
- reporter (reference: User)
- project (reference: Project)
- dueDate (datetime)
- startDate (datetime)
- completedAt (datetime)
- estimatedHours (decimal)
- actualHours (decimal)
- subtasks (array: Task)
- dependencies (array: Task)
- labels (array: Label)
- attachments (array: Media)
- comments (array: Comment)
- watchers (array: User)
```
- **Features:** Status updates, subtasks, dependencies, time tracking
- **Best for:** Project management, personal productivity
- **Examples:** Asana, Todoist, Jira

### Media/Gallery
Visual or audio content as primary focus.
```
Media
- id (uuid, auto)
- filename (text, required)
- originalName (text)
- mimeType (text, required)
- size (number, bytes)
- url (url, required)
- thumbnailUrl (url)
- dimensions (object: width, height)
- duration (number, seconds, for video/audio)
- uploadedBy (reference: User)
- uploadedAt (datetime, auto)
- title (text)
- altText (text)
- caption (text)
- tags (array: Tag)
- metadata (object: exif, location, device)
- collections (array: Collection)
- downloads (number)
- likes (array: User)
```
- **Features:** Lightbox, download, share, collections
- **Best for:** Photography, art, media libraries
- **Examples:** Unsplash, Instagram, YouTube

## Specialized Content Types

### Listings/Classifieds
Items or services offered by users.
```
Listing
- title (text, required)
- slug (text, unique)
- description (rich text)
- price (decimal)
- currency (select: USD/EUR/GBP)
- priceType (select: fixed/negotiable/free/contact)
- category (reference: Category)
- subcategory (reference: Category)
- condition (select: new/like-new/good/fair/poor)
- location (object: address, city, state, country, coordinates)
- images (array: Media, max: 10)
- seller (reference: User)
- contactMethod (select: message/phone/email)
- phoneNumber (tel)
- availability (select: available/pending/sold)
- views (number)
- favorites (array: User)
- postedAt (datetime, auto)
- expiresAt (datetime)
- featured (boolean)
```
- **Features:** Map view, saved searches, messaging
- **Best for:** Marketplaces, real estate, job boards
- **Examples:** Craigslist, Airbnb, Indeed

### Forms/Surveys
Structured data collection from users.
```
Form
- title (text, required)
- slug (text, unique)
- description (text)
- fields (array: FormField)
  - type (select: text/email/number/select/radio/checkbox/textarea/file)
  - label (text, required)
  - name (text, required)
  - placeholder (text)
  - required (boolean)
  - validation (object: pattern, min, max)
  - options (array: text, for select/radio/checkbox)
  - conditionalLogic (object: showIf, hideIf)
- submissions (array: FormSubmission)
- settings (object)
  - allowMultiple (boolean)
  - requireAuth (boolean)
  - notifyEmail (email)
  - successMessage (text)
  - redirectUrl (url)
- status (select: active/closed/draft)
- createdBy (reference: User)
- responses (number)
```
- **Features:** Progress bar, save draft, conditional fields
- **Best for:** Applications, feedback, research
- **Examples:** Typeform, Google Forms, SurveyMonkey

### Invoices/Orders
Transactional documents with line items.
```
Invoice
- invoiceNumber (text, unique, auto)
- orderNumber (text, unique)
- customer (reference: Customer)
- issueDate (date, required)
- dueDate (date)
- status (select: draft/sent/paid/overdue/cancelled)
- lineItems (array: LineItem)
  - description (text)
  - quantity (number)
  - unitPrice (decimal)
  - tax (decimal)
  - discount (decimal)
  - total (decimal, calculated)
- subtotal (decimal, calculated)
- taxTotal (decimal, calculated)
- discountTotal (decimal)
- total (decimal, calculated)
- currency (select: USD/EUR/GBP)
- paymentMethod (select: card/bank/paypal/cash)
- paymentStatus (select: pending/processing/completed/failed)
- notes (text)
- terms (text)
- attachments (array: Media)
```
- **Features:** PDF export, payment, tracking, history
- **Best for:** E-commerce, billing, services
- **Examples:** Stripe Invoices, QuickBooks, Shopify

### Reports/Analytics
Data visualization and insights.
```
Report
- title (text, required)
- type (select: dashboard/detailed/summary)
- dateRange (object: start, end)
- filters (array: Filter)
  - field (text)
  - operator (select: equals/contains/greater/less)
  - value (text)
- metrics (array: Metric)
  - name (text)
  - value (number)
  - change (decimal, percentage)
  - trend (select: up/down/stable)
- dimensions (array: text)
- visualizations (array: Visualization)
  - type (select: line/bar/pie/table/heatmap)
  - data (object)
  - config (object)
- schedule (object: frequency, recipients)
- createdBy (reference: User)
- lastUpdated (datetime, auto)
- exports (array: Export)
```
- **Features:** Export, schedule, share, drill-down
- **Best for:** Dashboards, business intelligence
- **Examples:** Google Analytics, Mixpanel, Tableau

### Cards/Flashcards
Bite-sized content for quick consumption.
```
Card
- front (text, required)
- back (text, required)
- deck (reference: Deck)
- category (reference: Category)
- difficulty (select: easy/medium/hard)
- type (select: basic/cloze/image/audio)
- image (reference: Media)
- audio (reference: Media)
- hint (text)
- explanation (text)
- tags (array: Tag)
- statistics (object)
  - views (number)
  - correct (number)
  - incorrect (number)
  - lastSeen (datetime)
  - nextReview (datetime)
  - interval (number, days)
- createdBy (reference: User)
- isPublic (boolean)
```
- **Features:** Flip, swipe, progress, spaced repetition
- **Best for:** Learning apps, reference, games
- **Examples:** Anki, Duolingo, Pinterest

## Content Relationships

### One-to-Many
Single parent with multiple children.
- **Example:** Author → Articles, Category → Products
- **Display:** List view, grid view, table view

### Many-to-Many
Multiple connections between items.
- **Example:** Articles ↔ Tags, Users ↔ Groups
- **Display:** Tag clouds, relationship graphs

### Hierarchical
Nested parent-child relationships.
- **Example:** Categories → Subcategories → Items
- **Display:** Tree view, breadcrumbs, nested lists

### Sequential
Ordered content with previous/next.
- **Example:** Course lessons, onboarding steps
- **Display:** Progress bar, step indicators, pagination

### Network
Complex interconnected relationships.
- **Example:** Social connections, knowledge graphs
- **Display:** Network diagrams, connection maps

---

*Content types are the building blocks of your application. Choose and combine them thoughtfully to create experiences that feel intuitive and serve your users' needs effectively.*