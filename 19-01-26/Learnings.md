# Power Automate Tutorial - Complete Beginner to Pro Notes

## Table of Contents
1. Introduction & Course Overview
2. What is Power Automate?
3. Power Platform Ecosystem
4. Navigation & Interface
5. Types of Triggers & Cloud Flows
6. Building Your First Flow - Templates
7. Building Your First Flow - Describe it to Design it
8. Working with Microsoft Forms Integration
9. Dynamic Content & Expressions
10. Date & Number Formatting
11. SharePoint List Integration
12. Conditional Logic
13. Approval Flows
14. HTML Tables & Email Reports
15. Best Practices & Tips

---

## 1. Introduction & Course Overview

### What You'll Learn
This comprehensive 3-hour course covers Power Automate from beginner to professional level, including:
- Understanding triggers and flow types
- Building automated workflows
- Conditional logic and decision-making
- Approval processes
- Robotic Process Automation basics
- Administrative best practices

### Course Resources
- **Recording Available**: Session is recorded for replay with pause/rewind capabilities
- **Course Files**: Downloadable materials provided to follow along with every step
- **Platform**: Power Automate in the cloud (make.powerautomate.com)

### Instructor Background
- Jonathan Silven, Power Platform Team at Pragmatic Works
- Former high school teacher (10 years teaching history, economics)
- Focuses on foundational concepts and practical skills
- Teaching style: Explain core concepts first, then add complexity

---

## 2. What is Power Automate?

### Primary Purpose
Power Automate was created to help **individual business users be more productive** by automating rule-based, task-based processes that take 5-15 minutes of manual work.

### Key Benefits
- **Save Time**: Automate repetitive tasks
- **Focus on Critical Work**: Free up time for tasks requiring human analysis and decision-making
- **Increase Productivity**: Let automation handle routine processes
- **Reduce Errors**: Consistent execution of processes

### Examples of Tasks to Automate
- Monitoring data and sending conditional emails
- Updating records based on triggers
- Scheduling and calendar management
- Data collection and organization
- Approval workflows
- Notifications and alerts

---

## 3. Power Platform Ecosystem

### The Five Standalone Applications

#### 1. **Power BI**
- Data visualization and business intelligence
- Create reports and dashboards

#### 2. **Power Apps**
- Build custom business applications
- Low-code/no-code development

#### 3. **Copilot Studio**
- Create AI-powered chatbots and virtual agents

#### 4. **Power Pages**
- Build external-facing websites

#### 5. **Power Automate** (Focus of this course)
- **At the core of Power Platform**
- Connects all other services through open API connections
- Passes data between services seamlessly

### Two Versions of Power Automate

#### **Power Automate Cloud** (Today's Focus)
- Access: make.powerautomate.com
- Uses connectors with live API connections
- Works in browser
- Integrates with cloud services

#### **Power Automate Desktop** (Not covered today)
- Downloaded desktop application
- Robotic Process Automation (RPA)
- Works with browser navigation and desktop applications
- No API connections required
- Previous Learn with the Nerds session available (1 year ago)

---

## 4. Navigation & Interface

### Accessing Power Automate

#### Method 1: Direct Website
1. Search for "Power Automate" in Bing/Google
2. Go to make.powerautomate.com
3. Click "Sign In" with Microsoft 365 work/school account

#### Method 2: Microsoft 365 Portal
1. Navigate to Microsoft 365 (office.com)
2. Click on "Apps" in the left navigation
3. Scroll to "Productivity" section
4. Click "Power Automate"

### Left Navigation Panel

#### **Home**
- Quick access to recent flows
- Describe it to Design it feature
- Quick start options

#### **My Flows**
- View all flows you've created
- See flow status (on/off)
- Access flow run history

#### **+ Create**
- Build new flows
- Choose flow type
- Access templates
- Use Describe it to Design it

#### **Templates**
- Pre-built flows by Microsoft and community
- Browse by category
- Search functionality
- Learn from existing solutions

#### **Approvals**
- Manage approval requests
- View approval history
- Respond to pending approvals

#### **Connectors**
- Browse available connectors (900+)
- See connector documentation
- Understand authentication requirements

#### **Data**
- Work with Dataverse tables
- Manage connections
- View custom connectors

---

## 5. Types of Triggers & Cloud Flows

### Understanding Triggers
**A trigger is the starting point of every flow** - it's the event that sets the automation in motion.

### The Three Types of Cloud Flows

#### **1. Automated Cloud Flow (Event Trigger)**
**Most Popular Type**

**Definition**: Starts when something happens outside of Power Automate

**Common Examples**:
- When a new email arrives
- When a file is created in OneDrive/SharePoint
- When a new form response is submitted
- When a Teams message is posted with specific keywords
- When a new item is added to a SharePoint list
- When a tweet mentions your company

**Use Cases**:
- Automatic email notifications
- Data synchronization
- File processing
- Alert systems

**How to Identify**: Look for keywords like "When...", "On...", "Upon..."

---

#### **2. Instant Cloud Flow (Manual/Button Trigger)**
**On-Demand Execution**

**Definition**: Runs when YOU choose to run it by pressing a button

**Button Locations**:
- Power Automate website
- Power Apps applications
- Power Automate mobile app
- Microsoft Teams
- SharePoint (on specific items)
- Flow button widget

**Common Examples**:
- Manually send a report
- Request approval on-demand
- Process selected items
- Trigger data refresh
- Generate documents

**Use Cases**:
- Ad-hoc reporting
- Manual data processing
- User-initiated approvals
- On-demand notifications

**Advantages**:
- Full control over when flow runs
- Can pass parameters/inputs
- Great for occasional tasks

---

#### **3. Scheduled Cloud Flow (Recurrence Trigger)**
**Time-Based Automation**

**Definition**: Runs on a schedule you set

**Scheduling Options**:
- **Frequency**: Seconds, minutes, hours, days, weeks, months
- **Interval**: Every X units (e.g., every 2 days, every 3 hours)
- **Specific Times**: Choose exact hour and minute
- **Time Zones**: Select your timezone for accurate scheduling
- **Days of Week**: For weekly schedules, choose specific days (e.g., only Mondays)
- **Advanced**: Can set multiple schedules if needed

**Examples**:
- Daily summary email at 9 AM
- Weekly report every Monday at 10 AM
- Hourly data sync
- Monthly reminder on the 1st
- Every 15 minutes during business hours

**Use Cases**:
- Recurring reports
- Regular data backups
- Scheduled reminders
- Periodic cleanup tasks
- Time-based notifications

---

### Decision Framework: Choosing Your Trigger Type

**Ask yourself these questions**:

1. **When should this flow run?**
   - Something happens → Automated
   - I decide when → Instant
   - Specific times/dates → Scheduled

2. **Who/What initiates it?**
   - External event → Automated
   - Me/User → Instant
   - Clock/Calendar → Scheduled

3. **How often?**
   - Varies/unpredictable → Automated or Instant
   - Regular intervals → Scheduled

---

## 6. Building Your First Flow - Templates

### What Are Templates?

**Templates are pre-built flows** created by:
- Microsoft
- Power Automate team
- Community members

**Purpose**:
- Quick start solutions
- Learning tool to see how others build
- Customizable starting points
- Time-savers for common scenarios

### Accessing Templates

1. Click **"Templates"** in left navigation
2. Browse or search for what you need
3. View template details before using

### Browsing Templates

#### **Filter by Category** (Top of page)
- All
- Approvals
- Calendar
- Data collection
- Email
- Notifications
- Remote work
- Visio
- And many more...

**Example**: Click "Remote work" to see templates for:
- Team notifications
- Virtual meeting helpers
- Time tracking
- Collaboration tools

#### **Search Templates**
- Type keywords in search bar
- Searches within selected category
- Click "All" to search everything

**Example Search**: "Microsoft Teams"
- Shows all templates using Teams
- Can refine by adding more keywords like "notification" or "approval"

### Template Information Display

Each template shows:

1. **Icons**: Connectors/services used
2. **Creator**: Microsoft, Community, or user name
3. **Flow Type**: Automated, Instant, or Scheduled icon
4. **Download Count**: Number at bottom-right (popularity indicator)
5. **Title**: Brief description of what it does

### Using a Template

#### Step 1: Select Template
Click on any template to view details

#### Step 2: Review Details
- **Description**: What the template does
- **Connectors Required**: Services needed
- **Connection Status**: Green checkmark or "Sign In" button

#### Step 3: Check Connections
**Important**: You must have access to all required connectors

**Connection Indicators**:
- ✅ **Green Checkmark**: Connected and ready (Microsoft 365 single sign-on)
- 🔵 **Blue "Sign In" Button**: Need to authenticate

**If using Microsoft 365 services**:
- Connections usually work immediately
- Single sign-on is enabled

**If using external services**:
- Must sign in to that service
- Need valid account credentials
- May require premium connector license

#### Step 4: Create from Template
1. Click "Continue" or "Create Flow"
2. Connections establish automatically
3. Flow opens in designer
4. Customize as needed
5. Save and test

### Template Example Walkthrough

**Scenario**: "Send Teams message on new email"

1. Search for "send message in teams"
2. Select appropriate template
3. Review: Uses Outlook + Teams
4. Check connections (should be green ✅)
5. Click to create
6. Customize:
   - Which email folder to monitor
   - Which Teams channel to post in
   - Message format
7. Save and enable

---

## 7. Building Your First Flow - Describe it to Design it

### What is Describe it to Design it?

**AI-powered flow creation** using Copilot technology
- Type what you want in plain English
- AI suggests trigger and actions
- Generates flow structure automatically
- Saves time on setup

### Accessing the Feature

**Location 1**: Home page
- Center of screen
- Text box labeled "Describe it to Design it"

**Location 2**: Create page
- Same text box at top
- Additional creation options below

### How to Use It

#### Step 1: Write Your Prompt
**Be as descriptive as possible** - more detail = better results

**Good Prompt Example**:
```
When a Microsoft Form is submitted, send an email to the 
responder with a summary of their answers
```

**Better Prompt Example**:
```
When a new response is submitted to my feedback form, 
automatically send a thank you email to the responder 
including their name, the date they submitted, and a 
summary of their responses
```

**Best Prompt Example**:
```
When someone submits the "Meeting Request" form, 
send them an email receipt showing their name, email, 
meeting topic, preferred date, and description. Format 
the date as DD-MMM-YYYY
```

#### Step 2: Review AI Suggestions
After typing prompt, click **"Generate"**

AI shows:
- **Trigger**: How flow will start
- **Actions**: Steps that will execute
- **Connections**: Services that will be used

#### Step 3: Evaluate and Refine

**Options at this stage**:

**If suggestions look good**:
- Click "Next" to proceed
- Set up connections
- Begin customization

**If suggestions need work**:
- Click "This isn't what I'm looking for"
- AI will provide alternative suggestions
- Can edit your prompt and try again

**Edit Prompt**:
- Modify text in prompt box
- Click "Generate" again
- Get new suggestions

#### Step 4: Proceed with Creation
1. Click "Next"
2. Verify connector access
3. Click "Create Flow"
4. Opens in designer for customization

---

## 8. Working with Microsoft Forms Integration

### Project: Meeting Request Form with Email Receipt

**Goal**: When someone submits a meeting request form, automatically send them an email receipt with their submission details

### Setting Up the Microsoft Form

#### Access Microsoft Forms
1. Use provided template link in course files
2. Or create your own form at forms.microsoft.com

#### Using the Template (From Course Files)
1. Open "Microsoft Form Template Link.txt"
2. Copy the URL
3. Paste in browser
4. Click **"Duplicate"**
5. Form copies to your account
6. Rename if desired

#### Form Structure - Meeting Request
**Fields included**:
1. **Your Name** (Text)
2. **Your Email** (Text) - *Important for anonymous forms*
3. **Meeting Topic** (Choice: Power BI, Power Apps, Power Automate, etc.)
4. **Preferred Date** (Date picker)
5. **Details about Meeting** (Long text)

**Why ask for email?**
- Forms can be anonymous
- Browser privacy settings may hide responder email
- Incognito/private browsing blocks metadata
- Asking directly ensures you have it

#### Preview Your Form
1. Click **"Preview"** button
2. See user experience
3. Test submission (keep browser open for testing later)

### Building the Flow with Describe it to Design it

#### Step 1: Create the Prompt
Navigate to Power Automate > Create > Describe it to Design it

**Prompt**:
```
When a form is submitted, send an email to the responder 
with their submission details
```

Click **"Generate"**

#### Step 2: Review AI Suggestions
AI suggests:
1. **Trigger**: When a new response is submitted
2. **Action 1**: Get response details
3. **Action 2**: Send an email

This looks good! Click **"Next"**

#### Step 3: Verify Connections
- Microsoft Forms ✅
- Office 365 Outlook ✅

Click **"Create Flow"**

---

### Configuring the Flow

#### Understanding the Designer

**Right Side Panel**: Copilot
- Ask questions
- Get help with actions
- Troubleshoot issues
- Learn about features

**Center Canvas**: Your flow
- Trigger at top
- Actions below in sequence
- Click any box to configure

**Left Side Panel**: Configuration
- Opens when you click a step
- Shows all settings for that step
- Close by clicking X or clicking away

---

#### Configuring the Trigger: "When a new response is submitted"

1. **Click on the trigger box** in center
2. Left panel opens with settings
3. **Form Id** dropdown appears

**Select Your Form**:
- Click dropdown
- Shows all your forms
- Select "Meeting Request (Copy)" or your form name

**If form doesn't appear**:
- Refresh browser (F5)
- Form must be created first
- Check you're in right environment

**Once selected**:
- Green "Invalid parameters" message disappears
- Shows form title for confirmation
- Connected to your email/account

---

#### Configuring Action 1: "Get response details"

**Why this step is required**:
Microsoft Forms integration has only 2 actions:
1. **Trigger**: When a new response is submitted (gets response ID only)
2. **Action**: Get response details (gets actual answers)

**They ALWAYS go together** - you cannot get form answers without both!

**Configuration**:
1. Click on "Get response details" box
2. **Form Id**: Select same form (Meeting Request Copy)
3. **Response Id**: Already filled with Dynamic Content

#### Understanding Dynamic Content

**What is Dynamic Content?**
- Outputs from previous steps
- Becomes inputs for later steps
- Represented by green text boxes
- Passes data through the flow

**The Lightning Bolt Icon** ⚡
- Click to see available Dynamic Content
- Shows all outputs from previous steps
- Click to insert into current step

**In this step**:
- Response ID is already added (green box)
- This is the unique identifier for the form submission
- Came from the trigger
- Tells this action which specific response to get details for

**To see Dynamic Content**:
1. Click in "Response Id" field
2. Lightning bolt ⚡ appears on left
3. Click lightning bolt
4. See available fields:
   - Response Id
   - (That's it from the trigger - just the ID)

---

#### Configuring Action 2: "Send an email (V2)"

Click on "Send an email (V2)" box

##### Understanding Office 365 Outlook Actions

**What this action does**:
- Sends email FROM your account
- Uses your Office 365 credentials
- Email appears in your Sent Items
- Shows as from YOU

**Important Notes**:
- Email comes from whoever created the flow
- To send on behalf of someone else: requires additional setup (see Devon Knight's YouTube video)
- To send as shared mailbox: requires permissions and configuration

##### Configuring the Email

**Field 1: To**

Options:
- Type an email address directly (hardcoded)
- Use Dynamic Content (recommended for automation)

**Using Dynamic Content**:
1. Click in "To" field
2. Click "Enter custom value"
3. Lightning bolt ⚡ appears
4. Click lightning bolt
5. Dynamic Content panel opens

**Available Fields** (from Get response details):
- Response Id
- Responders' Email ⚠️
- Submission time
- Your Name
- Your Email ✅
- Meeting Topic
- Preferred Date
- Details about Meeting

**Which email to use?**
- "Your Email" (the one we asked in the form) ✅ Recommended
- "Responders' Email" (from form metadata) ⚠️ May be blank

**Why "Your Email" is better**:
- Always filled if question is required
- Not affected by privacy settings
- Not affected by anonymous submissions
- Not affected by browser settings

**Select**: "Your Email"
- It inserts into "To" field as green box
- Will automatically populate with their email each time

---

**Field 2: Subject**

Type your subject line:
```
Thank you for your meeting request
```

Can mix text and Dynamic Content:
```
Meeting Request Received - [Meeting Topic]
```

To add Dynamic Content in subject:
1. Type text
2. Click where you want Dynamic field
3. Click lightning bolt ⚡
4. Select field (e.g., "Meeting Topic")
5. Continues typing

---

**Field 3: Body**

This is your email message content.

**Formatting Options** (toolbar above):
- **B** Bold
- *I* Italic
- <U> Underline
- Font size
- Bullet points
- Numbered lists
- Links
- Code view (HTML) 🔵 Advanced option

**Create Email Template**:

```
Hello [Your Name],

Here are the details about your meeting request:

Device: [Meeting Topic]
Description: [Details about Meeting]  
Preferred Date: [Preferred Date]

We will get back to you as soon as we can.

Best regards
```

**Adding Dynamic Content to Body**:
1. Type "Hello "
2. Click lightning bolt ⚡
3. Select "Your Name"
4. Continue typing
5. For each field, repeat:
   - Type label (e.g., "Topic: ")
   - Click lightning bolt
   - Select Dynamic Content
   - Press Enter for new line

**Pro Tip**: Use bullet points or numbered lists for better readability

**HTML Code View** (</> button):
- For advanced users
- Paste HTML email templates
- Can export from Outlook as HTML
- Insert Dynamic Content into HTML
- Full control over styling

---

### Testing the Flow

#### ALWAYS Test Before Going Live

**Testing Strategy**:
1. Build one section at a time
2. Test after each major addition
3. Verify outputs before adding more steps
4. Easier to troubleshoot small sections

#### Step 1: Save the Flow
Top-right corner: Click **"Save"**
- Blue button
- Flow is now live (but we'll test first)
- Wait for "Flow saved" confirmation banner

#### Step 2: Initiate Test
Top-right corner: Click **"Test"** (next to Save)

**Test Options**:

**1. Manually** (Perform the trigger action yourself)
- Best for first test
- You control when it runs
- Good for learning

**2. Automatically** (Use previous run data)
- Available after first successful run
- Replays with same data
- Faster for retesting
- Great for editing/debugging

**For First Test**: Select "Manually"
- Radio button: "Perform the trigger action"
- Click **"Test"** button at bottom

#### Step 3: Trigger the Flow
**Screen shows**: Spinning loader - "Waiting for trigger..."

Now perform the action that starts the flow:

1. Go to your form (browser tab you kept open)
2. Fill out the form:
   - **Your Name**: Jonathan Silven
   - **Your Email**: your.email@company.com
   - **Meeting Topic**: Power Automate
   - **Preferred Date**: Select Monday
   - **Details**: "Want to discuss a potential hackathon and boot camp"
3. Click **"Submit"**

#### Step 4: Watch Flow Execute
Return to Power Automate tab

**Flow Run Display**:
- Each step shows as it executes
- ✅ Green checkmark = Success
- Trigger → Action 1 → Action 2
- Typically completes in seconds

**When complete**:
- All steps show green ✅
- "Your flow ran successfully" message

#### Step 5: Verify Results
Check your email inbox

**Email Received**:
- **From**: Your email address (Office 365 Outlook connection)
- **To**: Email from form submission
- **Subject**: "Thank you for your meeting request"
- **Body**: Shows all dynamic content populated:
  - Hello Jonathan Silven,
  - Topic: Power Automate
  - Date: (date value from form)
  - Description: Want to discuss a potential hackathon and boot camp

**Success!** ✅ Flow is working

---

## 9. Dynamic Content & Expressions

### Understanding Dynamic Content (Detailed)

**Definition**: Data that flows through your automation
- Outputs from one step
- Become inputs for another
- Automatically updates each run
- No hardcoding needed

**Visual Indicator**:
- Green text boxes in your flow
- Shows field name
- Represents placeholder for actual data

**How It Works**:
1. Trigger or action produces output
2. Output becomes available as Dynamic Content
3. Use in subsequent steps
4. Data passes through automatically
5. Different data each time flow runs

**Example Flow**:
```
Trigger: Form submitted
  ↓ Outputs: Response ID, Name, Email, Date
  
Action 1: Get details
  ↓ Uses: Response ID
  ↓ Outputs: All form answers
  
Action 2: Send email
  ↓ Uses: Email, Name, Topic, Date
```

### Accessing Dynamic Content

**The Lightning Bolt** ⚡ **Icon**:
- Appears when you click in a field
- Click it to see available Dynamic Content
- Different for each step (shows content available UP TO that point)

**Dynamic Content Panel**:
- Lists all available outputs
- Organized by action/trigger that created them
- Search box at top (for many fields)
- Click any field to insert

**Content Availability**:
- Can only use content from previous steps
- Cannot use content from steps that haven't run yet
- Content accumulates as flow progresses

---

### Expressions vs. Dynamic Content

**Dynamic Content**: 
- Data passed as-is
- No transformation
- Simple insertion
- Lightning bolt ⚡

**Expressions**:
- Functions that transform data
- Mathematical operations
- String manipulation
- Date formatting
- **fx** button

---

### Using the Expression Builder

#### Accessing Expressions

When in any field that accepts Dynamic Content:
1. Click in the field
2. See two tabs:
   - **Dynamic content** (Lightning bolt ⚡)
   - **Expression** (fx symbol)
3. Click **Expression** tab

#### Expression Panel Features

**Function Categories** (left side):
- String functions
- Collection functions
- Logical functions
- Conversion functions
- Math functions
- Date and time functions
- Workflow functions
- And more...

**Search Box**:
- Type function name
- Filters list
- Shows description

**Function List**:
- Click any function to see description
- Click arrow to see syntax/parameters
- Click function name to insert

---

## 10. Date & Number Formatting

### Why Format Data?

**Raw data from forms/lists**:
- May not be user-friendly
- Different regional formats
- Need currency symbols
- Want consistent display

**Formatting benefits**:
- Better readability
- Professional appearance
- Regional customization
- Clear communication

---

### Formatting Dates

#### The Problem
Forms return dates as: `2026-01-20T00:00:00Z`
- Year-Month-Day format
- 24-hour time
- UTC timezone
- Not user-friendly

#### The Solution: formatDateTime()

**Function**: `formatDateTime()`
**Purpose**: Transform date to readable format

#### Step-by-Step Date Formatting

**Scenario**: Format "Preferred Date" in our email

**Step 1: Remove Dynamic Content**
1. Go to "Send an email" step
2. Find the "Preferred Date" Dynamic Content (green box)
3. Click the **X** on the green box to remove it
4. Cursor ready in that spot

**Step 2: Open Expression Builder**
1. Click **fx** (Expression tab)
2. Type: `format`
3. See list of format functions
4. Click on **formatDateTime**

**Description shows**:
```
formatDateTime(timestamp, format?, locale?)
Returns: String in date format
```

**Step 3: Start the Function**
1. Function name appears in expression box
2. Type opening parenthesis: `(`
3. Now need to provide parameters

**Parameter Help**:
Shows: `formatDateTime(timestamp: string, format: string?, locale: string?)`
- `timestamp`: The date to format (required)
- `format`: How to display it (optional)
- `locale`: Language/region (optional)

**Step 4: Add the Date (timestamp parameter)**
1. Cursor is inside parentheses
2. Click **Dynamic content** tab
3. Select "Preferred Date"
4. Switches back to Expression tab
5. Shows: `formatDateTime(triggerOutputs()?['body/r8B...']`

**This long code is**:
- The reference to the Dynamic Content field
- How Power Automate accesses form data
- You don't need to understand it
- Just know it represents "Preferred Date"

**Step 5: Add Format String**
1. After the Dynamic Content reference
2. Type a comma: `,`
3. Type single quote: `'` (starts the format string)
4. Type your format pattern
5. Type closing single quote: `'`

**Format Pattern Syntax**:
- `d` or `dd` = Day (1-2 digits)
- `ddd` = Day abbreviated (Mon, Tue)
- `dddd` = Day full name (Monday, Tuesday)
- `M` or `MM` = Month (1-2 digits)
- `MMM` = Month abbreviated (Jan, Feb)
- `MMMM` = Month full name (January, February)
- `yy` = Year (2 digits)
- `yyyy` = Year (4 digits)
- `h` or `hh` = Hour (12-hour)
- `H` or `HH` = Hour (24-hour)
- `m` or `mm` = Minutes
- `s` or `ss` = Seconds

**Examples**:
```
'dd-MM-yyyy'         → 20-01-2026
'MM/dd/yyyy'         → 01/20/2026
'dd-MMM-yyyy'        → 20-Jan-2026
'MMMM dd, yyyy'      → January 20, 2026
'dddd, MMMM dd'      → Monday, January 20
```

**For our example**:
```
formatDateTime(body('Get_response_details')?['r8b...'], 'dd-MMM-yyyy')
```
Result: 20-Jan-2026

**Step 6: Optional - Add Locale**
To specify language/region:
1. After format string
2. Add comma: `,`
3. Add locale code in quotes

**Locale Examples**:
```
'en-US'  → English (United States)
'en-GB'  → English (Great Britain)
'fr-FR'  → French (France)
'es-ES'  → Spanish (Spain)
'pt-PT'  → Portuguese (Portugal)
'de-DE'  → German (Germany)
```

**Complete with locale**:
```
formatDateTime(body('Get_response_details')?['r8b...'], 'dd-MMM-yyyy', 'en-US')
```

**If omitted**: Uses your environment's default locale

**Step 7: Close and Insert**
1. Type closing parenthesis: `)`
2. Click **"Add"** or **"OK"**
3. Expression inserts into email body
4. Appears as Dynamic Content (but formatted)

#### Testing the Formatted Date

1. **Save** the flow
2. Click **Test**
3. Choose **"Automatically"** (use previous run data)
4. Select the successful run from earlier
5. Click **Test**
6. Check email

**Result**: Date now shows as `20-Jan-2026` instead of `2026-01-20T00:00:00Z`

**Troubleshooting**:
If formatting doesn't work:
- Check for typos in format string
- Verify single quotes are used
- Ensure parentheses are balanced
- Re-edit and save again (new designer sometimes needs this)

---

### Formatting Numbers (Currency)

#### The Problem
Numbers from forms/SharePoint:
- No currency symbol
- No thousands separator
- Variable decimal places
- Example: `1225` or `1225.5`

#### The Solution: formatNumber()

**Function**: `formatNumber()`
**Purpose**: Format numbers as currency, percentages, or with specific decimal places

#### Step-by-Step Currency Formatting

**Scenario**: Format "Estimated Cost" as USD currency

**Step 1: Remove Dynamic Content**
1. In "Send an email" step
2. Find "Estimated Cost" Dynamic Content
3. Click X to remove
4. Cursor ready

**Step 2: Open Expression Builder**
1. Click **fx**
2. Type: `format`
3. Select **formatNumber**

**Step 3: Add Opening Parenthesis**
```
formatNumber(
```

**Step 4: Select the Number**
1. Click **Dynamic content** tab
2. Find "Estimated Cost"
3. Click it (or search for "cost")
4. Returns to Expression tab

**Step 5: Add Format Code**
1. Type comma: `,`
2. Type single quote: `'`
3. Type format code
4. Type closing quote: `'`

**Format Codes**:

**Currency (automatic locale)**:
```
'C'  or 'C0'  → $1,225 (no decimals)
'C1'          → $1,225.0 (1 decimal)
'C2'          → $1,225.00 (2 decimals) ← Recommended
'C3'          → $1,225.000 (3 decimals)
```

**The 'C' means**:
- Use currency format
- Includes currency symbol
- Adds thousands separator (comma)
- Number after C = decimal places

**Other Formats**:
```
'N2'   → 1,225.00 (number with 2 decimals, no symbol)
'P2'   → 12.25% (percentage with 2 decimals)
'#,#'  → 1,225 (thousands separator, no decimals)
```

**For our example**:
```
formatNumber(outputs('Get_response_details')?['Field_5'], 'C2')
```

**Step 6: Optional - Specify Locale**

Default behavior:
- Uses your environment's locale
- In US: $ (dollar)
- In UK: £ (pound)
- In EU: € (euro)
- In Japan: ¥ (yen)

To force specific currency:
```
formatNumber(number, 'C2', 'locale-code')
```

**Examples**:
```
'en-US'  → $1,225.00 (US Dollar)
'en-GB'  → £1,225.00 (British Pound)
'fr-FR'  → 1 225,00 € (Euro - French style)
'de-DE'  → 1.225,00 € (Euro - German style)
'ja-JP'  → ¥1,225 (Japanese Yen)
```

**Complete example**:For US Dollars specifically:
```
formatNumber(outputs('Get_response_details')?['Field_5'], 'C2', 'en-US')
```

**Step 7: Close and Add**
1. Type: `)`
2. Click **Add**
3. Expression inserted

#### Testing Currency Format

1. Save flow
2. Test automatically with previous data
3. Check email

**Result**: 
- Before: `1225` or `1225.5`
- After: `$1,225.00`

---

### Combining Formatted Data

**You can use multiple formatted expressions in one email**:

```
Hello [Name],

Your request has been received.

Meeting Topic: [Topic]
Preferred Date: [formatDateTime(..., 'MMMM dd, yyyy')]
Estimated Cost: [formatNumber(..., 'C2')]

We'll be in touch soon!
```

**Result**:
```
Hello Jonathan Silven,

Your request has been received.

Meeting Topic: Power Automate
Preferred Date: January 20, 2026
Estimated Cost: $1,225.00

We'll be in touch soon!
```

---

### Common Expression Errors & Solutions

**Error**: "Unable to process template language expressions"
- **Cause**: Missing quote, parenthesis, or comma
- **Solution**: Check expression syntax carefully

**Error**: Expression not showing formatted
- **Cause**: Sometimes new designer doesn't save properly
- **Solution**: Re-edit expression, ensure it shows in field, save again

**Blank output**:
- **Cause**: Wrong Dynamic Content reference
- **Solution**: Make sure you selected correct field

**Wrong format**:
- **Cause**: Typo in format string (M vs m, d vs D)
- **Solution**: Remember: capital M = month, lowercase m = minute

---

## 11. SharePoint List Integration

### Understanding SharePoint Lists

**What is SharePoint?**
- Microsoft 365 collaboration platform
- Document storage and management
- Team sites and communication
- Integrated with Office 365

**What are SharePoint Lists?**
- Structured data storage (like Excel tables)
- Multiple column types available
- Better than Excel files for automation
- Built-in version history
- Permissions and security
- No file locking issues

**Why Use Lists Instead of Excel?**
- **Concurrent access**: Multiple users can edit simultaneously
- **Better integration**: Direct API connections
- **No file conflicts**: No "file in use" errors
- **Richer data types**: People picker, choice fields, lookups
- **Scalability**: Handle thousands of records
- **Security**: Item-level permissions possible

---

### Accessing SharePoint

#### Method 1: Microsoft 365 App Launcher
1. Click waffle icon (top-left of any Microsoft 365 page)
2. Select **SharePoint**
3. Opens SharePoint home

#### Method 2: Direct URL
- Navigate to: `yourcompany.sharepoint.com`
- Shows your sites and recent activity

#### Method 3: From Power Automate
- When configuring SharePoint actions
- Can browse to sites directly

---

### Creating a SharePoint List

#### Navigation
1. Go to a SharePoint site
2. Click **New** dropdown
3. Select **List**

#### Creation Options

**1. Blank List**
- Start from scratch
- Add columns manually
- Most flexible

**2. From Excel**
- Upload Excel file
- Auto-creates columns from headers
- Quick setup

**3. From CSV** ✅ (We'll use this)
- Import CSV file
- Preserves data types (with schema export)
- Easiest for replication

**4. From Template**
- Pre-built list structures
- Common business scenarios
- Asset tracker, Issue tracker, etc.

---

### Using the Provided CSV Template

#### Step 1: Locate Course File
From course materials:
- File: **"Device Request.csv"**
- Contains: Pre-configured columns with data types

#### Step 2: Import to SharePoint
1. In SharePoint site, click **New** → **List**
2. Select **"From CSV"**
3. Click **"Upload file"**
4. Browse to Device Request.csv
5. Click **Open**

#### Step 3: Review Structure
CSV shows:
- **Column names** (headers)
- **Data types** (above column names)
- **Sample data** (optional, for reference)

**Columns Included**:

| Column Name | Data Type | Purpose |
|-------------|-----------|---------|
| Title | Single line text | Device name/type |
| Description | Single line text | Details about request |
| Requester | Person | Who made request |
| Request Date | Date and Time | When requested |
| Priority | Choice | Critical/High/Medium/Low |
| Estimated Cost | Number | Price estimate |
| Approved | Yes/No | Approval status |
| Manager Comments | Multiple lines text | Feedback/notes |

#### Step 4: Create List
1. Click **Next**
2. **List name**: "Device Request" (or customize)
3. Review column mapping
4. Click **Create**

**Result**: List created with all columns and data types

---

### Understanding SharePoint Column Types

**Single Line of Text**
- Short text entries
- Limited to 255 characters
- Examples: Name, Title, Email

**Multiple Lines of Text**
- Long text entries
- Can enable rich text formatting
- Examples: Description, Comments, Notes

**Number**
- Numeric values
- Can set min/max
- Decimal places configuration
- Examples: Cost, Quantity, Age

**Date and Time**
- Calendar picker
- Can include time or date only
- Timezone aware
- Examples: Due Date, Request Date, Birth Date

**Yes/No (Boolean)**
- Checkbox
- True/False values
- Default can be Yes or No
- Examples: Approved, Active, Complete

**Choice**
- Dropdown or radio buttons
- Pre-defined options
- Can allow custom values
- Examples: Priority, Status, Department

**Person or Group**
- People picker
- Looks up Microsoft 365 users
- Can allow multiple selections
- Stores user ID, name, email
- Examples: Requester, Manager, Assigned To

**Lookup**
- Reference another list
- Creates relationships
- Examples: Product from Products list

**Managed Metadata**
- Enterprise taxonomy
- Hierarchical terms
- Centralized management

---

### Customizing Your List

#### Hiding Unwanted Columns
Sometimes CSV import creates extra columns (like "Field_0")

**To hide**:
1. Click column header dropdown
2. Select **Column settings**
3. Choose **Hide this column**

OR:
1. Click **+ Add column**
2. Select **Show/hide columns**
3. Uncheck unwanted columns

#### Adding Columns
1. Click **+ Add column**
2. Choose column type
3. Configure settings
4. Click **Save**

#### Setting Required Fields
1. Click column header dropdown
2. **Column settings** → **Edit**
3. Check "Require that this column contains information"
4. **Save**

#### Default Values
1. Edit column settings
2. Set **Default value**
3. Auto-fills for new items

---

### List Forms and Views

#### Default Form
When you click **"New"** or edit an item:
- Shows all visible columns
- Can be customized with Power Apps
- Can hide/show fields
- Can rearrange order

#### Hiding Fields from Form
Not ready for user input yet (like Approved, Manager Comments):

**Two options**:

**Option 1: Column settings**
1. Column header dropdown
2. **Column settings** → **Edit**
3. Under "Additional Settings"
4. Uncheck "Show in new form" or "Show in edit form"

**Option 2: Permissions**
- Set column permissions
- More advanced

**For our list**: Hide Approved and Manager Comments initially

#### Views
Default view shows all items in table format

**Can create custom views**:
- Filtered (show only approved)
- Grouped (by priority)
- Sorted (by date)
- Different columns visible

---

### Testing the List

#### Add a Test Item
1. Click **New**
2. Fill in form:
   - **Title**: Large Monitor
   - **Description**: Mine is super old
   - **Requester**: Click people picker, select yourself
   - **Request Date**: Select today
   - **Priority**: Medium
   - **Estimated Cost**: 1225
3. Click **Save**

**Important Note About People Picker**:
- May load slowly sometimes
- Type name or email
- Wait for suggestions
- Select from dropdown
- Shows photo, name, email when selected

**Result**: New item appears in list view

---

## 12. Building the Device Request Automation Flow

### Flow Goal

**Objective**: When someone submits a device request to our SharePoint list, automate the following:

1. ✅ Send email receipt to requester
2. ✅ If expensive (over $200), get manager approval
3. ✅ If approved, update the list
4. ✅ Notify requester of decision

**Flow Type**: Automated Cloud Flow (triggered by SharePoint item creation)

---

### Creating the Flow

#### Step 1: Navigate to Create
Power Automate → **Create** → **Automated cloud flow**

#### Step 2: Name the Flow
**Flow name**: `New Device Request with Approval`

**Naming Best Practices**:
- Descriptive name
- Include trigger source (SharePoint, Forms, etc.)
- Include main action (approval, notification, etc.)
- Examples:
  - "New Device Request with Approval"
  - "Expense Report - Auto Approval"
  - "Form Submission to Teams"

#### Step 3: Choose Trigger
Search for: `SharePoint`

**Available SharePoint triggers**:
- When an item is created ✅ (We'll use this)
- When an item is created or modified
- When an item is deleted
- For a selected item (manual/instant)
- When a file is created
- Many others...

**Select**: "When an item is created"

**Why this trigger?**
- Matches our scenario: NEW requests
- Aligns with SharePoint terminology: "New item"
- Runs once per new item
- Simple and clear

Click **Create**

---

### Configuring the Trigger

Flow designer opens with trigger at top.

#### Click on Trigger Box
Left panel shows trigger settings.

#### Configure Trigger

**1. Site Address**
This is your SharePoint site URL.

**Dropdown shows**:
- Recently accessed sites
- Frequent sites
- "Enter custom value" option

**If your site doesn't appear**:
- Choose "Enter custom value"
- Paste site URL from browser
- Format: `https://yourcompany.sharepoint.com/sites/YourSite`

**For this example**: Select your teaching/test site

**2. List Name**
After selecting site, this dropdown populates with all lists on that site.

**Select**: Device Request (or your list name)

**If list doesn't appear**:
- Refresh browser
- Check you selected correct site
- Verify list exists
- Wait a moment (sometimes delayed)

**Trigger Configuration Complete** ✅

---

### Adding the Email Receipt Action

#### Step 1: Add Action
Below trigger, click **+ (plus icon)**
Click **Add an action**

#### Step 2: Search for Email
Type: `send an email`

#### Step 3: Choose Connector
**Options appear**:
- Mail (Power Automate) ⚠️ May be disabled for newer tenants
- Office 365 Outlook ✅ Recommended
- Outlook.com (personal accounts)
- Gmail (requires Gmail account)

**Select**: Office 365 Outlook

#### Step 4: Choose Action
**Send an email (V2)** ✅ Latest version

Click it.

---

### Configuring the Email

#### Field: To
**Goal**: Send to the person who made the request

**Steps**:
1. Click in "To" field
2. Click "Enter custom value"
3. Lightning bolt ⚡ appears
4. Click it

**Dynamic Content Available**:
From "When an item is created":
- ID (item ID number)
- Title
- Description
- Requester (person object)
- Request Date
- Priority
- Estimated Cost
- Approved
- Manager Comments
- And many system fields...

**Person Column Fields**:
When you have a Person column (like Requester), you get multiple properties:

**Click "See more"** or **search "requester"**:
- Requester
- Requester Claims
- Requester Department
- Requester Display Name
- **Requester Email** ✅ (This is what we need!)
- Requester Job Title
- Requester Picture

**Select**: Requester Email

**Result**: Green box inserted in "To" field

---

#### Field: Subject
Type: `Details about your device request`

Or make it dynamic:
```
Device Request Received - [Title]
```

To add Dynamic Content:
1. Type text: "Device Request Received - "
2. Click lightning bolt ⚡
3. Select "Title"
4. Result: `Device Request Received - Large Monitor`

---

#### Field: Body

**Email Structure**:
```
Hello [Requester Display Name],

Here are some details about your request:

Device: [Title]
Description: [Description]
Priority: [Priority Value]
Estimated Cost: [Estimated Cost]

We will get back to you as soon as we can.
```

**Building the Body**:

1. Type: "Hello "
2. Lightning bolt ⚡ → Select "Requester Display Name"
3. Type: "," and press Enter twice

4. Type: "Here are some details about your request:"
5. Press Enter twice

6. Type: "Device: "
7. Lightning bolt ⚡ → Select "Title"
8. Press Enter

9. Type: "Description: "
10. Lightning bolt ⚡ → Select "Description"
11. Press Enter

12. Type: "Priority: "
13. Lightning bolt ⚡ → Search "priority"
14. **Important**: Select "Priority Value" (not just "Priority")
    - "Priority" gives internal ID
    - "Priority Value" gives readable text (Critical, High, Medium, Low)
15. Press Enter

16. Type: "Estimated Cost: "
17. Lightning bolt ⚡ → Select "Estimated Cost"
18. Press Enter twice

19. Type: "We will get back to you as soon as we can."

**Why "Priority Value"?**
- Choice columns store both ID and display text
- Always use "Value" version for user-facing content
- Same applies to: Status Value, Category Value, etc.

---

### Formatting the Cost Field

**Current Issue**: Cost shows as `1225` (no formatting)

**Solution**: Format as currency

#### Steps:
1. In email body, find Estimated Cost Dynamic Content
2. Click the **X** to remove it
3. Click **fx** (Expression)
4. Type: `formatNumber(`
5. Click **Dynamic content** tab
6. Select "Estimated Cost"
7. Switch back to **Expression** tab
8. After the field reference, type: `, 'C2'`
9. Type: `)`
10. Click **Add**

**Complete expression**:
```
formatNumber(triggerOutputs()?['body/Estimated_x0020_Cost'], 'C2')
```

**Result**: Shows as `$1,225.00`

---

### Testing the Email Flow

#### Step 1: Save
Top-right: **Save**
Wait for confirmation.

#### Step 2: Test
Top-right: **Test**

#### Step 3: Choose Test Type
**Manual**: Perform trigger action yourself ✅
- We'll add a new item to test

Click **Test** button

#### Step 4: Trigger the Flow
**Screen shows**: Waiting for trigger...

**Go to SharePoint**:
1. Navigate to Device Request list
2. Click **New**
3. Fill form:
   - **Title**: New Computer
   - **Description**: Want a fast one
   - **Requester**: Your name
   - **Request Date**: Today
   - **Priority**: Critical
   - **Estimated Cost**: 2500
4. Click **Save**

#### Step 5: Watch Flow Run
Return to Power Automate

**Flow execution**:
- Trigger fires ✅
- Send email action runs ✅
- Green checkmarks appear
- "Flow ran successfully"

#### Step 6: Check Email
Open your inbox

**Email received**:
```
Subject: Details about your device request

Hello Jonathan Silven,

Here are some details about your request:

Device: New Computer
Description: Want a fast one
Priority: Critical
Estimated Cost: $2,500.00

We will get back to you as soon as we can.
```

**Success!** ✅ First part of automation working.

---

## 13. Conditional Logic

### Understanding Conditions

**What is a Condition?**
- An IF statement in your flow
- Evaluates data against criteria
- Creates two branches: True and False
- Only ONE branch executes per run

**When to Use Conditions**:
- Different actions based on data values
- Route flow based on criteria
- Make decisions dynamically
- Handle multiple scenarios in one flow

**Visual Structure**:
```
Condition: Is Cost > $200?
    ├── Yes (True branch)
    │   └── Get approval
    │   └── Check approval response
    │   └── Update list
    │
    └── No (False branch)
        └── Auto-approve
        └── Update list
```

---

### Adding a Condition

#### Step 1: Add Action After Email
Below "Send an email" step:
1. Click **+ (plus icon)**
2. Click **Add an action**

#### Step 2: Search for Condition
Type: `condition`

**Result**: Shows "Condition" control (not an action from a specific connector)

**Controls vs Actions**:
- **Controls**: Built-in flow logic (Condition, Loop, etc.)
- **Actions**: Connector-specific operations

**Select**: Condition (under "Control")

---

### Configuring the Condition

Condition box appears with three parts:
1. **Choose a value** (left box)
2. **Operator** (middle dropdown)
3. **Choose a value** (right box)

#### Our Logic: Check if Expensive
**Goal**: If Estimated Cost > $200, require approval

#### Left Box: Choose a Value
1. Click in left box
2. Lightning bolt ⚡ appears
3. Click it
4. Search: "cost"
5. Select: **Estimated Cost**

**Result**: Dynamic Content inserted

#### Middle: Operator
Click dropdown to see options:

**Available Operators**:
- is equal to
- is not equal to
- is greater than ✅ (We'll use this)
- is greater than or equal to
- is less than
- is less than or equal to
- contains
- does not contain
- starts with
- does not start with
- ends with
- does not end with

**Operator Selection Tips**:
- **Numbers**: Use >, <, >=, <=, =
- **Text**: Use contains, starts with, equals
- **Yes/No**: Use equals with true/false
- **Dates**: Use >, < for before/after

**Select**: "is greater than"

#### Right Box: Set Threshold
1. Click in right box
2. Type: `200`

**This is hardcoded** - the threshold value stays the same.

**Alternative**: Could use Dynamic Content if threshold is stored elsewhere (like a settings list)

**Final Condition**:
```
Estimated Cost  is greater than  200
```

---

### Understanding True and False Branches

Condition creates two sections below:

#### **If yes** (True branch)
- Executes when condition is TRUE
- In our case: When cost > $200
- Will contain approval process

#### **If no** (False branch)
- Executes when condition is FALSE
- In our case: When cost ≤ $200
- Will contain auto-approval

**Important**: Only ONE branch runs per execution
- Flow evaluates condition
- Goes down one path only
- Skips the other path completely

---

### Renaming the Condition (Best Practice)

**Why Rename?**
- Default name: "Condition" or "Condition 2"
- Not descriptive
- Confusing in complex flows
- Hard to troubleshoot

**How to Rename**:
1. Click on the condition box title
2. Edit mode activates
3. Type new name: `Check if over $200`
4. Click away or press Enter

**Best Practice Naming**:
- Describe what you're checking
- Be specific
- Examples:
  - "Check if over $200"
  - "Verify approval status"
  - "Is requester a manager?"
  - "Check if priority is critical"

**Benefits**:
- Future you will thank you
- Team members understand flow
- Easier debugging
- Professional documentation

---

## 14. Approval Flows

### Understanding Approvals in Power Automate

**What are Approvals?**
- Built-in approval process functionality
- Send approval requests
- Track responses
- Make decisions based on responses

**Types of Approval Actions**:

1. **Power Automate Approvals** (Internal only)
   - Uses Dataverse
   - Creates approval records
   - Respond in Teams, Email, Power Automate app
   - Full audit trail
   - Supports multi-stage approvals
   - **Limitation**: Requires internal Microsoft 365 users

2. **Send email with options** (Internal or External) ✅ We'll use this
   - Office 365 Outlook action
   - Simple email with buttons
   - No Dataverse required
   - Works with external users
   - Lightweight solution
   - **Perfect for**: Simple yes/no, approve/reject scenarios

---

### Why "Send email with options"?

**Advantages**:
- ✅ Works with external email addresses
- ✅ No premium licensing needed
- ✅ Doesn't create Dataverse tables
- ✅ Simpler setup
- ✅ Email-based (most universal)
- ✅ Standard connectors only

**Best Use Cases**:
- Simple approve/reject decisions
- External stakeholders
- Quick yes/no questions
- Situations where full approval infrastructure isn't needed

**When to Use Power Automate Approvals Instead**:
- Multi-stage approvals
- Need detailed approval history
- Want delegation features
- Complex approval routing
- Internal users only

---

### Getting the Manager Dynamically

**Scenario**: We want to send approval request to requester's manager

**Challenge**: Manager changes per requester - need to find dynamically

**Solution**: Office 365 Users connector → "Get manager (V2)" action

---

#### Adding "Get Manager" Action

**Location**: Inside "If yes" branch of our condition

1. In "If yes" section, click **Add an action**
2. Search: `get manager`
3. Select connector: **Office 365 Users**
4. Select action: **Get manager (V2)**

---

#### Configuring Get Manager

**Field: User (UPN)**
UPN = User Principal Name (essentially the email address)

1. Click in field
2. Lightning bolt ⚡
3. Search: "requester email"
4. Select: **Requester Email**

**What this does**:
- Takes requester's email
- Looks up in Azure Active Directory (Entra ID)
- Finds their direct manager
- Returns manager's information

**Important Requirements**:
✅ Requester must be internal Microsoft 365 user
✅ Manager must be set in Entra ID
✅ Organizational hierarchy must be configured

**If not configured**: Action will fail

---

#### Manager Information Retrieved

Once action runs, it provides outputs:

**Available Dynamic Content from Get Manager**:
- Display Name
- Given Name
- Mail (Email) ✅ We'll use this
- Job Title
- Department
- Office Location
- Mobile Phone
- Business Phones
- ID
- And more...

**We'll use**: Mail (manager's email address)

---

### Alternative: Hardcode Manager Email

**If organizational hierarchy isn't set up**, or **for testing**:

Instead of "Get manager" action:
1. Skip that step
2. In approval email, hardcode manager email
3. Type directly: `manager@company.com`

**For this tutorial**: Using hardcoded email (Devon Knight) for demonstration

---

### Adding "Send email with options" Action

#### Step 1: Add Action
After "Get manager" (or in "If yes" if skipping Get manager):
1. Click **Add an action**
2. Search: `send email with options`

#### Step 2: Select Action
Connector: **Office 365 Outlook**
Action: **Send email with options**

**Not to be confused with**:
- Send an email (V2) - No buttons
- Send an email from a shared mailbox - Different sender

---

### Configuring the Approval Email

#### Understanding the Parameters

When you click on "Send email with options", you may see many fields.

**Show/Hide Parameters**:
- Click **chevron (v)** dropdown next to any parameter
- Select **"Clear all"** to hide everything
- Then select dropdown again
- Check only the ones you need:
  - To ✅
  - Subject ✅
  - Header Text
  - Selection Text
  - Body ✅
  - User Options ✅

---

#### Field 1: To

**Who approves?**

**Option A**: Use manager's email (if Get manager action succeeded)
1. Lightning bolt ⚡
2. Under "Get manager", select: **Mail**

**Option B**: Hardcode for testing
1. Type email directly
2. Example: `devon.knight@pragmaticworks.com`

**For tutorial**: Using hardcoded (Devon's email)

---

#### Field 2: Subject
Describe what needs approval

Example:
```
New Device Request Waiting Your Approval
```

Or with Dynamic Content:
```
Device Request for [Title] - Approval Needed
```

To add Dynamic:
1. Type: "Device Request for "
2. Lightning bolt ⚡ → "Title"
3. Type: " - Approval Needed"

---

#### Field 3: Header Text
Optional - Appears at top of email card

Example:
```
Please review the details below
```

Leave blank if not needed.

---

#### Field 4: Selection Text
Optional - Header above the buttons

Example:
```
Make a selection
```

Or:
```
Do you approve this request?
```

---

#### Field 5: Body
Main email message content

**Best Practice**: Include all relevant information for decision-making

**Structure**:
```
Please review the details and make a selection to approve or reject:

Device: [Title]
Description: [Description]
Priority: [Priority Value]
Estimated Cost: [formatNumber(Estimated Cost, 'C2')]
Requester: [Requester Display Name]
```

**Building It**:
1. Type: "Please review the details and make a selection to approve or reject:"
2. Press Enter twice
3. Type: "Device: "
4. Lightning bolt ⚡ → "Title"
5. Press Enter

Continue pattern for each field.

**Pro Tip**: Copy from earlier email
- Highlight email body from "Send an email" step
- Ctrl+C (copy)
- Click in Body field of "Send email with options"
- Ctrl+V (paste)
- Modify as needed

---

#### Field 6: User Options ⭐ CRITICAL

**This defines the buttons**

**Format**: Comma-separated list of button labels

**Examples**:
```
Approve, Reject
```
```
Yes, No
```
```
Accept, Decline, Need More Info
```

**For our flow**:
```
Approve, Reject
```

**Important Notes**:
- Exact spelling matters (case-sensitive)
- No extra spaces (unless intentional)
- You'll reference these exact words later
- Can have 2+ options
- User sees them as buttons

**Result**: Email will have two buttons: "Approve" and "Reject"

---

### How the Approval Email Works

#### What the Approver Sees

**Email arrives** with:
- Subject line
- Header text (if provided)
- Body with all details
- Two sets of identical buttons (design choice by Microsoft)
- Selection text above buttons

**Approver Actions**:
1. Reviews information
2. Clicks **Approve** or **Reject**
3. Optional: Can add comments (if configured)
4. Selection is recorded

**Response is Immediate**:
- No need to open Power Automate
- No need to go to SharePoint
- Just click button in email
- Flow continues automatically

---

### Capturing the Approval Response

**After sending approval email, we MUST check the response**

**Why?**
- Need to know: Did they approve or reject?
- Different actions based on response
- Update records accordingly

**How?**
Use another **Condition** control

---

### Adding Condition After Approval

#### Step 1: Add Action
Below "Send email with options":
1. Click **+ plus icon**
2. **Add an action**
3. Search: `condition`
4. Select: **Condition** (Control)

#### Step 2: Rename Condition
Click on title, change to:
```
Check manager selection
```

---

### Configuring Approval Response Condition

#### Left Box: Selected Option

1. Click in left box
2. Lightning bolt ⚡
3. Look under "Send email with options"
4. Find: **SelectedOption**
5. Click it

**SelectedOption Dynamic Content**:
- Contains the exact button text clicked
- "Approve" or "Reject" (in our case)
- Exactly as spelled in User Options

---

#### Middle: Operator

Select: **is equal to**

**Why "is equal to"?**
- Exact match required
- Case-sensitive
- Must match User Options spelling exactly

---

#### Right Box: Expected Value

Type: `Approve`

**Critical**: Must match EXACTLY what's in User Options
- Same capitalization
- Same spelling
- No extra spaces

**Final Condition**:
```
SelectedOption  is equal to  Approve
```

**Logic**:
- **If yes** (True): They clicked Approve
- **If no** (False): They clicked Reject (or anything else)

---

### Best Practice: Keep It in the Affirmative

**Better to check FOR approval than AGAINST rejection**

**Good** ✅:
```
If SelectedOption equals "Approve"
    Then: Update as approved
    Else: Update as rejected
```

**Avoid** ❌:
```
If SelectedOption equals "Reject"
    Then: Update as rejected
    Else: Update as approved
```

**Why?**
- Clearer logic
- Easier to understand
- Better for team collaboration
- Fewer logic errors

---

## 15. Updating SharePoint Based on Approval

### The Goal

After approval decision:
- **If Approved**: Update SharePoint item
  - Set "Approved" column to Yes
  - Add manager comments
  - Notify requester

- **If Rejected**: Update SharePoint item
  - Set "Approved" column to No
  - Add manager comments
  - Notify requester

---

### Adding Update Item Action (Approved Branch)

#### Step 1: Add Action in True Branch
In "If yes" of "Check manager selection" condition:
1. Click **Add an action**
2. Search: `sharepoint update`
3. Select connector: **SharePoint**
4. Select action: **Update item**

---

#### Configuring Update Item

**Field 1: Site Address**
Same as trigger - select your SharePoint site

**Field 2: List Name**
Same as trigger - select: **Device Request**

**Field 3: Id** ⭐ CRITICAL

**This tells SharePoint WHICH item to update**

1. Click in Id field
2. Lightning bolt ⚡
3. Under "When an item is created" (the trigger)
4. Select: **ID**

**Why from the trigger?**
- ID is the unique identifier
- Created when item was first added
- Stays the same throughout flow
- Ensures we update the correct item

**What if you don't add ID?**
- Flow will fail
- Error: "Cannot update item without ID"
- Or updates wrong item (dangerous!)

---

**Field 4: Show Advanced Options**

After selecting ID, additional parameters may appear:

Click **"Show advanced options"** or dropdown to see all list columns:
- Title
- Description
- Requester
- Request Date
- Priority
- Estimated Cost
- **Approved** ✅ We'll set this
- **Manager Comments** ✅ We'll set this

**You only need to fill in fields you want to UPDATE**

---

**Setting Approved Field**:

**Field: Approved**

This is a Yes/No (Boolean) field.

**Dropdown options**:
- Yes
- No
- Ask in Power Apps
- Expression
- Dynamic Content

**Select**: **Yes**

**Result**: Sets Approved column to Yes (checked) in SharePoint

---

**Setting Manager Comments Field**:

**Field: Manager Comments**

**Options**:
1. **Hardcode a message**:
   ```
   Approved by manager on [today's date]
   ```

2. **Use Dynamic Content**:
   - If using Power Automate Approvals connector, you get response comments
   - With Email options, no comments field available
   - Can still add dynamic data

3. **Hybrid Approach** ✅ Best:
   ```
   Approved by [Manager Name] on [today]
   ```

**Building Hybrid Comment**:

1. Type: "Approved by "
2. Lightning bolt ⚡
3. Under "Get manager" (if you used it)
4. Select: **Display Name**
5. Type: " on "
6. Lightning bolt ⚡
7. Under "When an item is created"
8. Select: **Created** (or use expression for today's date)

**Alternative without Get Manager**:
```
Approved by Devon Knight on [Created date]
```

Or simply:
```
Request approved
```

---

#### Testing Update Action

**Don't test full flow yet** - we'll add more first.

But conceptually, when this runs:
1. SharePoint item gets updated
2. Approved column changes to Yes
3. Manager Comments populated
4. Item shows in list with updates

---

### Handling the Rejection Path

In "If no" branch (when they clicked Reject):

**Option 1**: Add complete "Update item" manually
- Same steps as approved
- Change Approved to **No**
- Change comments to **"Request rejected"**

**Option 2**: Copy/Paste ✅ Faster

---

#### Using Copy/Paste for Similar Actions

**New Designer Feature**: Right-click to copy actions

#### Steps:
1. In "If yes" branch, find "Update item" action
2. **Right-click** on it (or Ctrl+C)
3. Select **Copy action**
4. Navigate to "If no" branch
5. Click **Add an action**
6. **Right-click** (or Ctrl+V)
7. Select **Paste action**

**Result**: Exact copy of Update item appears in False branch

---

#### Modifying the Copied Action

Now customize for rejection:

1. Click on the copied "Update item"
2. Rename: "Update item - Rejected" (or similar)
3. Site Address: Already correct ✅
4. List Name: Already correct ✅
5. ID: Already correct ✅
6. **Approved**: Change to **No**
7. **Manager Comments**: Change to:
   ```
   Request rejected
   ```
   or
   ```
   Rejected by [Manager Name]
   ```

---

### Adding Notification Emails

**Next Step**: Notify requester of decision

**In True Branch** (Approved):
- Send email: "Your request was approved"

**In False Branch** (Rejected):
- Send email: "Your request was rejected"

---

#### Adding Email in True Branch

After "Update item" in "If yes":

1. **Add an action**
2. Search: `send an email`
3. **Office 365 Outlook** → **Send an email (V2)**

**Configure**:
- **To**: Requester Email (Dynamic Content)
- **Subject**: `Your request was approved`
- **Body**:
  ```
  Hello [Requester Display Name],
  
  Good news! Your request for [Title] has been approved.
  
  Estimated Cost: [formatNumber Estimated Cost, 'C2']
  
  We'll be in touch soon to complete the order.
  ```

---

#### Copy/Paste Email to False Branch

1. Right-click "Send an email" in True branch
2. **Copy action**
3. Go to False branch ("If no")
4. **Add an action**
5. **Paste action**

**Modify for rejection**:
- **Subject**: `Your request was not approved`
- **Body**:
  ```
  Hello [Requester Display Name],
  
  Unfortunately, your request for [Title] was not approved at this time.
  
  If you have questions, please contact your manager.
  ```

---

### Handling Requests Under $200

**Remember**: We have two condition branches at the TOP level:
1. **If yes** (over $200): All the approval logic we just built
2. **If no** (≤$200): Auto-approve

---

#### Auto-Approval Path

In the "If no" branch of our FIRST condition ("Check if over $200"):

**Goal**: Automatically approve without manager involvement

1. **Add an action**
2. Search: `sharepoint update`
3. **SharePoint** → **Update item**

**Configure**:
- **Site Address**: Your site
- **List Name**: Device Request
- **ID**: ID (from trigger)
- **Approved**: **Yes**
- **Manager Comments**:
  ```
  Automatically approved - under $200 threshold
  ```

---

#### Notify Requester of Auto-Approval

After the auto-approve update:

1. **Add an action**
2. **Office 365 Outlook** → **Send an email (V2)**

**Or**: Copy from True branch and modify

**Configure**:
- **To**: Requester Email
- **Subject**: `Your request was automatically approved`
- **Body**:
  ```
  Hello [Requester Display Name],
  
  Your request for [Title] has been automatically approved.
  
  Estimated Cost: [formatNumber Estimated Cost, 'C2']
  
  Your device will be ordered shortly.
  ```

---

### Complete Flow Structure

```
Trigger: When an item is created (SharePoint)
  ↓
Action: Send email (receipt to requester)
  ↓
Condition: Check if over $200
  ├── Yes (>$200)
  │   ├── Get manager
  │   ├── Send email with options (approval request)
  │   └── Condition: Check manager selection
  │       ├── Yes (Approved)
  │       │   ├── Update item (Approved = Yes)
  │       │   └── Send email (approval notification)
  │       └── No (Rejected)
  │           ├── Update item (Approved = No)
  │           └── Send email (rejection notification)
  │
  └── No (≤$200)
      ├── Update item (Auto-approved)
      └── Send email (auto-approval notification)
```

---

## 16. Testing the Complete Flow

### Save the Flow

Top-right: **Save**

Wait for "Your flow is ready to go" message

---

### Test with Manual Trigger

**Test**: Top-right

**Choose**: Manually (Perform trigger action)

**Test**

Screen: "Waiting for trigger..."

---

### Create Test Request (Over $200)

Go to SharePoint → Device Request list

**New item**:
- **Title**: New Computer
- **Description**: Want a fast one
- **Requester**: Your name
- **Request Date**: Today
- **Priority**: Critical
- **Estimated Cost**: **2500** (over $200)
- **Save**

---

### Watch Flow Execute

Return to Power Automate

**Flow runs**:
1. ✅ When an item is created
2. ✅ Send an email (receipt)
3. ✅ Condition: Check if over $200 (TRUE - goes to Yes branch)
4. ✅ Get manager (finds manager info)
5. ✅ Send email with options (approval sent)
6. ⏳ Waiting for response...

---

### Approve the Request

**Approver (Devon in this case)**:
- Receives email
- Sees device details
- Clicks **Approve** button

---

### Flow Continues

After approval clicked:

5. ✅ Send email with options (response received)
6. ✅ Condition: Check manager selection (TRUE - Approve)
7. ✅ Update item (Approved = Yes, comments added)
8. ✅ Send an email (requester notified of approval)

**All green checkmarks** ✅

---

### Verify Results

#### Check Email Inbox
**Should have received**:
1. Initial receipt email
2. Approval notification email

#### Check SharePoint List
Go to Device Request list

**Item should show**:
- **Approved**: Yes ✅
- **Manager Comments**: "Approved by Devon Knight" (or your text)

---

### Test Rejection Path

1. Create new item with cost over $200
2. When approval email arrives
3. Click **Reject** button
4. Flow updates item to **Approved: No**
5. Requester gets rejection email

---

### Test Auto-Approval (Under $200)

1. Create new item
2. **Estimated Cost**: **150** (under $200)
3. **Save**

**Flow should**:
- Send receipt email
- Check condition (FALSE - goes to No branch)
- Auto-update to Approved: Yes
- Send auto-approval email
- **Skip entire approval process**

---

## 17. HTML Tables & Email Reports

### The Scenario

**Goal**: Every Monday morning, send an email with ALL device requests in a formatted table

**Why?**
- Weekly review of requests
- Track what's been approved/rejected
- See all requests at once
- Easy to scan in email

---

### The Problem with Multiple Records

**If you try to send an email with multiple SharePoint items**:

```
Get items (returns 20 items)
  ↓
Send an email with [Title]
```

**What happens**:
- Power Automate automatically creates "Apply to each" loop
- Sends 20 separate emails (one per item)
- Inbox flooded ❌
- Not user-friendly

**We want**: ONE email with ALL items in a table

---

### The Solution: HTML Table

**HTML Table**:
- Data operation that converts array/list into HTML table
- Can be embedded in email body
- Shows all records at once
- Can be styled with CSS

---

### Creating the Scheduled Flow

#### Step 1: New Flow
Power Automate → **Create** → **Scheduled cloud flow**

#### Step 2: Configure Schedule
**Flow name**: `Weekly Device Request Report`

**Starting**:
- Date: Tomorrow (or next Monday)
- Time: 10:00 AM
- Timezone: Your timezone (auto-detected or select)

**Repeat every**:
- Interval: **1**
- Frequency: **Week**
- On these days: **Monday** ✅

**Create**

---

### Understanding Recurrence Trigger

**Trigger created**: Recurrence

**Configuration visible**:
- Interval: 1
- Frequency: Week
- Time Zone: Eastern Time (or your zone)
- On these days: Monday
- At these hours: 10
- At these minutes: 0

**Can modify**:
- Click on trigger to change
- Add multiple days (Monday, Wednesday, Friday)
- Change time
- Change frequency

---

### Getting All SharePoint Items

#### Step 1: Add Action
Below Recurrence: **Add an action**

#### Step 2: Search
Type: `sharepoint get items`

**SharePoint** → **Get items**

**Not**:
- Get item (singular) - Gets one specific item by ID
- Get items (plural) ✅ - Gets multiple/all items

---

#### Configuring Get Items

**Site Address**: Your SharePoint site

**List Name**: Device Request

**Optional**: Filter Query, Top Count, etc.

**For now**: Leave optional fields blank (gets ALL items)

---

**Advanced Options** (Optional):

**Filter Query** (OData):
- Get only approved: `Approved eq true`
- Get only pending: `Approved eq false`
- Get only critical: `Priority eq 'Critical'`
- Future dates: `Request_x0020_Date gt '[today]'`

**Top Count**:
- Limit results (e.g., 10 most recent)

**Order By**:
- Sort results
- Example: `Request_x0020_Date desc` (newest first)

**For tutorial**: No filters - get everything

---

### Creating HTML Table

#### Step 1: Add Action
After "Get items": **Add an action**

#### Step 2: Search
Type: `html table`

**Data Operations** → **Create HTML table**

**Important**: NOT under a specific connector - it's a built-in Data Operation

---

#### Configuring Create HTML Table

**Field: From**

This is the array/list of items to convert.

1. Click in "From" field
2. Lightning bolt ⚡
3. Under "Get items"
4. Select: **value**

**"value" is**:
- The array of all items returned
- All rows from SharePoint list
- The complete dataset

---

**Field: Columns** (Optional)

**Default**: Automatic
- Includes ALL columns from SharePoint
- System columns too (Created, Modified, ID, etc.)
- Can be messy

**Custom**: ✅ Recommended
- Choose which columns to include
- Set custom headers
- Control order

**To customize**:
1. Click **"Switch to input entire array"** (changes mode)

   **Wait, that's not what we want!**

2. If that appears, click it again to get back

**Actually**:
1. Toggle should say "Automatic" or "Custom"
2. Click to switch to **"Custom"**

---

**Adding Custom Columns**:

When in Custom mode:
- **Header** column
- **Value** column
- Add rows for each field you want

**Click: + Add new** (or similar)

**First Column**:
- **Header**: `Device` (what user sees)
- **Value**: Lightning bolt ⚡ → **Title**

**Second Column**:
- **Header**: `Description`
- **Value**: Lightning bolt ⚡ → **Description**

**Third Column**:
- **Header**: `Requester`
- **Value**: Lightning bolt ⚡ → **Requester Display Name** (not Email)

**Fourth Column**:
- **Header**: `Priority`
- **Value**: Lightning bolt ⚡ → **Priority Value**

**Fifth Column** (Optional):
- **Header**: `Cost`
- **Value**: Lightning bolt ⚡ → **Estimated Cost**
  - Or use formatNumber expression

**Sixth Column** (Optional):
- **Header**: `Approved?`
- **Value**: Lightning bolt ⚡ → **Approved**

**Continue as needed**

---

### Styling the HTML Table (Optional but Recommended)

**Problem**: Default HTML table is plain text
- No borders
- No background colors
- Hard to read
- Unprofessional

**Solution**: Add CSS styling with Compose action

---

#### Adding Compose Action

After "Create HTML table":

1. **Add an action**
2. Search: `compose`
3. **Data Operations** → **Compose**

**What is Compose?**
- Simple action
- Takes inputs
- Generates outputs
- Like a text box or variable
- Great for building content

---

#### Adding CSS Styling

In **Inputs** field of Compose:

**Paste this CSS** (provided in course files):

```html
<style>
table {
  border-collapse: collapse;
  width: 100%;
  font-family: Arial, sans-serif;
}

th {
  background-color: #0078D4;
  color: white;
  padding: 12px;
  text-align: left;
  border: 1px solid #ddd;
}

td {
  padding: 10px;
  border: 1px solid #ddd;
  text-align: left;
}

tr:nth-child(even) {
  background-color: #f2f2f2;
}

tr:hover {
  background-color: #e6f2ff;
}
</style>
```

**After the `</style>` tag**, add Dynamic Content:

1. Click after closing `</style>`
2. Lightning bolt ⚡
3. Under "Create HTML table"
4. Select: **Output**

**Complete Inputs**:
```html
<style>
  /* All the CSS above */
</style>
[Output from Create HTML table]
```

---

**What This Does**:
- `<style>` tag contains CSS
- CSS formats the table:
  - Blue header background (#0078D4 - Microsoft blue)
  - White text in header
  - Borders around cells
  - Alternating row colors (zebra striping)
  - Hover effect (row highlights)
  - Full width
  - Arial font
- Then includes the actual table HTML

**Customization**:
- Change colors (hex codes)
- Modify width (100%, 75%, etc.)
- Change fonts
- Adjust padding
- Add more styling

---

### Sending the Table in Email

#### Add Email Action
After Compose:

1. **Add an action**
2. **Office 365 Outlook** → **Send an email (V2)**

#### Configure Email

**To**: Your email (or manager, team distribution list)

**Subject**:
```
Weekly Device Request Summary
```

Or with date:
```
Device Requests for Week of [Monday's date]
```

**Body**:
Type introductory text:
```
Please review all device requests below:

[TABLE HERE]
```

**For [TABLE HERE]**:
1. Place cursor there
2. Lightning bolt ⚡
3. Under "Compose"
4. Select: **Outputs**

**Complete Body**:
```
Please review all device requests below:

[Styled HTML table will appear here]

Let me know if you have questions.
```

---

### Testing the Report Flow

#### Save
Top-right: **Save**

#### Test
**Test** → **Manually** → **Test**

**Or**: **Automatically** (if you have a previous run)

**Flow executes**:
1. ✅ Recurrence (triggers)
2. ✅ Get items (retrieves all requests)
3. ✅ Create HTML table (converts to table)
4. ✅ Compose (adds styling)
5. ✅ Send an email (sends table)

---

### Check Email Result

**Email received**:
- **Subject**: Weekly Device Request Summary
- **Body**: 
  - Intro text
  - **Beautifully formatted table**:
    - Blue header row
    - White text in headers
    - All columns you selected
    - Alternating row colors
    - Borders
    - Professional appearance

**Table Contents**:
All items from SharePoint list in one table

**Responsive**:
- Width adjusts to window
- Can scroll if needed

---

### Advanced: Filtering the Table

**Want only certain items?**

In **"Get items"** action:

**Filter Query Examples**:

**Only approved requests**:
```
Approved eq true
```

**Only pending (not approved)**:
```
Approved eq false
```

**Only critical priority**:
```
Priority eq 'Critical'
```

**Cost over $1000**:
```
Estimated_x0020_Cost gt 1000
```

**Requests from last 7 days**:
```
Request_x0020_Date ge '[utcNow('yyyy-MM-dd')]'
```

**Combine filters (AND)**:
```
Approved eq true and Priority eq 'Critical'
```

**Resources**:
- Jonathan has a YouTube video on OData filtering
- Search: "Power Automate OData filter query"

---

## 18. Best Practices & Tips

### Flow Organization

**1. Rename Steps**
- Always rename conditions, actions
- Be descriptive
- Future you will thank you

**2. Add Comments**
- Describe complex logic
- Document why you did something
- Right-click → "Add a note"

**3. Group Related Actions**
- Use Scope control to group actions
- Collapse/expand for better view
- Easier troubleshooting

---

### Testing Strategy

**1. Test Level-by-Level**
- Don't build entire flow then test
- Test after each major section
- Easier to find errors

**2. Use Automatic Testing**
- After first successful run
- Saves time during development
- No need to retrigger each time

**3. Check Each Output**
- Click on successful actions
- View outputs/inputs tabs
- Verify data is correct
- Learn what's available

---

### Error Handling

**1. Configure Run After**
- Right-click action → "Configure run after"
- Choose: "has failed", "is skipped", "has timed out"
- Create error handling paths

**2. Use Try-Catch Pattern**
- Scope for try
- Scope for catch
- Configure run after

**3. Send Error Notifications**
- Email yourself when flow fails
- Include error details
- Easier to troubleshoot

---

### Performance Tips

**1. Limit Get Items**
- Use "Top Count" to limit results
- Filter to only what you need
- Reduces processing time

**2. Avoid Infinite Loops**
- Be careful with "When modified" triggers
- Don't update the same item that triggered the flow
- Use conditions to prevent loops

**3. Use Select Action**
- Transform arrays efficiently
- Choose only needed columns
- Reduces data passed through flow

---

### Security Considerations

**1. Manage Connections**
- Know which account is used
- Don't share sensitive flows with personal connections
- Use service accounts for production

**2. Limit Access**
- Share flows only with necessary people
- Review permissions regularly
- Remove access when no longer needed

**3. Protect Sensitive Data**
- Don't hardcode passwords
- Use Azure Key Vault for secrets
- Be careful with external connectors

---

### Documentation

**1. Name Flows Clearly**
- Include trigger source
- Include main purpose
- Examples:
  - "SharePoint Device Request - Approval Flow"
  - "Forms Submission - Auto Email"

**2. Add Descriptions**
- Flow description field
- Explain purpose
- Include owner contact info

**3. Document Complex Logic**
- Use comments/notes
- Create flow diagrams
- Keep external documentation

---

### Version Control

**1. Export Flows**
- Download as .zip
- Store in version control
- Backup important flows

**2. Use Solutions** (Advanced)
- Package flows together
- Move between environments
- Better for ALM (Application Lifecycle Management)

**3. Track Changes**
- Note what changed in flow description
- Keep change log
- Easier to troubleshoot issues

---

### Monitoring & Maintenance

**1. Review Run History**
- Check for failures regularly
- Identify patterns
- Fix recurring issues

**2. Set Up Alerts**
- Email on failure
- Monitor critical flows
- Proactive vs reactive

**3. Regular Reviews**
- Quarterly review of all flows
- Remove unused flows
- Update deprecated actions
- Check for better methods

---

### Common Mistakes to Avoid

**1. Not Testing Thoroughly**
- Test all branches
- Test with different data
- Test edge cases

**2. Hardcoding Too Much**
- Use Dynamic Content
- Use variables/compose for reusable values
- Makes flows flexible

**3. Creating Overly Complex Flows**
- Break into multiple flows if needed
- Use child flows
- Keep it simple

**4. Ignoring Limits**
- API call limits
- Timeout limits (30 seconds for instant flows)
- Connector limits

**5. Not Planning for Errors**
- Assume things will fail
- Add error handling
- Graceful degradation

---

## 19. Additional Resources

### Pragmatic Works Offerings

**1. On-Demand Learning**
- Subscription: $39/month
- 100s of courses
- Power Automate, Power Apps, Power BI, Fabric, etc.
- All Learn with the Nerds recordings
- **Free Power Automate courses this weekend!**

**2. Cert XP**
- Certification exam prep
- PL-900 (Power Platform Fundamentals)
- PL-200 (Power Platform Functional Consultant)
- PL-400 (Power Platform Developer)
- Gamified learning
- Quick Coach video explanations

**3. Boot Camps**
- Multi-day intensive training
- Public or private
- Virtual or on-site
- Power Automate boot camp available
- Other Power Platform topics

**4. Virtual Mentoring**
- 1-on-1 support
- 30 min to 2 hours
- Your specific problems
- Guided learning

**5. Hackathons**
- 1-day intensive
- Your data, your scenario
- Build real solutions
- Expert guidance

**6. Season Learning Pass**
- Annual subscription
- Unlimited boot camps
- Virtual mentoring hours
- All on-demand content
- Cert XP access
- Private Teams channel
- Learning advisor

---

### YouTube Resources

**Pragmatic Works YouTube Channel**:
- Free tutorials
- Learn with the Nerds series
- Product demos
- Tips and tricks

**Recommended Videos**:
- Power Automate Desktop (previous Learn with the Nerds)
- OData Filter Queries (Jonathan Silven)
- Send Email on Behalf Of (Devon Knight)
- Power Platform best practices

---

### Microsoft Resources

**Power Automate Documentation**
**Power Automate Documentation**: - docs.microsoft.com/power-automate - Official documentation - Connector reference - Expression reference - Best practices **Power Platform Community**: - powerusers.microsoft.com - Forums - User groups - Community calls **Microsoft Learn**: - Free learning paths - Hands-on labs - Certifications --- ### Upcoming Events **Intergalactic Learn with the Nerds Day** - **Date**: June 20, 2026 - **Duration**: Full day (8 sessions) - **Topics**: - Power Platform certifications - Copilot in Power BI - Women in Technology panel - Hot wing challenge - And more! - **Access**: 24-hour free access to ALL On-Demand content - **Register**: Use QR code (shown in session)

