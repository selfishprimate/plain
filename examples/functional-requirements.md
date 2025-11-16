# Functional Requirements: Examples & Patterns

This guide helps you define what your product must do through functional requirements.

---

## What are Functional Requirements?

Functional requirements describe the specific behaviors, features, and functions your product must have. They answer: "What should the system do?"

**Purpose:**
- Define exact features and capabilities
- Guide development priorities
- Set clear acceptance criteria
- Prevent scope creep
- Enable accurate estimation

**Format:** Feature → What it does → How it behaves

---

## Example 1: Task Management App (Taskly)

### User Management

**FR-1.1: User Registration**
- Users can create accounts using email and password
- System validates email format and password strength (min 8 characters, 1 uppercase, 1 number)
- System sends verification email upon registration
- Users cannot access the app until email is verified

**FR-1.2: User Authentication**
- Users can log in with email/password or Google OAuth
- System remembers users for 30 days ("Remember me" option)
- System locks account after 5 failed login attempts
- Users can reset password via email link

**FR-1.3: User Profile**
- Users can update name, email, avatar, timezone
- Users can change password (requires current password)
- Users can delete account (requires confirmation)
- Users can export all their data

---

### Task Management

**FR-2.1: Create Tasks**
- Users can create tasks with title (required), description (optional), due date, priority
- Users can assign tasks to projects
- Users can add tags to tasks
- System auto-saves drafts every 5 seconds

**FR-2.2: View Tasks**
- Users can view tasks in list, board (kanban), or calendar view
- Users can filter tasks by status, priority, project, tag, date range
- Users can sort tasks by due date, priority, created date, alphabetically
- Users can search tasks by title and description

**FR-2.3: Update Tasks**
- Users can edit task details
- Users can change task status (To Do → In Progress → Done)
- Users can move tasks between projects
- System logs all changes with timestamp and user

**FR-2.4: Delete Tasks**
- Users can delete tasks (soft delete, moved to trash)
- Tasks remain in trash for 30 days
- Users can restore tasks from trash
- Users can permanently delete tasks from trash

---

### Project Management

**FR-3.1: Create Projects**
- Users can create unlimited projects
- Each project has name, description, color
- Projects can have start/end dates
- Projects can be archived

**FR-3.2: Project Views**
- Users can view all tasks within a project
- Users can see project progress (% of completed tasks)
- Users can view project statistics (total tasks, completed, overdue)

---

### Collaboration (Pro Feature)

**FR-4.1: Team Workspaces**
- Users can create team workspaces
- Users can invite members via email
- Workspace owners can assign roles (Admin, Member, Viewer)
- Members can see all workspace projects and tasks

**FR-4.2: Task Assignment**
- Users can assign tasks to team members
- Assignees receive email and in-app notifications
- Users can reassign tasks
- Unassigned tasks visible to all members

**FR-4.3: Comments**
- Users can comment on tasks
- Comments support markdown formatting
- Users can mention team members with @username
- Mentioned users receive notifications

---

### Notifications

**FR-5.1: In-App Notifications**
- Users receive notifications for:
  - Task assignments
  - Task comments and mentions
  - Approaching due dates (24 hours before)
  - Overdue tasks
- Users can mark notifications as read
- Notifications clear after 30 days

**FR-5.2: Email Notifications**
- Users receive daily digest email (optional)
- Users can customize notification preferences
- Users can unsubscribe from specific notification types

---

## Example 2: E-commerce Platform (Shopnest)

### Product Catalog

**FR-1.1: Product Listing**
- System displays products with image, name, price, rating
- Products show stock status (In Stock, Low Stock, Out of Stock)
- Out of stock products are not purchasable but remain visible
- System displays 24 products per page

**FR-1.2: Product Search**
- Users can search products by name, description, SKU
- Search returns results in real-time (as user types)
- Search highlights matching keywords
- System logs search queries for analytics

**FR-1.3: Product Filters**
- Users can filter by category, price range, brand, rating, availability
- Multiple filters can be applied simultaneously
- Active filters displayed as removable chips
- Filter counts update in real-time

**FR-1.4: Product Details**
- Product page shows images (gallery with zoom), description, specifications, price
- Users can select variants (size, color) if applicable
- Users can see shipping estimate based on location
- Users can view related products

---

### Shopping Cart

**FR-2.1: Add to Cart**
- Users can add products to cart (logged in or guest)
- Cart persists in localStorage for 7 days for guests
- Logged-in users' carts sync across devices
- System prevents adding out-of-stock items

**FR-2.2: Cart Management**
- Users can update quantities
- Users can remove items
- Cart displays item subtotal, tax, shipping estimate, total
- System applies discount codes
- System validates stock availability before checkout

**FR-2.3: Save for Later**
- Users can move items from cart to "Save for Later" list
- Saved items persist indefinitely
- Users can move saved items back to cart

---

### Checkout

**FR-3.1: Guest Checkout**
- Guests can checkout with email only (no account required)
- System offers account creation after purchase
- Guest orders tracked via email and order number

**FR-3.2: Shipping Information**
- Users enter shipping address with validation
- System calculates shipping cost based on address and cart weight
- System offers shipping options (Standard, Express)
- Users can save multiple addresses (logged in only)

**FR-3.3: Payment**
- System accepts credit cards via Stripe
- System supports PayPal and Apple Pay
- Payment information not stored (handled by Stripe)
- Users can save payment methods (Stripe Customer Portal)

**FR-3.4: Order Confirmation**
- System generates unique order number
- Users receive confirmation email with order details
- System displays order confirmation page with tracking info
- Users can view order in "My Orders" (logged in users)

---

### Order Management

**FR-4.1: Order Tracking**
- Users can track orders with order number and email
- System updates order status (Processing → Shipped → Delivered)
- Users receive email notifications on status changes
- Tracking numbers provided when available

**FR-4.2: Order History**
- Logged-in users see all past orders
- Orders show date, items, total, status
- Users can reorder with one click
- Users can download invoices

**FR-4.3: Returns**
- Users can initiate returns within 30 days
- System generates return label
- Users select return reason
- Refund processed within 5-7 business days after receipt

---

## Example 3: Wellness App (Wellnest)

### Journaling

**FR-1.1: Create Entry**
- Users can create daily journal entries
- Entries include mood selector (7 emotions), text area, tags
- System timestamps each entry
- Entries private by default

**FR-1.2: Guided Prompts**
- System provides daily journaling prompts
- Users can skip prompts and free-write
- Prompts rotate daily
- Users can favorite prompts

**FR-1.3: View Entries**
- Users can view entries in timeline or calendar view
- Users can search entries by keyword or tag
- Users can filter by mood or date range
- Entries displayed with mood icon and preview

---

### Mood Tracking

**FR-2.1: Log Mood**
- Users can log mood multiple times per day
- Mood scale: 1-5 or emoji-based (7 emotions)
- Users can add note to mood log (optional)
- System prompts for mood once per day

**FR-2.2: Mood Visualizations**
- Users view mood trends over time (line chart)
- Users see weekly/monthly mood averages
- Users view mood calendar (heat map)
- System identifies patterns ("You feel better on weekends")

---

### Insights

**FR-3.1: Streak Tracking**
- System tracks consecutive days of journaling
- Users see current streak and longest streak
- System sends encouragement notifications
- Streaks reset if day is missed

**FR-3.2: Analytics**
- Users see total entries, average mood, most common tags
- System generates weekly recap email
- Premium users access advanced insights

---

## Example 4: SaaS Analytics Tool (Shopmetrics)

### Data Integration

**FR-1.1: Connect Store**
- Users can connect Shopify store via OAuth
- Users can connect WooCommerce via API key
- System validates connection and displays store name
- System imports last 90 days of data on first connection

**FR-1.2: Data Sync**
- System syncs data every 6 hours automatically
- Users can trigger manual sync (rate-limited to once per hour)
- System displays last sync time
- Failed syncs trigger email notification

---

### Dashboard

**FR-2.1: Overview Metrics**
- Dashboard displays total revenue, orders, average order value, conversion rate
- Users can select date range (Last 7 days, 30 days, 90 days, Custom)
- Metrics show change vs previous period (% increase/decrease)
- Metrics update in real-time

**FR-2.2: Visualizations**
- Revenue chart (line or bar, daily/weekly/monthly grouping)
- Top products table (sortable by revenue, quantity, views)
- Traffic sources pie chart
- Conversion funnel

---

### Reports

**FR-3.1: Auto-Generated Reports**
- System emails weekly summary every Monday
- Report includes key metrics and top products
- Users can customize report frequency (daily, weekly, monthly, off)
- Reports exportable as PDF

**FR-3.2: Custom Reports**
- Users can create custom reports with filters
- Reports can be saved and shared via link
- Reports support CSV export

---

## Functional Requirements Template

```markdown
### [Feature Category]

**FR-[X.Y]: [Feature Name]**
- [Actor] can [action] [object/outcome]
- System [behavior/validation]
- [Conditions, constraints, rules]
- [Error handling or edge cases]

**Acceptance Criteria:**
- [ ] [Specific testable criterion]
- [ ] [Another criterion]

**Priority:** [High / Medium / Low]
**Estimated Effort:** [S / M / L / XL]
```

---

## Example with Acceptance Criteria

**FR-1.1: User Registration**
- Users can create accounts using email and password
- System validates email format (RFC 5322 standard)
- Password must be minimum 8 characters with 1 uppercase, 1 number, 1 special character
- System sends verification email within 30 seconds
- Users cannot log in until email verified

**Acceptance Criteria:**
- [ ] Registration form validates email in real-time
- [ ] Password strength indicator shows weak/medium/strong
- [ ] Verification email contains clickable link valid for 24 hours
- [ ] Clicking verification link activates account and redirects to login
- [ ] Error messages display for duplicate email
- [ ] CAPTCHA prevents bot registrations

**Priority:** High
**Estimated Effort:** M

---

## Writing Good Functional Requirements

### 1. Be Specific
```
❌ Users can search
✅ Users can search tasks by title and description with real-time results
```

### 2. Use Active Voice
```
❌ The password should be validated
✅ System validates password strength (min 8 characters, 1 uppercase, 1 number)
```

### 3. Include Constraints
```
❌ Users can upload images
✅ Users can upload images (max 5MB, formats: JPG, PNG, WebP)
```

### 4. Define Behavior
```
❌ Tasks can be deleted
✅ Users can delete tasks (soft delete, moved to trash for 30 days, then permanently deleted)
```

---

## Common Requirement Categories

| Category | Examples |
|---|---|
| **Authentication** | Sign up, login, password reset, OAuth, MFA |
| **Authorization** | User roles, permissions, access control |
| **CRUD Operations** | Create, read, update, delete resources |
| **Search & Filter** | Search, sort, filter, pagination |
| **Notifications** | Email, push, in-app, SMS |
| **Integrations** | Third-party APIs, webhooks, OAuth |
| **Reporting** | Analytics, exports, dashboards |
| **Settings** | User preferences, account management |
| **Collaboration** | Comments, sharing, mentions, real-time |
| **Payments** | Checkout, subscriptions, refunds |

---

## Prioritization Framework

### MoSCoW Method

**Must Have** — Critical features (MVP)
- User authentication
- Core functionality
- Data security

**Should Have** — Important but not critical
- Notifications
- Profile customization
- Export features

**Could Have** — Nice to have
- Dark mode
- Advanced filters
- Integrations

**Won't Have** — Out of scope
- Mobile app (for now)
- AI features (future)

---

## Resources

- **User Story Mapping:** https://www.jpattonassociates.com/user-story-mapping/
- **Requirements Best Practices:** https://www.iiba.org
- **Gherkin Syntax:** https://cucumber.io/docs/gherkin/
