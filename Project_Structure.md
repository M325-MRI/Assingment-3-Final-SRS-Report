# Project Structure Guide
## Capital Radiology Online System Wireframes

### Table of Contents
1. [Project Organization](#project-organization)
2. [Wireframe Naming Conventions](#wireframe-naming-conventions)
3. [Folder Structure](#folder-structure)
4. [Linking and Navigation Flow](#linking-and-navigation-flow)
5. [Version Control Strategy](#version-control-strategy)
6. [Asset Management](#asset-management)
7. [Documentation Standards](#documentation-standards)
8. [Collaboration Guidelines](#collaboration-guidelines)
9. [Export and Delivery](#export-and-delivery)
10. [Maintenance Procedures](#maintenance-procedures)

---

## Project Organization

### 1. Balsamiq Project Setup

#### Project Properties
```
Project Name: Capital_Radiology_Online_System
Project Type: Web Application
Target Platform: Desktop & Mobile Web
Created Date: 2025-08-07
Last Modified: [Auto-updated]
Version: 1.0.0

Project Description:
Comprehensive wireframe system for Capital Radiology's MRI scan and reporting web portal. 
Includes patient portal, doctor dashboard, admin interface, and technician tools with 
mobile-responsive design considerations.

Stakeholders:
- Product Owner: [Name]
- UX Designer: [Name]  
- Development Team: [Team Names]
- Medical Staff: [Doctor/Admin Names]

Contact Information:
- Project Manager: [Email]
- Technical Lead: [Email]
- Design Lead: [Email]
```

#### Project Settings
```
Canvas Settings:
- Default Canvas Size: 1200x800 (Desktop), 375x812 (Mobile)
- Grid: 10px grid, Snap to Grid enabled
- Font: Balsamiq Sans (default)
- Color Mode: RGB
- Export Format: PNG, PDF

Wireframe Settings:
- Show Notes: Enabled
- Show UI Library: Enabled
- Skin: Wireframe skin (recommended for stakeholder reviews)
- Markup: Enabled for annotations

Version Control:
- Auto-save: Enabled (every 2 minutes)
- Version history: Keep last 50 versions
- Backup frequency: Daily
```

---

## Wireframe Naming Conventions

### 2. Naming Standards

#### Naming Format
```
[PORTAL]_[SECTION]_[PAGE]_[VARIANT]

Components:
- PORTAL: Patient | Doctor | Admin | Technician | Shared
- SECTION: Auth | Dashboard | Appointments | Reports | Settings | etc.
- PAGE: Specific page name
- VARIANT: Desktop | Mobile | Tablet (if responsive versions needed)

Examples:
✅ Patient_Auth_Login_Desktop
✅ Patient_Dashboard_Overview_Mobile
✅ Doctor_Reports_Create_Desktop
✅ Admin_Users_Management_Desktop
✅ Technician_Upload_DICOM_Desktop
✅ Shared_Components_Navigation
```

#### Naming Rules
```
Rules:
1. Use PascalCase for all names (capitalize first letter of each word)
2. No spaces or special characters (use underscores)
3. Keep names under 50 characters
4. Be descriptive but concise
5. Use consistent terminology across all wireframes
6. Version suffixes only for major iterations (_v2, _v3)

Avoid:
❌ patient login screen
❌ Patient-Login-Screen
❌ PatientLoginScreenForMobileDevices
❌ login_patient_v1_final_UPDATED
❌ Screen1, Wireframe2, etc.
```

#### Standard Page Names
```
Authentication:
- Login
- Registration  
- ForgotPassword
- ResetPassword
- VerifyEmail

Dashboard:
- Overview
- Welcome

Appointments:
- BookAppointment
- ViewAppointments
- AppointmentDetails
- Reschedule
- Cancel

Reports:
- ViewReports
- ReportDetails
- CreateReport
- ReviewReport

Settings:
- Profile
- Notifications
- Security
- Preferences

Admin:
- UserManagement
- SystemSettings
- Analytics
- AuditLogs

Medical:
- DICOMViewer
- PatientHistory
- EquipmentStatus
- UploadFiles
```

---

## Folder Structure

### 3. Organized Wireframe Folders

#### Primary Folder Structure
```
Capital_Radiology_Online_System/
│
├── 📁 01_Project_Overview/
│   ├── Project_Sitemap
│   ├── User_Flow_Diagram
│   ├── Navigation_Structure
│   └── Responsive_Breakpoints
│
├── 📁 02_Authentication/
│   ├── Shared_Auth_Login_Desktop
│   ├── Shared_Auth_Login_Mobile
│   ├── Shared_Auth_Registration_Desktop
│   ├── Shared_Auth_Registration_Mobile
│   ├── Shared_Auth_ForgotPassword
│   └── Shared_Auth_ResetPassword
│
├── 📁 03_Patient_Portal/
│   ├── 📁 Dashboard/
│   │   ├── Patient_Dashboard_Overview_Desktop
│   │   ├── Patient_Dashboard_Overview_Mobile
│   │   └── Patient_Dashboard_Overview_Tablet
│   │
│   ├── 📁 Appointments/
│   │   ├── Patient_Appointments_Book_Step1
│   │   ├── Patient_Appointments_Book_Step2  
│   │   ├── Patient_Appointments_Book_Step3
│   │   ├── Patient_Appointments_Book_Step4
│   │   ├── Patient_Appointments_View_Desktop
│   │   ├── Patient_Appointments_View_Mobile
│   │   ├── Patient_Appointments_Details
│   │   ├── Patient_Appointments_Reschedule
│   │   └── Patient_Appointments_Cancel
│   │
│   ├── 📁 Reports/
│   │   ├── Patient_Reports_List_Desktop
│   │   ├── Patient_Reports_List_Mobile
│   │   ├── Patient_Reports_Details
│   │   ├── Patient_Reports_Download
│   │   └── Patient_Reports_History
│   │
│   ├── 📁 Profile/
│   │   ├── Patient_Profile_View
│   │   ├── Patient_Profile_Edit
│   │   ├── Patient_Profile_Security
│   │   └── Patient_Profile_Notifications
│   │
│   └── 📁 Billing/
│       ├── Patient_Billing_Overview
│       ├── Patient_Billing_Details
│       ├── Patient_Billing_Payment
│       └── Patient_Billing_History
│
├── 📁 04_Doctor_Portal/
│   ├── 📁 Dashboard/
│   │   └── Doctor_Dashboard_Overview_Desktop
│   │
│   ├── 📁 Patients/
│   │   ├── Doctor_Patients_Queue
│   │   ├── Doctor_Patients_Details
│   │   └── Doctor_Patients_History
│   │
│   ├── 📁 DICOM_Viewer/
│   │   ├── Doctor_DICOM_Viewer_Main
│   │   ├── Doctor_DICOM_Viewer_Tools
│   │   └── Doctor_DICOM_Viewer_Annotations
│   │
│   ├── 📁 Reports/
│   │   ├── Doctor_Reports_Create
│   │   ├── Doctor_Reports_Templates
│   │   ├── Doctor_Reports_Review
│   │   └── Doctor_Reports_Sign
│   │
│   └── 📁 Schedule/
│       ├── Doctor_Schedule_View
│       └── Doctor_Schedule_Manage
│
├── 📁 05_Admin_Portal/
│   ├── 📁 Dashboard/
│   │   └── Admin_Dashboard_Overview_Desktop
│   │
│   ├── 📁 User_Management/
│   │   ├── Admin_Users_List
│   │   ├── Admin_Users_Add
│   │   ├── Admin_Users_Edit
│   │   ├── Admin_Users_Roles
│   │   └── Admin_Users_Permissions
│   │
│   ├── 📁 Appointments/
│   │   ├── Admin_Appointments_Overview
│   │   ├── Admin_Appointments_Schedule
│   │   └── Admin_Appointments_Manage
│   │
│   ├── 📁 Analytics/
│   │   ├── Admin_Analytics_Dashboard
│   │   ├── Admin_Analytics_Reports
│   │   └── Admin_Analytics_Usage
│   │
│   └── 📁 System/
│       ├── Admin_System_Settings
│       ├── Admin_System_Security
│       ├── Admin_System_Logs
│       └── Admin_System_Backup
│
├── 📁 06_Technician_Portal/
│   ├── 📁 Dashboard/
│   │   └── Technician_Dashboard_Overview_Desktop
│   │
│   ├── 📁 Equipment/
│   │   ├── Technician_Equipment_Status
│   │   ├── Technician_Equipment_Schedule
│   │   └── Technician_Equipment_Maintenance
│   │
│   ├── 📁 Uploads/
│   │   ├── Technician_Upload_DICOM
│   │   ├── Technician_Upload_Progress
│   │   └── Technician_Upload_History
│   │
│   └── 📁 Patients/
│       ├── Technician_Patients_Queue
│       └── Technician_Patients_Details
│
├── 📁 07_Shared_Components/
│   ├── Shared_Navigation_Header
│   ├── Shared_Navigation_Sidebar
│   ├── Shared_Navigation_Mobile
│   ├── Shared_Forms_Components
│   ├── Shared_Tables_Components
│   ├── Shared_Modal_Components
│   ├── Shared_Notification_Components
│   └── Shared_Footer_Components
│
├── 📁 08_Error_States/
│   ├── Shared_Error_404
│   ├── Shared_Error_500
│   ├── Shared_Error_403
│   ├── Shared_Error_Maintenance
│   └── Shared_Error_Offline
│
├── 📁 09_Loading_States/
│   ├── Shared_Loading_Page
│   ├── Shared_Loading_Data
│   ├── Shared_Loading_Upload
│   └── Shared_Loading_Components
│
└── 📁 10_Archive/
    ├── 📁 Version_1_0/
    ├── 📁 Version_1_1/
    └── 📁 Deprecated/
```

### 4. Folder Descriptions

#### Folder Purposes
```
01_Project_Overview:
- High-level system documentation
- Site maps and user flows
- Navigation architecture
- Responsive design guidelines

02_Authentication:
- Shared login/registration screens
- Password reset flows
- Account verification
- Security-related screens

03-06_Portal Folders:
- Portal-specific wireframes
- Organized by feature/function
- Consistent sub-folder structure
- Both desktop and mobile versions

07_Shared_Components:
- Reusable UI components
- Navigation elements
- Form components
- Modal and dialog boxes

08_Error_States:
- Error page designs
- Offline states
- Maintenance pages
- Permission denied screens

09_Loading_States:
- Loading animations
- Progress indicators
- Skeleton screens
- Data loading states

10_Archive:
- Previous versions
- Deprecated wireframes
- Backup copies
- Change history
```

---

## Linking and Navigation Flow

### 5. Wireframe Linking Strategy

#### Link Types and Usage
```
Navigation Links:
- Primary navigation menu items
- Breadcrumb navigation links
- Tab navigation links
- Mobile bottom navigation

Action Links:
- Button clicks → Next page
- Form submissions → Success/Error pages
- Cancel actions → Previous page
- Edit actions → Edit forms

Flow Links:
- Multi-step processes (appointments, registration)
- Wizard navigation (next/previous)
- Conditional flows (based on user type/status)
- Return to start links

External Links:
- Help documentation
- Support contact
- Policy pages
- External systems (if applicable)
```

#### Linking Best Practices
```
Consistency:
- Use same link style throughout project
- Consistent navigation patterns
- Standard link colors and behaviors

Documentation:
- Comment complex navigation flows
- Document conditional logic
- Explain multi-step processes
- Note responsive behavior differences

Testing:
- Verify all links work correctly
- Test navigation flows end-to-end
- Check mobile navigation behavior
- Validate form submission flows
```

#### Link Documentation Format
```
Link Documentation Template:

From: [Source Wireframe]
To: [Destination Wireframe]  
Trigger: [Click/Submit/Select action]
Condition: [If applicable - user type, validation, etc.]
Notes: [Special behavior, responsive considerations]

Examples:
From: Patient_Dashboard_Overview_Desktop
To: Patient_Appointments_Book_Step1
Trigger: "Book Appointment" button click
Condition: User must be logged in
Notes: Mobile version shows full-screen modal

From: Patient_Appointments_Book_Step2
To: Patient_Appointments_Book_Step3
Trigger: "Next" button click  
Condition: Valid date/time selection required
Notes: Validation errors prevent progression
```

---

## Version Control Strategy

### 6. Version Management

#### Version Numbering
```
Format: Major.Minor.Patch (e.g., 1.0.0)

Major Version (X.0.0):
- Complete redesign
- New portal addition
- Major functionality changes
- Breaking changes to navigation

Minor Version (1.X.0):
- New features/screens
- Significant UI improvements
- New user flows
- Component library updates

Patch Version (1.0.X):
- Bug fixes
- Minor adjustments
- Content updates
- Small refinements
```

#### Change Documentation
```
Version History Template:

Version: 1.2.1
Date: 2025-08-07
Changes:
- Added mobile responsive version of patient dashboard
- Updated DICOM viewer tool panel layout
- Fixed navigation consistency across doctor portal
- Improved form validation states

Migration Notes:
- New mobile breakpoint considerations
- Updated component library references
- Navigation changes affect all portals

Next Version (1.3.0) Planning:
- Technician portal enhancements
- Advanced search functionality
- New reporting templates
- Accessibility improvements
```

#### Backup Strategy
```
Daily Backups:
- Automatic project file backup
- Cloud storage sync (if available)
- Local file system backup
- Version tagged backups

Weekly Archives:
- Complete project export
- PDF documentation generation
- Asset file compilation
- Change log update

Monthly Reviews:
- Version consolidation
- Archive old versions
- Clean up deprecated wireframes
- Update documentation
```

---

## Asset Management

### 7. Image and Resource Organization

#### Image Assets
```
Image Categories:
- Logo files (SVG preferred, PNG fallback)
- Icon sets (consistent style)
- Sample photos (patients, medical equipment)
- DICOM sample images
- Device mockups (mobile, tablet, desktop)
- Branding elements

File Naming:
Logo_Capital_Radiology_Primary.svg
Icon_Calendar_24px.svg
Photo_MRI_Machine_Sample.jpg
DICOM_Brain_Sample_001.jpg
Mockup_iPhone_12_Pro.png

Storage Location:
- Project assets folder
- Cloud storage backup
- Shared team location
- Version controlled
```

#### Icon Standards
```
Icon Requirements:
- Format: SVG or PNG
- Sizes: 16px, 24px, 32px, 48px
- Style: Consistent line weight and style
- Color: Monochrome (colorized in Balsamiq)
- Accessibility: High contrast, clear details

Icon Categories:
- Navigation (home, menu, back)
- Actions (add, edit, delete, save)
- Status (success, error, warning, info)
- Medical (heart, clipboard, calendar)
- Interface (search, filter, sort)
- Communication (email, phone, message)
```

#### Custom Components
```
Component Assets:
- Medical equipment illustrations
- DICOM viewer interface elements
- Custom form controls
- Specialized icons (radiology-specific)
- Branded elements

Component Documentation:
- Usage guidelines
- Size specifications
- Color variations
- Responsive behavior
- Accessibility notes
```

---

## Documentation Standards

### 8. Annotation and Notes

#### Wireframe Annotations
```
Annotation Types:

Functional Notes:
- User interaction descriptions
- Business logic explanations
- Validation requirements
- Error handling scenarios

Technical Notes:
- API integration points
- Database field references
- Performance considerations
- Third-party integrations

Design Notes:
- Responsive behavior details
- Animation specifications
- Accessibility requirements
- Browser compatibility notes

Content Notes:
- Dynamic content sources
- Localization requirements
- Content management notes
- SEO considerations
```

#### Note Formatting Standards
```
Note Categories:
🔧 Technical implementation
💡 Design rationale  
⚠️ Important considerations
✅ Requirements/specifications
📱 Mobile-specific notes
🎨 Visual design notes
🔗 Related wireframes/flows

Note Template:
Category: [Icon] [Type]
Description: [Clear, concise explanation]
Action Required: [If applicable]
Related: [Links to other wireframes]
Priority: [High/Medium/Low]

Example:
💡 Design Rationale
The patient dashboard prioritizes upcoming appointments and pending reports 
to reduce cognitive load and improve task completion rates.
Related: Patient_Appointments_View_Desktop
Priority: High
```

#### Requirements Traceability
```
Requirements Mapping:
- Link wireframes to functional requirements
- Reference user stories/use cases
- Connect to business objectives
- Map to technical specifications

Traceability Format:
Requirement ID: REQ-001
Description: Patient can book MRI appointments online
Wireframes: 
- Patient_Appointments_Book_Step1
- Patient_Appointments_Book_Step2
- Patient_Appointments_Book_Step3
- Patient_Appointments_Book_Step4
Status: Implemented in wireframes
```

---

## Collaboration Guidelines

### 9. Team Workflow

#### Review Process
```
Review Stages:

1. Internal Design Review:
- Design team self-review
- Component consistency check
- Navigation flow validation
- Responsive design verification

2. Stakeholder Review:
- Business requirements validation
- User experience evaluation
- Content accuracy verification
- Approval workflow

3. Technical Review:
- Development feasibility assessment
- Technical constraint identification
- Integration complexity evaluation
- Implementation timeline estimation

4. Final Approval:
- Consolidated feedback integration
- Final sign-off from stakeholders
- Release for development
- Documentation handoff
```

#### Feedback Management
```
Feedback Categories:
- Critical: Blocking issues, must fix
- Major: Important changes, should fix  
- Minor: Nice-to-have improvements
- Question: Clarification needed

Feedback Format:
Reviewer: [Name]
Date: [Date]
Wireframe: [Specific wireframe]
Category: [Critical/Major/Minor/Question]
Location: [Specific element/area]
Issue: [Description of problem]
Suggestion: [Proposed solution]
Status: [Open/In Progress/Resolved/Closed]

Resolution Process:
1. Log all feedback in central location
2. Prioritize by category and impact
3. Assign resolution responsibility
4. Update wireframes accordingly
5. Communicate changes to reviewers
6. Verify resolution acceptance
```

#### Access Control
```
Access Levels:
- View Only: Stakeholders, viewers
- Comment Only: Reviewers, business users
- Edit: Design team members
- Admin: Project lead, design manager

Sharing Settings:
- Internal team: Full access
- Stakeholders: View and comment
- Developers: View with specs access
- External reviewers: Time-limited access

Collaboration Tools:
- Built-in Balsamiq comments
- External feedback tools (if needed)
- Version comparison tools
- Change notification system
```

---

## Export and Delivery

### 10. Export Specifications

#### Export Formats
```
PDF Export:
- Purpose: Stakeholder reviews, documentation
- Settings: High quality, vector graphics
- Organization: One wireframe per page
- Includes: Annotations, notes, navigation links
- File naming: Capital_Radiology_Wireframes_v1.0.pdf

PNG Export:
- Purpose: Development reference, presentations  
- Resolution: 2x for retina displays
- Background: Transparent or white
- Individual files per wireframe
- Consistent sizing and margins

HTML Export:
- Purpose: Interactive prototypes
- Includes: Clickable navigation
- Mobile responsive behavior
- Browser compatibility testing
- Hosting considerations
```

#### Developer Handoff Package
```
Deliverables:
1. Complete wireframe PDF documentation
2. Interactive HTML prototype (if available)
3. Component specifications document
4. Asset files (icons, images)
5. Flow diagrams and site map
6. Requirements traceability matrix
7. Design system guidelines
8. Technical notes and annotations

Package Structure:
Capital_Radiology_Wireframes_Delivery/
├── 📄 Wireframes_Complete_v1.0.pdf
├── 🌐 Interactive_Prototype/ (HTML files)
├── 📋 Component_Specifications.pdf
├── 🎨 Asset_Files/ (icons, images)
├── 🔄 Flow_Diagrams.pdf
├── 📊 Requirements_Matrix.xlsx
├── 📘 Design_System_Guidelines.pdf
└── 📝 Technical_Notes.pdf
```

#### Quality Assurance Checklist
```
Pre-Delivery Checklist:

Navigation & Flow:
☐ All navigation links function correctly
☐ User flows are complete and logical
☐ Breadcrumb navigation is consistent
☐ Mobile navigation works properly
☐ Error states are included
☐ Loading states are defined

Design Consistency:
☐ Component library is applied consistently
☐ Typography follows established hierarchy
☐ Color usage matches brand guidelines
☐ Spacing and alignment are uniform
☐ Responsive breakpoints are defined
☐ Accessibility considerations are addressed

Content & Requirements:
☐ All required features are represented
☐ Content is accurate and appropriate
☐ User personas and scenarios are covered
☐ Business requirements are met
☐ Technical constraints are considered
☐ Legal and compliance needs are addressed

Documentation:
☐ Annotations are clear and complete
☐ Technical specifications are detailed
☐ Requirements traceability is maintained
☐ Change log is up to date
☐ Asset files are organized and named correctly
☐ Export quality is verified
```

---

## Maintenance Procedures

### 11. Ongoing Management

#### Regular Maintenance Tasks
```
Weekly Tasks:
- Review and respond to feedback
- Update wireframes based on requirements changes
- Maintain component library consistency
- Check link functionality
- Update change documentation

Monthly Tasks:
- Archive old versions
- Update asset libraries
- Review and update documentation
- Consolidate feedback and learnings
- Plan next iteration improvements

Quarterly Tasks:
- Complete project review
- Update design system guidelines
- Technology and tool evaluation
- Team process improvements
- Stakeholder satisfaction assessment
```

#### Change Management Process
```
Change Request Process:

1. Request Submission:
- Formal change request with rationale
- Impact assessment requirement
- Priority classification
- Stakeholder approval needed

2. Impact Analysis:
- Affected wireframes identification
- Design consistency implications
- Development impact assessment
- Timeline and resource requirements

3. Implementation:
- Wireframe updates
- Documentation updates  
- Navigation flow adjustments
- Component library maintenance

4. Review and Approval:
- Updated wireframe review
- Stakeholder sign-off
- Version control update
- Communication to all parties
```

#### Performance Monitoring
```
Project Health Metrics:
- Wireframe completion percentage
- Review cycle time
- Feedback resolution rate
- Stakeholder satisfaction scores
- Change request frequency
- Export quality metrics

Success Indicators:
- On-time delivery achievement
- Stakeholder approval rates
- Developer handoff smoothness
- Requirement coverage completeness
- Design consistency maintenance
- User flow completeness
```

This comprehensive project structure guide ensures organized, maintainable, and professional wireframe development for the Capital Radiology Online System, supporting effective collaboration and successful project delivery.