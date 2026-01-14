

# What I Learned – Power Automate 

## 1. What is Power Automate & Why We Use It

**Power Automate** is a Microsoft tool used to **automate workflows and backend logic**.

### Why it is needed

* Power Apps is mainly for **UI (screens, forms, buttons)**
* Power Automate handles **processing, automation, and integrations**

### What Power Automate can do

* Send emails
* Save data to SharePoint / Excel / Dataverse
* Run approvals
* Work on schedules
* Automate desktop tasks
* Handle complex logic (conditions, loops, JSON)

### Simple Example

> User submits a form → Email goes automatically → Data gets saved → No manual work

---

## 2. What I See When I Open Power Automate

When I open **Power Automate**, I see:

### Main Options

* **Home** – Overview and recent flows
* **Create** – To create new flows
* **Templates** – Ready-made flows (Outlook → OneDrive, Approvals, etc.)
* **My flows** – All flows created by me
* **Approvals** – Approval requests
* **Learn** – Microsoft learning modules
* **Solutions** – For advanced enterprise setups
* **Process Mining** – Analyze and improve processes

---

## 3. Environments – Very Important Concept

### What is an Environment

An **Environment** is like a **workspace** where flows, apps, and data live.

### Why environments are used

* To separate **development, testing, and production**
* To control **access and data security**

### Example Environments You Saw

* **Dev** – Build and test flows
* **QA / UAT** – Testing
* **Prod** – Actual business usage
* **Default** – Basic environment

### Simple Meaning

> Same flow, different environments = safer deployments

---

## 4. Ways to Create a Flow (Core Learning)

### 1️⃣ Start from Blank

You manually choose:

* Trigger
* Actions
* Conditions

Used when you need **custom logic**.

---

### 2️⃣ Automated Cloud Flow

Triggered by an event:

* New email arrives
* New SharePoint item created

**Example**

```
When email arrives → Save attachment to OneDrive
```

---

### 3️⃣ Instant Cloud Flow

Triggered manually:

* Button click
* Power Apps call

**Example**

```
Click button → Send email
```

---

### 4️⃣ Scheduled Cloud Flow

Runs on time:

* Daily
* Weekly
* Monthly

**Example**

```
Every day at 10 AM → Send reminder email
```

---

### 5️⃣ Describe It to Design It (Copilot)

* You describe the flow in plain English
* AI creates the flow structure

**Example**

> “Create a flow that runs daily and emails Excel contacts”

---

### 6️⃣ Desktop Flow

* Automates **desktop actions**
* Uses **Power Automate Desktop**
* Works like a bot

---

### 7️⃣ Process Mining

* Used to **analyze and optimize processes**
* Not for building flows directly

---

## 5. Triggers & Actions (Very Core Concept)

### Trigger

* Starts the flow
* Only **one trigger per flow**

**Examples**

* When an email arrives
* Recurrence
* Power Apps trigger

---

### Actions

* Steps performed after trigger

**Examples**

* Get items
* Send email
* Create file
* Condition

---

### Flow Structure

```
Trigger
 ↓
Action
 ↓
Action
 ↓
Condition
```

---

## 6. Building a Scheduled Flow (Excel → Email)

### What We Did

* Used **Recurrence trigger**
* Read Excel rows from OneDrive
* Sent email to each contact

### Why Excel Must Be a Table

* Power Automate can only read **tables**
* Not normal Excel ranges

---

### Flow Logic

```
Recurrence
 ↓
List rows from Excel
 ↓
Apply to each row
 ↓
Send Email
```

---

## 7. Conditions & Expressions (Logic Building)

### Condition

Used to make decisions

**Example**

* If today is weekend → Don’t run
* If status = Approved → Continue

---

### Expressions (Advanced Logic)

Used for:

* Date checks
* Calculations
* Boolean logic

### Example (Weekend Check)

```
or(
  equals(dayOfWeek(utcNow()), 0),
  equals(dayOfWeek(utcNow()), 6)
)
```

👉 0 = Sunday
👉 6 = Saturday

---

## 8. Cloud Flow vs Desktop Flow

### Cloud Flow

* Runs in Microsoft cloud
* Works with online services
* No machine dependency

### Desktop Flow

* Runs on a physical/virtual machine
* Automates apps like Excel, browser, legacy systems

---

## 9. Attended vs Unattended Desktop Flow

### Attended Mode

* User is logged in
* Manual start
* Needs user presence

### Unattended Mode

* Runs without login
* Needs **unattended bot license**
* Used for scheduled automation

---

## 10. Power Automate + Power Apps (Backend Concept)

### How They Work Together

* Power Apps → Frontend
* Power Automate → Backend

### Example

```
Power Apps Button
 ↓
Power Automate Flow
 ↓
Process + Save Data
 ↓
Return Status
```

---

## 11. Synchronous vs Asynchronous Calls

### Asynchronous

* App doesn’t wait
* Used for background tasks

### Synchronous

* App waits for response
* Used for validations and confirmations

---

## 12. JSON & Data Exchange

### Simple Parameters

* Text
* Number
* Boolean

### Complex Parameters

* JSON objects
* Used when sending multiple fields

### Why JSON is Important

* Clean structure
* Scalable
* Professional integration

---

## Final Understanding (Interview Ready)

> I learned how Power Automate is used as a backend automation tool, how environments help manage solutions, how to create different types of flows, how triggers and actions work, how to use scheduled flows, conditions, and expressions, the difference between cloud and desktop flows, attended vs unattended execution, and how Power Automate integrates with Power Apps using synchronous, asynchronous, and JSON-based communication.

---

