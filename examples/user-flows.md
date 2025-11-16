# User Flows: Examples & Patterns

This guide provides examples of user flows and helps you document how users navigate through your product.

---

## What is a User Flow?

A user flow describes the step-by-step path a user takes to accomplish a specific goal within your product.

**Purpose:**
- Identify friction points
- Ensure logical navigation
- Document user journey
- Guide UI/UX design
- Help developers understand context

**Format:**
- Numbered steps
- Actions → System responses
- Decision points (if/else)
- Error states

---

## Example 1: Sign Up Flow (Email/Password)

### Goal: New user creates an account

**Flow:**
1. User lands on homepage
2. User clicks "Sign Up" button in header
3. System displays sign-up modal/page with form:
   - Email input
   - Password input
   - Confirm password input
   - Terms & conditions checkbox
4. User fills out form
5. User clicks "Create Account" button
6. **System validates inputs:**
   - ✅ If valid → Create account, send verification email
   - ❌ If invalid → Show error messages next to fields
7. User is redirected to onboarding page or dashboard
8. Success toast appears: "Account created! Check your email to verify."

**Alternative Path (OAuth):**
1. User clicks "Sign up with Google"
2. System opens Google OAuth popup
3. User authenticates with Google
4. System creates account with Google profile data
5. User is redirected to dashboard
6. Welcome message displayed

**Edge Cases:**
- Email already exists → Show error: "Account already exists. Try logging in."
- Weak password → Show inline validation feedback
- Network error → Show retry button
- User closes modal → Save draft in localStorage (optional)

---

## Example 2: Checkout Flow (E-commerce)

### Goal: User completes a purchase

**Flow:**
1. User views product page
2. User selects quantity/variant (size, color)
3. User clicks "Add to Cart"
4. System adds item to cart, shows confirmation toast
5. User clicks "View Cart" or cart icon
6. System displays cart page with:
   - Item list
   - Quantity adjusters
   - Price breakdown
   - "Proceed to Checkout" button
7. User clicks "Proceed to Checkout"
8. **If not logged in:**
   - System shows login/signup prompt
   - User logs in → Continue to step 9
9. System displays checkout form:
   - Shipping address
   - Billing address (optional: same as shipping)
   - Payment method
10. User fills out form
11. User clicks "Place Order"
12. **System validates and processes:**
    - ✅ If successful → Charge payment, create order
    - ❌ If payment fails → Show error, allow retry
13. System displays order confirmation page
14. Confirmation email sent

**Alternative Path (Guest Checkout):**
- Skip login, allow email-only checkout
- Offer account creation after purchase

**Edge Cases:**
- Item out of stock → Remove from cart, notify user
- Promo code invalid → Show error message
- Address validation fails → Suggest corrections
- Payment declined → Show error with retry/change payment option

---

## Example 3: Search & Filter Flow (SaaS Tool Directory)

### Goal: User finds a specific AI tool

**Flow:**
1. User lands on homepage
2. User sees search bar and category filters
3. User types keyword (e.g., "image generator") in search bar
4. System displays real-time filtered results
5. User applies additional filters:
   - Category: "Design"
   - Pricing: "Free"
   - Rating: "4+ stars"
6. System updates results in real-time
7. User clicks on a tool card
8. System opens tool detail page with:
   - Description
   - Features
   - Pricing
   - Screenshots
   - Link to official website
   - Bookmark button
9. User clicks "Bookmark" button
10. **If not logged in:**
    - System prompts login/signup
    - User logs in → Bookmark saved
11. **If logged in:**
    - System saves bookmark
    - Button changes to "Bookmarked" state
    - Toast: "Added to bookmarks"
12. User clicks "Visit Website" button
13. System opens tool's website in new tab

**Alternative Path (Browse by Category):**
1. User clicks on category card (e.g., "Writing Tools")
2. System displays filtered tool list
3. Continue from step 5

**Edge Cases:**
- No results found → Show "No tools match your filters. Try adjusting."
- Search query too short → Show prompt: "Type at least 2 characters"
- Slow network → Show loading skeleton

---

## Example 4: Onboarding Flow (Productivity App)

### Goal: Guide new user to first task creation

**Flow:**
1. User completes sign-up
2. System displays onboarding welcome screen
3. User clicks "Get Started"
4. **Step 1: Profile Setup**
   - User enters name, selects timezone
   - User clicks "Next"
5. **Step 2: Choose Use Case**
   - System shows options:
     - "Personal tasks"
     - "Freelance work"
     - "Team projects"
   - User selects "Freelance work"
   - User clicks "Next"
6. **Step 3: Create First Task**
   - System displays task creation tutorial overlay
   - User creates a sample task
   - User clicks "Create Task"
7. **Step 4: Success**
   - System shows congratulations message
   - User clicks "Go to Dashboard"
8. System redirects to dashboard
9. Dashboard displays tutorial tooltips (dismissible)

**Skip Option:**
- "Skip onboarding" button available
- User can complete later via settings

---

## Example 5: Password Reset Flow

### Goal: User recovers forgotten password

**Flow:**
1. User clicks "Forgot password?" on login page
2. System displays password reset page
3. User enters email address
4. User clicks "Send Reset Link"
5. **System validates email:**
   - ✅ If email exists → Send reset link email
   - ❌ If email not found → Show generic message (security)
6. System displays: "If that email exists, we sent a reset link."
7. User checks email
8. User clicks reset link in email
9. System validates token:
   - ✅ Valid → Show password reset form
   - ❌ Expired/invalid → Show error with "Request new link" option
10. User enters new password
11. User confirms new password
12. User clicks "Reset Password"
13. **System validates password:**
    - ✅ If valid → Update password
    - ❌ If invalid → Show requirements
14. System displays success message
15. User clicks "Log in"
16. System redirects to login page

**Edge Cases:**
- Link expired → Show "Link expired. Request new one."
- Password too weak → Show strength indicator and requirements
- User tries to reuse old password → Prevent (optional security)

---

## Example 6: Social Sharing Flow

### Goal: User shares a tool on Twitter

**Flow:**
1. User is viewing tool detail page
2. User clicks "Share on Twitter" button
3. System opens Twitter share dialog (popup or new tab)
4. Dialog is pre-populated with:
   - Tool name
   - Short description
   - Link to tool page
   - Hashtags (optional)
5. User edits tweet text (optional)
6. User clicks "Tweet"
7. Twitter posts tweet
8. System tracks share event (analytics)
9. User returns to tool page
10. System shows toast: "Shared on Twitter!"

**Alternative (Copy Link):**
1. User clicks "Copy Link" button
2. System copies URL to clipboard
3. Toast: "Link copied!"

---

## Example 7: Collaborative Editing Flow (Real-time)

### Goal: Multiple users edit a document simultaneously

**Flow:**
1. User A opens document
2. System loads document content
3. User A starts editing
4. **User B joins the same document**
5. System shows User B's avatar/cursor to User A
6. User B starts editing
7. System syncs changes in real-time:
   - User A sees User B's changes instantly
   - User B sees User A's changes instantly
8. User A tries to edit same paragraph as User B
9. System handles conflict:
   - Option 1: Last write wins
   - Option 2: Show merge dialog
   - Option 3: Lock paragraph while editing
10. User A saves changes
11. System auto-saves for all users
12. User B leaves document
13. System removes User B's presence indicator

**Edge Cases:**
- Connection lost → Show "You're offline. Changes saved locally."
- Reconnection → Sync local changes
- Edit conflicts → Merge or prompt user

---

## Example 8: Subscription Upgrade Flow (SaaS)

### Goal: Free user upgrades to Pro plan

**Flow:**
1. User encounters paywall feature (e.g., "Export to CSV")
2. System shows upgrade prompt:
   - Feature locked message
   - "Upgrade to Pro" button
3. User clicks "Upgrade to Pro"
4. System displays pricing page with plan comparison
5. User selects "Pro Plan ($9.99/month)"
6. User clicks "Continue"
7. System displays payment form (Stripe Checkout)
8. User enters payment details
9. User clicks "Subscribe"
10. **System processes payment:**
    - ✅ Success → Upgrade account, enable features
    - ❌ Failed → Show error, allow retry
11. System redirects to success page
12. Success message: "Welcome to Pro!"
13. Confirmation email sent
14. User can now access Pro features

**Alternative (Trial):**
- Offer 14-day free trial
- No credit card required
- Auto-remind before trial ends

---

## User Flow Patterns

### Pattern 1: Happy Path (Success)
Focus on the ideal scenario where everything works.

### Pattern 2: Error Handling
Document what happens when things go wrong.

### Pattern 3: Alternative Paths
Show different ways to achieve the same goal.

### Pattern 4: Decision Trees
Use branching logic for complex flows.

**Example Decision Tree:**
```
User clicks "Sign Up"
├─ If has social account
│  └─ OAuth flow
└─ If no social account
   └─ Email/password flow
```

---

## Creating User Flows

### Step 1: Define the Goal
What is the user trying to accomplish?

### Step 2: Identify Entry Point
Where does the flow start? (homepage, email link, notification)

### Step 3: List Steps Sequentially
Write each action and system response.

### Step 4: Add Decision Points
What happens if validation fails? What are alternative paths?

### Step 5: Define Success State
How does the user know they've completed the goal?

### Step 6: Document Edge Cases
What could go wrong? How do you handle it?

---

## User Flow Template

```
### Goal: [What user wants to achieve]

**Flow:**
1. User [action]
2. System [response]
3. User [action]
4. **System validates:**
   - ✅ If [condition] → [outcome]
   - ❌ If [condition] → [outcome]
5. [Continue steps...]
6. Success state: [final message/screen]

**Alternative Path:**
[Describe alternate way to achieve goal]

**Edge Cases:**
- [Error scenario] → [How to handle]
- [Edge case] → [Solution]
```

---

## Visualizing User Flows

**Tools:**
- **Figma / FigJam** — Visual flowcharts
- **Miro** — Collaborative whiteboard
- **Whimsical** — Flow diagrams
- **Lucidchart** — Professional flowcharts
- **Draw.io** — Free, web-based

**Symbols:**
- Rectangle → Action/Screen
- Diamond → Decision point
- Arrow → Flow direction
- Circle → Start/End

---

## Testing User Flows

### Checklist:
- [ ] All steps documented
- [ ] Error states defined
- [ ] Alternative paths included
- [ ] Success criteria clear
- [ ] Edge cases handled
- [ ] Accessibility considered (keyboard navigation)
- [ ] Mobile and desktop flows differ?

---

## Common Flow Types

| **Flow Type** | **Goal** | **Example** |
|---|---|---|
| Onboarding | Guide new user | Profile setup, tutorial |
| Authentication | Log in/sign up | Email, OAuth, magic link |
| Transaction | Complete purchase | Checkout, payment |
| Content Creation | Create item | New task, blog post, design |
| Search & Filter | Find item | Product search, tool discovery |
| Social Interaction | Share, comment | Tweet share, comment post |
| Settings/Preferences | Update account | Change password, theme |
| Error Recovery | Recover from error | Password reset, retry payment |

---

## Resources

- **Laws of UX:** https://lawsofux.com
- **User Flow Best Practices:** https://www.nngroup.com/articles/
- **Figma Templates:** Community user flow templates
