# BS Realty LLC — System User Manual

**Version 1.0 | March 2026**
**Prepared for: BS Realty LLC Internal Team**

---

## Table of Contents

1. [System Overview](#1-system-overview)
2. [Accessing the System](#2-accessing-the-system)
3. [Client-Facing Website](#3-client-facing-website)
   - 3.1 [Homepage](#31-homepage)
   - 3.2 [Scheduling an Appointment](#32-scheduling-an-appointment)
   - 3.3 [Property Inquiry Form](#33-property-inquiry-form)
   - 3.4 [Insurance Quote Request](#34-insurance-quote-request)
   - 3.5 [Home Improvement Quote](#35-home-improvement-quote)
   - 3.6 [Contact Us Form](#36-contact-us-form)
   - 3.7 [Job Listings & Applying for a Job](#37-job-listings--applying-for-a-job)
   - 3.8 [Become an Agent](#38-become-an-agent)
4. [Admin Dashboard — Getting In](#4-admin-dashboard--getting-in)
   - 4.1 [Logging In](#41-logging-in)
   - 4.2 [Dashboard Layout & Navigation](#42-dashboard-layout--navigation)
   - 4.3 [Notifications Panel](#43-notifications-panel)
   - 4.4 [User Profile Menu](#44-user-profile-menu)
5. [Dashboard Overview Page](#5-dashboard-overview-page)
6. [Managing Contacts](#6-managing-contacts)
7. [Managing Appointments](#7-managing-appointments)
   - 7.1 [Appointment List & Filtering](#71-appointment-list--filtering)
   - 7.2 [Viewing Appointment Details](#72-viewing-appointment-details)
   - 7.3 [Updating Appointment Status](#73-updating-appointment-status)
   - 7.4 [Cancelling an Appointment (With Reason)](#74-cancelling-an-appointment-with-reason)
   - 7.5 [Disabling & Enabling Appointments](#75-disabling--enabling-appointments)
   - 7.6 [Rescheduled Appointments](#76-rescheduled-appointments)
   - 7.7 [Exporting Appointments to CSV](#77-exporting-appointments-to-csv)
8. [Managing Property Inquiries](#8-managing-property-inquiries)
9. [Managing Insurance Quotes](#9-managing-insurance-quotes)
10. [Managing Home Improvement Quotes](#10-managing-home-improvement-quotes)
11. [Managing Job Applications](#11-managing-job-applications)
12. [Managing Agent Applications](#12-managing-agent-applications)
13. [User Management](#13-user-management)
14. [Analytics](#14-analytics)
15. [Surveys & Testimonials](#15-surveys--testimonials)
16. [Appointment Preferences (Configuration)](#16-appointment-preferences-configuration)
    - 16.1 [Appointment Categories](#161-appointment-categories)
    - 16.2 [Meeting Preferences](#162-meeting-preferences)
    - 16.3 [Business Hours](#163-business-hours)
    - 16.4 [Blocked Dates](#164-blocked-dates)
17. [Settings Page](#17-settings-page)
18. [Status Reference Guide](#18-status-reference-guide)
19. [Role & Permission Guide](#19-role--permission-guide)
20. [Email Notifications — What Gets Sent Automatically](#20-email-notifications--what-gets-sent-automatically)
21. [Frequently Asked Questions](#21-frequently-asked-questions)

---

## 1. System Overview

**BS Realty LLC** is a comprehensive real estate services platform that connects clients with a full suite of services including:

- **Real Estate** – Buy, sell, and rent properties.
- **Mortgage Services** – Home loans and refinancing guidance.
- **Insurance** – Auto, Home, Commercial, and Workers' Compensation quotes.
- **Home Improvement** – Renovation and contractor quote requests.
- **Tax & Financial Counseling** – Professional accounting services.
- **Careers** – Job postings and online applications.
- **Agent Recruitment** – Online agent application portal.

The platform is divided into two major parts:

| Part | Who Uses It | URL |
|------|-------------|-----|
| **Public Website** | Clients, visitors | `https://bsrealtyllc.com` |
| **Admin Dashboard** | Admins, Agents | `https://bsrealtyllc.com/dashboard` |

---

## 2. Accessing the System

### Public Website
No login is required. Anyone can browse the site, fill out forms, and schedule appointments.

### Admin Dashboard
Access requires a registered account with the role of **Admin** or **Agent**. You must log in at `/login`. Authentication is handled through the **Single Sign-On (SSO)** service, which also manages your password, two-factor authentication (2FA), and active sessions.

> **Important:** New admin or agent accounts must be approved by an existing administrator before they become active.

---

## 3. Client-Facing Website

### 3.1 Homepage

The homepage is the first thing visitors see. It is organized into the following sections:

| Section | Description |
|---------|-------------|
| **Hero Banner** | Company headline, tagline, and call-to-action buttons. |
| **Services Preview** | A snapshot of all services offered (Real Estate, Mortgage, Insurance, etc.), each linking to a dedicated services page. |
| **Testimonials** | Real client reviews and ratings (approved by admin via the Surveys module). |
| **Accomplishments** | Key company milestones and counters (e.g., properties sold, clients served). |
| **Our Journey** | Timeline of the company's growth story. |
| **Courses / Training** | Educational content and training programs offered by BS Realty. |
| **Appointment Booking** | Quick-access appointment scheduling form embedded directly on the homepage. |

---

### 3.2 Scheduling an Appointment

Clients can book a consultation directly from the website.

**How to book:**

1. Navigate to the **Schedule an Appointment** section (on the homepage or at `/appointment`).
2. Fill in the required fields:
   - **Full Name** – Your legal name.
   - **Email Address** – Where your confirmation will be sent.
   - **Phone Number** – 10-digit number (formatting like dashes/parentheses is accepted).
   - **Service Category** – Select the type of consultation:
     - Real Estate Consultation
     - Mortgage Services
     - Home Improvement
     - Tax and Accounting
     - Other
   - **Meeting Preference** – Choose how you would like to meet (e.g., In-Person, Virtual/Online, Phone Call). Available preferences depend on the selected category.
   - **Date** – Pick from the calendar. Only available (non-blocked) dates are selectable.
   - **Time Slot** – Available time slots are shown based on the date, category, and preference. Already-booked slots are grayed out.
   - **Your Timezone** – The system detects it automatically but you can change it. All times are stored and confirmed in the **business timezone** (Eastern Time).
   - **Message** *(optional)* – Any additional notes or context for your appointment.

3. Click **Book Appointment**.

**What happens next:**
- You receive a **confirmation email** with full appointment details.
- The BS Realty admin team is **notified in real time** via the dashboard notification system.
- The appointment appears in the admin dashboard for the team to review.

> **Note:** Bookings must be made at least **24 hours in advance** and no more than the maximum advance days allowed (configurable by admin). Weekend bookings may or may not be available depending on the system configuration.

---

### 3.3 Property Inquiry Form

For clients interested in buying, selling, or renting property.

**Navigate to:** `/property-inquiry`

**The form collects:**

| Section | Details |
|---------|---------|
| **Contact Info** | Name, phone, email, preferred contact method (Phone, Text, or Email) |
| **Real Estate Needs** | What the client wants: Buy, Sell, Rent, commercial property, land, etc. |
| **Property Type** | Single-family, Condo, Multi-family, Land, New Construction |
| **Budget & Timeline** | Price range and expected timeframe (Immediately, 1–3 months, 3+) |
| **Preferred Locations** | City, neighborhood, or area preferences |
| **Financing** | Cash purchase, Mortgage loan, or Refinance |
| **Loan Officer Assistance** | Whether they want help with financing |
| **Investment Interest** | Residential, Commercial, Land Development, or None |
| **Insurance Interest** | Homeowners, Renters, Auto, Business insurance, or None |
| **Additional Notes** | Open-ended comments |
| **Concerns** | Specific worries or questions |

After submission, the inquiry is logged in the admin dashboard and a **real-time notification** is sent to admins.

---

### 3.4 Insurance Quote Request

For clients who want insurance pricing.

**Navigate to:** `/insurance-quote`

This is a multi-section form:

| Section | Key Fields |
|---------|-----------|
| **Personal Info** | Full name, date of birth, gender, email, phone |
| **Quote Type** | Auto, Home, Commercial, Workers' Compensation (multiple can be selected) |
| **Driver's License** | DL number, state, expiry, license status |
| **Address** | Primary address, years at address, previous address |
| **Personal Details** | Marital status, occupation, military status |
| **Co-Applicants** | Whether there are additional drivers/household members (up to 10) |
| **Auto Section** *(if Auto selected)* | Prior carrier, years insured, VIN, vehicle use, mileage, coverage types |
| **Property Section** *(if Home selected)* | Property address, dwelling usage, foundation type, roof type |
| **Accident/Violation History** | For auto quotes, any past accidents or violations |
| **Paperless Preference** | Whether the client prefers paperless communication |

---

### 3.5 Home Improvement Quote

For clients needing renovation or home repair services.

**Navigate to:** `/home-improvement-quote`

**The form collects:**
- **Type of Help Needed** – Installation, replacement, repair, etc.
- **Items to Install/Replace** – Specific items (e.g., windows, flooring, HVAC)
- **Property Type** – Residential or Commercial
- **Areas of Work** – Kitchen, Bathroom, Basement, Exterior, etc.
- **Project Timeline** – How soon the work is needed
- **Project Description** – Free-text description of the scope
- **Property Address** – Where the work will happen
- **Contact Info** – Name, email, phone
- **Update Preferences** – Whether the client wants text and/or email updates during the project

---

### 3.6 Contact Us Form

For general inquiries not covered by other forms.

**Navigate to:** `/contact`

**Required fields:**
- Full Name
- Email Address
- Phone Number
- Subject
- Message

> The form includes **reCAPTCHA** verification to prevent spam. If your submission fails, ensure you complete the CAPTCHA challenge.

---

### 3.7 Job Listings & Applying for a Job

**Navigate to:** `/job-listings`

The Jobs page displays all currently open positions at BS Realty. Each listing shows:
- Job Title
- Location
- Employment Type (Full-time, Part-time, Contract, Freelance, Internship)
- Salary/Compensation Range
- Requirements & Qualifications

**To apply:**
1. Click on a job listing to view full details at `/job-details/[job-slug]`.
2. Click **Apply Now** to open the application form.
3. Complete all sections:

| Section | Fields |
|---------|--------|
| **Contact Info** | Name, email, phone |
| **Work Preferences** | Full-time/Part-time, Remote/On-site/Hybrid, Start availability |
| **Experience** | Years of experience, technical skills, programming languages/tools |
| **Compensation** | Expected compensation or salary range |
| **Work Style** | Experience with startups, availability across time zones |
| **Portfolio** | Links, certifications, description of past/recent projects |
| **Motivation** | Why they want to work at BS Realty, referral information |
| **Resume** | Upload your resume (PDF, DOC, DOCX — 5MB max) |

4. Submit the application.

After submission, you receive a confirmation and the admin team is notified.

---

### 3.8 Become an Agent

For real estate professionals who want to join the BS Realty team.

**Navigate to:** `/become-agent`

**The form collects:**

| Field | Details |
|-------|---------|
| Name, Email, Phone | Contact details |
| License Status | Licensed, Inactive, Expired, Pre-licensing, or None |
| License Number & States | For licensed agents |
| Years of Experience | 0–1, 1–3, 3–5, 5–10, or 10+ years |
| Current Brokerage | If currently affiliated |
| Areas of Expertise | Real Estate, Mortgage, Tax, Insurance, Home Improvement, Others |
| Availability | Full-time, Part-time, or Both |
| Work Eligibility | US Citizen, Permanent Resident, H1B, TN Visa, Other Visa |
| How Did You Hear | Online Search, Social Media, Referral, etc. |
| Resume | Upload required |
| License Copy | Upload (optional) |
| ID Card | Upload (optional) |

---

## 4. Admin Dashboard — Getting In

### 4.1 Logging In

1. Go to `/login`.
2. Enter your **email address** and **password** linked to your SSO account.
3. If 2FA is enabled, complete the verification step.
4. You are redirected to the **Dashboard Overview**.

> If you cannot log in, contact your administrator or visit the SSO portal to reset your password.

---

### 4.2 Dashboard Layout & Navigation

The dashboard uses a consistent layout:

```
┌─────────────────────────────────────────────────────────────────┐
│  [Sidebar - Left]         [Top Bar]              [Content Area] │
│                                                                  │
│  ┌ BS Realty Logo ──────┐  ┌ ─── Notification Bell | User ─ ┐  │
│  │ Dashboard            │  └────────────────────────────────┘  │
│  │                      │                                        │
│  │ MAIN                 │   ┌─────────────────────────────────┐ │
│  │  ○ Overview          │   │                                 │ │
│  │  ○ Contacts          │   │       Page Content              │ │
│  │  ○ Appointments      │   │                                 │ │
│  │  ○ Property Inquiries│   └─────────────────────────────────┘ │
│  │  ○ Insurance Quotes  │                                        │
│  │  ○ Home Improvement  │                                        │
│  │                      │                                        │
│  │ JOBS                 │                                        │
│  │  ○ Job Applications  │                                        │
│  │  ○ Agent Applications│                                        │
│  │                      │                                        │
│  │ ADMIN                │                                        │
│  │  ○ Users             │                                        │
│  │  ○ Analytics         │                                        │
│  │  ○ Surveys           │                                        │
│  │  ○ Notifications     │                                        │
│  │  ○ Apt. Preferences  │                                        │
│  │  ○ Settings          │                                        │
│  │                      │                                        │
│  │ [Logout Button]      │                                        │
│  └──────────────────────┘                                        │
└─────────────────────────────────────────────────────────────────┘
```

**Sidebar Controls:**
- Click the **« / »** arrow buttons at the top of the sidebar to **collapse or expand** it. Collapsed mode shows only icons; expanded mode shows icons + labels.
- Your sidebar preference is **saved automatically** between sessions.
- On mobile, tap the **hamburger menu (☰)** in the top bar to open the sidebar as an overlay.

**Navigation sections differ by role:**
- **Admins** see all sections listed above.
- **Agents** see a limited subset relevant to their responsibilities (primarily operational sections, not system administration).

---

### 4.3 Notifications Panel

The **bell icon (🔔)** in the top-right corner shows real-time alerts for new incoming activity.

- A **red badge** with a number indicates how many unread notifications you have. If there are more than 9, it shows **9+**.
- Click the bell to open the **Notifications Dropdown**, which shows the most recent notifications with:
  - An icon for the notification type
  - Title and a short message snippet
  - Time ago (e.g., "2m ago", "3h ago", "1d ago")

**Notification Types:**

| Icon Color | Type |
|-----------|------|
| 🔵 Blue | New Contact Submission |
| 🟣 Indigo | New Appointment Booked |
| 🟢 Green | Property Inquiry |
| 🟡 Yellow | Insurance Quote |
| 🟣 Purple | Job Application |
| 🟠 Orange | Agent Application |
| 🔴 Rose | Home Improvement Quote |
| 🩵 Teal | Client Registration |
| 🟡 Amber | Agent Registration |
| ⬜ Gray | Survey Submitted |

**Clicking a notification:**
- Navigates you directly to the relevant section/record.
- Automatically marks the item's status as "pending" (acknowledging you have seen it).
- Removes the notification from the unread count.

Click **"View all notifications →"** at the bottom of the dropdown to see the full Notifications page.

---

### 4.4 User Profile Menu

Click your **name/avatar** in the top-right corner. The dropdown shows:
- Your display name and email
- Your role badge (Admin, Agent, or Client)
- Links to **Profile** and **Settings**
- **Sign Out** button

---

## 5. Dashboard Overview Page

**Navigate to:** `/dashboard`

This is the first page you see after logging in. It provides a bird's-eye view of the system.

### Key Metrics (Stat Cards)

At the top, four gradient cards display live data:

| Card | What It Shows |
|------|--------------|
| **Total Clients** | Number of users with the "client" role |
| **Total Contacts** | Total general contact form submissions |
| **Appointments** | Total appointment bookings (all statuses) |
| **Total Agents** | Active agents in the system |

Each card also includes a **sparkline mini-chart** and a **trend indicator** (e.g., +12%, +25%).

### Service Requests Section

Below the stat cards, a 3-column breakdown shows quick counts for:
- **Property Inquiries** total
- **Insurance Quotes** total
- **Home Improvement Quotes** total

### Quick Actions Panel

A sidebar panel with shortcut buttons to navigate directly to:
- View Contacts
- Property Inquiries
- Insurance Quotes
- Home Improvement
- View Reports

---

## 6. Managing Contacts

**Navigate to:** `/dashboard/contacts`

This page lists all general contact form submissions received from the website's **Contact Us** page.

### Viewing Contacts
- Submissions are displayed in a data table with columns: **Name, Email, Phone, Subject, Status, Date, Actions**.
- Click the **eye icon (👁)** in the Actions column to open a full detail view of the contact.

### Searching & Filtering
- Use the **search bar** to find contacts by name, email, or phone.
- Use the **Status filter** dropdown to filter by:
  - **New** – Just submitted, not yet reviewed.
  - **Pending** – Being reviewed by the team.
  - **Completed** – Inquiry resolved.
  - **Cancelled** – Submission marked as not needed.

### Updating Status
Open a contact record and use the status action buttons to move it through the workflow.

### Spam Contacts
Contacts flagged as spam (`isSpam: true`) can be identified in the system. Spam contacts are tracked in the database for auditing.

### Exporting
Use the **Export CSV** button to download the current filtered list as a spreadsheet file.

---

## 7. Managing Appointments

**Navigate to:** `/dashboard/appointments`

The Appointments page is the most feature-rich operational section in the dashboard.

### 7.1 Appointment List & Filtering

The table shows all appointments with columns:
- **Client** – Client name and meeting preference type (sub-label)
- **Contact** – Email and formatted phone number
- **Date & Time** – Displayed in business timezone with abbreviation (e.g., EST)
- **Category** – Service type (Real Estate, Mortgage, etc.)
- **Status** – Color-coded badge
- **Booked On** – When the appointment was created

**Available filters:**
- **Status:** New | Pending | Confirmed | Completed | Cancelled
- **Category:** Real Estate Consultation | Mortgage Services | Home Improvement | Tax and Accounting | Other
- **Search:** Name, email, or phone

Use **Clear Filters** to reset all filters at once.

---

### 7.2 Viewing Appointment Details

Click the **eye icon (👁)** on any appointment row to open the **Appointment Details Modal**.

The modal displays:

**Rescheduled Banner** *(shown if this was rescheduled from a previous booking)*
- A purple banner appears with a "View original" button linking to the original appointment.

**Client Information:**
- Full name
- Phone (formatted)
- Email

**Service Details:**
- Category (e.g., Real Estate Consultation)
- Meeting Type / Preference (e.g., In-Person, Virtual)

**Schedule** *(shown in two time zones side by side):*

| Card | Shows |
|------|-------|
| 🔵 Business Time | Appointment time in the company's configured timezone (e.g., Eastern Time) |
| 🟢 Customer Time | Same appointment time converted to the client's timezone at booking |

**Message:** The client's optional note is displayed here.

**Cancellation Details** *(shown if status is Cancelled):*
- The cancellation reason provided by the admin
- Date and time of cancellation
- If the client rescheduled, a link to view the **new appointment**

---

### 7.3 Updating Appointment Status

From the Appointment Details modal footer, use the action buttons to update status:

| Button | Moves Status To | When to Use |
|--------|----------------|-------------|
| **Pending** | `pending` | Acknowledge booking, awaiting confirmation |
| **Confirm** | `confirmed` | Appointment has been confirmed with the client |
| **Complete** | `completed` | After the appointment has taken place |
| **Cancel** | Opens cancellation modal | When appointment must be cancelled |

> **Important:** When an appointment is marked **Completed**, the system automatically sends the client a **survey invite** by email, asking them to rate their experience.

---

### 7.4 Cancelling an Appointment (With Reason)

Cancelling an appointment is a two-step process:

1. Click the **Cancel** button in the appointment detail modal footer.
2. The **Cancel Appointment** modal opens. You must provide a **cancellation reason** (minimum 10 characters).
3. Click **Cancel Appointment** to confirm.

**What happens automatically:**
- The appointment status is set to `cancelled`.
- The client receives an **email and SMS** with:
  - Your cancellation reason/explanation.
  - A personalized **reschedule link** so they can book a new time slot.

This ensures a professional and transparent experience for the client.

---

### 7.5 Disabling & Enabling Appointments

**Disabling** is different from cancelling. A disabled appointment:
- Remains visible in the dashboard (it is **not deleted**).
- Cannot have its status changed.
- Does not show up to clients.

**To disable:** Click the **ban icon (🚫)** in the Actions column. Confirm the dialog.

**To enable (re-activate):** Disabled appointments show a **checkmark icon (✓)**. Click it to re-enable.

Disabled appointments show a **"Disabled" badge** on the client name in the table.

---

### 7.6 Rescheduled Appointments

When a client follows the reschedule link sent via cancellation email, a **new appointment** is created. The system automatically:
- Links the new appointment to the original via `rescheduledFrom`.
- Links the original appointment to the new one via `rescheduledTo`.
- Shows a **"Rescheduled" badge** (indigo) on the new appointment in the table.
- Displays "View original" and "View new" buttons in the respective modals so you can traverse the history easily.

---

### 7.7 Exporting Appointments to CSV

Click **Export CSV** in the top-right of the Appointments page. The export includes all currently filtered appointments with these fields:
- ID, Name, Email, Phone, Appointment Date, Time, Category, Preference, Message, Status, Created At, Updated At.

---

## 8. Managing Property Inquiries

**Navigate to:** `/dashboard/property-inquiries`

Lists all property inquiry form submissions.

**Column overview:**
- Name, Phone, Email
- Preferred Contact Method (Phone, Text, or Email)
- Real Estate Needs (Buy, Sell, Rent, etc.)
- Status badge

**Status lifecycle:** `new` → `pending` → `completed` | `cancelled`

**Actions:**
- Click the **eye icon** to view full inquiry details including budget, timeline, locations, financing type, investment interests, and insurance interests.
- Update the status via the detail modal.
- **Export CSV** button available for reporting.

---

## 9. Managing Insurance Quotes

**Navigate to:** `/dashboard/insurance-quotes`

Lists all insurance quote requests.

**Key data shown:**
- Full name, date of birth, contact info
- Quote types requested (Auto, Home, Commercial, Workers' Comp)
- Marital status, occupation
- Status badge

**Viewing details reveals:**
- Complete auto section (vehicle info, prior carrier, coverage preferences, accident/violation history)
- Complete property section (property address, dwelling usage, foundation, roof type)
- Co-applicant details

**Status lifecycle:** `new` → `pending` → `responded` → `closed`

> Note: The "responded" status is unique to insurance quotes, indicating a quote has been sent to the client.

---

## 10. Managing Home Improvement Quotes

**Navigate to:** `/dashboard/home-improvement-quotes`

Lists all home improvement quote requests.

**Data shown:**
- Customer name, email, phone
- Type of help needed
- Property type (Residential or Commercial)
- Timeline
- Status

**Detail view shows:**
- Full project description
- Specific areas of work
- Items to install/replace
- Property address
- Whether the client wants text/email updates

**Status lifecycle:** `new` → `pending` → `completed` | `cancelled`

---

## 11. Managing Job Applications

**Navigate to:** `/dashboard/job-applications`

Lists applications submitted for posted job positions.

**Data shown:**
- Applicant name, email, phone
- Position applied for
- Work arrangement preference (Full-time, Part-time, Contract, Freelance)
- Work setting (Remote, On-site, Hybrid)
- Availability (Immediately, 2 weeks, etc.)
- Status

**Detail view reveals:**
- Technical skills and programming languages
- Years of experience
- Portfolio links and past project descriptions
- Certifications
- Why they want to work at BS Realty
- Resume download link (original filename preserved)

**Status lifecycle:** `new` → `pending` → `reviewed` → `accepted` | `rejected`

**Actions:**
- Update status (reject or accept applicants)
- Disable/Enable applications
- Export CSV

---

## 12. Managing Agent Applications

**Navigate to:** `/dashboard/agent-applications`

Lists all applicants who want to join BS Realty as agents.

**Data shown:**
- Applicant name, email, phone
- License status (Licensed, Inactive, Expired, Pre-licensing, None)
- Years of real estate experience
- Availability (Full-time, Part-time, or Both)
- Status

**Detail view reveals:**
- License number and states licensed
- Current brokerage affiliation
- Areas of expertise
- Work eligibility (US Citizen, Visa type, etc.)
- How they heard about BS Realty
- Referrer name (if applicable)
- Resume, license document, and ID card download links

**Status lifecycle:** `new` → `pending` → `reviewed` → `accepted` | `rejected`

**Actions:**
- Update status to accept or reject candidates
- Disable/Enable applications
- Export CSV

---

## 13. User Management

**Navigate to:** `/dashboard/users`

Provides an overview of all registered users in the system.

**User roles:**

| Role | Description |
|------|-------------|
| **Admin** | Full access to all dashboard features and configuration |
| **Agent** | Operational access to manage client-facing modules |
| **Client** | Public-facing users who register on the website |

**User status:**
- **Active** – User can log in and access the system.
- **Inactive** – User account is deactivated.

**Approval workflow:**
- When a new client or agent registers, their account status starts as `new`.
- Admins review and approve/reject via the Users module.
- After approval, users can log in.

**Admin actions:**
- View user details (name, email, role, registration date)
- Toggle active/inactive status
- Approve or reject pending user registrations

---

## 14. Analytics

**Navigate to:** `/dashboard/analytics`

Provides data insights on system activity and form submission trends.

The analytics dashboard captures and displays event-based data including:
- Submission volume over time (contacts, appointments, inquiries, quotes, applications)
- Status distribution charts
- Activity trends by service category
- Peak activity periods

> Analytics data is event-driven — every form submission, status change, and registration is tracked as an `AnalyticsEvent` in the system.

---

## 15. Surveys & Testimonials

**Navigate to:** `/dashboard/surveys`

The Survey system is **automatically triggered** when an appointment is marked as **Completed**. The client receives an email with a personalized survey link.

### Survey Response Lifecycle

| Status | Meaning |
|--------|---------|
| `quarantined` | Survey just received, pending admin review |
| `approved` | Admin has reviewed and approved the response |
| `rejected` | Admin decided not to publish this review |
| `published` | Shown publicly on the website as a testimonial |

### Admin Actions on Surveys

1. **Review** – Read the rating (1–5 stars) and the client's written feedback.
2. **Edit** – Optionally rephrase or clean up the feedback text before approval (the `editedText` field stores the edited version).
3. **Approve** – Mark the survey as approved.
4. **Publish** – Once approved, publish it to display on the website's Testimonials section.
5. **Reject** – Mark unsuitable surveys as rejected.

> Surveys that are `quarantined` or `rejected` are **never shown** to the public. Only `published` surveys appear on the homepage.

---

## 16. Appointment Preferences (Configuration)

**Navigate to:** `/dashboard/appointment-preferences`

This section is where admins configure **how the appointment booking system works**. There are four subsections:

### 16.1 Appointment Categories

Categories define the **type of service** a client is booking.

**Each category has:**
- **Name** – e.g., "Real Estate Consultation"
- **Duration** – How long the appointment lasts (15 to 480 minutes / up to 8 hours)
- **Description** – What the category covers
- **Active/Inactive** – Toggle to make it available or hidden from the booking form
- **Sort Order** – Controls display order in the booking form

**Default categories:**
- Real Estate Consultation
- Mortgage Services
- Home Improvement
- Tax and Accounting
- Other

**Admin actions:**
- Add new categories
- Edit duration and descriptions
- Activate or deactivate categories

---

### 16.2 Meeting Preferences

Preferences define **how a meeting is conducted** — for example, In-Person vs. Virtual vs. Phone.

**Each preference has:**
- **Name** – e.g., "In-Person Meeting"
- **Description** – Details about this meeting type
- **Business Hours** – A schedule per day of week (Mon–Sun), with open/close times. This is independent per preference.
- **Allow Online Booking** – Whether clients can book this type via the website
- **Requires Special Equipment** – Flag for internal planning
- **Active/Inactive** – Toggle visibility on the booking form

**Why this matters:** The available **time slots** on the booking form depend entirely on the preference's business hours setup. If a preference is closed on Fridays, no Friday slots will appear when that preference is selected.

---

### 16.3 Business Hours

Global business hours define overall open/closed days and break times. These serve as a **secondary layer** of availability checking (on top of preference-specific hours).

**For each day (Sunday through Saturday):**
- **Open/Closed toggle**
- **Start Time** and **End Time**
- **Break Times** – You can add multiple break periods (e.g., 12:00–13:00 for lunch). Appointments cannot be booked during break windows.

---

### 16.4 Blocked Dates

Blocked dates prevent appointments from being booked on specific dates (e.g., holidays, company events, emergencies).

**Each blocked date has:**
- **Date** – The specific date to block
- **Title** – Free-text label (e.g., "Christmas Holiday", "Staff Training Day")
- **Description** – Optional additional details
- **All-Day vs. Time Range** – Block the entire day or just a specific time window
- **Recurring** – Optionally set the block to repeat `yearly`, `monthly`, or `weekly`
- **Active/Inactive** – Toggle to temporarily remove the block without deleting it

**Examples:**
- Block Dec 25 every year with recurrence: `yearly`
- Block lunch hour every Monday: `weekly`
- Block a single day for a one-time holiday

---

## 17. Settings Page

**Navigate to:** `/dashboard/settings`

The Settings page is organized into five tabs:

### Security
Password management, two-factor authentication (2FA), and session management are **handled through the central SSO portal**. A link to the SSO dashboard is provided here. You cannot change your password from within the BS Realty dashboard.

### Notifications
Control which types of events trigger email and in-app alerts:
- Contact form submissions
- New user registrations
- Appointment requests

You can also toggle **Bell Notifications** (in-app) and **SMS Notifications** on/off.

### Appearance
- **Theme:** Light or Dark *(persisted in settings)*
- **Sidebar Collapsed:** Set the sidebar to default to collapsed mode

### Language & Time
- **Language:** English, Spanish, French
- **Timezone:** UTC, Eastern Time, Pacific Time
- **Date Format:** MM/DD/YYYY | DD/MM/YYYY | YYYY-MM-DD

### Role & Access
An overview of user permission management and assignable modules. Links to User Management and Module Access controls.

> **Note:** Detailed role assignment per user is done from the **Users** section, not the Settings page.

---

## 18. Status Reference Guide

### Appointment Statuses

| Status | Badge Color | Meaning |
|--------|------------|---------|
| `new` | Blue | Just booked, no action taken yet |
| `pending` | Yellow | Acknowledged, awaiting confirmation |
| `confirmed` | Green | Confirmed with client |
| `completed` | Gray/Dark | Appointment has occurred |
| `cancelled` | Red | Cancelled (with reason, client notified) |

### Contact / Property Inquiry / Home Improvement Statuses

| Status | Meaning |
|--------|---------|
| `new` | Just received |
| `pending` | Under review |
| `completed` | Successfully resolved |
| `cancelled` | Closed without action |

### Insurance Quote Statuses

| Status | Meaning |
|--------|---------|
| `new` | Just received |
| `pending` | Being reviewed |
| `responded` | Quote has been sent to client |
| `closed` | Case closed |

### Job & Agent Application Statuses

| Status | Meaning |
|--------|---------|
| `new` | Just submitted |
| `pending` | Under review |
| `reviewed` | Team has reviewed the application |
| `accepted` | Applicant accepted |
| `rejected` | Applicant rejected |

### Survey Statuses

| Status | Meaning |
|--------|---------|
| `quarantined` | Awaiting admin review |
| `approved` | Approved for publishing |
| `rejected` | Will not be published |
| `published` | Live on website |

### User Status

| Status | Meaning |
|--------|---------|
| `new` | Newly registered, pending approval |
| `pending` | Under admin review |
| `approved` | Active and can log in |
| `rejected` | Application denied |

---

## 19. Role & Permission Guide

| Feature / Section | Admin | Agent |
|-------------------|-------|-------|
| Dashboard Overview | ✅ | ✅ |
| View Contacts | ✅ | ✅ |
| Update Contact Status | ✅ | ✅ |
| View Appointments | ✅ | ✅ |
| Cancel Appointments (with reason) | ✅ | ✅ |
| Disable/Enable Appointments | ✅ | ❌ |
| View Property Inquiries | ✅ | ✅ |
| View Insurance Quotes | ✅ | ✅ |
| View Home Improvement Quotes | ✅ | ✅ |
| View Job Applications | ✅ | ✅ |
| Accept/Reject Job Applicants | ✅ | ❌ |
| View Agent Applications | ✅ | ❌ |
| Accept/Reject Agent Applicants | ✅ | ❌ |
| User Management | ✅ | ❌ |
| Analytics | ✅ | ❌ |
| Surveys & Testimonials | ✅ | ❌ |
| Appointment Preferences Config | ✅ | ❌ |
| Blocked Dates Management | ✅ | ❌ |
| Settings | ✅ | ✅ (own profile) |
| Real-time Notifications (Bell) | ✅ | ❌ |
| Export CSV | ✅ | ✅ |

> Agents who try to access a restricted page are automatically redirected to `/dashboard` with an error notice.

---

## 20. Email Notifications — What Gets Sent Automatically

The system sends emails automatically based on specific trigger events. No manual action is required.

| Event | Email Sent to Client | Email Sent to Admin |
|-------|---------------------|---------------------|
| Appointment booked | ✅ Confirmation with date, time, category, preference | ✅ New booking alert |
| Appointment cancelled (admin cancels) | ✅ Cancellation reason + reschedule link | — |
| Appointment completed | ✅ Survey invite email | — |
| New contact form submission | — | ✅ Notification |
| New property inquiry | — | ✅ Notification |
| New insurance quote | — | ✅ Notification |
| New home improvement quote | — | ✅ Notification |
| New job application | — | ✅ Notification |
| New agent application | — | ✅ Notification |

> **Note:** If email delivery fails (e.g., SMTP connection issue), the appointment booking or form submission is **still saved** in the database. Email failure does not block the core workflow.

---

## 21. Frequently Asked Questions

**Q: A client says they didn't get a confirmation email for their appointment. What do I check?**
> A: Go to the appointment in the dashboard. If the appointment was saved successfully, the booking went through. Email delivery is logged — check with your server administrator for SMTP logs. Ask the client to check their spam/junk folder.

**Q: A time slot the client selected is showing as unavailable even though it should be open. Why?**
> A: Check the following in order: (1) Is the date blocked? Check `/dashboard/appointment-preferences` → Blocked Dates. (2) Is there already a booking at that time? Check existing appointments. (3) Is the business hours configuration for that preference and day correct? Check Meeting Preferences.

**Q: Can a client reschedule themselves?**
> A: Yes, but only after an admin cancels their appointment. When an admin cancels with a reason, the client receives an email with a unique reschedule link. Following that link allows them to pick a new date and time, which creates a new appointment in the system linked to the original.

**Q: How do I add a new job posting?**
> A: Job management is handled in the `/dashboard/jobs` section. Add the title, slug, description, location, type, salary, requirements, qualifications, skills, and what the company offers.

**Q: Can I delete a submission permanently?**
> A: Most records support **soft-disabling** (which hides them without deleting). Permanent deletion is available for appointments but use it carefully — deleted records cannot be recovered.

**Q: What happens to a survey invite if the client never fills it out?**
> A: The invite expires after a set time but the appointment status remains `completed`. No action is needed from your side.

**Q: What does "Disabled" mean on an appointment vs. "Cancelled"?**
> A: **Cancelled** = The appointment is formally cancelled; the client is notified and can reschedule. **Disabled** = An internal administrative action that hides/freezes the record without notifying the client; typically used for data cleanup or error correction.

**Q: I see "Rescheduled" badge on some appointments. What does it mean?**
> A: That appointment was created when a client used their reschedule link after a previous cancellation. The original appointment still exists in the system (with `rescheduledTo` indicating the new one). You can navigate between them using the "View original" / "View new" buttons in the detail modal.

**Q: How do I export data for reporting?**
> A: Every main section (Contacts, Appointments, Property Inquiries, etc.) has an **Export CSV** button in the top-right corner. The file downloads immediately with all current filter settings applied.

**Q: How do I change my password?**
> A: Go to `/dashboard/settings` → **Security** tab → click **"Open SSO Security Settings"**. This takes you to the central SSO portal where password and 2FA are managed.

---

*This document covers BS Realty LLC system version 1.0. For technical support or to report issues, please contact the development team.*

*Last Updated: March 2026*
