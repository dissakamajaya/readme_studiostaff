
STUDIOSTAFF®
House of EXP — Staff Operating System
User Guide & Operations Manual
Version 1.0  •  2025
Confidential — Internal Use Only

1. Overview
STUDIOSTAFF® is the internal staff operating system for House of EXP — a music studio and creative space in Bandung, Indonesia. It centralises project management, client tracking, finance, invoicing, academy operations, merchandise, and team collaboration into a single browser-based dashboard.

The system is built as a single-page web application (HTML + JavaScript) and can run fully offline using browser storage, or be deployed to the cloud using Vercel + Supabase for real-time multi-user sync.

1.1 Staff Accounts
User
Name
Role / Division
Colour
aldi
Aldi
Studio / Production
Red
dissa
Dissa
Studio / Operations
Purple
bil
Bil
Finance / Approver
Green

Password: Express (all staff share one password). Can be changed in the Vercel environment variable STUDIOSTAFF_PASSWORD.

1.2 Login
	•	Open the app URL in your browser.
	•	Click your name (Aldi, Dissa, or Bil).
	•	Type the password and press Sign In (or Enter).
	•	Session lasts 7 days; you will be automatically logged in on return visits.

To log out: click your avatar in the sidebar and select Log Out.

1.3 Navigation
The left sidebar organises all sections into groups. Click any item to navigate. On mobile, tap the hamburger icon to open the sidebar.

Group
Section
Purpose
Home
Dashboard
KPI overview, tasks, notifications, pending approvals
Home
Calendar
Monthly view of events, project deadlines, rentals, tasks
Home
Journal
Team daily log with reactions and threaded comments
Divisions
Studio
Projects, tasks, kanban board
Divisions
Rental
Equipment rental bookings and rental invoices
Divisions
Academy
Classes, student enrollment, academy invoices
Divisions
Merchandise
Product inventory, purchase orders, sales log
Operations
Domestic
Internal tasks, leave, food credits, reimbursements
Operations
Finance
Transactions, payroll, debt, bank accounts, statements
Operations
Invoice Builder
Quotes and invoices for all divisions
Operations
Docs
Internal documents, contracts, briefs, lyrics
External
Client Portal
Client-facing view of projects, quotes, invoices
System
Database
Full client list with grouping and sorting
System
Settings
Team accounts, database tools, CSV import

Sidebar collapse: Click the ‹ / › toggle button at the bottom of the sidebar to collapse it to icon-only mode. State is remembered across sessions.

2. Dashboard
The Dashboard is the home screen. It shows a snapshot of this month’s financial performance, assigned tasks, and pending approvals.

2.1 KPI Strip (Top Cards)
Card
What it Shows
Income (This Month)
Total income transactions logged this calendar month
Expense (This Month)
Total expense transactions this calendar month
Net Profit (This Month)
Income minus Expense for this month (green = positive)
Pending Invoices
Total value of unpaid invoices

2.2 Pending Approvals Panel
Any quote created with status "Awaiting Approval" appears here. Staff who did not create the quote can Approve (✓) or Reject (✕) directly from the dashboard. The creator sees "Awaiting peers".

2.3 Dashboard Tabs
	•	Summary — KPI cards + recent activity
	•	Priority Tasks — your high-priority assigned tasks
	•	All Tasks — all tasks assigned to you
	•	Recent Activities — auto-generated log of all changes

3. Studio (Projects & Tasks)

3.1 Projects
Studio tracks all recording, mixing, and production projects. Each project is linked to a client.

Creating a Project
	•	Click + New Project in the top bar.
	•	Fill in: Project Name, Client (optional), Type, Deadline, Status, Description.
	•	Project types include: Recording, Mixing, Mastering, Sound Design, Composition, Commercial Score, Podcast, Film Score, Video Games, Studio Rental, Company Profile, Voice Over, and more.
	•	Click Save Project.

Note: Progress percentage is calculated automatically from completed tasks. You cannot set it manually.

Project Views
	•	Table view — sortable list with progress bars and status
	•	Kanban view — drag tasks between To Do / In Progress / Done columns
	•	Task list — all tasks for the selected project

3.2 Tasks
	•	Click + New Task to create a task.
	•	Assign to one or more team members (Aldi, Dissa, Bil).
	•	Set priority: Normal, High.
	•	Set a due date if needed.
	•	Link to a project (optional).

Task statuses: To Do → In Progress → Done. Changing tasks to Done automatically updates the linked project’s progress percentage.

4. Rental
The Rental section manages studio space and equipment rental bookings.

4.1 Creating a Booking
	•	Click + New Booking.
	•	Select a client (or type a new client name).
	•	Choose equipment from the inventory list, or type a custom equipment description.
	•	Set start date and duration (6h / 12h / 24h / 2 Days / 3 Days / Custom).
	•	Toggle Crew and Delivery options if applicable.
	•	An estimated total is shown before saving.
	•	After saving, the system will offer to create a quote automatically.

4.2 Rental Invoice
Rental invoices appear in the Invoice Builder under the Rental label. They follow the same approval → paid workflow as studio invoices.

4.3 Rental Status
Status
Meaning
Active
Booking confirmed and in progress
Returned
Equipment has been returned
Cancelled
Booking was cancelled

5. Academy
The Academy section manages music classes, student enrollment, and session invoicing.

5.1 Classes
Creating a Class
	•	Click + New Class.
	•	Enter class name (e.g., "Music Production 101 — DAW").
	•	Select an instructor (Aldi, Dissa, or Ekky).
	•	Set a schedule date using the date picker.
	•	Set session time and any notes.
	•	Set maximum students.
	•	Click Save Class.

Class Actions
Action
Description
View
Opens class detail with enrolled students list
Edit (✎)
Edit class name, instructor, schedule, status
✓ Complete
Marks class as Completed
↺ Reschedule
Prompts for new date, marks as Rescheduled
✕ Cancel
Marks class as Cancelled
↩ Active
Restores any non-active class back to Active
📄 Batch Invoice
Creates invoices for all enrolled students at once

5.2 Students
	•	Click + Add Student.
	•	Enter student name, class, phone, email, enroll date.
	•	Student is automatically linked to a class.

Each student row has a 📄 Invoice button. Clicking it prompts for the session fee and creates an invoice linked to that student.

5.3 Academy Invoice Workflow
How Academy Invoicing Works
1. Create a class and enroll students.
2. Click the document icon on any student row to create an individual invoice, or click Batch Invoice in the class detail view to invoice all active students at once.
3. Enter the session fee when prompted.
4. The invoice appears in Invoice Builder under the Academy label with status "Awaiting Approval".
5. A team member approves the invoice.
6. Convert to Invoice and Mark as Paid when payment is received.
7. Payment is automatically logged as an income transaction.

6. Merchandise
The Merch section manages EXP and NAH branded products, purchase orders, and sales tracking.

6.1 Inventory (Products)
Adding a Product
	•	Click + New Product in the Inventory tab.
	•	Enter: Product Name, Emoji (optional), Brand (EXP / NAH / X).
	•	Select Category: AP (Apparel), AC (Accessories), CL (Collectibles).
	•	Set SKU Number — the SKU is auto-built as BRAND-CAT-XXX (e.g., EXP-AP-001).
	•	Set Sell Price, Member Price, and Initial Stock.
	•	Optionally add Year and Edition/Colour.
	•	Click Save Product.

Current stock is automatically calculated as: Initial Stock − Total Sales Qty. You do not need to update stock manually.

6.2 Purchase Orders
	•	Go to the Purchases tab.
	•	Click + New Purchase.
	•	Select a product from the inventory.
	•	Enter qty, total cost, supplier name, and status.
	•	Status options: In Production, Due, Paid.
	•	"Mark as Paid" automatically logs the cost as a Merchandise expense transaction.

6.3 Sales Log
	•	Go to the Sales Log tab.
	•	Click + Log Sale.
	•	Select product, optional customer name, qty, unit price, sale type.
	•	Sale types: Sales, Bundle, Free.
	•	Sales with a price automatically log income as a Merchandise transaction.
	•	Click Make Invoice to generate a quote for the sale.

7. Domestic
Domestic handles internal studio housekeeping: operational tasks, staff leave, food credits, and expense reimbursements.

7.1 Tasks Tab
Internal operational tasks (cleaning, equipment maintenance, errands). Create with + New Domestic Task. Assign to a team member, set priority and due date.

7.2 Leave Notice
Staff submit leave requests here. Bil (approver) reviews and approves or rejects. Status flow: Pending → Approved / Rejected.

7.3 Food Credits
Track daily meal allowances. Each entry is logged per staff member. Bil approves all food credit requests. Approving auto-logs a Food expense transaction.

7.4 Reimbursements
Staff submit expense reimbursement requests with amount, description, and receipt reference. Bil approves. Approving auto-logs a Reimbursement expense transaction.

8. Finance
Finance is the central hub for all money movement at House of EXP.

8.1 Bank Accounts
The bank strip at the top of Finance shows live balances for all three accounts:
Account
ID
Owner
Colour
EXP-BCA
bca
Studio
Blue
EXP-Jenius
jenius
Studio
Purple
NAH
nah
Rental
Amber

Balances update automatically when: transactions are logged, invoices are paid, payroll is paid, or purchases are marked paid.

8.2 Overview Tab
	•	Income, Expense, and Net Profit — This Month only
	•	Pending Invoices total
	•	All Time Income / All Time Expense / Net (shown at the bottom strip)
	•	Recent Transactions list
	•	Outstanding Debts list

8.3 Income & Expense Tabs
Both tabs have the same controls:
	•	Search bar — filter by description, category, label, or bank
	•	Period filter — All / Week / Month
	•	Sort — Newest / Oldest
	•	Label filter — Studio / Rental / Academy / Merchandise / Domestic
	•	Group By — None / By Bank / By Category / By Label

Groups are collapsible: click the group header to collapse/expand. Edit button (✎) appears on each row. CSV-imported rows show a "CSV" badge and cannot be deleted.

8.4 Logging a Transaction
	•	Click + Log Transaction in the top bar or Finance section.
	•	Enter Description, Amount, Type (Income / Expense).
	•	Select Category (Studio Booking, Project, Rental, Salary, etc., or Custom).
	•	Set Division / Label.
	•	Select Bank Account (required).
	•	Set Date. Click Save.

Selecting "Custom..." in Category shows a text input for a custom category name.

8.5 Payroll Tab
	•	Click + Log Payroll.
	•	Select employee, amount, month, year, bank account.
	•	Payroll is created with status "Awaiting Approval".
	•	Bil reviews and clicks Mark Paid — this deducts from the selected bank account and logs a Salary expense transaction.

8.6 Debt Tab
Tracks amounts owed by or to House of EXP.
	•	Payable — We owe someone (shows in red)
	•	Receivable — Someone owes us (shows in green)

Partial settlement: click Settle on a debt, enter the partial amount. The remaining balance is tracked. Status changes from Outstanding → Partially Settled → Settled.

8.7 Statements Tab
Financial statements for predefined periods:
	•	This Week / This Month / This Quarter / This Year

Each statement shows: Total Income, Total Expense, Net Profit for the period, plus a breakdown by division. The top of the Statements page always shows All Time summary cards (Income, Expense, Net).

9. Invoice Builder
The Invoice Builder is where all quotes and invoices are created, approved, and tracked across all divisions.

9.1 Quotation vs Invoice
Document
Number Format
Purpose
Quotation
#QEXP-01
Sent to client for approval before work begins
Invoice
#EXP-001
Issued after work is complete or payment is due

Numbers are sequential and auto-assigned. The next number continues from the last one created.

9.2 Creating a Quote
	•	Click + New Quote.
	•	Select a client.
	•	Choose category (Studio / Rental / Academy).
	•	Link to a project (optional).
	•	Add line items: description, quantity, and unit price.
	•	Apply a discount % if needed.
	•	Set a due date and notes.
	•	Click Save Quotation. Status defaults to "Awaiting Approval".

9.3 Approval Workflow
Quote Approval Flow
Step 1: Creator saves the quote (Awaiting Approval)
Step 2: Another team member clicks Approve or Reject
Step 3: If approved, convert to Invoice by clicking "→ Convert to Invoice"
Step 4: Mark as Paid when payment is received
Step 5: Payment auto-logs as income transaction + updates bank balance

9.4 Filtering Invoices
	•	Filter by label: Studio / Rental / Academy
	•	Sort by date, amount, or status
	•	View button opens the invoice detail
	•	✎ Edit button allows editing status, discount %, due date, and notes

9.5 PDF Download
Click the 📄 Download PDF button inside any invoice or quote detail view. The system opens a print-ready A4 page in a new tab.

Invoice PDF includes:
	•	House of EXP header (address, phone, email, website)
	•	Bill To (client name, contact info)
	•	All line items with qty and unit price
	•	Subtotal, discount, and total
	•	Payment method: BCA 1394227369 — Islam Bilhaqy (invoices only)
	•	Thank you message (invoices only)

Quote PDF does not include payment details — only the line items and total.

10. Docs
Docs stores internal documents: contracts, briefs, agreements, lyrics, revisions, and notes.

10.1 Creating a Document
	•	Click + New Doc.
	•	Enter title, type, and status.
	•	Link to a project and/or client (optional).
	•	Mention team members (they receive a notification).
	•	Write content in the text area.
	•	Click Save Doc.

10.2 Document Types
Type
Colour
Use
Contract
Purple
Legal agreements with clients
Agreement
Blue
Internal or partner agreements
Brief
Amber
Project or campaign briefs
Material
Green
Reference materials, assets
Lyric
Red
Song lyrics
Revision
Teal
Revision notes and change requests
Notes
Gray
General notes and memos
Other
Gray
Anything else

10.3 Filtering Documents
	•	Search by title or related project/client
	•	Filter by type
	•	Filter by status (Draft / Final / Signed / Archived)

11. Calendar
The Calendar shows a monthly view of all time-sensitive items across the system.

11.1 What appears on the Calendar
Icon
Type
Source
◆
Custom Events
Events created via + Add Event
▣
Project Deadlines
Deadline field on each project
●
Task Due Dates
Due date field on each task (red = high priority)
📦
Rental Bookings
Start date of each rental booking

11.2 Adding an Event
	•	Click + Add Event.
	•	Enter title, date, and toggle All Day if the event lasts all day (hides time field).
	•	If not all day: set start time and duration (30 min / 1h / 2h / 4h / 8h / Custom).
	•	Select a colour and optionally add notes.
	•	Click Save Event.

11.3 Navigation
	•	‹ Prev and Next › buttons navigate between months
	•	Today button returns to the current month

12. Journal
The Journal is a team daily log. Use it to record what happened each day: sessions, decisions, issues, and wins.

12.1 Creating a Journal Entry
	•	Click + Add Journal.
	•	Write your entry in the text area.
	•	Select a label (Studio / Rental / Academy / Domestic).
	•	Click Save.

12.2 Reactions & Comments
	•	React to any entry with: 👍 😢 🔥 😂
	•	Click a reaction to toggle it on/off. Count shows how many reacted.
	•	Click into an entry to expand the comment thread.
	•	Type a comment and press Enter or Send.
	•	You can delete your own comments (click ✕).

13. Client Portal
The Client Portal is an internal-facing view that shows a selected client’s complete history in one place. It is intended for use during client meetings or for internal reference, not for sharing with clients directly.

13.1 Using the Portal
	•	Use the search bar to filter clients by name.
	•	Select a client from the dropdown.
	•	The portal shows: client info, all their projects, rentals, quotes, and invoices.
	•	Totals show: Lifetime Paid value, Outstanding (unpaid) balance.

14. Database (Client List)
The Database section is the master client list with sorting, grouping, and inline editing.

14.1 Client Labels
Each client has a Label that determines which division they primarily belong to:
	•	Studio — recording and production clients
	•	Booking — rental / event clients
	•	Academy — music class students or parents

Change a client’s label directly in the table using the dropdown in the Label column. No need to open the edit modal.

14.2 Grouping & Sorting
	•	Group By: None / By Label / By Type
	•	Sort By: Name / Created Date / Lifetime Value
	•	Click a group header to collapse/expand that group

14.3 Quick Actions
Button
Action
View
Open client portal for this client
✎ Edit
Open edit modal (name, type, email, phone, address, notes)
+ Proj
Quickly create a new project linked to this client
✕ Delete
Delete client (requires confirmation)

15. Settings

15.1 Team Members
Shows the list of staff with their colour indicator. "You" is shown next to your own account.

15.2 Database Management
Button
Action
🌱 Seed Database
Loads 725 real EXP financial transactions from 2023–2024 history
🗑️ Reset Database
Wipes ALL data (irreversible — requires confirmation)

Warning: Reset cannot be undone. Use only to start fresh with a clean workspace.

15.3 CSV Import
Import data in bulk using CSV files. Supported import targets:
Target
Required Fields
Optional Fields
Studio Projects
name
clientName, type, deadline, status, desc
Merch Inventory
name
brand, category, sku, price, memberPrice, initialStock
Merch Purchases
productName, qty, totalCost
supplier, status
Merch Sales
productName
clientName, qty, unitPrice, type, date
Finance Income
description, amount
category, division, bank, date
Finance Expense
description, amount
category, division, bank, date
Docs
title
type, status, related, content
Clients
name
type, email, phone, address, label, notes

How to import:
	•	Click any import card (e.g., Finance Income).
	•	Download the template CSV to see the expected column format.
	•	Fill in your data and save the file.
	•	Upload the file.
	•	The system auto-maps columns by header name (flexible — order does not matter).
	•	Review the column mapping and adjust if needed.
	•	Click Import Data.

All imports are append-only — existing data is never overwritten or deleted.

16. Notifications
The bell icon in the topbar shows unread notifications. Notifications are created automatically when:
	•	A task is assigned to you
	•	A document mentions you
	•	A quote you created is approved or rejected
	•	A payroll or reimbursement is approved
	•	A quote has been in "Awaiting Approval" for more than 7 days
	•	Academy invoices are created in batch

Click a notification to navigate to the relevant item. Click Mark all read to clear the badge.

17. Deployment Guide (Vercel + Supabase)
STUDIOSTAFF® can be deployed to the cloud for real-time multi-user access. The standalone HTML file works fully offline without any server.

17.1 Architecture
Layer
Technology
Purpose
Frontend
Single-page HTML (530KB)
Browser-based UI, runs on any device
API
Vercel Serverless Functions
Auth, session management, data sync
Database
Supabase (PostgreSQL)
Persistent storage for all workspace data

17.2 Supabase Setup
	•	Create a new project at supabase.com.
	•	Choose region: Southeast Asia (Singapore) for best performance in Indonesia.
	•	In SQL Editor, run the contents of supabase_schema.sql.
	•	Go to Settings → API and copy: Project URL and service_role key.

17.3 Vercel Deployment
	•	Install Vercel CLI: npm install -g vercel
	•	Navigate to the studiostaff-deploy folder.
	•	Run: npm install
	•	Run: vercel login
	•	Run: vercel — follow prompts.
	•	Add environment variables in Vercel Dashboard → Project → Settings → Environment Variables:

Variable
Value
SUPABASE_URL
https://xxxx.supabase.co
SUPABASE_SERVICE_KEY
eyJ... (service_role key)
STUDIOSTAFF_PASSWORD
Express (or your chosen password)

	•	Redeploy: vercel —prod

17.4 Data Sync
All data is stored as a single JSON blob in the Supabase ss_workspace table. Every save operation sends the full workspace to the API, which stores it. Sessions are tracked in ss_sessions with a 7-day expiry. If the API is unreachable, the app automatically falls back to browser localStorage.

17.5 Security Notes
	•	The SUPABASE_SERVICE_KEY is server-side only and never sent to the browser.
	•	All /api/data requests require a valid session token.
	•	Sessions expire after 7 days of inactivity.
	•	Row Level Security (RLS) is enabled on all Supabase tables.

18. Quick Reference

18.1 Top Bar Buttons
Button
Action
+ New Client
Create a new client
📥 Import CSV
Open the CSV import modal

18.2 Status Reference
Status
Colour
Used In
Awaiting Approval
Amber
Quotes, Payroll, Leave, Food Credits, Reimbursements
Approved
Green
Quotes, Leave, Food Credits, Reimbursements
Rejected
Red
Quotes, Leave, Food Credits, Reimbursements
Active
Green
Projects, Clients, Classes, Rentals
On Hold
Red
Projects
Done / Completed
Gray
Projects, Classes
Cancelled
Red
Classes, Rentals
Rescheduled
Amber
Classes
Paid
Green
Invoices, Payroll
Outstanding
Red
Debts
Partially Settled
Amber
Debts
Settled
Green
Debts

18.3 Common Workflows
Studio Recording Project End-to-End
1. Add client (Database or + New Client)
2. Create project (Studio → + New Project)
3. Add tasks to the project
4. Create a quote (Invoice Builder → + New Quote)
5. Quote is approved by a peer
6. Convert to Invoice
7. Client pays → Mark as Paid
8. Payment auto-logged as income to selected bank account

Merchandise Sale End-to-End
1. Add product to inventory (Merch → Inventory → + New Product)
2. Log purchase order when stock arrives (Merch → Purchases → + New Purchase)
3. Mark purchase Paid (logs expense)
4. Log sale (Merch → Sales Log → + Log Sale)
5. Sale auto-logs income
6. Optionally: Make Invoice from the sale for formal documentation

Academy Class End-to-End
1. Create class (Academy → Classes → + New Class)
2. Enroll students (Academy → Students → + Add Student)
3. After session: click Batch Invoice in class detail
4. Set session fee → invoices created for all students
5. Approve invoices in Invoice Builder
6. Mark as Paid when collected

18.4 Studio Contact Info
Field
Value
Studio Name
House of EXP
Address
Kyomi Space, Jl. Ir. H. Juanda No.130, Dago, Coblong, Bandung 40135
Phone
+62-812-147-159-13
Email
sonicdesignexp@gmail.com
Website
expstudio.notion.site
Bank Name
BCA
Account Number
1394227369
Account Holder
Islam Bilhaqy

STUDIOSTAFF® v1.0  —  House of EXP  —  2025
