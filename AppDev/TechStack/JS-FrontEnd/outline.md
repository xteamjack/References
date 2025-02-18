# Tailwind Desiging
Layout Design
Cards
Welcome Page
Landing Page Layout
- Top Nav
- Side Nav
- Footer
Components
- User Profile for Top Nav | Side Nav
- 
Dashboard Page
Metro Layouts
Form
Data Page
- Grid
- Table
Component Libraries (Tailwind Supported)
- ShadCn: Good simple, but limited
- Skeleton: Svelt only??, good theme customization
- NextUI.org
Icon Library
- Lucide: Supports all frameworks
- 



# TypeScript

# JS Frameworks
Getting Started
- Project Setup
- Tailwind
App Layout
- Layouts and Hierarchy
- Standard Layout Design (Top, Side, Main, Bottom)
Routing
- App Routing
- Page Routing
- Dynamic Routing
- Grouping Routes (Add extra folders but ignore in folder names in routes)
- Partials ???
- Nested Routing ???
- Custom Routing
Authentication
- SaaS auth Providers
  - Clerk: All standard fn are available as components, customize pages
  - Kinde: Too much work for standard functions
- ClerkJS
  - Register, Login, Forgot, 
  - Agreement page after authentication
  - oAuth
  - MFA, OTP
  - Email links with auth tokens (Send a email and authorize based on them)
    - How to secure if someone copy paste the link
- Custom Auth
Data Binding
- One / Two way binding

Custom Components
- Basic Component
- Props Passing
- CSS Extension on basic components
- Child Components
- Custom Component as Child

Form
- Simple form
- Form Field Component
- Cascading Drop Down
- File upload
  - Input control
  - Drag and Drop with predesignated area or whole page
- Error Handing
  - Client Side
  - Server side
- Toaster Notifications

Component Library
- ShadCn

Panels & Dialogs
- Pull down panels
  - Pin action
- Dialog Boxes
  - Modal
  - Non Modal
  - Alert Dialog
- Splitter Panels

API
- API Calls
- Data Binding
Database adapters
- Server Side
  - RDBMS ORM (Prisma)
  - Mongo DB
  - Fetch data and bind (Client Side Components)
  - Pagination
- API Data Fetch
  - Pagination
- Standard Pagination
- Filters
- Infinite Pagination
- Table Data Binding
- Grid Data Binding to Panels
- Advanced Filters

State management
- Setup Store
- Secure auth token in store (no spoofing)
  - Persistance auth token
- Shopping cart 
  - across browser tabs
  - across browser instances

Cross Cut
- Error handing
  - Error Page (Dev| Prod)
  - Global Error Handler
  - Connection lost notification
- User Experience
  - Loader Component
  - Skeleton component
- Payment Gateway