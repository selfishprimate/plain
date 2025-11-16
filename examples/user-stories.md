# User Stories: Examples & Writing Guide

This guide helps you write effective user stories that capture user needs and drive development.

---

## What are User Stories?

User stories describe features from the end-user's perspective. They follow a simple format: **As a [user type], I want [goal], so that [benefit].**

**Purpose:**
- Focus on user value, not technical implementation
- Enable conversation and collaboration
- Keep requirements flexible and adaptable
- Facilitate estimation and planning
- Drive user-centered development

**Format:** As a [who], I want [what], so that [why]

---

## User Story Template

```
As a [user type/persona],
I want [goal/desire],
So that [benefit/value].

Acceptance Criteria:
- [ ] [Specific testable criterion]
- [ ] [Another criterion]

Priority: [High / Medium / Low]
Story Points: [1, 2, 3, 5, 8, 13]
```

---

## Example 1: Task Management App (Taskly)

### Authentication Stories

**US-1.1: Sign Up**
```
As a new user,
I want to create an account with my email and password,
So that I can start organizing my tasks.

Acceptance Criteria:
- [ ] Email validation shows error for invalid format
- [ ] Password must be at least 8 characters
- [ ] Verification email sent upon registration
- [ ] Cannot access app until email verified
- [ ] Success message displayed after registration

Priority: High
Story Points: 5
```

**US-1.2: Social Login**
```
As a busy professional,
I want to sign up with my Google account,
So that I can get started quickly without creating another password.

Acceptance Criteria:
- [ ] "Sign up with Google" button visible on signup page
- [ ] OAuth flow opens in popup
- [ ] Account created with Google profile info (name, email, avatar)
- [ ] User redirected to dashboard after successful signup
- [ ] Error message shown if Google account already connected

Priority: Medium
Story Points: 3
```

**US-1.3: Password Reset**
```
As a returning user who forgot my password,
I want to reset my password via email,
So that I can regain access to my account.

Acceptance Criteria:
- [ ] "Forgot password?" link visible on login page
- [ ] Email field validates format
- [ ] Reset link sent to email within 1 minute
- [ ] Link expires after 1 hour
- [ ] New password meets security requirements
- [ ] Success message shown after password reset

Priority: High
Story Points: 3
```

---

### Task Management Stories

**US-2.1: Create Task**
```
As a freelancer,
I want to quickly capture tasks as they come to mind,
So that I don't forget important work.

Acceptance Criteria:
- [ ] Task creation modal opens with Cmd+N (Mac) or Ctrl+N (Windows)
- [ ] Only title is required
- [ ] Optional fields: description, due date, priority, project, tags
- [ ] Task auto-saves as draft every 5 seconds
- [ ] Task created and added to list immediately
- [ ] Success toast appears

Priority: High
Story Points: 5
```

**US-2.2: Filter Tasks**
```
As a project manager,
I want to filter tasks by status, priority, and project,
So that I can focus on what's most important right now.

Acceptance Criteria:
- [ ] Filter panel accessible from toolbar
- [ ] Multiple filters can be applied simultaneously
- [ ] Active filters displayed as removable chips
- [ ] Task count updates in real-time
- [ ] "Clear all filters" button available when filters active
- [ ] Filter state persists across sessions

Priority: Medium
Story Points: 5
```

**US-2.3: Bulk Actions**
```
As a power user,
I want to select multiple tasks and perform actions on them,
So that I can save time on repetitive operations.

Acceptance Criteria:
- [ ] Checkbox appears on task hover
- [ ] Shift+click selects range of tasks
- [ ] Bulk action bar appears when tasks selected
- [ ] Available actions: Delete, Complete, Move to project, Change priority
- [ ] Confirmation required for destructive actions
- [ ] Success message shows number of tasks affected

Priority: Low
Story Points: 8
```

---

### Collaboration Stories

**US-3.1: Assign Task**
```
As a team lead,
I want to assign tasks to team members,
So that everyone knows their responsibilities.

Acceptance Criteria:
- [ ] Assignee dropdown shows all workspace members
- [ ] Can search members by name
- [ ] Assigned member receives email and in-app notification
- [ ] Task shows assignee's avatar
- [ ] Can reassign to another member
- [ ] Can unassign (leave unassigned)

Priority: High
Story Points: 5
```

**US-3.2: Comment on Task**
```
As a team member,
I want to comment on tasks,
So that I can communicate context and updates with my team.

Acceptance Criteria:
- [ ] Comment box visible on task detail page
- [ ] Supports markdown formatting
- [ ] Can mention team members with @username
- [ ] Mentioned members receive notification
- [ ] Comments show author, timestamp, edited indicator
- [ ] Can edit/delete own comments

Priority: Medium
Story Points: 8
```

---

## Example 2: E-commerce Platform (Shopnest)

### Shopping Stories

**US-4.1: Browse Products**
```
As a shopper,
I want to browse products by category,
So that I can discover items I'm interested in.

Acceptance Criteria:
- [ ] Category menu visible in header
- [ ] Clicking category shows filtered product list
- [ ] Products display image, name, price, rating
- [ ] 24 products per page with pagination
- [ ] "Out of stock" badge visible when applicable
- [ ] Breadcrumb navigation shows current category

Priority: High
Story Points: 5
```

**US-4.2: Search Products**
```
As a shopper looking for something specific,
I want to search products by keyword,
So that I can quickly find what I need.

Acceptance Criteria:
- [ ] Search bar prominent in header
- [ ] Real-time results appear as I type (after 2 characters)
- [ ] Results show product image, name, price
- [ ] Keywords highlighted in results
- [ ] "No results" message with suggestions
- [ ] Recent searches saved (last 5)

Priority: High
Story Points: 8
```

**US-4.3: Add to Cart**
```
As a shopper,
I want to add products to my cart,
So that I can purchase multiple items together.

Acceptance Criteria:
- [ ] "Add to Cart" button visible on product page
- [ ] Can select quantity before adding
- [ ] Can select variants (size, color) if applicable
- [ ] Success toast appears with "View Cart" link
- [ ] Cart icon shows item count
- [ ] Cannot add out-of-stock items

Priority: High
Story Points: 5
```

---

### Checkout Stories

**US-5.1: Guest Checkout**
```
As a first-time shopper,
I want to checkout without creating an account,
So that I can complete my purchase quickly.

Acceptance Criteria:
- [ ] "Continue as Guest" option on checkout
- [ ] Only requires email for order confirmation
- [ ] Shipping and payment forms same as logged-in users
- [ ] Order confirmation sent to email
- [ ] Option to create account after purchase

Priority: High
Story Points: 5
```

**US-5.2: Apply Discount Code**
```
As a budget-conscious shopper,
I want to apply a discount code to my order,
So that I can save money.

Acceptance Criteria:
- [ ] "Have a discount code?" link on checkout
- [ ] Code input validates on blur
- [ ] Invalid code shows error message
- [ ] Valid code applies discount and updates total
- [ ] Discount displayed in order summary
- [ ] Can remove applied code

Priority: Medium
Story Points: 3
```

---

## Example 3: Social App (Connectly)

### Social Interaction Stories

**US-6.1: Create Post**
```
As a user,
I want to share updates with my friends,
So that I can stay connected.

Acceptance Criteria:
- [ ] "What's on your mind?" prompt visible on feed
- [ ] Supports text (max 5000 characters)
- [ ] Can upload images (max 10, 5MB each)
- [ ] Can add location (optional)
- [ ] Can tag friends
- [ ] Privacy selector (Public, Friends, Only Me)
- [ ] Post appears in feed immediately

Priority: High
Story Points: 8
```

**US-6.2: Like Post**
```
As a user,
I want to like posts from friends,
So that I can show appreciation without commenting.

Acceptance Criteria:
- [ ] Like button (heart icon) visible on each post
- [ ] Clicking toggles like on/off
- [ ] Like count updates immediately
- [ ] Post author receives notification
- [ ] Can see list of users who liked
- [ ] Unlike removes notification

Priority: Medium
Story Points: 3
```

**US-6.3: Comment on Post**
```
As a user,
I want to comment on posts,
So that I can engage in conversations.

Acceptance Criteria:
- [ ] Comment box below each post
- [ ] Enter key submits comment
- [ ] Comment appears immediately with optimistic update
- [ ] Can edit/delete own comments
- [ ] Post author receives notification
- [ ] Can reply to comments (nested)

Priority: High
Story Points: 5
```

---

## Example 4: SaaS Dashboard (Analytics Pro)

### Analytics Stories

**US-7.1: View Dashboard**
```
As a business owner,
I want to see key metrics on my dashboard,
So that I can monitor my business performance at a glance.

Acceptance Criteria:
- [ ] Dashboard shows total revenue, orders, customers, conversion rate
- [ ] Metrics show % change vs previous period
- [ ] Date range selector (Last 7, 30, 90 days, Custom)
- [ ] Visualizations: revenue chart, top products, traffic sources
- [ ] Data refreshes every 5 minutes
- [ ] Loading states shown during data fetch

Priority: High
Story Points: 13
```

**US-7.2: Export Report**
```
As a data analyst,
I want to export reports as CSV,
So that I can analyze data in Excel.

Acceptance Criteria:
- [ ] "Export" button visible on reports
- [ ] CSV includes all visible columns and filters
- [ ] Filename includes report name and date
- [ ] Download triggers immediately
- [ ] Toast confirms successful export
- [ ] Works for up to 10,000 rows

Priority: Medium
Story Points: 3
```

---

## Writing Good User Stories

### 1. Focus on Value, Not Implementation

```
❌ As a user, I want a login form with email and password fields
✅ As a new user, I want to create an account, so that I can save my preferences
```

### 2. Use Specific Personas

```
❌ As a user, I want to search
✅ As a busy professional, I want to quickly search my tasks by keyword
```

### 3. Include the "So That" (Benefit)

```
❌ As a shopper, I want to add items to cart
✅ As a shopper, I want to add items to cart, so that I can purchase multiple items together
```

### 4. Keep Stories Small

```
❌ As a user, I want a complete profile management system
✅ Broken into:
    - As a user, I want to update my profile photo
    - As a user, I want to change my email address
    - As a user, I want to update my bio
```

### 5. Make Acceptance Criteria Testable

```
❌ The page should load fast
✅ Page loads in under 2 seconds on 4G connection
```

---

## User Story Formats

### Classic Format
```
As a [persona],
I want [goal],
So that [benefit].
```

### Job-to-be-Done Format
```
When [situation],
I want to [motivation],
So I can [expected outcome].

Example:
When I'm overwhelmed by tasks,
I want to quickly capture them,
So I can stop worrying and focus on one thing.
```

### Feature-Driven Format
```
In order to [benefit],
As a [persona],
I want [goal].

Example:
In order to stay organized,
As a freelancer,
I want to create projects and assign tasks to them.
```

---

## INVEST Criteria

Good user stories should be:

**I — Independent**
- Story can be developed in any order
- Not dependent on other stories

**N — Negotiable**
- Details can be discussed
- Not a contract or requirement

**V — Valuable**
- Delivers value to the user
- Has a clear benefit

**E — Estimable**
- Team can estimate effort
- Clear enough to size

**S — Small**
- Completable in one sprint
- Not too large or complex

**T — Testable**
- Has clear acceptance criteria
- Can be verified

---

## Story Mapping Example

### Epic: User Management

**User Story Map:**
```
Sign Up → Verify Email → Complete Profile → Invite Friends
   ↓           ↓              ↓               ↓
Login    Reset Password  Edit Profile   Accept Invite
```

**Prioritized Backlog:**
1. Sign up (email/password)
2. Login
3. Reset password
4. Verify email
5. Edit profile
6. Invite friends

---

## Estimation: Story Points

| Points | Complexity | Example |
|---|---|---|
| **1** | Trivial | Add a label, change button text |
| **2** | Simple | Add a filter, simple form validation |
| **3** | Easy | Password reset, basic CRUD operation |
| **5** | Medium | User registration, search feature |
| **8** | Complex | Real-time notifications, bulk actions |
| **13** | Very Complex | Payment integration, analytics dashboard |

**Note:** Stories > 13 points should be broken down into smaller stories.

---

## Common Story Types

| Story Type | Example |
|---|---|
| **Feature** | As a user, I want to create tasks |
| **Enhancement** | As a power user, I want keyboard shortcuts |
| **Bug Fix** | As a user, I expect the save button to work |
| **Spike** | Research best authentication library |
| **Technical** | As a developer, I want automated tests |
| **UX Improvement** | As a user, I want clearer error messages |

---

## Resources

- **User Story Guide:** https://www.mountaingoatsoftware.com/agile/user-stories
- **Story Mapping:** https://www.jpattonassociates.com/user-story-mapping/
- **INVEST Criteria:** https://agileforall.com/new-to-agile-invest-in-good-user-stories/
- **Acceptance Criteria:** https://www.leadingagile.com/2014/09/acceptance-criteria/
