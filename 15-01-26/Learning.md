# [Power Automate – Admin Center, Flows & Button Sharing ](https://learn.microsoft.com/en-us/training/modules/administer-flows/)

---

## 1. Admin Center – What it is and why it’s used

The **Admin Center** is the main place where admins manage everything related to Power Automate, like:

* Environments
* Data policies
* Flows (sharing, exporting, monitoring)

Any change done here is applied **immediately** for users.

### How I open it

* From Power Automate → **Settings (⚙️)** → **Admin Center**
* Or directly open Admin Center using work account

---

### Simple View

```
Admin Center
   ↓
Manage environments
Manage data rules
Manage flows
```

---

## 2. Environments – What I understood

An **environment** is like a separate workspace where apps, data, and flows are stored.

### Easy example:

Think of environments like **folders**:

* One folder for **testing**
* One folder for **production**
* One folder for **HR**
* One folder for **Finance**

Each folder keeps things separate and safe.

### Common usage:

* Test environment → testing flows
* Production environment → real users
* Team-wise environments → different departments

### Simple Diagram

```
Company
 ├─ Dev Environment
 ├─ Test Environment
 └─ Prod Environment
```

---

## 3. Data Policies – What I understood

Data policies are used to **control how data is shared** between connectors.

* Power Automate already follows company security
* Data policies add **extra safety**
* They stop flows from connecting unsafe or restricted data

### Easy example:

* Allowed: Outlook → SharePoint
* Blocked: Outlook → Personal Gmail

### Simple Flow

```
Flow tries to connect data
        ↓
Data Policy Check
   ↓ Allowed / Blocked
```

---

## 4. Export and Import Flows

### What Export means

Export = save a flow so it can be:

* Shared with others
* Moved to another environment

### What Import means

Import = use that saved flow again.

---

### Export a Flow (Simple Steps)

1. Open **Power Automate**
2. Go to **Cloud flows**
3. Click **three dots (⋮)** → **Export**
4. Select **Package (.zip)**

While exporting:

* Give **name**
* Add **description**
* Choose:

  * New flow
  * Update existing flow

👉 The ZIP file includes:

* Flow logic
* Required connections

⚠️ Some environments don’t allow ZIP → they use **Solutions**

---

### Export Flow Diagram

```
Flow
 ↓
Export
 ↓
ZIP File
 ↓
Shared / Stored
```

---

### Import a Flow (Simple Steps)

1. Open **Power Automate**
2. Go to **My flows**
3. Click **Import**
4. Upload ZIP file
5. Select connections
6. Click **Import**

After import, the flow appears in **My flows** and can be used.

---

### Import Flow Diagram

```
ZIP File
 ↓
Import
 ↓
Select connections
 ↓
Flow ready to use
```

---

## 5. Button Flows – What they are

A **button flow** is a flow that runs when I **press a button on my mobile**.

### Easy examples:

* Press button → send email
* Press button → create reminder
* Press button → log work update

---

## 6. Share Button Flows (Using Mobile App)

### How sharing works

* Sharing is done from **Power Automate mobile app**
* Shared users can run the button like their own

### Steps:

1. Open mobile app
2. Go to **Buttons**
3. Click **three dots (⋮)**
4. Click **Invite others**
5. Select user/group
6. Send

---

### Button Sharing Diagram

```
My Button
   ↓
Shared with teammate
   ↓
They press button
   ↓
Flow runs
```

---

## 7. Connections in Shared Buttons

When sharing, I can choose whose connection is used.

### Option 1: My connection

* Flow runs using my account
* User can’t see my credentials

### Option 2: User’s connection (better)

* Flow runs using their account
* More secure

### Example:

If button sends email:

* My connection → email sent from me
* User connection → email sent from them

---

## 8. Stop Sharing a Button

Steps:

1. Go to **Buttons**
2. Click **⋮ → Invite others**
3. Select user
4. Click **Remove**

---

## 9. Monitor Button Runs

* Open mobile app
* Go to **Activity**
* See:

  * Who ran the flow
  * When it ran
  * Status

---

## 10. Use, Reshare, or Remove Shared Buttons

* **Use**: Add from **Get more**
* **Reshare**: Share button link
* **Remove**: Click **Remove** if not needed

---

## Overall Simple Flow (End-to-End)

```
Admin Center
   ↓
Create / Manage Flow
   ↓
Export (ZIP)
   ↓
Import
   ↓
Share Button
   ↓
Monitor Runs
```

---

### Final Simple Understanding

I learned how to manage environments and data rules using the Admin Center, save and reuse flows by exporting and importing them, share button flows using the mobile app, control connections for security, and track flow runs.
