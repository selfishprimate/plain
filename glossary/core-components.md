# Core Components

Essential UI building blocks that form the foundation of modern web applications. Each component serves specific interaction patterns and can be combined to create complex interfaces. Components are listed alphabetically for easy reference.

## Quick Navigation

[A](#a) • [B](#b) • [C](#c) • [D](#d) • [E](#e) • [F](#f) • [G](#g) • [H](#h) • [I](#i) • [K](#k) • [L](#l) • [M](#m) • [N](#n) • [O](#o) • [P](#p) • [R](#r) • [S](#s) • [T](#t) • [V](#v)

---

## A

### Accordion
Vertically stacked panels that expand/collapse to reveal content sections.
- **Purpose:** Space-efficient content organization
- **Use Cases:**
  - FAQs sections
  - Product specifications
  - Settings panels with grouped options
  - Multi-step form sections
  - Documentation navigation
- **Key Features:** Single or multiple panels open, animated transitions, keyboard navigation
- **Accessibility:** Arrow keys navigation, ARIA expanded states

### Alert
Inline messages that communicate important information or feedback to users.
- **Purpose:** Display contextual notifications and warnings
- **Use Cases:**
  - Form validation errors
  - System status messages
  - Success confirmations
  - Warning notifications
  - Information banners
- **Key Features:** Severity levels (error, warning, info, success), dismissible option, icons
- **Variants:** Inline, banner, floating

### Alert Dialog
Modal dialog that interrupts workflow to convey critical information requiring user acknowledgment.
- **Purpose:** Capture attention for important decisions or warnings
- **Use Cases:**
  - Destructive action confirmations
  - Unsaved changes warnings
  - Session timeout alerts
  - Critical error messages
  - Legal agreements
- **Key Features:** Focus trap, backdrop, action buttons
- **Accessibility:** Focus management, escape key handling

### Aspect Ratio
Container that maintains consistent width-to-height ratio regardless of viewport size.
- **Purpose:** Preserve media proportions and prevent layout shift
- **Use Cases:**
  - Video embeds (16:9, 4:3)
  - Image containers
  - Maps and charts
  - Social media embeds
  - Responsive cards
- **Key Features:** Responsive scaling, content overflow handling
- **Common Ratios:** 16:9, 4:3, 1:1, 21:9

### Autocomplete
Text input with filtered suggestions based on user typing.
- **Purpose:** Speed up data entry and improve accuracy
- **Use Cases:**
  - Search boxes
  - Address forms
  - Tag selection
  - Email recipients
  - Command palettes
- **Key Features:** Debounced search, keyboard navigation, custom filtering
- **Variants:** Single select, multi-select, async loading

### Avatar
Visual representation of a user or entity, typically circular.
- **Purpose:** Identify users and personalize interface
- **Use Cases:**
  - User profiles
  - Comment sections
  - Chat interfaces
  - Team member lists
  - Navigation menus
- **Key Features:** Image fallback, initials, status indicators
- **Sizes:** xs, sm, md, lg, xl

### Avatar Group
Collection of overlapping avatars representing multiple users.
- **Purpose:** Show group membership or participants
- **Use Cases:**
  - Project team members
  - Meeting participants
  - Shared document collaborators
  - Group chat members
  - Viewer list
- **Key Features:** Max display count, overflow indicator, stacking direction
- **Variants:** Stacked, grid layout

## B

### Badge
Small status descriptor for UI elements, typically showing counts or labels.
- **Purpose:** Highlight status, counts, or categories
- **Use Cases:**
  - Notification counts
  - Status indicators (new, sale, beta)
  - Category tags
  - User roles
  - Version numbers
- **Key Features:** Color variants, sizes, removable option
- **Placement:** Inline, corner overlay, standalone

### Banner
Full-width message area for important announcements or alerts.
- **Purpose:** Communicate site-wide information
- **Use Cases:**
  - System maintenance notices
  - Cookie consent
  - Promotional announcements
  - Breaking news
  - Emergency alerts
- **Key Features:** Sticky positioning, dismissible, action buttons
- **Types:** Informational, warning, success, error

### Bottom Navigation
Mobile-style navigation bar fixed at screen bottom.
- **Purpose:** Primary navigation for mobile experiences
- **Use Cases:**
  - Mobile web apps
  - PWAs
  - Responsive navigation
  - Quick action access
  - Tab switching
- **Key Features:** 3-5 items, icons with labels, active state
- **Behavior:** Fixed position, hide on scroll option

### Breadcrumb
Navigation trail showing current page location in site hierarchy.
- **Purpose:** Orientation and navigation within nested structures
- **Use Cases:**
  - E-commerce category navigation
  - Documentation structure
  - File system paths
  - Multi-step processes
  - Settings navigation
- **Key Features:** Clickable parent links, current page indicator, separators
- **Patterns:** Chevron, slash, arrow separators

### Button
Interactive element that triggers actions when clicked.
- **Purpose:** Primary interaction element for user actions
- **Use Cases:**
  - Form submission
  - Dialog triggers
  - Navigation actions
  - Feature toggles
  - Command execution
- **Variants:** Primary, secondary, ghost, outline, destructive
- **States:** Default, hover, active, disabled, loading
- **Sizes:** xs, sm, md, lg, xl

### Button Group
Set of related buttons grouped together visually.
- **Purpose:** Organize related actions
- **Use Cases:**
  - Text formatting toolbar
  - View switchers
  - Pagination controls
  - Filter options
  - Sort controls
- **Key Features:** Visual connection, single selection option
- **Layouts:** Horizontal, vertical, segmented

## C

### Calendar
Date selection interface showing month/year views.
- **Purpose:** Visual date selection and scheduling
- **Use Cases:**
  - Date pickers
  - Event scheduling
  - Booking systems
  - Task deadlines
  - Birthday selection
- **Key Features:** Month navigation, date ranges, disabled dates
- **Variants:** Single date, date range, multi-select

### Card
Container component that groups related information.
- **Purpose:** Create visual hierarchy and group content
- **Use Cases:**
  - Product listings
  - Blog post previews
  - User profiles
  - Dashboard widgets
  - Feature highlights
- **Key Features:** Header, body, footer sections, media support
- **Variants:** Elevated, outlined, interactive

### Carousel
Slideshow component for cycling through content.
- **Purpose:** Display multiple items in limited space
- **Use Cases:**
  - Image galleries
  - Product showcases
  - Testimonials
  - News highlights
  - Onboarding flows
- **Key Features:** Auto-play, indicators, navigation controls
- **Types:** Single item, multi-item, fade, slide

### Chart
Data visualization components for displaying statistics.
- **Purpose:** Visual representation of data
- **Use Cases:**
  - Analytics dashboards
  - Financial reports
  - Progress tracking
  - Comparison displays
  - Trend analysis
- **Types:** Line, bar, pie, area, scatter, radar
- **Features:** Interactive tooltips, legends, animations

### Checkbox
Toggle control for binary choices, allows multiple selections.
- **Purpose:** Enable multiple option selection
- **Use Cases:**
  - Multiple choice forms
  - Feature toggles
  - Terms acceptance
  - Filter options
  - Bulk selection
- **States:** Unchecked, checked, indeterminate
- **Features:** Label association, group validation

### Chip
Compact element representing input, attribute, or action.
- **Purpose:** Display selected items or filters
- **Use Cases:**
  - Selected filters
  - Tags input
  - Contact selection
  - Skill badges
  - Search suggestions
- **Features:** Deletable, clickable, icon support
- **Variants:** Input, choice, filter, action

### Collapsible
Container that expands/collapses to show/hide content.
- **Purpose:** Progressive disclosure of information
- **Use Cases:**
  - Advanced settings
  - Additional details
  - Code examples
  - Long descriptions
  - Read more sections
- **Features:** Animated transitions, trigger customization
- **States:** Collapsed, expanded

### Color Picker
Interface for selecting colors from a palette or spectrum.
- **Purpose:** Enable color selection for customization
- **Use Cases:**
  - Theme customization
  - Design tools
  - Product variants
  - Calendar categories
  - Chart colors
- **Features:** HEX/RGB/HSL support, eyedropper, presets
- **Types:** Spectrum, swatches, input-based

### Combobox
Combination of text input and dropdown for selection.
- **Purpose:** Search and select from large datasets
- **Use Cases:**
  - Country selection
  - Product search
  - User mentions
  - Command menus
  - Location search
- **Features:** Filtering, create options, async loading
- **Behavior:** Type to search, keyboard navigation

### Command
Command palette for quick actions and navigation.
- **Purpose:** Power-user interface for quick access
- **Use Cases:**
  - Application navigation
  - Quick actions
  - Global search
  - Settings access
  - Keyboard shortcuts
- **Features:** Fuzzy search, nested commands, shortcuts display
- **Activation:** Keyboard shortcut (Cmd/Ctrl + K)

### Context Menu
Right-click menu providing contextual actions.
- **Purpose:** Context-specific actions on elements
- **Use Cases:**
  - File operations
  - Text editing options
  - Table row actions
  - Image manipulation
  - Copy/paste operations
- **Features:** Nested menus, keyboard shortcuts, icons
- **Behavior:** Right-click or long-press activation

## D

### Data Table
Complex table component with sorting, filtering, and pagination.
- **Purpose:** Display and interact with structured data
- **Use Cases:**
  - Admin dashboards
  - Report displays
  - User management
  - Order lists
  - Inventory management
- **Features:** Sort, filter, pagination, row selection, column resize
- **Advanced:** Virtualization, export, inline editing

### Date Picker
Calendar-based date selection component.
- **Purpose:** User-friendly date input
- **Use Cases:**
  - Booking forms
  - Event creation
  - Report filters
  - Birthday input
  - Deadline setting
- **Features:** Min/max dates, date ranges, presets
- **Formats:** Various date formats, localization

### Date Range Picker
Dual calendar for selecting date ranges.
- **Purpose:** Select start and end dates
- **Use Cases:**
  - Hotel bookings
  - Analytics periods
  - Leave requests
  - Report ranges
  - Project timelines
- **Features:** Presets (last 7 days, month), max range limit
- **Validation:** No overlap, minimum duration

### Dialog
Modal overlay for focused interactions.
- **Purpose:** Focused interaction without leaving page
- **Use Cases:**
  - Forms submission
  - Confirmations
  - Media previews
  - Settings panels
  - Login/signup
- **Features:** Backdrop, close button, scrollable content
- **Sizes:** sm, md, lg, xl, full

### Divider
Visual separator between content sections.
- **Purpose:** Create visual hierarchy and separation
- **Use Cases:**
  - Section breaks
  - List item separation
  - Navigation groups
  - Form sections
  - Card divisions
- **Variants:** Horizontal, vertical, dashed, dotted
- **Features:** Text label option, spacing control

### Drawer
Panel that slides in from screen edge.
- **Purpose:** Secondary content or navigation access
- **Use Cases:**
  - Mobile navigation
  - Filter panels
  - Shopping cart
  - Chat interfaces
  - Settings sidebar
- **Positions:** Left, right, top, bottom
- **Features:** Overlay option, swipe gestures

### Dropdown Menu
Toggleable menu for displaying choices.
- **Purpose:** Space-efficient option selection
- **Use Cases:**
  - User account menu
  - Settings options
  - Sort selection
  - More actions menu
  - Language selector
- **Features:** Nested items, dividers, keyboard navigation
- **Trigger:** Click, hover, right-click

## E

### Empty State
Placeholder shown when no content is available.
- **Purpose:** Guide users when content is absent
- **Use Cases:**
  - No search results
  - Empty lists
  - First-time setup
  - Error states
  - Zero data
- **Features:** Illustration, message, action button
- **Types:** No data, no results, error, first use

### Error Boundary
Component that catches JavaScript errors in component tree.
- **Purpose:** Graceful error handling in production
- **Use Cases:**
  - Application stability
  - Third-party widget isolation
  - Feature degradation
  - Error reporting
  - User feedback
- **Features:** Fallback UI, error logging, retry action
- **Implementation:** React error boundary pattern

## F

### File Upload
Interface for uploading files to the application.
- **Purpose:** Enable file submission from users
- **Use Cases:**
  - Profile photo upload
  - Document submission
  - Bulk import
  - Media galleries
  - Attachment handling
- **Features:** Drag and drop, progress indication, validation
- **Types:** Single, multiple, dropzone

### Floating Action Button (FAB)
Circular button for primary screen action.
- **Purpose:** Promote primary action
- **Use Cases:**
  - Compose new item
  - Add record
  - Start chat
  - Quick action menu
  - Create post
- **Position:** Bottom right (typically)
- **Features:** Extended variant with label, mini size

### Form
Container for collecting user input with validation.
- **Purpose:** Structured data collection
- **Use Cases:**
  - User registration
  - Settings updates
  - Contact forms
  - Checkout process
  - Survey collection
- **Features:** Validation, error handling, submit states
- **Components:** Fields, labels, help text, error messages

## G

### Grid
Layout component for arranging items in rows and columns.
- **Purpose:** Create structured layouts
- **Use Cases:**
  - Image galleries
  - Product listings
  - Card layouts
  - Dashboard widgets
  - Icon sets
- **Features:** Responsive columns, gap control, alignment
- **Types:** Fixed, fluid, masonry

## H

### Heatmap
Visual representation of data using color intensity.
- **Purpose:** Show data density or intensity patterns
- **Use Cases:**
  - Analytics visualization
  - Calendar activity
  - Geographic data
  - User behavior
  - Performance metrics
- **Features:** Color scales, tooltips, zoom capability
- **Types:** Calendar, geographic, matrix

### Hero
Prominent banner section typically at page top.
- **Purpose:** Make strong first impression
- **Use Cases:**
  - Landing pages
  - Marketing sites
  - Product launches
  - Campaign pages
  - Homepage headers
- **Features:** Background images/videos, CTAs, animations
- **Components:** Headline, subtitle, CTA buttons, media

### Hover Card
Popup card shown on hover with additional information.
- **Purpose:** Preview content without navigation
- **Use Cases:**
  - User profile preview
  - Link previews
  - Product quick view
  - Tooltip extensions
  - Definition popups
- **Features:** Delayed show/hide, rich content support
- **Trigger:** Hover with delay

## I

### Icon
Symbolic graphics representing actions, objects, or concepts.
- **Purpose:** Visual communication and enhancement
- **Use Cases:**
  - Navigation items
  - Button labels
  - Status indicators
  - Feature representation
  - Action triggers
- **Types:** Outlined, filled, two-tone
- **Sizes:** xs, sm, md, lg, xl

### Image
Graphic content display with loading and error states.
- **Purpose:** Display visual content
- **Use Cases:**
  - Product photos
  - User avatars
  - Blog illustrations
  - Gallery items
  - Background images
- **Features:** Lazy loading, placeholder, error fallback
- **Optimization:** Responsive sizes, formats (WebP, AVIF)

### Input
Text field for user data entry.
- **Purpose:** Collect text-based user input
- **Use Cases:**
  - Form fields
  - Search boxes
  - Comments
  - Messages
  - Settings values
- **Types:** Text, email, password, number, tel, url
- **Features:** Placeholder, validation, icons, clear button

### Input OTP
Specialized input for one-time passwords.
- **Purpose:** Secure code entry for authentication
- **Use Cases:**
  - Two-factor authentication
  - Email verification
  - Phone verification
  - Password reset
  - Secure transactions
- **Features:** Auto-focus next, paste handling, masking
- **Length:** Typically 4-6 digits

## K

### Kanban Board
Drag-and-drop board for organizing items in columns.
- **Purpose:** Visual task/item management
- **Use Cases:**
  - Project management
  - Task tracking
  - Content planning
  - Workflow visualization
  - Sprint planning
- **Features:** Drag and drop, swim lanes, WIP limits
- **Components:** Columns, cards, headers

### Keyboard Shortcuts
Display of available keyboard commands.
- **Purpose:** Show power-user features
- **Use Cases:**
  - Help documentation
  - Command palette
  - Tooltip hints
  - Settings page
  - Onboarding
- **Features:** OS detection, key combination display
- **Format:** Modifier + Key notation

## L

### Label
Text description associated with form controls.
- **Purpose:** Identify form inputs and improve accessibility
- **Use Cases:**
  - Form fields
  - Checkboxes
  - Radio buttons
  - Switches
  - Sliders
- **Features:** Required indicator, help icon, error state
- **Positioning:** Above, inline, floating

### List
Structured collection of related items.
- **Purpose:** Display sequential or related content
- **Use Cases:**
  - Navigation menus
  - Search results
  - Activity feeds
  - Settings options
  - File listings
- **Types:** Unordered, ordered, description lists
- **Features:** Icons, actions, dividers, grouping

### Loading
Indicator showing content or action is in progress.
- **Purpose:** Provide feedback during async operations
- **Use Cases:**
  - Page loads
  - Form submissions
  - Data fetching
  - File uploads
  - Process execution
- **Types:** Spinner, skeleton, progress bar, dots
- **Variants:** Inline, overlay, full-page

## M

### Map
Interactive geographic display component.
- **Purpose:** Show location-based information
- **Use Cases:**
  - Store locators
  - Delivery tracking
  - Event locations
  - Property listings
  - Route planning
- **Features:** Markers, zoom controls, layers
- **Providers:** Google Maps, Mapbox, OpenStreetMap

### Mega Menu
Large dropdown panel with multiple sections and columns.
- **Purpose:** Navigate complex site structures
- **Use Cases:**
  - E-commerce categories
  - Enterprise navigation
  - Product features
  - Service offerings
  - Documentation sections
- **Features:** Multi-column layout, images, featured items
- **Activation:** Hover or click

### Menu
List of options or commands.
- **Purpose:** Provide action or navigation choices
- **Use Cases:**
  - Navigation
  - Context actions
  - Settings
  - User preferences
  - Filters
- **Features:** Icons, shortcuts, nested items, dividers
- **Types:** Vertical, horizontal, nested

### Menu Bar
Horizontal bar containing multiple menus.
- **Purpose:** Application-level navigation and commands
- **Use Cases:**
  - Desktop applications
  - Admin panels
  - Editor interfaces
  - IDEs
  - Complex tools
- **Features:** Dropdown menus, keyboard navigation
- **Pattern:** File, Edit, View, etc.

### Modal
Overlay dialog requiring user interaction.
- **Purpose:** Focus user attention on specific task
- **Use Cases:**
  - Confirmations
  - Forms
  - Media viewers
  - Wizards
  - Warnings
- **Features:** Backdrop, close methods, size variants
- **Behavior:** Focus trap, escape key closing

## N

### Navigation Menu
Primary site navigation component.
- **Purpose:** Main site/app navigation
- **Use Cases:**
  - Site headers
  - App navigation
  - Documentation nav
  - Mobile menus
  - Sidebars
- **Features:** Active states, dropdowns, mobile responsive
- **Types:** Horizontal, vertical, hamburger

### Notification
Temporary message informing users of events or status.
- **Purpose:** Inform users of system events
- **Use Cases:**
  - Success messages
  - Error alerts
  - System updates
  - New messages
  - Reminders
- **Features:** Auto-dismiss, actions, stacking
- **Position:** Top, bottom, corners

### Number Input
Specialized input for numeric values.
- **Purpose:** Controlled number entry
- **Use Cases:**
  - Quantity selection
  - Price input
  - Age entry
  - Settings values
  - Score input
- **Features:** Min/max, step, increment buttons
- **Validation:** Range, decimal places

## O

### Off-Canvas
Hidden panel that slides into view.
- **Purpose:** Secondary content without page change
- **Use Cases:**
  - Mobile navigation
  - Filter panels
  - Shopping cart
  - Help panels
  - Settings
- **Features:** Push/overlay modes, backdrop
- **Positions:** Left, right, top, bottom

## P

### Pagination
Navigation between pages of content.
- **Purpose:** Navigate large datasets
- **Use Cases:**
  - Search results
  - Table data
  - Blog posts
  - Product listings
  - Gallery pages
- **Features:** Page numbers, prev/next, page size
- **Variants:** Numbered, simple, load more, infinite

### Popover
Floating panel anchored to trigger element.
- **Purpose:** Show additional content on demand
- **Use Cases:**
  - Help information
  - User cards
  - Menus
  - Tooltips
  - Previews
- **Features:** Positioning, arrow, click outside to close
- **Trigger:** Click, hover, focus

### Progress
Visual indicator of task completion status.
- **Purpose:** Show operation progress
- **Use Cases:**
  - File uploads
  - Form completion
  - Loading states
  - Skill levels
  - Goal tracking
- **Types:** Linear, circular, stepped
- **Features:** Percentage, labels, animation

## R

### Radio Group
Set of mutually exclusive options.
- **Purpose:** Single selection from multiple options
- **Use Cases:**
  - Payment methods
  - Delivery options
  - Survey questions
  - Settings choices
  - Plan selection
- **Features:** Default selection, disabled options
- **Layout:** Vertical, horizontal, grid

### Range Slider
Input for selecting value from a range.
- **Purpose:** Visual value selection
- **Use Cases:**
  - Price filters
  - Volume control
  - Brightness adjustment
  - Timeline scrubbing
  - Rating input
- **Features:** Min/max, steps, labels, dual handles
- **Display:** Value tooltip, tick marks

### Rating
Star or numeric rating component.
- **Purpose:** Collect or display ratings
- **Use Cases:**
  - Product reviews
  - Feedback forms
  - Service ratings
  - Content ratings
  - Skill assessment
- **Features:** Half stars, custom icons, read-only mode
- **Types:** Stars, hearts, thumbs, numeric

### Resizable
Component allowing user to resize panels.
- **Purpose:** Adjustable layout sections
- **Use Cases:**
  - Split panels
  - Code editors
  - File explorers
  - Email clients
  - IDEs
- **Features:** Min/max constraints, handle styling
- **Direction:** Horizontal, vertical, both

## S

### Scroll Area
Container with custom scrollbars.
- **Purpose:** Consistent scroll styling
- **Use Cases:**
  - Long content areas
  - Code blocks
  - Chat windows
  - Sidebars
  - Modals
- **Features:** Custom scrollbar styling, auto-hide
- **Types:** Vertical, horizontal, both

### Search
Input optimized for search functionality.
- **Purpose:** Enable content discovery
- **Use Cases:**
  - Site search
  - Data filtering
  - Navigation
  - Documentation
  - Product search
- **Features:** Suggestions, recent searches, filters
- **Types:** Instant, with button, command palette

### Select
Dropdown for choosing from predefined options.
- **Purpose:** Single selection from list
- **Use Cases:**
  - Country selection
  - Category choice
  - Sort options
  - Language picker
  - Size selection
- **Features:** Search, groups, custom rendering
- **Variants:** Native, custom styled

### Separator
Visual divider between interface sections.
- **Purpose:** Visual content separation
- **Use Cases:**
  - Menu sections
  - List items
  - Form groups
  - Toolbar groups
  - Content sections
- **Orientation:** Horizontal, vertical
- **Styles:** Solid, dashed, dotted

### Sheet
Modal panel sliding from screen edge.
- **Purpose:** Secondary content or actions
- **Use Cases:**
  - Mobile menus
  - Filter panels
  - Settings
  - Cart review
  - Quick edit
- **Features:** Swipe to dismiss, multiple sizes
- **Positions:** Top, right, bottom, left

### Skeleton
Placeholder showing content structure while loading.
- **Purpose:** Perceived performance improvement
- **Use Cases:**
  - Content loading
  - Image placeholders
  - List items
  - Cards
  - Tables
- **Features:** Animation, shapes matching content
- **Types:** Text, avatar, image, custom

### Slider
Single value selection from range.
- **Purpose:** Visual numeric input
- **Use Cases:**
  - Volume control
  - Brightness setting
  - Price range
  - Progress input
  - Timeline control
- **Features:** Marks, labels, tooltips
- **Orientation:** Horizontal, vertical

### Snackbar
Brief notification appearing temporarily.
- **Purpose:** Non-intrusive feedback
- **Use Cases:**
  - Action confirmations
  - Quick messages
  - Undo options
  - Status updates
  - Tips
- **Features:** Auto-dismiss, action button
- **Position:** Bottom, top

### Sonner
Toast notification system (specific implementation).
- **Purpose:** Elegant toast notifications
- **Use Cases:**
  - Success messages
  - Error handling
  - Loading states
  - Promises
  - Updates
- **Features:** Promise API, custom rendering
- **Types:** Success, error, loading, promise

### Speed Dial
Floating action button with sub-actions.
- **Purpose:** Quick access to multiple actions
- **Use Cases:**
  - Create options
  - Share menu
  - Quick actions
  - Tools menu
  - Contact options
- **Features:** Animation, labels, backdrop
- **Direction:** Up, down, left, right

### Spinner
Rotating indicator for loading states.
- **Purpose:** Indicate processing
- **Use Cases:**
  - Loading states
  - Async operations
  - Form submission
  - Data fetching
  - Processing
- **Sizes:** xs, sm, md, lg, xl
- **Variants:** Circle, dots, bars

### Split Button
Button with primary action and dropdown.
- **Purpose:** Primary action with alternatives
- **Use Cases:**
  - Save options
  - Send variations
  - Export formats
  - Run commands
  - Create types
- **Features:** Default action, menu options
- **Behavior:** Click for primary, arrow for menu

### Spotlight
Overlay search interface.
- **Purpose:** Global search and navigation
- **Use Cases:**
  - Application search
  - Command palette
  - File finder
  - Help search
  - Quick navigation
- **Features:** Fuzzy search, categories, shortcuts
- **Activation:** Keyboard shortcut

### Stepper
Multi-step process indicator.
- **Purpose:** Guide through multi-step processes
- **Use Cases:**
  - Checkout flow
  - Onboarding
  - Form wizards
  - Setup guides
  - Tutorials
- **Features:** Step validation, navigation, progress
- **Types:** Horizontal, vertical, simple, detailed

### Switch
Toggle control for on/off states.
- **Purpose:** Binary setting control
- **Use Cases:**
  - Feature toggles
  - Preferences
  - Notifications
  - Dark mode
  - Privacy settings
- **States:** On, off, disabled
- **Features:** Labels, icons, loading state

## T

### Table
Structured data display in rows and columns.
- **Purpose:** Display tabular data
- **Use Cases:**
  - Data lists
  - Reports
  - Comparisons
  - Schedules
  - Pricing tables
- **Features:** Headers, sorting, responsive design
- **Variants:** Basic, striped, bordered

### Tabs
Layered sections of content.
- **Purpose:** Organize related content
- **Use Cases:**
  - Settings groups
  - Product details
  - Profile sections
  - Documentation
  - Dashboard views
- **Features:** Icons, badges, lazy loading
- **Orientation:** Horizontal, vertical

### Tag
Label for categorization or identification.
- **Purpose:** Categorize and label items
- **Use Cases:**
  - Blog categories
  - Product tags
  - Status labels
  - Skills
  - Filters
- **Features:** Colors, removable, clickable
- **Sizes:** sm, md, lg

### Textarea
Multi-line text input field.
- **Purpose:** Extended text input
- **Use Cases:**
  - Comments
  - Descriptions
  - Messages
  - Notes
  - Feedback
- **Features:** Auto-resize, character count, resize handle
- **Validation:** Min/max length, required

### Timeline
Chronological display of events.
- **Purpose:** Show temporal sequences
- **Use Cases:**
  - Activity history
  - Project milestones
  - Order tracking
  - Change logs
  - Social feeds
- **Features:** Icons, dates, descriptions
- **Orientation:** Vertical, horizontal

### Time Picker
Interface for selecting time values.
- **Purpose:** Time input control
- **Use Cases:**
  - Appointment scheduling
  - Reminders
  - Event times
  - Alarms
  - Deadlines
- **Features:** 12/24 hour format, minute steps
- **Types:** Dropdown, clock face, input

### Toast
Non-blocking notification message.
- **Purpose:** Temporary feedback messages
- **Use Cases:**
  - Save confirmations
  - Error messages
  - Success alerts
  - Info updates
  - Warnings
- **Features:** Auto-dismiss, stacking, actions
- **Position:** Top, bottom, corners

### Toggle
Control switching between two states.
- **Purpose:** Binary state control
- **Use Cases:**
  - Settings options
  - Feature flags
  - View modes
  - Filters
  - Preferences
- **Features:** Icons, labels, groups
- **Types:** Button toggle, switch

### Toggle Group
Set of toggle buttons with single or multiple selection.
- **Purpose:** Option selection from group
- **Use Cases:**
  - Text formatting
  - View switchers
  - Size selection
  - Alignment tools
  - Filters
- **Features:** Single/multiple selection, icons
- **Layout:** Horizontal, vertical

### Toolbar
Container for action buttons and controls.
- **Purpose:** Group related actions
- **Use Cases:**
  - Text editors
  - Image editors
  - Table controls
  - Form builders
  - Admin actions
- **Features:** Grouping, separators, overflow
- **Position:** Top, bottom, floating

### Tooltip
Contextual help text on hover.
- **Purpose:** Provide additional information
- **Use Cases:**
  - Help text
  - Abbreviations
  - Icon labels
  - Truncated text
  - Keyboard shortcuts
- **Features:** Delay, positioning, rich content
- **Trigger:** Hover, focus, click

### Tree View
Hierarchical list with expandable nodes.
- **Purpose:** Display nested structures
- **Use Cases:**
  - File explorers
  - Navigation menus
  - Organization charts
  - Category trees
  - Settings panels
- **Features:** Expand/collapse, checkboxes, drag and drop
- **Interaction:** Keyboard navigation, multi-select

### Typeahead
Text input with real-time suggestions.
- **Purpose:** Predictive text input
- **Use Cases:**
  - Search boxes
  - Address entry
  - Email composition
  - Tags input
  - Command input
- **Features:** Highlighting, keyboard navigation
- **Data:** Static, async, filtered

## V

### Video Player
Media player for video content.
- **Purpose:** Display and control video playback
- **Use Cases:**
  - Media galleries
  - Tutorials
  - Product demos
  - Entertainment
  - Training
- **Features:** Controls, fullscreen, captions, quality
- **Types:** HTML5, YouTube, Vimeo embed

### Virtual List
Efficiently renders large lists by virtualizing.
- **Purpose:** Performance optimization for long lists
- **Use Cases:**
  - Large datasets
  - Infinite scroll
  - Chat messages
  - Log viewers
  - File lists
- **Features:** Dynamic height, horizontal scroll
- **Performance:** Only renders visible items

---

## Component Categories

### Layout Components
Grid, Container, Divider, Spacer, Stack

### Navigation Components
Breadcrumb, Menu, Navigation Menu, Pagination, Stepper, Tabs

### Data Entry Components
Input, Textarea, Select, Checkbox, Radio, Switch, Slider, Date Picker

### Data Display Components
Table, List, Card, Avatar, Badge, Tag, Timeline

### Feedback Components
Alert, Notification, Toast, Progress, Spinner, Skeleton

### Overlay Components
Dialog, Drawer, Modal, Popover, Tooltip

### Action Components
Button, FAB, Speed Dial, Toolbar

---

*These components form the building blocks of modern user interfaces. Choose components that match your design system and user needs, ensuring consistency across your application.*