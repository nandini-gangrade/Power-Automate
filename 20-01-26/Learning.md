# [YOUTUBE](https://www.youtube.com/watch?v=KsgxDz-nY_I&t=2s)

## What is Power Automate?

**Simple Answer**: 
Power Automate is like having a robot assistant that does boring, repetitive computer tasks for you automatically, so you can focus on more important work.

**Real-Life Example**:
Imagine you work in an office and every time someone fills out a request form, you have to:
1. Read the form
2. Send them a confirmation email
3. Check if it needs approval
4. Send it to your manager
5. Update a spreadsheet
6. Send another email when it's approved

Instead of doing this 20 times a day, Power Automate does ALL of it automatically - even while you're sleeping!

---

## Where Does Power Automate Live?

### The Power Platform Family (5 Tools)
Think of Microsoft's Power Platform like a toolbox with 5 different tools:

1. **Power BI** = Creates charts and reports from data (like making a colorful graph)
2. **Power Apps** = Builds custom mobile/web apps (like creating your own iPhone app)
3. **Power Automate** = Automates workflows (our focus - the robot assistant)
4. **Co-pilot Studio** = Builds chatbots (like customer service robots)
5. **Power Pages** = Creates websites (like building a company website)

**Power Automate is in the CENTER** - it connects all of them together!

### Two Types of Power Automate

#### Type 1: Power Automate Cloud (What We Learned)
- **Where**: Website (make.powerautomate.com) - works in browser
- **What it does**: Connects to cloud services (email, SharePoint, Teams, Forms)
- **Like**: Using Gmail or Facebook - everything is online
- **Example**: When email arrives, automatically save attachment to OneDrive

#### Type 2: Power Automate Desktop (Not Covered)
- **Where**: Software on your computer
- **What it does**: Controls things on your computer screen
- **Like**: Recording yourself clicking buttons, then replaying it
- **Example**: Opening Excel, copying data, pasting into another program

---

## The Three Types of Flows (The 3 Ways to Start Automation)

Think of these as three different alarm clocks:

### 1. Automated Flow = Motion Sensor Light
- **Trigger**: Something happens automatically
- **Real Examples**:
  - When email arrives → Do something
  - When file uploaded → Do something  
  - When form submitted → Do something
  - When message posted in Teams → Do something

**Story Example**: 
"Like a motion sensor light - you walk in the room (trigger happens), light turns on automatically (flow runs). You don't press any button!"

### 2. Instant Flow = Light Switch
- **Trigger**: YOU press a button
- **Real Examples**:
  - Press button on phone → Send my location to family
  - Click button in Teams → Generate report
  - Press button in app → Submit expense report

**Story Example**:
"Like a light switch - YOU decide when to flip it. The light doesn't turn on by itself."

### 3. Scheduled Flow = Timer Light
- **Trigger**: Runs on a schedule you set
- **Real Examples**:
  - Every Monday at 9 AM → Send weekly report
  - Every hour → Check for new data
  - Every day at 5 PM → Backup files

**Story Example**:
"Like a timer that turns your porch light on at 7 PM every night. It knows the schedule and does it automatically."

---

## Key Concepts Explained Simply

### Dynamic Content (The Magic Copy-Paste)

**What it is**: Information from one step that you can use in later steps

**Simple Analogy**:
Think of it like a form letter:
- Original: "Dear [NAME], thank you for ordering [PRODUCT]"
- Dynamic: "Dear **John**, thank you for ordering **blue shoes**"
- Dynamic: "Dear **Sarah**, thank you for ordering **red hat**"

The [NAME] and [PRODUCT] are "dynamic content" - they change automatically based on who submitted!

**In Power Automate**:
- Someone submits form with their email: **john@email.com**
- You can reuse that email in:
  - Send email TO: **john@email.com** (dynamic!)
  - Email body: "Hello **john@email.com**" (dynamic!)
  - Subject: "Thanks **john@email.com**" (dynamic!)

**How to spot it**: Little green boxes with lightning bolt ⚡

---

### Connectors (The Bridges)

**What they are**: Connections between Power Automate and other apps

**Simple Analogy**:
Like electrical outlets:
- Your phone charger (Power Automate) needs to plug into the wall (Gmail, SharePoint, Teams)
- The outlet is the "connector"
- Once plugged in, electricity (data) can flow

**Examples**:
- **SharePoint connector** = Can read/write to SharePoint lists
- **Outlook connector** = Can send/receive emails  
- **Forms connector** = Can get form responses
- **Teams connector** = Can post messages

**Two Types**:
1. **Standard** = Free with Microsoft 365 (what we used)
2. **Premium** = Need special license (more expensive tools)

---

### Conditions (The Decision Maker)

**What it is**: IF-THEN-ELSE logic (like a fork in the road)

**Simple Analogy**:
```
IF it's raining
  THEN bring umbrella
ELSE
  Don't bring umbrella
```

**Power Automate Example**:
```
IF request costs more than $200
  THEN send to manager for approval
ELSE  
  Automatically approve it
```

**Visual**: 
- Looks like a diamond with two paths
- Left path = TRUE (yes, condition met)
- Right path = FALSE (no, condition not met)
- **Only ONE path runs** - never both!

---

## The Two Real Examples We Built

### Example 1: Microsoft Forms Auto-Reply

**The Problem**: 
Someone fills out a meeting request form, but they don't get confirmation. They wonder "Did it work?"

**The Solution We Built**:
1. **WHEN** someone submits form (TRIGGER - Automated)
2. **GET** their answers from the form
3. **SEND** them email with:
   - "Hello [their name]"
   - "Here are your meeting details:"
   - Date you picked: [date they chose]
   - Topic: [topic they wrote]
   - Description: [description they wrote]

**What They Learned**:
- ✅ This is like an automatic receipt at a store
- ✅ The person gets confirmation immediately (even at 2 AM!)
- ✅ You don't have to manually send 50 emails
- ✅ Used Dynamic Content (their name, their choices)
- ✅ Formatted the date to look nice (Jan 20, 2026 instead of 2026-01-20)

**If Someone Asks You**: 
"I learned how to make a form that automatically emails people their submission as a receipt, like when you buy something online and get a confirmation email."

---

### Example 2: Device Request Approval Workflow

**The Problem**: 
Employees need new equipment (laptop, monitor). Someone has to:
- Track all requests manually
- Email employee "we got it"
- Decide if it needs approval
- Ask manager if expensive
- Update the tracking list
- Tell employee the decision

This could take hours every week!

**The Solution We Built**:

#### Step 1: Someone Requests Device
- They fill out SharePoint list (like Excel online)
- Enter: Device name, description, cost, date needed

#### Step 2: Automatic Email Receipt
- **IMMEDIATELY** they get email: "We received your request for [device name]"
- Shows all their details

#### Step 3: Check if Expensive
- **IF** cost > $200
  - Go to Step 4 (get approval)
- **ELSE** (cost ≤ $200)
  - Automatically approve
  - Update list: "Auto-approved"
  - Email person: "Approved!"

#### Step 4: Get Manager (Only if Expensive)
- Power Automate **automatically finds their manager** (magic!)
- No need to type manager's email - it looks it up!

#### Step 5: Send Approval Email to Manager
- Manager gets email with buttons:
  - **[Approve]** **[Reject]**
- Email shows all request details

#### Step 6: Manager Clicks Button
- Manager clicks **Approve** or **Reject**
- That's it! Just one click.

#### Step 7: Check Manager's Decision
- **IF** manager clicked "Approve"
  - Update SharePoint: "Approved by [manager name] on [today's date]"
  - Email employee: "Good news! Approved!"
- **ELSE** (clicked "Reject")  
  - Email employee: "Sorry, not approved"

**What They Learned**:
- ✅ Entire process runs automatically (could be 3 AM Sunday!)
- ✅ Multiple conditions (IF expensive, IF approved)
- ✅ Dynamic manager lookup (don't need to know who manager is)
- ✅ Email with clickable buttons
- ✅ Updates SharePoint list automatically
- ✅ Formatted currency ($1,225.00 instead of 1225)

**If Someone Asks You**:
"I learned how to build an approval system where employees request equipment, it automatically emails them confirmation, finds their manager if it's expensive, sends the manager an email with approve/reject buttons, and then updates everything automatically based on what the manager clicks."

---

### Example 3: Weekly Summary Email (HTML Table)

**The Problem**:
You have 50 device requests in SharePoint. You want to email your boss every Monday with a nice table showing all of them. Doing this manually = copy/paste nightmare!

**The Solution We Built**:

#### Step 1: Schedule (Every Monday 10 AM)
- Trigger: Recurrence (Scheduled flow)

#### Step 2: Get All Requests from SharePoint
- Grabs all 50 rows

#### Step 3: Create HTML Table
- Converts 50 rows into a nice table
- Choose which columns to show:
  - Device Name
  - Requester  
  - Description
  - Cost

#### Step 4: Style the Table (Make it Pretty)
- Add company colors
- Add borders
- Make headers bold
- This is like adding formatting in Word

#### Step 5: Send Email
- ONE email with beautiful table
- Shows all 50 requests in organized way

**What They Learned**:
- ✅ WITHOUT Power Automate: Would send 50 separate emails (disaster!)
- ✅ WITH Power Automate: One email with nice table
- ✅ Runs every Monday automatically
- ✅ Can customize colors/fonts (company branding)
- ✅ Professional looking

**If Someone Asks You**:
"I learned how to create a scheduled report that runs every Monday, gets all records from a SharePoint list, puts them in a nicely formatted table with company colors, and emails it automatically. Instead of getting 50 separate emails, you get one clean summary."

---

## Important Concepts (Deep Dive for Questions)

### Q: "What's the difference between Trigger and Action?"

**Trigger** = The STARTING POINT (always only ONE trigger)
- Answers: "What starts this flow?"
- Examples: Form submitted, Email arrives, Monday at 9 AM

**Action** = The STEPS (can have many actions)
- Answers: "What should happen?"
- Examples: Send email, Create file, Update list, Get data

**Analogy**:
- **Trigger** = Alarm clock rings (starts your morning)
- **Actions** = Brush teeth, eat breakfast, get dressed (all the steps after)

---

### Q: "What is this 'Dynamic Content' really?"

**Technical but Simple Answer**:
Every step in Power Automate produces OUTPUT (information). 

Dynamic Content = Using the OUTPUT from earlier steps as INPUT for later steps.

**Example Flow**:
```
Step 1: Form submitted
  OUTPUT: Name=John, Email=john@email.com, Phone=555-1234

Step 2: Send email
  INPUT needed: Who to send to?
  USE Dynamic Content: john@email.com (from Step 1 output!)

Step 3: Add to SharePoint
  INPUT needed: What name?
  USE Dynamic Content: John (from Step 1 output!)
```

**Why it's "Dynamic"**: 
- Next person submits: Name=Sarah, Email=sarah@email.com
- Flow automatically uses NEW values
- You don't change anything - it adapts!

---

### Q: "How does Conditional Logic work?"

**The Condition Box**:
```
[Choose a value] [Operator] [Compare to value]
```

**Example 1: Simple**:
```
[Cost] [is greater than] [200]
```
- If Cost = $50 → FALSE path
- If Cost = $300 → TRUE path

**Example 2: Text**:
```
[Priority] [is equal to] [Critical]
```
- If Priority = "Medium" → FALSE path  
- If Priority = "Critical" → TRUE path

**Example 3: Email**:
```
[Manager Email] [is equal to] [bob@company.com]
```

**Operators You Can Use**:
- `is equal to` = exact match
- `is not equal to` = anything except
- `is greater than` = bigger number
- `is less than` = smaller number
- `contains` = text includes something
- `does not contain` = text doesn't include

---

### Q: "What's this 'Get Manager' thing?"

**The Magic**:
Microsoft stores your company's organization chart in the cloud (Azure Active Directory / Entra ID).

**It knows**:
- John reports to Sarah
- Sarah reports to Bob  
- Bob reports to CEO

**Get Manager Action**:
```
INPUT: John's email (john@company.com)
AUTOMATIC LOOKUP: Who is John's manager?
OUTPUT: Sarah's email (sarah@company.com)
```

**Requirements** (Important!):
- ✅ Only works for INTERNAL employees
- ✅ HR must have set up reporting structure
- ✅ If not set up = Error!

**Use Case**:
You don't need to know who anyone's manager is! Power Automate looks it up automatically based on employee who submitted request.

---

### Q: "What are the approval options?"

#### Option 1: Power Automate Approvals Connector
**Good for**: Internal employees only

**Features**:
- Shows up in Outlook
- Shows up in Teams
- Shows up on phone app
- Can add comments
- Can attach files
- Tracks everything

**Downside**: 
- Only works for people in your company
- Uses storage (Dataverse tables)

---

#### Option 2: Send Email with Options (What We Used)
**Good for**: Anyone (internal OR external)

**Features**:
- Just an email with buttons
- Works for:
  - Your employees
  - Customers
  - Partners
  - Vendors
  - Anyone with email!

**How it works**:
```
To: manager@company.com
Subject: Please approve device request
Body: Employee needs new laptop costing $1,200
Buttons: [Approve] [Reject]
```

Manager clicks button → Flow knows which button → Does next step

**Customizable**:
- You choose button text: "Approve/Reject", "Yes/No", "Option A/Option B"
- Can have 3-4 buttons if needed

---

### Q: "How do you test flows?"

#### Method 1: Manual Test (First Time)
1. Click **Save**
2. Click **Test** (top right)
3. Choose "Manually"
4. Click **Test**
5. DO THE TRIGGER ACTION:
   - If trigger = form submission → Submit the form
   - If trigger = email → Send an email
   - If trigger = create item → Create SharePoint item
6. Watch it run!
7. Green checkmarks ✓ = Success!
8. Red X = Failed (click to see why)

---

#### Method 2: Automatic Test (After First Success)
1. Click **Test**
2. Choose "Automatically"  
3. Choose "Use recently used trigger"
4. Click **Test**
5. **Don't do anything!** It replays the last trigger
6. Much faster!

**Why This is Amazing**:
- You're editing the "Send Email" step
- You want to test 10 times to get wording right
- WITHOUT automatic test: Submit form 10 times (annoying!)
- WITH automatic test: Just click Test → uses same form submission

---

### Q: "What's the HTML table for?"

**The Problem**:
You have 30 records. You want to email them.

**What happens without HTML table**:
```
For each record:
  Send email with that record
```
Result: 30 emails sent! 😱

**What happens WITH HTML table**:
```
Get all 30 records
Put in one table
Send ONE email with table
```
Result: 1 email with nice table! 😊

**The Table Looks Like**:
```
┌────────────┬──────────────┬────────┐
│ Device     │ Requester    │ Cost   │
├────────────┼──────────────┼────────┤
│ Laptop     │ John Smith   │ $1,200 │
│ Monitor    │ Sarah Jones  │ $300   │
│ Mouse      │ Bob Lee      │ $25    │
└────────────┴──────────────┴────────┘
```

**Styling (CSS)**:
Makes it pretty with:
- Company colors
- Bold headers
- Borders
- Spacing

---

## Formatting Deep Dive

### Date Formatting

**The Problem**: 
Form gives you: `2026-01-20` (hard to read)
You want: `20-Jan-2026` (easier to read)

**The Solution**: `formatDateTime()` function

**Syntax**:
```
formatDateTime([dynamic content], 'd-MMM-yyyy')
```

**Pattern Codes**:
- `d` = Day (1-31)
- `dd` = Day with zero (01-31)
- `M` = Month number (1-12)
- `MM` = Month with zero (01-12)
- `MMM` = Month short (Jan, Feb, Mar)
- `MMMM` = Month full (January, February)
- `yy` = Year 2-digit (26)
- `yyyy` = Year 4-digit (2026)

**Examples**:
```
d-MMM-yyyy        → 20-Jan-2026
MM/dd/yyyy        → 01/20/2026
MMMM d, yyyy      → January 20, 2026
dd-MM-yy          → 20-01-26
```

---

### Currency Formatting

**The Problem**:
SharePoint gives you: `1225` (just a number)
You want: `$1,225.00` (formatted currency)

**The Solution**: `formatNumber()` function

**Syntax**:
```
formatNumber([dynamic content], 'C2')
```

**What it means**:
- `C` = Currency (automatically uses $ for US, £ for UK, € for EU)
- `2` = Two decimal places

**Examples**:
- `C2` → `$1,225.00` (US)
- `C0` → `$1,225` (no decimals)

**Different Countries**:
```
formatNumber([cost], 'C2', 'en-US')  → $1,225.00
formatNumber([cost], 'C2', 'en-GB')  → £1,225.00
formatNumber([cost], 'C2', 'de-DE')  → 1.225,00 €
```

---

## Best Practices (Things to Remember)

### 1. Always Rename Your Steps
**Bad**:
- Condition
- Condition 2  
- Send an email
- Send an email 2

**Good**:
- Check if over $200
- Check manager selection
- Send receipt to requester
- Send approval to manager

**Why**: You (and your team) can understand flow 6 months later!

---

### 2. Test in Small Pieces
Don't build entire 20-step flow then test!

**Instead**:
1. Build trigger + first action → Test
2. Add second action → Test
3. Add condition → Test
4. Keep going...

**Why**: If something breaks, you know exactly which step caused it!

---

### 3. Use Copy/Paste
If you're sending 3 similar emails, don't recreate each one!

1. Build first email perfectly
2. Right-click → Copy
3. Go to where you need it → Paste
4. Change small details

**Saves tons of time!**

---

### 4. Save Before Testing
Always click **Save** before **Test**!

**Why**: Test button might be grayed out if not saved.

---

### 5. Check Your Connections
Before running flow, make sure you're logged into:
- SharePoint ✓
- Outlook ✓  
- Forms ✓
- Teams ✓

**Look for**: Green checkmarks on connections

---

## Common Mistakes & How to Avoid

### Mistake 1: Not Getting Form Response Details
**Wrong**:
```
Trigger: When form submitted
Action: Send email with [form data]  ❌ Won't work!
```

**Right**:
```
Trigger: When form submitted
Action: Get response details  ← MUST HAVE!
Action: Send email with [form data]  ✓ Works!
```

**Why**: Trigger only gives you response ID number, not actual answers!

---

### Mistake 2: Hardcoding Values
**Wrong**:
```
Send email to: john@company.com  ← Only works for John!
```

**Right**:
```
Send email to: [Requester Email]  ← Works for anyone!
```

**Why**: Dynamic content makes flow work for everyone automatically!

---

### Mistake 3: Forgetting Condition After Approval
**Wrong**:
```
Send approval
Update item  ❌ Updates even if rejected!
```

**Right**:
```
Send approval
Condition: Check if approved
  IF True → Update item
  IF False → Send rejection email
```

**Why**: Need to check which button was clicked!

---

### Mistake 4: Misspelling in Conditions
**Wrong**:
```
IF [Selected Option] is equal to "approve"  ← lowercase!
But button says "Approve"  ← capital A!
Result: Never matches! ❌
```

**Right**:
```
IF [Selected Option] is equal to "Approve"  ← Exact match!
Button says "Approve"
Result: Works! ✓
```

**Why**: Spelling and capitals must match EXACTLY!

---

### Mistake 5: Not Using Right List/Site
**Wrong**:
```
Trigger: When item created in List A
Action: Update item in List B  ❌ Wrong list!
```

**Right**:
```
Trigger: When item created in List A
Action: Update item in List A  ✓ Same list!
Action: Use ID from trigger  ✓ Same item!
```

---

## Answering Common Questions

### "How long did it take to build these?"

**Example 1 (Form Auto-Reply)**:
- For beginner following tutorial: 15-20 minutes
- For someone experienced: 5 minutes
- Once built: Runs forever automatically!

**Example 2 (Approval Workflow)**:
- For beginner: 45-60 minutes
- For experienced: 15-20 minutes
- Saves: Hours per week of manual work!

**Example 3 (HTML Table)**:
- For beginner: 20 minutes
- For experienced: 5 minutes
- Runs every week automatically!

---

### "What can I actually do with this?"

**Real-World Examples**:

1. **HR**:
   - New employee form → Automatically create accounts, assign equipment, schedule training

2. **IT**:
   - Support ticket submitted → Email confirmation, assign to tech, track status

3. **Sales**:
   - New lead in form → Add to CRM, notify sales rep, send welcome email

4. **Finance**:
   - Expense report → Route to manager, check amount, auto-approve if small

5. **Marketing**:
   - Event registration → Add to attendee list, send confirmation, add to calendar

6. **Education**:
   - Student submits assignment → Confirm receipt, check due date, alert teacher

7. **Customer Service**:
   - Complaint form → Log ticket, email customer, notify supervisor if urgent

---

### "What's the hardest part?"

**For most beginners**: Understanding Dynamic Content

**The mental shift**:
- Old way: "I'll type John's email here"
- New way: "I'll use the email that was submitted" (works for anyone!)

**Once you get it**: Everything else clicks!

---

### "Do I need to know coding?"

**Short answer**: No!

**What we used**:
- ✅ Point and click interface
- ✅ Dropdown menus
- ✅ Drag and drop
- ✅ Pre-built actions

**Only "code" was**:
- Two simple formulas for formatting (provided in course)
- Copy/paste HTML styling (provided in course)

**If you can use**: 
- Email ✓
- Dropdowns ✓  
- Fill out forms ✓

**Then you can**: Build Power Automate flows!

---

## Resources Mentioned

### What Was Provided:
1. **Course Materials**: Downloadable files
   - CSV for SharePoint import
   - Form template link
   - HTML styling template

2. **YouTube Channel**: Pragmatic Works
   - This full session recorded
   - Other Power Automate tutorials
   - Filtering tutorial mentioned
   - "Send email on behalf of" tutorial

3. **Follow-up**: Q&A session next week

---

### Learning Options:
1. **Free**: 
   - YouTube videos
   - Community plan on platform
   - This recorded session

2. **Paid**:
   - On-Demand courses ($39/month)
   - Cert XP (exam prep)
   - Boot camps (intensive training)
   - Virtual mentoring (1-on-1 tutoring)
   - Season Learning Pass (all-access)

---

## Summary: What You Learned

### Core Concepts:
✅ What Power Automate is (automation tool)
✅ Three types of flows (Automated, Instant, Scheduled)
✅ Triggers vs Actions
✅ Dynamic Content (reusing data)
✅ Connectors (bridges to other apps)
✅ Conditions (IF-THEN logic)
✅ Approvals (getting yes/no decisions)
✅ Testing (manual and automatic)

### Practical Skills:
✅ Build form auto-reply
✅ Create approval workflow  
✅ Format dates and currency
✅ Find managers automatically
✅ Send emails with buttons
✅ Create HTML tables
✅ Schedule weekly reports

### Best Practices:
✅ Rename steps clearly
✅ Test incrementally  
✅ Use dynamic content
✅ Copy/paste to save time
✅ Check spelling in conditions

---

## How to Explain What You Learned (Interview Style)

### Q: "What did you learn in this training?"

**Good Answer**:
"I learned Power Automate, which is Microsoft's automation tool. I can now build workflows that automatically handle repetitive tasks. For example, I built a system where when someone submits a form, it automatically sends them a confirmation email, routes expensive requests to their manager for approval via email buttons, and updates our tracking system based on the manager's decision - all without any human intervention. I also learned to create scheduled reports that format data into nice tables and email them weekly."

### Q: "Can you give a specific example?"

**Good Answer**:
"Sure! One example was a device request approval workflow. When an employee requests equipment through a SharePoint list, the flow automatically:
1. Sends them confirmation with their request details
2. Checks if it costs over $200
3. If expensive, looks up their manager automatically and sends an approval email with Approve/Reject buttons
4. Based on what the manager clicks, updates the SharePoint list and notifies the employee

The whole thing runs 24/7 automatically. Before automation, someone would manually do all these steps for every single request."

### Q: "What's the business value?"

**Good Answer**:
"The main value is time savings and consistency. If an organization gets 20 device requests per week, and each takes 15 minutes to process manually, that's 5 hours per week - over 250 hours per year. Power Automate handles it instantly. Plus, it never forgets a step, always sends the confirmation, and works even on weekends. It lets people focus on work that actually needs human judgment instead of repetitive administrative tasks."

---

## Final Key Takeaways for Knowledge Transfer

1. **Power Automate = Automation for repetitive tasks**
2. **Three flow types = How you start (event, button, schedule)**
3. **Dynamic Content = Data flows from step to step automatically**
4. **Conditions = Make decisions (IF-THEN-ELSE)**
5. **No coding needed = Point-and-click interface**
6. **Real business value = Saves hours of manual work weekly**
7. **Scales infinitely = Handle 1 or 1,000 requests with same effort**
