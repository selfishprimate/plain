# Core Components: UI Building Blocks

This guide helps you define and document the essential UI components for your product.

---

## What are Core Components?

Core components are the reusable UI building blocks used throughout your product. They ensure consistency, speed up development, and create a cohesive user experience.

**Examples:** Button, Input, Card, Modal, Dropdown, Navigation, etc.

---

## Essential Components Checklist

### Form Components
- [ ] Button
- [ ] Input (text, email, password, number)
- [ ] Textarea
- [ ] Checkbox
- [ ] Radio button
- [ ] Select / Dropdown
- [ ] Switch / Toggle
- [ ] File upload
- [ ] Date picker
- [ ] Search input

### Layout Components
- [ ] Container
- [ ] Grid
- [ ] Card
- [ ] Divider
- [ ] Spacer

### Navigation Components
- [ ] Header / Navbar
- [ ] Sidebar
- [ ] Breadcrumb
- [ ] Tabs
- [ ] Pagination
- [ ] Menu / Dropdown menu

### Feedback Components
- [ ] Alert
- [ ] Toast / Notification
- [ ] Progress bar
- [ ] Spinner / Loader
- [ ] Skeleton loader
- [ ] Badge
- [ ] Tooltip

### Overlay Components
- [ ] Modal / Dialog
- [ ] Drawer / Sheet
- [ ] Popover
- [ ] Dropdown

### Display Components
- [ ] Avatar
- [ ] Icon
- [ ] Image
- [ ] Table
- [ ] List
- [ ] Accordion
- [ ] Collapse

---

## Component 1: Button

**Purpose:** Trigger actions

**Variants:**
- Primary — main CTAs
- Secondary — alternative actions
- Ghost — minimal, text-like
- Danger — destructive actions
- Link — styled as link

**States:**
- Default
- Hover
- Active / Pressed
- Focus
- Disabled
- Loading

**Sizes:**
- sm (small)
- md (medium / default)
- lg (large)

**Example (Shadcn/UI style):**
```jsx
<Button variant="primary" size="md">
  Click Me
</Button>

<Button variant="danger" size="sm" disabled>
  Delete
</Button>

<Button variant="ghost" loading>
  <Spinner /> Loading...
</Button>
```

**Accessibility:**
- Use `<button>` element
- Visible focus state
- Disabled state with `aria-disabled`
- Loading state with `aria-busy`

---

## Component 2: Input

**Purpose:** Text entry

**Types:**
- text
- email
- password
- number
- search
- url
- tel

**States:**
- Default
- Focus
- Error
- Success
- Disabled

**Features:**
- Label
- Placeholder
- Helper text
- Error message
- Prefix / suffix (icons)

**Example:**
```jsx
<Input
  type="email"
  label="Email"
  placeholder="you@example.com"
  error={errors.email}
  helperText="We'll never share your email"
  required
/>
```

**Accessibility:**
- Always include `<label>`
- Link label with `htmlFor` or wrap input
- Error messages with `aria-describedby`
- Use `aria-invalid` for errors

---

## Component 3: Card

**Purpose:** Group related content

**Variants:**
- Default
- Outlined (border only)
- Elevated (shadow)
- Interactive (hover effects)

**Structure:**
- Header (optional)
- Body
- Footer (optional)
- Image (optional)

**Example:**
```jsx
<Card>
  <CardHeader>
    <CardTitle>Card Title</CardTitle>
    <CardDescription>Description</CardDescription>
  </CardHeader>
  <CardContent>
    <p>Card content goes here.</p>
  </CardContent>
  <CardFooter>
    <Button>Action</Button>
  </CardFooter>
</Card>
```

**Use Cases:**
- Product cards
- Dashboard widgets
- Feature showcases
- Blog post previews

---

## Component 4: Modal / Dialog

**Purpose:** Display content above page

**Types:**
- Alert dialog (confirm/cancel)
- Form modal (data entry)
- Info modal (display info)
- Full-screen modal

**Features:**
- Backdrop / overlay
- Close button (X)
- ESC to close
- Focus trap
- Scroll lock

**Example:**
```jsx
<Modal open={isOpen} onClose={handleClose}>
  <ModalHeader>
    <ModalTitle>Confirm Delete</ModalTitle>
  </ModalHeader>
  <ModalContent>
    <p>Are you sure you want to delete this item?</p>
  </ModalContent>
  <ModalFooter>
    <Button variant="ghost" onClick={handleClose}>
      Cancel
    </Button>
    <Button variant="danger" onClick={handleDelete}>
      Delete
    </Button>
  </ModalFooter>
</Modal>
```

**Accessibility:**
- `role="dialog"`
- `aria-modal="true"`
- `aria-labelledby` for title
- Focus trap (tab stays inside)
- Return focus on close
- ESC key to close

---

## Component 5: Toast / Notification

**Purpose:** Brief feedback messages

**Types:**
- Success (green)
- Error (red)
- Warning (yellow/orange)
- Info (blue)

**Features:**
- Auto-dismiss (3-5 seconds)
- Manual dismiss (X button)
- Action button (optional)
- Position (top-right, bottom-center, etc.)

**Example:**
```jsx
toast.success('Task created successfully!');
toast.error('Failed to save changes');
toast.info('New update available', {
  action: {
    label: 'Refresh',
    onClick: () => window.location.reload()
  }
});
```

**Accessibility:**
- `role="status"` or `role="alert"`
- `aria-live="polite"` or `"assertive"`
- Screen reader announces message

---

## Component 6: Dropdown / Select

**Purpose:** Choose from list of options

**Types:**
- Single select
- Multi-select
- Searchable
- Grouped options

**States:**
- Closed
- Open
- Selected
- Disabled

**Example:**
```jsx
<Select
  options={[
    { value: 'todo', label: 'To Do' },
    { value: 'in_progress', label: 'In Progress' },
    { value: 'done', label: 'Done' }
  ]}
  value={status}
  onChange={setStatus}
  placeholder="Select status"
/>
```

**Accessibility:**
- Use native `<select>` when possible
- Custom: `role="listbox"`, `aria-expanded`
- Keyboard navigation (arrow keys)

---

## Component 7: Tabs

**Purpose:** Switch between views

**Example:**
```jsx
<Tabs defaultValue="profile">
  <TabsList>
    <TabsTrigger value="profile">Profile</TabsTrigger>
    <TabsTrigger value="settings">Settings</TabsTrigger>
    <TabsTrigger value="billing">Billing</TabsTrigger>
  </TabsList>
  <TabsContent value="profile">
    Profile content
  </TabsContent>
  <TabsContent value="settings">
    Settings content
  </TabsContent>
</Tabs>
```

**Accessibility:**
- `role="tablist"`, `role="tab"`, `role="tabpanel"`
- Arrow keys to navigate tabs
- `aria-selected` for active tab

---

## Component 8: Badge

**Purpose:** Labels, counts, status indicators

**Variants:**
- Default
- Primary
- Success
- Warning
- Error
- Outline

**Sizes:**
- sm
- md

**Example:**
```jsx
<Badge>New</Badge>
<Badge variant="success">Active</Badge>
<Badge variant="error">3 errors</Badge>
```

**Use Cases:**
- Status indicators
- Notification counts
- Tags/labels
- Feature flags ("Beta", "New")

---

## Component 9: Avatar

**Purpose:** User profile images

**Variants:**
- Image
- Initials (fallback)
- Icon

**Sizes:**
- xs, sm, md, lg, xl

**Example:**
```jsx
<Avatar
  src="/user.jpg"
  alt="John Doe"
  fallback="JD"
  size="md"
/>
```

**Accessibility:**
- Always include `alt` text
- Fallback for missing images

---

## Component 10: Table

**Purpose:** Display structured data

**Features:**
- Sortable columns
- Pagination
- Row selection
- Expandable rows
- Sticky header

**Example:**
```jsx
<Table>
  <TableHeader>
    <TableRow>
      <TableHead>Name</TableHead>
      <TableHead>Email</TableHead>
      <TableHead>Role</TableHead>
    </TableRow>
  </TableHeader>
  <TableBody>
    <TableRow>
      <TableCell>John Doe</TableCell>
      <TableCell>john@example.com</TableCell>
      <TableCell>Admin</TableCell>
    </TableRow>
  </TableBody>
</Table>
```

**Accessibility:**
- Use semantic `<table>` elements
- `<th>` for headers with `scope`
- Caption for table description

---

## Component Patterns

### Compound Components

**Group related components together.**

**Example:**
```jsx
<Card>
  <CardHeader />
  <CardContent />
  <CardFooter />
</Card>
```

**Benefits:**
- Flexible composition
- Clear API
- Reusable patterns

---

### Polymorphic Components

**Same component, different HTML elements.**

**Example:**
```jsx
<Button as="a" href="/about">
  Link Button
</Button>

<Button as="div" onClick={handleClick}>
  Div Button
</Button>
```

---

### Controlled vs Uncontrolled

**Controlled (React):**
```jsx
<Input value={name} onChange={(e) => setName(e.target.value)} />
```

**Uncontrolled:**
```jsx
<Input defaultValue="John" ref={inputRef} />
```

---

## Component Organization

### Folder Structure

**Option 1: Flat**
```
components/
  Button.tsx
  Input.tsx
  Card.tsx
```

**Option 2: Grouped**
```
components/
  forms/
    Button.tsx
    Input.tsx
  layout/
    Card.tsx
    Container.tsx
  feedback/
    Toast.tsx
    Alert.tsx
```

**Option 3: Atomic Design**
```
components/
  atoms/
    Button.tsx
    Icon.tsx
  molecules/
    SearchBar.tsx
    Card.tsx
  organisms/
    Header.tsx
    Sidebar.tsx
```

---

## Component Documentation

**What to document:**
- Purpose / use cases
- Props / API
- Variants / states
- Examples
- Accessibility notes
- Design tokens

**Tools:**
- Storybook
- Docusaurus
- Styleguidist
- Internal wiki

---

## Design System Tokens

**Define reusable values:**

```css
/* Colors */
--color-primary: #2563EB;
--color-success: #10B981;

/* Spacing */
--space-2: 8px;
--space-4: 16px;

/* Typography */
--text-sm: 14px;
--text-base: 16px;

/* Radius */
--radius-sm: 4px;
--radius-md: 8px;

/* Shadow */
--shadow-sm: 0 1px 2px rgba(0,0,0,0.05);
```

**Usage:**
```jsx
<Button style={{
  backgroundColor: 'var(--color-primary)',
  padding: 'var(--space-4)',
  borderRadius: 'var(--radius-md)'
}}>
  Click Me
</Button>
```

---

## Testing Components

### Visual Regression
- Chromatic
- Percy

### Unit Testing
- Jest + React Testing Library
- Vitest

### Accessibility Testing
- axe-core
- jest-axe

**Example Test:**
```jsx
import { render, screen } from '@testing-library/react';

test('Button renders correctly', () => {
  render(<Button>Click Me</Button>);
  expect(screen.getByText('Click Me')).toBeInTheDocument();
});
```

---

## Component Libraries

**Don't reinvent the wheel:**

### Headless (Unstyled)
- Radix UI
- Headless UI
- React Aria

### Styled (Pre-designed)
- Shadcn/UI
- Material UI
- Chakra UI

### Hybrid (Copy-paste)
- Shadcn/UI (copies into your project)

---

## Checklist

- [ ] Define core components needed
- [ ] Document variants and states
- [ ] Create design system tokens
- [ ] Build or adopt component library
- [ ] Ensure accessibility
- [ ] Add visual regression tests
- [ ] Document in Storybook or similar
- [ ] Share with team

---

## Resources

- **Radix UI:** https://radix-ui.com
- **Shadcn/UI:** https://ui.shadcn.com
- **Material UI:** https://mui.com
- **Storybook:** https://storybook.js.org
- **Component Examples:** https://component.gallery
