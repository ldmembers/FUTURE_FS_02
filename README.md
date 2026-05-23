LeadFlow CRM — Client Lead Management System

A production-grade Mini CRM built as a single HTML file. No backend, no npm, no build step. Open in any browser and start managing leads.


Table of Contents

Project Overview
Live Demo Credentials
Features
Tech Stack
Project Structure
Setup Instructions
Login & OTP Flow
Pages & Modules
Data Model
Keyboard Shortcuts
Responsive Design
Customization Guide
Screenshots
Future Roadmap
Author


Project Overview
LeadFlow CRM is a Client Lead Management System that solves the #1 problem for every agency, freelancer, and startup:

"A potential client filled our contact form — now what?"

This system helps you:

Store every incoming lead in one place
Track where each lead is in your pipeline (New → Contacted → Converted)
Add follow-up notes and activity history per lead
Analyze your conversion rates, sources, and trends
Access all of this from a secure, beautiful admin dashboard

Built for: Freelancers, agencies, startups, and anyone learning full-stack CRM concepts.

Live Demo Credentials
Username  :  admin
Password  :  admin123
OTP       :  Shown on screen after login (auto-generated)

Features
🔐 Authentication
FeatureDescriptionLogin ScreenFull-screen branded login with floating geometric shapesPassword ToggleShow/hide password with eye iconCredential ValidationWrong credentials trigger shake animation + error messageTwo-Factor OTP6-digit OTP auto-generated after loginOTP InputIndividual digit boxes with auto-advance, paste supportCountdown TimerAnimated SVG ring counting down 60 secondsResend OTPNew OTP generated after timer expiresWrong OTPBoxes cleared with shake animation on failureSecure LogoutClears all state and returns to login
📊 Dashboard
FeatureDescriptionKPI CardsTotal, New, Contacted, Converted, Lost counts with trend badgePulse IndicatorAnimated dot on New leads countLine Chart30-day lead trend using Chart.jsDoughnut ChartStatus distribution with legendPipeline FunnelVisual horizontal funnel New → Contacted → ConvertedSource Bar ChartLead count per source with color-coded barsRecent ActivityLast 8 actions across all leads with timestamps
👥 All Leads
FeatureDescriptionFull TableName, company, email, phone, source, status, priority, dateReal-time SearchSearches name, email, company, phone simultaneouslyStatus Filter PillsALL / New / Contacted / Converted / Lost with countsSort ControlsDate (newest/oldest), Name A-Z, Status, PriorityStatus BadgesColor-coded pills: Cyan=New, Amber=Contacted, Green=Converted, Red=LostPriority BadgesHigh (red), Medium (amber), Low (green)3-Dot Action MenuView/Edit, Change Status (all options), Delete per rowRow ClickClick any row to open the Lead Detail DrawerBulk SelectCheckboxes on each row + "Select All" in headerBulk Status ChangeChange status for multiple leads at onceBulk DeleteDelete multiple leads with confirmationEmpty StateIllustrated empty state when no results found
➕ Add Lead
FeatureDescriptionFull FormName, email, phone, company, source, status, message, priorityReal-time ValidationInline red errors under invalid fields on inputPriority PickerVisual toggle pills: Low / Medium / HighSource DropdownWebsite, Referral, LinkedIn, Cold Email, Instagram, OtherSuccess ToastGreen notification on successful submissionAuto RedirectNavigates to All Leads after saving
🔍 Lead Detail Drawer
FeatureDescriptionSlide-in PanelSmooth drawer from the right (520px wide)Pipeline TrackerVisual step indicator — click any step to update statusInline EditToggle edit mode to update name, email, phone, companyNotes TimelineNewest-first list of all follow-up notesAdd NoteTextarea with instant timeline updateActivity HistoryAuto-generated log of all status changes and actionsQuick DeleteDelete button inside drawer with confirmation
📈 Reports
FeatureDescriptionConversion RatePercentage with progress barActive PipelineNew + Contacted countAvg Notes per LeadEngagement metricMonthly Bar ChartLeads vs Conversions over 5 months
⚙️ Settings
FeatureDescriptionAccount InfoAdmin name and email display2FA ToggleEnable/disable two-factor authenticationNotification TogglesNew lead alerts, status change alerts, weekly summaryPipeline StagesVisual view of configured stagesVersion InfoApp version and build info
🧩 System Features
FeatureDescriptionToast NotificationsSuccess, error, info, warning — auto-dismiss in 3.5sConfirm ModalCustom confirmation dialog before destructive actionsLive ClockNavbar shows current date and time, updates every secondKeyboard ShortcutsN = Add Lead, Esc = Close drawer/modalGlobal SearchSearch bar in navbar jumps to leads page with resultsResponsive LayoutMobile sidebar, card layouts, full mobile support

Tech Stack
LayerTechnologyPurposeStructureHTML5Semantic markupStylingCSS3 (Variables, Grid, Flexbox, Animations)All visual designLogicVanilla JavaScript (ES6+)All interactivity and stateChartsChart.js 4.4.1 (CDN)Line, Doughnut, Bar chartsFontsGoogle Fonts — Outfit + DM MonoTypographyIconsUnicode/EmojiLightweight iconsBackendNonePure frontend, all data in-memoryDatabaseNoneJavaScript arrays (state)
No build tools. No package manager. No framework dependencies.

Project Structure
leadflow-crm/
│
├── LeadFlow-CRM.html          # Complete application (single file)
├── README.md                  # This file
└── SETUP.md                   # Step-by-step setup instructions
Inside the HTML file:
LeadFlow-CRM.html
├── <head>
│   ├── Google Fonts import
│   ├── Chart.js CDN script
│   └── <style> — All CSS (1,000+ lines)
│       ├── CSS Variables / Root
│       ├── Animated Grid Background
│       ├── Login Screen Styles
│       ├── App Layout (Sidebar + Topbar)
│       ├── Dashboard Components
│       ├── Leads Table
│       ├── Add Lead Form
│       ├── Lead Detail Drawer
│       ├── Toast Notifications
│       ├── Confirm Modal
│       ├── Reports Page
│       ├── Settings Page
│       └── Responsive / Mobile
│
└── <body>
    ├── Background Effects (Grid, Glow, Shapes)
    ├── Toast Container
    ├── Login Screen
    │   ├── Step 1: Credentials
    │   └── Step 2: OTP Verification
    ├── App Screen
    │   ├── Sidebar Navigation
    │   └── Main Area
    │       ├── Topbar (Clock, Search, Notifications)
    │       ├── Dashboard Page
    │       ├── All Leads Page
    │       ├── Add Lead Page
    │       ├── Reports Page
    │       └── Settings Page
    ├── Lead Detail Drawer
    ├── Confirm Modal
    └── <script> — All JavaScript
        ├── Data (12 dummy leads)
        ├── Utility Functions
        ├── Toast System
        ├── Modal System
        ├── Login & OTP Logic
        ├── App Initialization
        ├── Navigation
        ├── Dashboard Render
        ├── Leads Table Render
        ├── Bulk Actions
        ├── Add Lead Form
        ├── Drawer Logic
        └── Reports Render

Setup Instructions
Option 1 — Instant (No Tools Required)

Download LeadFlow-CRM.html
Double-click the file
Opens in your default browser — done ✅

Option 2 — VS Code + Live Server

Download LeadFlow-CRM.html
Open VS Code
Install the Live Server extension by Ritwick Dey
Open the file in VS Code
Right-click → "Open with Live Server"
Runs at [http://127.0.0.1:5500/LeadFlow-CRM.html](https://claude.ai/public/artifacts/9c680f78-55a0-4abe-af33-919eefa49580)

Option 3 — Python Local Server
bash# Python 3
python -m http.server 8080

# Then open:
#[ http://localhost:8080/LeadFlow-CRM.html](https://claude.ai/public/artifacts/9c680f78-55a0-4abe-af33-919eefa49580)
Option 4 — Node.js Local Server
bashnpx serve .
# or
npx http-server -p 8080

Login & OTP Flow
┌─────────────────────────────────────┐
│          STEP 1: CREDENTIALS        │
│                                     │
│  Username: admin                    │
│  Password: admin123                 │
│                                     │
│  [Wrong] → Shake + Error message   │
│  [Correct] → Slide to OTP step     │
└─────────────────────────────────────┘
                  ↓
┌─────────────────────────────────────┐
│          STEP 2: OTP VERIFY         │
│                                     │
│  OTP shown in hint (demo mode)      │
│  [ _ ] [ _ ] [ _ ] [ _ ] [ _ ] [ _ ]│
│                                     │
│  60s countdown ring                 │
│  Auto-advance between boxes         │
│  Paste support (copy-paste 6 digits)│
│                                     │
│  [Wrong] → Shake + Clear boxes     │
│  [Correct] → Fade to Dashboard     │
│  [Expired] → Resend OTP button     │
└─────────────────────────────────────┘
                  ↓
┌─────────────────────────────────────┐
│           APP DASHBOARD             │
└─────────────────────────────────────┘

Pages & Modules
Dashboard (/dashboard)
Real-time pipeline overview. Charts re-render whenever you add or update leads.
All Leads (/leads)
The main workspace. Every lead is a table row. Click to open the detail drawer. Use filter pills to focus on a specific stage.
Add Lead (/addlead)
Clean form for manually entering a new lead. Useful when someone reaches out by phone or email directly.
Reports (/reports)
Analytics view with conversion metrics and monthly trend chart.
Settings (/settings)
Preference toggles for notifications and two-factor authentication.

Data Model
Each lead follows this structure:
javascript{
  id: "id-abc123",                    // Unique identifier
  name: "Priya Sharma",               // Full name
  email: "priya@techspark.in",        // Email address
  phone: "+91 98765 43210",           // Phone number
  company: "TechSpark India",         // Company name
  source: "Website",                  // Website | Referral | LinkedIn |
                                      // Cold Email | Instagram | Other
  status: "New",                      // New | Contacted | Converted | Lost
  priority: "High",                   // Low | Medium | High
  message: "Interested in...",        // Initial inquiry message
  notes: [
    {
      id: "id-note1",
      text: "Called on May 18...",
      timestamp: "2026-05-18T10:30:00",
      author: "Admin"
    }
  ],
  activityLog: [
    {
      id: "id-act1",
      action: "Lead created",
      timestamp: "2026-05-15T09:00:00"
    },
    {
      id: "id-act2",
      action: "Status changed to Contacted",
      timestamp: "2026-05-20T09:00:00"
    }
  ],
  createdAt: "2026-05-15T09:00:00",   // ISO 8601 creation timestamp
  updatedAt: "2026-05-18T10:30:00"    // ISO 8601 last updated timestamp
}

Keyboard Shortcuts
KeyActionNOpen Add New Lead formEscClose drawer / Close modal

Note: Shortcuts are disabled when focus is inside an input, textarea, or select element.


Responsive Design
BreakpointLayoutDesktop (>720px)Fixed sidebar, full table, all columns visibleMobile (≤720px)Collapsible sidebar (hamburger), compact topbar, horizontal scroll on table

Customization Guide
Change Login Credentials
Find in the <script> section:
javascriptif(u==='admin' && p==='admin123') {
Replace admin and admin123 with your preferred credentials.
Add More Lead Sources
Find the source dropdown in the Add Lead form:
html<select id="f-source">
  <option value="Website">🌐 Website</option>
  <!-- Add your custom source here -->
  <option value="Twitter">🐦 Twitter</option>
</select>
Also add the icon to the srcIcon object in JavaScript:
javascriptconst srcIcon = {
  Website: '🌐',
  Twitter: '🐦',   // add this
  ...
};
Change Color Theme
Edit CSS variables at the top of the <style> tag:
css:root {
  --bg: #06090f;          /* Main background */
  --cyan: #00e5ff;        /* Primary accent */
  --green: #00e676;       /* Success / Converted */
  --amber: #ffc107;       /* Warning / Contacted */
  --red: #ff1744;         /* Danger / Lost */
}
Add Pre-loaded Leads
In the <script> section, add to the leads array using the mkLead() helper:
javascriptmkLead(
  'l13',                  // unique id
  'Your Lead Name',       // name
  'email@company.com',    // email
  '+91 12345 67890',      // phone
  'Company Name',         // company
  'Website',              // source
  'New',                  // status
  'Medium',               // priority
  'Their inquiry message',// message
  [],                     // notes array
  [{id:uid(), action:'Lead created', timestamp:now()}], // activity log
  now(),                  // createdAt
  now()                   // updatedAt
)
Connect to a Real Backend
Replace the in-memory leads array operations with fetch() API calls:
javascript// Example: Load leads from API
async function loadLeads() {
  const res = await fetch('/api/leads');
  leads = await res.json();
  renderLeads();
}

// Example: Save a new lead
async function saveLead(lead) {
  await fetch('/api/leads', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(lead)
  });
}

Screenshots
ScreenDescriptionLoginFull-screen with floating geometric shapes and brand logoOTP6-box digit input with animated countdown ringDashboardKPI cards, line chart, doughnut chart, funnel, activity feedAll LeadsSearchable, filterable, sortable table with bulk actionsAdd LeadValidated form with priority pickerLead DrawerSlide-in panel with pipeline tracker and notesReportsMetrics cards and monthly comparison chart

Future Roadmap

 LocalStorage persistence (data survives page refresh)
 Export leads to CSV / Excel
 Email integration (send follow-up emails from the app)
 Drag-and-drop Kanban board view
 Dark/Light mode toggle
 Lead import from CSV
 Custom pipeline stages
 Role-based access (Admin, Viewer, Sales Rep)
 Node.js + MongoDB backend version
 REST API with JWT authentication
 WhatsApp / SMS follow-up integration


Author
LeadFlow CRM — Built as Task 2 (2026) for Future Interns Program

"I built this system to manage real clients."


Built with: HTML, CSS, JavaScript, Chart.js
Design: Dark Corporate Luxe aesthetic
Fonts: Outfit (UI) + DM Mono (data)


License
This project is open source and available for educational and portfolio use.
Feel free to fork, modify, and build upon it.
