# Balsamiq Wireframe Implementation Guide
## Capital Radiology Online System

### Table of Contents
1. [Project Setup](#project-setup)
2. [Canvas Configuration](#canvas-configuration)
3. [Patient Dashboard Wireframe](#patient-dashboard-wireframe)
4. [Patient Authentication Flow](#patient-authentication-flow)
5. [Appointment Booking System](#appointment-booking-system)
6. [Doctor Dashboard](#doctor-dashboard)
7. [DICOM Image Viewer Interface](#dicom-image-viewer-interface)
8. [Admin Portal](#admin-portal)
9. [Technician Dashboard](#technician-dashboard)
10. [Navigation Implementation](#navigation-implementation)
11. [Responsive Design Guidelines](#responsive-design-guidelines)

---

## Project Setup

### Initial Project Configuration
1. **Open Balsamiq Wireframes** (Cloud or Desktop version)
2. **Create New Project**: "Capital_Radiology_Online_System"
3. **Set Project Properties**:
   - Project Name: Capital Radiology Online System
   - Description: MRI scan and reporting web portal
   - Created by: [Your Name]
   - Date: 2025-08-07

### Project Structure Organization
Create wireframe folders:
- `01_Authentication`
- `02_Patient_Portal`
- `03_Doctor_Portal`
- `04_Admin_Portal`
- `05_Technician_Portal`
- `06_Shared_Components`

---

## Canvas Configuration

### Standard Canvas Settings
- **Canvas Size**: 1200px × 800px (Desktop), 375px × 812px (Mobile)
- **Grid Settings**: Show Grid, Snap to Grid enabled
- **Grid Size**: 10px
- **Background Color**: #F8F9FA (Light Gray)

### Color Palette
- **Primary Blue**: #0056B3
- **Secondary Blue**: #E3F2FD
- **Success Green**: #28A745
- **Warning Orange**: #FD7E14
- **Danger Red**: #DC3545
- **Text Dark**: #212529
- **Text Light**: #6C757D
- **Border Gray**: #DEE2E6

### Typography Standards
- **Headers**: Balsamiq Sans, Bold, 18-24px
- **Sub-headers**: Balsamiq Sans, SemiBold, 14-16px
- **Body Text**: Balsamiq Sans, Regular, 12-14px
- **Small Text**: Balsamiq Sans, Regular, 10-12px

---

## Patient Dashboard Wireframe

### Step 1: Create Patient Dashboard Canvas
1. **Create New Wireframe**: Name "Patient_Dashboard"
2. **Canvas Size**: 1200px × 800px
3. **Background**: White (#FFFFFF)

### Step 2: Header Implementation

#### Top Navigation Bar
1. **Add Rectangle**: 
   - Position: X:0, Y:0
   - Size: W:1200, H:60
   - Fill: #0056B3
   - Border: None

2. **Add Logo**:
   - Component: Image placeholder
   - Position: X:20, Y:10
   - Size: W:150, H:40
   - Text: "Capital Radiology Logo"
   - Alt text: "{Logo}"

3. **Add Current User Info**:
   - Component: Label
   - Position: X:850, Y:15
   - Text: "Welcome, Sarojkent"
   - Color: White
   - Font: Bold, 14px

4. **Add Current Date/Time**:
   - Component: Label
   - Position: X:850, Y:35
   - Text: "2025-08-07 11:54:47 UTC"
   - Color: #E3F2FD
   - Font: Regular, 12px

5. **Add Logout Button**:
   - Component: Button
   - Position: X:1050, Y:15
   - Size: W:100, H:30
   - Text: "Logout"
   - Style: Secondary
   - Background: Transparent
   - Border: White, 1px

### Step 3: Main Navigation Menu

#### Sidebar Navigation
1. **Add Navigation Container**:
   - Component: Rectangle
   - Position: X:0, Y:60
   - Size: W:250, H:740
   - Fill: #F8F9FA
   - Border: Right, #DEE2E6, 1px

2. **Add Navigation Items**:
   ```
   Dashboard (Active)
   - Icon: Home icon
   - Position: X:20, Y:80
   - Background: #E3F2FD
   
   My Appointments
   - Icon: Calendar icon  
   - Position: X:20, Y:120
   
   MRI Reports
   - Icon: File-text icon
   - Position: X:20, Y:160
   
   Medical History
   - Icon: List icon
   - Position: X:20, Y:200
   
   Billing & Payments
   - Icon: Credit-card icon
   - Position: X:20, Y:240
   
   Profile Settings
   - Icon: User icon
   - Position: X:20, Y:280
   
   Help & Support
   - Icon: Help-circle icon
   - Position: X:20, Y:320
   ```

### Step 4: Main Content Area

#### Dashboard Overview Cards
1. **Add Content Container**:
   - Position: X:250, Y:60
   - Size: W:950, H:740
   - Fill: #FFFFFF
   - Padding: 30px

2. **Add Page Title**:
   - Component: Title
   - Position: X:280, Y:90
   - Text: "Patient Dashboard"
   - Font: Bold, 24px
   - Color: #212529

3. **Add Welcome Message**:
   - Component: Paragraph
   - Position: X:280, Y:130
   - Text: "Welcome back, Sarojkent! Here's your health summary."
   - Font: Regular, 14px
   - Color: #6C757D

#### Quick Stats Cards Row
1. **Upcoming Appointments Card**:
   - Component: Rectangle
   - Position: X:280, Y:170
   - Size: W:200, H:120
   - Fill: #E3F2FD
   - Border: #0056B3, 1px
   - Corner Radius: 8px
   
   **Card Content**:
   - Icon: Calendar (X:300, Y:190)
   - Title: "Upcoming" (X:300, Y:215, Bold, 14px)
   - Value: "2" (X:300, Y:235, Bold, 24px, #0056B3)
   - Subtitle: "Appointments" (X:300, Y:260, Regular, 12px)

2. **Pending Reports Card**:
   - Position: X:500, Y:170
   - Size: W:200, H:120
   - Fill: #FFF3CD
   - Border: #FD7E14, 1px
   
   **Card Content**:
   - Icon: File-text (X:520, Y:190)
   - Title: "Pending" (X:520, Y:215)
   - Value: "1" (X:520, Y:235, #FD7E14)
   - Subtitle: "Reports" (X:520, Y:260)

3. **Completed Scans Card**:
   - Position: X:720, Y:170
   - Size: W:200, H:120
   - Fill: #D1E7DD
   - Border: #28A745, 1px
   
   **Card Content**:
   - Icon: Check-circle (X:740, Y:190)
   - Title: "Completed" (X:740, Y:215)
   - Value: "5" (X:740, Y:235, #28A745)
   - Subtitle: "Scans" (X:740, Y:260)

4. **Outstanding Balance Card**:
   - Position: X:940, Y:170
   - Size: W:200, H:120
   - Fill: #F8D7DA
   - Border: #DC3545, 1px
   
   **Card Content**:
   - Icon: Dollar-sign (X:960, Y:190)
   - Title: "Balance" (X:960, Y:215)
   - Value: "$250" (X:960, Y:235, #DC3545)
   - Subtitle: "Outstanding" (X:960, Y:260)

### Step 5: Recent Activity Section

#### Recent Appointments Table
1. **Add Section Header**:
   - Component: Title
   - Position: X:280, Y:320
   - Text: "Recent Appointments"
   - Font: SemiBold, 18px

2. **Add Table Container**:
   - Component: Data Grid
   - Position: X:280, Y:350
   - Size: W:860, H:200
   - Headers: "Date | Time | Type | Status | Actions"
   
   **Table Rows**:
   ```
   2025-08-05 | 10:00 AM | Brain MRI | Completed | View Report
   2025-08-10 | 2:00 PM | Knee MRI | Scheduled | Reschedule
   2025-08-15 | 9:00 AM | Spine MRI | Scheduled | Cancel
   ```

3. **Add View All Link**:
   - Component: Link
   - Position: X:1050, Y:325
   - Text: "View All →"
   - Color: #0056B3

### Step 6: Quick Actions Section

#### Action Buttons
1. **Book New Appointment Button**:
   - Component: Button
   - Position: X:280, Y:580
   - Size: W:200, H:50
   - Text: "Book Appointment"
   - Style: Primary
   - Background: #0056B3
   - Icon: Plus icon

2. **View Reports Button**:
   - Component: Button
   - Position: X:500, Y:580
   - Size: W:200, H:50
   - Text: "View Reports"
   - Style: Secondary
   - Background: #6C757D
   - Icon: File-text icon

3. **Pay Bills Button**:
   - Component: Button
   - Position: X:720, Y:580
   - Size: W:200, H:50
   - Text: "Pay Bills"
   - Style: Success
   - Background: #28A745
   - Icon: Credit-card icon

### Step 7: Notifications Panel

#### Recent Notifications
1. **Add Notifications Container**:
   - Component: Rectangle
   - Position: X:280, Y:650
   - Size: W:860, H:120
   - Fill: #F8F9FA
   - Border: #DEE2E6, 1px
   - Corner Radius: 8px

2. **Add Notifications Header**:
   - Component: Label
   - Position: X:300, Y:670
   - Text: "Recent Notifications"
   - Font: SemiBold, 14px

3. **Add Notification Items**:
   ```
   • Your MRI report for 08/05 is now available
   • Appointment reminder: 08/10 at 2:00 PM
   • Payment received: $150 on 08/03
   ```

### Step 8: Footer Implementation
1. **Add Footer Container**:
   - Component: Rectangle
   - Position: X:0, Y:780
   - Size: W:1200, H:20
   - Fill: #F8F9FA
   - Border: Top, #DEE2E6, 1px

2. **Add Footer Text**:
   - Component: Label
   - Position: X:280, Y:785
   - Text: "© 2025 Capital Radiology. All rights reserved. | Privacy Policy | Terms of Service"
   - Font: Regular, 10px
   - Color: #6C757D

---

## Patient Authentication Flow

### Login Screen Wireframe

#### Step 1: Create Login Canvas
1. **Create New Wireframe**: Name "Patient_Login"
2. **Canvas Size**: 1200px × 800px
3. **Background**: Linear gradient #E3F2FD to #FFFFFF

#### Step 2: Login Form Implementation
1. **Add Main Container**:
   - Component: Rectangle
   - Position: X:400, Y:200
   - Size: W:400, H:400
   - Fill: #FFFFFF
   - Border: #DEE2E6, 1px
   - Corner Radius: 12px
   - Shadow: Drop shadow, 4px offset

2. **Add Logo/Branding**:
   - Component: Image
   - Position: X:500, Y:230
   - Size: W:200, H:60
   - Alt text: "{Capital Radiology Logo}"

3. **Add Form Title**:
   - Component: Title
   - Position: X:450, Y:310
   - Text: "Patient Login"
   - Font: Bold, 20px
   - Alignment: Center

4. **Add Email Field**:
   - Component: Text Input
   - Position: X:430, Y:350
   - Size: W:340, H:40
   - Placeholder: "Enter your email address"
   - Label: "Email Address"

5. **Add Password Field**:
   - Component: Text Input (Password)
   - Position: X:430, Y:410
   - Size: W:340, H:40
   - Placeholder: "Enter your password"
   - Label: "Password"

6. **Add Remember Me Checkbox**:
   - Component: Checkbox
   - Position: X:430, Y:470
   - Text: "Remember me"
   - Font: Regular, 12px

7. **Add Forgot Password Link**:
   - Component: Link
   - Position: X:650, Y:470
   - Text: "Forgot password?"
   - Color: #0056B3
   - Font: Regular, 12px

8. **Add Login Button**:
   - Component: Button
   - Position: X:430, Y:510
   - Size: W:340, H:45
   - Text: "Sign In"
   - Style: Primary
   - Background: #0056B3

9. **Add Registration Link**:
   - Component: Paragraph
   - Position: X:450, Y:570
   - Text: "Don't have an account? Register here"
   - Alignment: Center
   - Font: Regular, 12px
   - Link: "Register here" → #0056B3

### Registration Screen Wireframe

#### Step 1: Create Registration Canvas
1. **Create New Wireframe**: Name "Patient_Registration"
2. **Canvas Size**: 1200px × 900px
3. **Background**: Linear gradient #E3F2FD to #FFFFFF

#### Step 2: Registration Form Implementation
1. **Add Main Container**:
   - Position: X:350, Y:100
   - Size: W:500, H:700
   - Fill: #FFFFFF
   - Border: #DEE2E6, 1px
   - Corner Radius: 12px
   - Shadow: Drop shadow

2. **Add Form Fields**:
   ```
   Personal Information Section:
   - First Name (Required)
   - Last Name (Required)
   - Date of Birth (Date picker)
   - Gender (Dropdown: Male/Female/Other)
   - Phone Number (Required)
   
   Account Information Section:
   - Email Address (Required)
   - Password (Required, min 8 chars)
   - Confirm Password (Required)
   
   Medical Information Section:
   - Insurance Provider (Dropdown)
   - Policy Number
   - Emergency Contact Name
   - Emergency Contact Phone
   
   Agreement Section:
   - Terms & Conditions Checkbox
   - Privacy Policy Checkbox
   - Marketing Communications Checkbox (Optional)
   ```

3. **Add Progress Indicator**:
   - Component: Progress Bar
   - Position: X:380, Y:130
   - Progress: Step 1 of 1
   - Width: 440px

4. **Add Form Validation**:
   - Required field indicators (*)
   - Error message placeholders
   - Success confirmation states

---

## Appointment Booking System

### Step 1: Appointment Booking - Service Selection
1. **Create New Wireframe**: Name "Appointment_Booking_Step1"
2. **Add Breadcrumb Navigation**:
   ```
   Dashboard > Book Appointment > Select Service
   ```

3. **Add Service Cards**:
   ```
   Brain MRI
   - Duration: 45-60 minutes
   - Price: $800-$1200
   - Description: Detailed brain imaging
   
   Spine MRI
   - Duration: 30-45 minutes  
   - Price: $600-$1000
   - Description: Spinal cord and vertebrae imaging
   
   Knee MRI
   - Duration: 30-45 minutes
   - Price: $500-$800
   - Description: Joint and soft tissue imaging
   
   Full Body MRI
   - Duration: 90-120 minutes
   - Price: $2000-$3000
   - Description: Comprehensive body scan
   ```

### Step 2: Location and Date Selection
1. **Create New Wireframe**: Name "Appointment_Booking_Step2"
2. **Add Location Selector**:
   - Component: Dropdown
   - Options: Downtown, Suburban, Medical Center
   - Show available time slots per location

3. **Add Calendar Component**:
   - Component: Calendar
   - Highlight available dates
   - Show unavailable dates in gray
   - Current date highlighted

4. **Add Time Slot Grid**:
   - Morning slots: 8:00 AM - 12:00 PM
   - Afternoon slots: 1:00 PM - 5:00 PM
   - Evening slots: 6:00 PM - 8:00 PM

### Step 3: Patient Information Confirmation
1. **Create New Wireframe**: Name "Appointment_Booking_Step3"
2. **Add Patient Details Form**:
   - Pre-filled from user profile
   - Editable fields for updates
   - Insurance information
   - Special requirements/notes

3. **Add Appointment Summary**:
   - Service type
   - Date and time
   - Location
   - Estimated cost
   - Duration

### Step 4: Payment and Confirmation
1. **Create New Wireframe**: Name "Appointment_Booking_Step4"
2. **Add Payment Options**:
   - Insurance billing
   - Credit/Debit card
   - PayPal
   - Bank transfer

3. **Add Confirmation Details**:
   - Appointment reference number
   - Confirmation email sent
   - Calendar add options
   - Preparation instructions

---

## Doctor Dashboard

### Step 1: Create Doctor Dashboard Canvas
1. **Create New Wireframe**: Name "Doctor_Dashboard"
2. **Canvas Size**: 1400px × 900px (Wider for medical data)

### Step 2: Doctor Navigation Implementation
```
Left Sidebar Navigation:
- Dashboard (Home icon)
- Patient Queue (Users icon)
- DICOM Viewer (Image icon)
- Reports & Templates (File-text icon)
- Scheduling (Calendar icon)
- Patients Database (Database icon)
- Settings (Settings icon)
```

### Step 3: Patient Queue Section
1. **Add Patient List Table**:
   - Columns: Patient ID, Name, Scan Type, Status, Priority, Actions
   - Sortable columns
   - Filter options (scan type, status, date)
   - Search functionality

2. **Add Patient Status Indicators**:
   ```
   Waiting for Review (Orange badge)
   In Progress (Blue badge)  
   Completed (Green badge)
   Urgent (Red badge)
   ```

### Step 4: Quick Actions Panel
```
Action Buttons:
- Open DICOM Viewer
- Create New Report
- View Patient History
- Send Message to Admin
- Schedule Follow-up
```

### Step 5: Recent Reports Section
1. **Add Reports Table**:
   - Recent reports created
   - Status indicators
   - Patient details
   - Date/time stamps

2. **Add Performance Metrics**:
   ```
   Today's Statistics:
   - Reports Completed: 8
   - Pending Reviews: 3
   - Average Report Time: 25 mins
   - Patient Satisfaction: 4.8/5
   ```

---

## DICOM Image Viewer Interface

### Step 1: Create DICOM Viewer Canvas
1. **Create New Wireframe**: Name "DICOM_Image_Viewer"
2. **Canvas Size**: 1600px × 1000px (Large format for medical imaging)

### Step 2: Viewer Layout Implementation

#### Main Image Display Area
1. **Add Primary Image Container**:
   - Position: X:300, Y:60
   - Size: W:800, H:600
   - Fill: #000000 (Black background for medical images)
   - Border: #DEE2E6, 2px

2. **Add Image Placeholder**:
   - Component: Image
   - Alt text: "{DICOM Image Display}"
   - Overlay: Crosshair cursor indicator

#### Tool Panel (Left Sidebar)
1. **Add Tools Container**:
   - Position: X:0, Y:60
   - Size: W:280, H:940
   - Fill: #F8F9FA

2. **Add Tool Categories**:
   ```
   Zoom & Pan Tools:
   - Zoom In (Zoom-in icon)
   - Zoom Out (Zoom-out icon) 
   - Pan (Move icon)
   - Fit to Screen (Maximize icon)
   - Reset View (Refresh-cw icon)
   
   Measurement Tools:
   - Length Measurement (Ruler icon)
   - Area Measurement (Square icon)
   - Angle Measurement (Triangle icon)
   - Calibration (Settings icon)
   
   Window/Level Tools:
   - Window Width slider
   - Window Level slider
   - Preset buttons (Bone, Soft Tissue, Lung)
   
   Annotation Tools:
   - Arrow annotation (Arrow-up icon)
   - Text annotation (Type icon)
   - Circle annotation (Circle icon)
   - Rectangle annotation (Square icon)
   ```

#### Image Series Navigation
1. **Add Series Selector**:
   - Position: X:1120, Y:60
   - Size: W:480, H:200
   - Component: Thumbnail grid
   - Show image series thumbnails

2. **Add Series Information**:
   ```
   Patient: Sarojkent
   Study Date: 2025-08-07
   Modality: MRI
   Body Part: Brain
   Series: T1 Weighted (24 images)
   Slice: 12/24
   ```

#### Image Controls Panel
1. **Add Playback Controls**:
   - Position: X:1120, Y:280
   - Components: Play, Pause, Previous, Next buttons
   - Speed slider
   - Loop toggle

2. **Add Display Settings**:
   ```
   Brightness/Contrast sliders
   Invert colors checkbox  
   Show/hide annotations checkbox
   Grid overlay toggle
   Ruler display toggle
   ```

#### Report Integration Panel
1. **Add Quick Report Section**:
   - Position: X:1120, Y:450
   - Size: W:480, H:350
   - Component: Text area
   - Placeholder: "Add findings and observations..."

2. **Add Report Templates Dropdown**:
   - Pre-defined report templates
   - Common findings shortcuts
   - Normal/Abnormal quick selections

### Step 3: Patient Information Header
1. **Add Patient Info Bar**:
   - Position: X:0, Y:0
   - Size: W:1600, H:60
   - Fill: #0056B3
   -
   **Patient Details**:
   ```
   Patient ID: PAT-2025-001 | Name: Sarojkent | DOB: 1985-03-15
   Study: Brain MRI | Date: 2025-08-07 11:54:47 UTC
   Referring Doctor: Dr. Smith | Urgency: Routine
   ```

---

## Admin Portal

### Step 1: Create Admin Dashboard Canvas
1. **Create New Wireframe**: Name "Admin_Dashboard"  
2. **Canvas Size**: 1400px × 1000px

### Step 2: Admin Navigation Menu
```
Top Navigation Tabs:
- Dashboard Overview
- User Management  
- Appointment Management
- System Analytics
- Data Management
- Security & Audit
- Settings
```

### Step 3: Dashboard Overview Implementation

#### System Status Cards
1. **Add Status Cards Row**:
   ```
   Active Users Card:
   - Icon: Users
   - Value: 1,247
   - Change: +5.2% from last month
   - Color: Blue
   
   Today's Appointments:
   - Icon: Calendar
   - Value: 47
   - Change: 3 cancelled, 2 rescheduled
   - Color: Green
   
   Pending Reports:
   - Icon: File-text
   - Value: 12
   - Change: -15% from yesterday
   - Color: Orange
   
   System Uptime:
   - Icon: Activity
   - Value: 99.9%
   - Change: 24h no incidents
   - Color: Green
   ```

#### User Activity Chart
1. **Add Charts Container**:
   - Position: X:50, Y:200
   - Size: W:650, H:300
   
2. **Add Activity Chart**:
   - Component: Line Chart
   - Title: "Daily Active Users (Last 30 Days)"
   - X-axis: Dates
   - Y-axis: User count
   - Show trend line

#### System Alerts Panel
1. **Add Alerts Container**:
   - Position: X:720, Y:200
   - Size: W:630, H:300
   
2. **Add Alert Items**:
   ```
   High Priority:
   - DICOM storage 85% full
   - 3 failed login attempts from IP: xxx.xxx.xxx.xxx
   
   Medium Priority:
   - Scheduled maintenance in 2 days
   - SSL certificate expires in 30 days
   
   Low Priority:
   - New user registration: 5 pending approvals
   - Backup completed successfully
   ```

### Step 4: User Management Section

#### User Table Implementation
1. **Add User Management Table**:
   - Columns: User ID, Name, Role, Status, Last Login, Actions
   - Sortable columns
   - Bulk actions (Enable/Disable, Delete, Export)
   - Advanced filters (Role, Status, Department)

2. **Add User Actions**:
   ```
   - Add New User button
   - Import Users from CSV
   - Export User List
   - Send Password Reset
   - Assign Roles/Permissions
   ```

#### Role Management
1. **Add Roles Section**:
   ```
   Patient Role:
   - Book appointments
   - View reports
   - Manage profile
   
   Doctor Role:
   - View DICOM images
   - Create reports
   - Access patient data
   
   Technician Role:
   - Upload DICOM files
   - Manage equipment
   - Schedule scans
   
   Admin Role:
   - Full system access
   - User management
   - System configuration
   ```

---

## Technician Dashboard

### Step 1: Create Technician Dashboard Canvas
1. **Create New Wireframe**: Name "Technician_Dashboard"
2. **Canvas Size**: 1300px × 900px

### Step 2: Technician Navigation
```
Left Sidebar:
- Dashboard (Home)
- Upload DICOM (Upload)
- Equipment Status (Monitor)
- Patient Queue (Users)
- Scan Schedule (Calendar)
- Quality Control (Check-circle)
- Reports (File-text)
```

### Step 3: Equipment Status Panel

#### MRI Machine Status Cards
1. **Add Equipment Cards**:
   ```
   MRI Machine #1:
   - Status: Active (Green)
   - Current Patient: John Doe
   - Scan Type: Brain MRI
   - Time Remaining: 25 mins
   - Next Appointment: 2:30 PM
   
   MRI Machine #2:
   - Status: Maintenance (Orange)
   - Last Service: 2025-08-05
   - Next Service: 2025-08-12
   - Issue: Cooling system check
   - Technician: Mike Johnson
   
   MRI Machine #3:
   - Status: Available (Blue)
   - Ready for next patient
   - Last cleaned: 11:30 AM
   - Estimated ready: Now
   ```

### Step 4: DICOM Upload Interface

#### File Upload Section
1. **Add Upload Container**:
   - Component: File Upload Area
   - Support: Drag & drop, Browse files
   - File types: .dcm, .dicom
   - Max size: 2GB per file
   - Batch upload support

2. **Add Patient Association**:
   ```
   Patient Selection:
   - Search by Patient ID
   - Search by Name
   - Appointment ID lookup
   - Manual entry option
   ```

3. **Add Scan Details Form**:
   ```
   Scan Information:
   - Scan Type (Dropdown)
   - Body Part (Dropdown)  
   - Contrast Used (Yes/No)
   - Scan Duration (Auto-calculated)
   - Quality Rating (1-5 stars)
   - Notes/Observations
   ```

### Step 5: Patient Queue Management
1. **Add Patient Queue Table**:
   - Columns: Time, Patient, Scan Type, Status, Machine, Actions
   - Status indicators: Waiting, In Progress, Completed
   - Drag & drop reordering
   - Time slot management

---

## Navigation Implementation

### Global Navigation Standards

#### Header Navigation (All Portals)
1. **Standard Header Components**:
   ```
   Logo (Left aligned)
   Portal Name (Center)
   User Info (Right aligned)
   - User name
   - Current date/time
   - Logout button
   ```

2. **Responsive Navigation**:
   ```
   Desktop (>1024px):
   - Full horizontal navigation
   - Sidebar for sub-navigation
   
   Tablet (768px-1024px):
   - Collapsible sidebar
   - Touch-friendly buttons
   
   Mobile (<768px):
   - Hamburger menu
   - Bottom navigation for patients
   ```

#### Breadcrumb Navigation
1. **Implementation Standards**:
   ```
   Format: Portal > Section > Sub-section > Current Page
   Examples:
   - Patient Portal > Appointments > Book New > Select Service
   - Doctor Portal > Patients > View Details > DICOM Images
   - Admin Portal > User Management > Add User
   ```

2. **Breadcrumb Styling**:
   - Position: Below header, above main content
   - Font: Regular, 12px
   - Color: #6C757D
   - Separator: > or /
   - Links: #0056B3 (clickable items)

### Page State Indicators

#### Loading States
1. **Loading Components**:
   ```
   Page Loading:
   - Full page spinner
   - Progress bar for file uploads
   - Skeleton screens for data tables
   
   Component Loading:
   - Button spinners
   - Image placeholders
   - Chart loading animations
   ```

#### Error States
1. **Error Handling**:
   ```
   Network Errors:
   - Connection lost message
   - Retry button
   - Offline mode indicator
   
   Form Errors:
   - Field validation messages
   - Summary error list
   - Success confirmations
   ```

---

## Responsive Design Guidelines

### Mobile Patient Portal (375px width)

#### Mobile Dashboard Layout
1. **Mobile Header**:
   - Height: 60px
   - Logo: Compact version
   - Hamburger menu button
   - User avatar (small)

2. **Mobile Navigation**:
   ```
   Bottom Tab Navigation:
   - Dashboard (Home icon)
   - Appointments (Calendar icon)
   - Reports (File icon)
   - Profile (User icon)
   - More (Menu icon)
   ```

3. **Mobile Cards**:
   ```
   Card Layout:
   - Full width minus 20px margin
   - Stacked vertically
   - Touch-friendly buttons (min 44px height)
   - Swipe gestures for navigation
   ```

#### Mobile Form Design
1. **Form Layout**:
   ```
   Input Fields:
   - Full width
   - Increased height (50px)
   - Larger text size (16px to prevent zoom)
   - Proper input types (email, tel, date)
   ```

2. **Mobile Tables**:
   ```
   Responsive Table Options:
   - Horizontal scroll
   - Card-based layout
   - Expandable rows
   - Priority columns only
   ```

### Tablet Layout (768px width)

#### Tablet Adaptations
1. **Navigation**:
   - Collapsible sidebar
   - Tab-based navigation for content sections
   - Touch-friendly interface elements

2. **Content Layout**:
   ```
   Two-Column Layout:
   - Main content: 65% width
   - Sidebar: 35% width
   - Responsive breakpoints
   ```

### Desktop Enhancements (1200px+ width)

#### Advanced Features
1. **Multi-panel Layout**:
   ```
   Three-Panel Layout:
   - Navigation: 250px
   - Main content: flexible
   - Side panel: 300px
   ```

2. **Keyboard Navigation**:
   ```
   Keyboard Shortcuts:
   - Ctrl+N: New appointment
   - Ctrl+S: Save report
   - Ctrl+F: Search
   - Tab: Navigate form fields
   ```

---

## Implementation Checklist

### Phase 1: Basic Wireframes
- [ ] Patient Dashboard
- [ ] Login/Registration screens
- [ ] Basic navigation structure
- [ ] Mobile responsive layouts

### Phase 2: Advanced Features  
- [ ] DICOM viewer interface
- [ ] Doctor dashboard
- [ ] Admin portal
- [ ] Technician interface

### Phase 3: Integration & Testing
- [ ] Navigation flow testing
- [ ] Form validation workflows
- [ ] Responsive design validation
- [ ] Accessibility compliance

### Phase 4: Documentation
- [ ] Component library creation
- [ ] Style guide finalization
- [ ] User flow documentation
- [ ] Technical specifications

---

## Notes and Best Practices

### Design Consistency
1. **Use consistent spacing** (10px grid system)
2. **Maintain color palette** throughout all screens
3. **Apply typography standards** consistently
4. **Use standard iconography** from Balsamiq icon library

### Usability Guidelines
1. **Touch targets** minimum 44px for mobile
2. **Form labels** above input fields
3. **Error messages** clear and actionable
4. **Loading states** for all async operations

### Accessibility Considerations
1. **Color contrast** WCAG AA compliance
2. **Focus indicators** for keyboard navigation
3. **Alt text** for all images and icons
4. **Screen reader** friendly labels

This comprehensive guide provides step-by-step instructions for creating all wireframes in the Capital Radiology Online System using Balsamiq. Each section includes specific positioning, sizing, and styling details to ensure consistency across the entire project.