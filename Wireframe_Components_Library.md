# Wireframe Components Library
## Capital Radiology Online System

### Table of Contents
1. [Component Overview](#component-overview)
2. [Navigation Components](#navigation-components)
3. [Form Components](#form-components)
4. [Data Display Components](#data-display-components)
5. [Interactive Components](#interactive-components)
6. [Medical-Specific Components](#medical-specific-components)
7. [Layout Components](#layout-components)
8. [Icon Library](#icon-library)
9. [Component Usage Guidelines](#component-usage-guidelines)
10. [Symbol Library Creation](#symbol-library-creation)

---

## Component Overview

### Balsamiq Component Mapping
This library maps UI elements from the Capital Radiology Online System specifications to specific Balsamiq components, ensuring consistency and reusability across all wireframes.

### Component Categories
- **Navigation**: Headers, menus, breadcrumbs, tabs
- **Forms**: Inputs, buttons, validation, wizards
- **Data Display**: Tables, cards, charts, lists
- **Interactive**: Modals, tooltips, dropdowns, sliders
- **Medical**: DICOM viewers, equipment status, patient info
- **Layout**: Containers, grids, panels, spacers

---

## Navigation Components

### 1. Primary Navigation Header

#### **CR-NAV-001: Main Header**
**Balsamiq Component**: Rectangle + Labels + Button
```
Properties:
- Size: W:1200, H:60
- Fill: #0056B3
- Border: None
- Position: Top of canvas (Y:0)

Components:
- Logo placeholder (Image): X:20, Y:10, W:150, H:40
- User greeting (Label): "Welcome, [Username]", X:850, Y:15, Color:White, Bold
- Date/time (Label): "2025-08-07 11:54:47 UTC", X:850, Y:35, Color:#E3F2FD, Regular
- Logout button: X:1050, Y:15, W:100, H:30, Style:Secondary

Usage:
- All portal headers
- Consistent branding across system
- Real-time date/time display
```

#### **CR-NAV-002: Sidebar Navigation**
**Balsamiq Component**: Rectangle + List + Icons
```
Properties:
- Size: W:250, H:[Screen Height-60]
- Fill: #F8F9FA
- Border: Right, #DEE2E6, 1px
- Position: X:0, Y:60

Navigation Items Template:
- Item height: 40px
- Padding: 20px left, 10px top/bottom
- Active state: Background #E3F2FD
- Hover state: Background #F0F0F0
- Icon size: 20x20px, left aligned
- Text: 14px, SemiBold

Standard Items:
- Dashboard (Home icon)
- [Context-specific menu items]
- Settings (Settings icon)
- Help (Help-circle icon)

Usage:
- Patient portal navigation
- Doctor portal navigation
- Admin portal navigation
```

#### **CR-NAV-003: Breadcrumb Navigation**
**Balsamiq Component**: Label with links
```
Properties:
- Font: Regular, 12px
- Color: #6C757D
- Separator: " > " or " / "
- Link color: #0056B3
- Position: Below header, 20px margin

Template:
"Portal Name > Section > Sub-section > Current Page"

Usage:
- All pages except dashboard
- Indicates user location in system
- Provides navigation shortcuts
```

#### **CR-NAV-004: Bottom Tab Navigation (Mobile)**
**Balsamiq Component**: Rectangle + Icons + Labels
```
Properties:
- Size: W:375, H:60
- Fill: #FFFFFF
- Border: Top, #DEE2E6, 1px
- Position: Bottom of canvas

Tab Template:
- Tab width: 75px (5 tabs total)
- Icon size: 24x24px
- Label: 10px, Regular
- Active color: #0056B3
- Inactive color: #6C757D

Standard Tabs:
- Dashboard (Home)
- Appointments (Calendar)
- Reports (File-text)
- Profile (User)
- More (Menu)

Usage:
- Mobile patient portal only
- Touch-friendly navigation
- Always visible
```

---

## Form Components

### 2. Input Components

#### **CR-FORM-001: Text Input Field**
**Balsamiq Component**: Text Input
```
Properties:
- Height: 40px (desktop), 50px (mobile)
- Border: #DEE2E6, 1px
- Corner radius: 4px
- Padding: 12px
- Font: Regular, 14px
- Focus border: #0056B3, 2px

States:
- Default: Border #DEE2E6
- Focus: Border #0056B3, shadow
- Error: Border #DC3545, background #F8D7DA
- Success: Border #28A745, background #D1E7DD
- Disabled: Background #F8F9FA, text #6C757D

Label:
- Position: Above input, 8px margin
- Font: SemiBold, 12px
- Color: #212529
- Required indicator: Red asterisk (*)

Usage:
- All text inputs (name, email, phone, etc.)
- Consistent styling across forms
- Proper validation states
```

#### **CR-FORM-002: Password Input Field**
**Balsamiq Component**: Text Input (Password)
```
Properties:
- Same as Text Input Field
- Password type (masked characters)
- Show/hide toggle button (Eye icon)
- Strength indicator for new passwords

Strength Indicator:
- Weak: Red bar, 25% width
- Fair: Orange bar, 50% width  
- Good: Yellow bar, 75% width
- Strong: Green bar, 100% width

Usage:
- Login forms
- Registration forms
- Password change forms
```

#### **CR-FORM-003: Dropdown Select**
**Balsamiq Component**: Combo Box
```
Properties:
- Height: 40px
- Border: #DEE2E6, 1px
- Arrow icon: Down-chevron
- Placeholder text: "Select an option"

Options styling:
- Padding: 12px
- Hover: Background #F8F9FA
- Selected: Background #E3F2FD
- Max height: 200px (scrollable)

Usage:
- Service selection
- Location selection
- Time slot selection
- Filter dropdowns
```

#### **CR-FORM-004: Date/Time Picker**
**Balsamiq Component**: Date Chooser + Time Input
```
Properties:
- Date format: MM/DD/YYYY
- Time format: HH:MM AM/PM
- Calendar popup: Standard calendar widget
- Time slots: 15-minute increments

Calendar styling:
- Header: Month/year navigation
- Days: Clickable cells
- Disabled dates: Gray, not clickable
- Selected date: Blue background
- Today: Bold border

Usage:
- Appointment booking
- Date of birth entry
- Report date selection
```

#### **CR-FORM-005: File Upload**
**Balsamiq Component**: Rectangle + Button + Text
```
Properties:
- Drag & drop area: 400x200px
- Border: Dashed, #DEE2E6, 2px
- Background: #F8F9FA
- Upload button: "Browse Files"

States:
- Default: Dashed border
- Drag hover: Border #0056B3, background #E3F2FD
- Upload progress: Progress bar overlay
- Success: Green checkmark, file name display
- Error: Red X, error message

File info display:
- File name, size, type
- Remove button (X icon)
- Progress indicator during upload

Usage:
- DICOM file uploads
- Document attachments
- Profile photo uploads
```

### 3. Button Components

#### **CR-BTN-001: Primary Button**
**Balsamiq Component**: Button
```
Properties:
- Height: 40px (desktop), 50px (mobile)
- Background: #0056B3
- Text color: White
- Border: None
- Corner radius: 4px
- Font: SemiBold, 14px
- Padding: 12px 24px

States:
- Default: Background #0056B3
- Hover: Background #004494
- Active: Background #003875
- Disabled: Background #6C757D, cursor not-allowed
- Loading: Spinner icon + "Loading..."

Usage:
- Primary actions (Login, Save, Submit)
- Call-to-action buttons
- Form submissions
```

#### **CR-BTN-002: Secondary Button**  
**Balsamiq Component**: Button
```
Properties:
- Height: 40px (desktop), 50px (mobile)
- Background: Transparent
- Text color: #0056B3
- Border: #0056B3, 1px
- Corner radius: 4px
- Font: SemiBold, 14px

States:
- Default: Border #0056B3, text #0056B3
- Hover: Background #E3F2FD
- Active: Background #D1E7DD
- Disabled: Border #6C757D, text #6C757D

Usage:
- Secondary actions (Cancel, Back)
- Alternative options
- Less important actions
```

#### **CR-BTN-003: Success Button**
**Balsamiq Component**: Button  
```
Properties:
- Background: #28A745
- Text color: White
- Same dimensions as primary button

Usage:
- Positive confirmations
- Completion actions
- Success states
```

#### **CR-BTN-004: Danger Button**
**Balsamiq Component**: Button
```
Properties:  
- Background: #DC3545
- Text color: White
- Same dimensions as primary button

Usage:
- Destructive actions (Delete, Cancel)
- Critical confirmations
- Error states
```

#### **CR-BTN-005: Icon Button**
**Balsamiq Component**: Button + Icon
```
Properties:
- Size: 40x40px (square)
- Icon size: 20x20px (centered)
- Background: Transparent
- Border: #DEE2E6, 1px (optional)
- Corner radius: 4px

Common icons:
- Edit (Edit icon)
- Delete (Trash icon)
- View (Eye icon)
- Download (Download icon)
- Settings (Settings icon)

Usage:
- Table actions
- Toolbar buttons  
- Quick actions
```

---

## Data Display Components

### 4. Table Components

#### **CR-TABLE-001: Data Table**
**Balsamiq Component**: Data Grid
```
Properties:
- Border: #DEE2E6, 1px
- Header background: #F8F9FA
- Row height: 40px
- Padding: 12px per cell
- Striped rows: Alternate #FFFFFF and #F8F9FA

Header styling:
- Font: SemiBold, 12px
- Text color: #495057
- Sort icons: Up/down arrows
- Resizable columns

Row styling:
- Font: Regular, 14px
- Hover: Background #E3F2FD
- Selected: Background #D1E7DD

Actions column:
- Icon buttons (Edit, Delete, View)
- Dropdown for more actions
- Consistent 120px width

Usage:
- Patient lists
- Appointment schedules
- Report listings
- User management
```

#### **CR-TABLE-002: Mobile Card Table**
**Balsamiq Component**: Rectangle (Card container)
```
Properties (per card):
- Width: Screen width - 40px margin
- Min height: 120px
- Background: #FFFFFF
- Border: #DEE2E6, 1px
- Corner radius: 8px
- Shadow: 0 2px 4px rgba(0,0,0,0.1)
- Margin bottom: 16px

Card structure:
- Header: Primary info (name, ID)
- Body: Secondary details
- Footer: Actions or status
- Expandable for more details

Usage:
- Mobile table alternatives
- Patient cards on mobile
- Appointment cards
```

### 5. Card Components

#### **CR-CARD-001: Statistics Card**
**Balsamiq Component**: Rectangle + Icon + Labels
```
Properties:
- Size: W:200, H:120
- Background: Based on data type
- Border: 1px, matching background
- Corner radius: 8px
- Padding: 20px

Structure:
- Icon: 32x32px, top-left
- Title: Below icon, 14px SemiBold
- Value: Large text, 24px Bold, colored
- Subtitle: Bottom, 12px Regular
- Change indicator: Optional, right-aligned

Color schemes:
- Blue (#E3F2FD): General stats
- Green (#D1E7DD): Positive metrics
- Orange (#FFF3CD): Warnings
- Red (#F8D7DA): Critical alerts

Usage:
- Dashboard overview cards
- KPI displays
- Quick statistics
```

#### **CR-CARD-002: Patient Info Card**
**Balsamiq Component**: Rectangle + Labels + Avatar
```
Properties:
- Width: 300px, Height: auto
- Background: #FFFFFF
- Border: #DEE2E6, 1px
- Corner radius: 8px
- Padding: 20px

Structure:
- Patient avatar: 60x60px circle, top-left
- Name: 18px Bold, next to avatar
- ID/DOB: 12px Regular, below name
- Contact: Phone, email
- Status: Colored badge

Usage:
- Patient details display
- Doctor dashboard patient cards
- Search results
```

### 6. Chart Components

#### **CR-CHART-001: Line Chart**
**Balsamiq Component**: Line Chart
```
Properties:
- Background: #FFFFFF
- Grid lines: #F0F0F0
- Axis labels: 12px Regular
- Data lines: 2px width
- Data points: 4px circles
- Tooltip on hover

Color scheme:
- Primary line: #0056B3
- Secondary line: #28A745
- Tertiary line: #FD7E14

Usage:
- User activity trends
- System performance metrics
- Appointment volume charts
```

#### **CR-CHART-002: Bar Chart**  
**Balsamiq Component**: Column Chart
```
Properties:
- Bar color: #0056B3
- Bar spacing: 8px
- Value labels: Above bars
- Hover effects: Darker shade

Usage:
- Monthly reports
- Comparative data
- Resource utilization
```

---

## Interactive Components

### 7. Modal Components

#### **CR-MODAL-001: Standard Modal**
**Balsamiq Component**: Modal Dialog
```
Properties:
- Overlay: rgba(0,0,0,0.5)
- Modal width: 500px (desktop), 90% (mobile)
- Background: #FFFFFF
- Border radius: 8px
- Shadow: 0 4px 12px rgba(0,0,0,0.15)

Structure:
- Header: Title + close button (X)
- Body: Content area, scrollable
- Footer: Action buttons (right-aligned)

Header:
- Height: 60px
- Title: 18px Bold
- Close button: 32x32px, top-right

Footer:
- Height: 60px
- Buttons: Primary + Secondary
- Right-aligned with 12px gap

Usage:
- Confirmations
- Forms
- Detail views
- Image previews
```

#### **CR-MODAL-002: Confirmation Modal**
**Balsamiq Component**: Alert Dialog
```
Properties:
- Smaller width: 400px
- Icon: Warning, Success, or Error
- Title: Bold, 16px
- Message: Regular, 14px
- Buttons: Cancel + Confirm

Usage:
- Delete confirmations
- Action confirmations
- Success messages
```

### 8. Form Validation Components

#### **CR-VALIDATION-001: Error Message**
**Balsamiq Component**: Alert (Error state)
```
Properties:
- Background: #F8D7DA
- Border: #DC3545, 1px
- Text color: #721C24
- Icon: Alert-circle (red)
- Padding: 12px
- Corner radius: 4px

Usage:
- Form field errors
- Page-level errors
- API error messages
```

#### **CR-VALIDATION-002: Success Message**
**Balsamiq Component**: Alert (Success state)
```
Properties:
- Background: #D1E7DD
- Border: #28A745, 1px
- Text color: #155724
- Icon: Check-circle (green)
- Padding: 12px
- Corner radius: 4px

Usage:
- Form submissions
- Action confirmations
- Success notifications
```

---

## Medical-Specific Components

### 9. DICOM Viewer Components

#### **CR-MEDICAL-001: DICOM Image Container**
**Balsamiq Component**: Image + Rectangle overlay
```
Properties:
- Background: #000000 (black)
- Border: #333333, 2px
- Aspect ratio: Maintain original
- Zoom controls: Overlay buttons
- Crosshair cursor: Always visible

Overlay elements:
- Patient info: Top-left corner
- Image info: Top-right corner
- Tools: Left sidebar
- Measurements: Overlay annotations

Usage:
- DICOM image display
- Medical image viewing
- Annotation overlays
```

#### **CR-MEDICAL-002: Image Tools Panel**
**Balsamiq Component**: Rectangle + Button List
```
Properties:
- Width: 280px
- Background: #F8F9FA
- Border: Right, #DEE2E6, 1px

Tool categories:
- Zoom & Pan: 5 tools
- Measurement: 4 tools  
- Window/Level: 3 presets + sliders
- Annotation: 4 tools

Button styling:
- Size: 40x40px
- Icon: 24x24px
- Tooltip on hover
- Active state: Blue background

Usage:
- DICOM viewer sidebar
- Image manipulation tools
- Medical annotations
```

#### **CR-MEDICAL-003: Equipment Status Card**
**Balsamiq Component**: Rectangle + Status indicator
```
Properties:
- Size: W:300, H:150
- Background: #FFFFFF
- Border: Based on status color
- Corner radius: 8px

Status indicators:
- Active: Green border, green dot
- Maintenance: Orange border, orange dot
- Offline: Red border, red dot
- Available: Blue border, blue dot

Card content:
- Equipment name: Bold, 16px
- Status: Colored badge
- Current activity: Regular text
- Time remaining: If applicable
- Actions: Button group

Usage:
- Technician dashboard
- Equipment monitoring
- Status displays
```

### 10. Patient Information Components

#### **CR-MEDICAL-004: Patient Header**
**Balsamiq Component**: Rectangle + Labels + Avatar
```
Properties:
- Height: 80px
- Background: #F8F9FA
- Border: Bottom, #DEE2E6, 1px

Content layout:
- Patient photo: 60x60px, left
- Name: 20px Bold, next to photo
- ID & Demographics: Below name
- Alert indicators: Right side
- Action buttons: Far right

Alert types:
- Allergies: Red badge
- Special needs: Orange badge
- VIP patient: Gold badge

Usage:
- Patient detail pages
- Medical record headers
- Doctor portal views
```

---

## Layout Components

### 11. Container Components

#### **CR-LAYOUT-001: Page Container**
**Balsamiq Component**: Rectangle
```
Properties:
- Width: 100% (responsive)
- Background: #FFFFFF
- Padding: 30px
- Min-height: Screen height - header - footer

Usage:
- Main content wrapper
- Consistent page margins
- Responsive behavior
```

#### **CR-LAYOUT-002: Section Container**
**Balsamiq Component**: Rectangle
```
Properties:
- Width: 100%
- Background: #FFFFFF
- Border: #DEE2E6, 1px (optional)
- Corner radius: 8px
- Margin bottom: 30px
- Padding: 20px

Usage:
- Content sections
- Form sections
- Card containers
```

#### **CR-LAYOUT-003: Grid System**
**Balsamiq Component**: Multiple Rectangles
```
12-Column Grid:
- Column width: 75px + 20px gutter
- Container width: 1200px
- Responsive breakpoints:
  - Desktop: 1200px+
  - Tablet: 768px-1199px
  - Mobile: <768px

Usage:
- Responsive layouts
- Content alignment
- Component positioning
```

---

## Icon Library

### 12. Standard Icons (24x24px)

#### Navigation Icons
```
- home: Dashboard/Home
- menu: Hamburger menu
- chevron-right: Navigation arrows
- chevron-left: Back buttons
- chevron-down: Dropdowns
- chevron-up: Collapse/expand
```

#### Action Icons
```
- plus: Add/Create new
- edit: Edit/Modify
- trash-2: Delete
- eye: View/Show
- eye-off: Hide
- download: Download files
- upload: Upload files
- save: Save changes
- refresh-cw: Reload/Refresh
- search: Search functionality
- filter: Filter options
- sort: Sort options
```

#### Status Icons
```
- check-circle: Success/Completed
- x-circle: Error/Failed
- alert-circle: Warning/Alert
- info: Information
- clock: Pending/In progress
- user-check: Active user
- user-x: Inactive user
```

#### Medical Icons
```
- activity: Heartbeat/Health
- clipboard: Medical records
- file-text: Reports
- camera: Imaging/Photos
- monitor: Equipment
- calendar: Appointments
- pill: Medications
- heart: Health/Wellness
```

#### Communication Icons
```
- mail: Email
- phone: Phone calls
- message-square: Messages
- bell: Notifications
- send: Send message
```

### 13. Icon Usage Guidelines

#### Size Standards
```
Small icons: 16x16px (table actions, input decorations)
Medium icons: 24x24px (buttons, navigation)
Large icons: 32x32px (cards, features)
Extra large: 48x48px (empty states, illustrations)
```

#### Color Guidelines
```
Default: #495057 (medium gray)
Active/Primary: #0056B3 (blue)
Success: #28A745 (green)
Warning: #FD7E14 (orange)
Danger: #DC3545 (red)
Disabled: #6C757D (light gray)
```

---

## Component Usage Guidelines

### 14. Implementation Standards

#### Spacing System
```
Base unit: 8px
Scale: 8, 16, 24, 32, 40, 48, 64px

Component margins:
- Between sections: 32px
- Between components: 16px
- Inside components: 8px
- Fine adjustments: 4px
```

#### Responsive Behavior
```
Desktop (1200px+):
- Full component features
- Multi-column layouts
- Hover states active

Tablet (768-1199px):
- Simplified layouts
- Touch-friendly sizing
- Collapsible sections

Mobile (<768px):
- Single column
- Full-width components
- Bottom navigation
- Larger touch targets
```

#### Accessibility Requirements
```
Color contrast: WCAG AA (4.5:1 ratio)
Focus indicators: 2px blue outline
Keyboard navigation: Tab order logical
Screen reader: Alt text for images
Touch targets: Minimum 44px
```

---

## Symbol Library Creation

### 15. Creating Balsamiq Symbols

#### Symbol Creation Process
1. **Design Individual Component**
   - Create complete component with all states
   - Use consistent naming conventions
   - Include all necessary elements

2. **Convert to Symbol**
   - Select all component elements
   - Right-click → "Convert to Symbol"
   - Name with prefix "CR-[CATEGORY]-[NUMBER]"
   - Add description and usage notes

3. **Add to Library**
   - Save to project symbol library
   - Export for reuse across projects
   - Document in component library

#### Symbol Naming Convention
```
Format: CR-[CATEGORY]-[ID]-[NAME]

Examples:
- CR-NAV-001-MainHeader
- CR-FORM-001-TextInput
- CR-BTN-001-PrimaryButton
- CR-TABLE-001-DataTable
- CR-MEDICAL-001-DICOMViewer
```

#### Symbol Parameters
```
For dynamic content:
- {username} - User display name
- {date} - Current date/time
- {status} - Status indicators
- {count} - Numeric values
- {title} - Section titles
- {content} - Body content
```

### 16. Library Management

#### Version Control
```
Version format: v1.0.0 (Major.Minor.Patch)
- Major: Breaking changes
- Minor: New components
- Patch: Bug fixes/improvements

Change log:
- Document all updates
- Migration guides for breaking changes
- Backward compatibility notes
```

#### Quality Assurance
```
Component checklist:
☐ Consistent sizing
☐ Proper alignment
☐ Color compliance
☐ Responsive behavior
☐ Accessibility features
☐ Documentation complete
☐ Symbol parameters work
☐ All states included
```

---

## Usage Examples

### 17. Common Component Combinations

#### Patient Dashboard Layout
```
Components used:
- CR-NAV-001: Main Header
- CR-NAV-002: Sidebar Navigation  
- CR-CARD-001: Statistics Cards (4x)
- CR-TABLE-001: Appointments Table
- CR-BTN-001: Action Buttons (3x)
```

#### Login Form Layout
```
Components used:
- CR-FORM-001: Email Input
- CR-FORM-002: Password Input
- CR-BTN-001: Login Button
- CR-BTN-002: Register Link
```

#### DICOM Viewer Layout
```
Components used:
- CR-MEDICAL-001: Image Container
- CR-MEDICAL-002: Tools Panel
- CR-MEDICAL-004: Patient Header
- CR-BTN-005: Icon Buttons (multiple)
```

This component library ensures consistency across all wireframes in the Capital Radiology Online System and provides clear guidance for implementing each UI element in Balsamiq.