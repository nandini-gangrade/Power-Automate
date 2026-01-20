# 📘 POWER AUTOMATE — COMPLETE 80/20 NOTES (DETAILED, FROM ZERO)

---

## 1. Why Power Automate Exists (This Shapes Everything)

In most companies:

* Data already exists (SharePoint, Forms, Excel, Outlook)
* People still do repetitive work manually
* Mistakes happen because humans forget steps

Power Automate exists to:

* **Remove manual steps**
* **Enforce rules**
* **Ensure consistency**
* **Connect systems automatically**

🧠 **80/20 insight**:
Power Automate is not about tools — it’s about **process thinking**.

---

## 2. The Only Mental Model You Need

Every real Power Automate solution follows this:

```
Something happens
→ Read data
→ Decide (logic)
→ Do something
→ Update system
→ Inform people
```

If a flow does not follow this, it’s either wrong or incomplete.

---

## 3. Trigger — The Entry Point of Automation

A **trigger** answers only one question:

> *When should this flow run?*

Examples:

* When a SharePoint item is created
* When a form is submitted
* When an email arrives
* Every day at 9 AM

### Important truths:

* One flow = **one trigger**
* Trigger should be **as specific as possible**
* Bad trigger = unnecessary runs = performance issues

🧠 **80/20 trick**:
Choose the trigger carefully — it reduces complexity later.

---

## 4. Reading Data — Where Most Logic Depends

Once triggered, the flow usually needs data.

### Common sources:

* SharePoint lists
* Forms responses
* Emails
* Excel rows

### Get Item vs Get Items:

* **Get item** → single record (ID known)
* **Get items** → multiple records (filter needed)

🧠 **80/20 rule**:
Most slow flows are slow because `Get items` is misused.

---

## 5. Dynamic Content — Data Passing Between Steps

Dynamic content is how data moves inside a flow.

Example:

* SharePoint Title
* Requester Email
* Approval Response

Instead of hardcoding values, I **always use dynamic content**.

🧠 **Why this matters**:

* Makes flows reusable
* Prevents breaking when data changes

---

## 6. Conditional Logic — The Brain of Power Automate

Conditions answer:

> *What should happen in different situations?*

Example:

* If amount > 10,000 → manager approval
* Else → auto approve

This is implemented using **Condition actions**.

🧠 **80/20 thinking**:

* Almost all business logic = if / else
* Master conditions → master Power Automate

---

## 7. Expressions — When Conditions Are Not Enough

Sometimes:

* Data is text, but logic needs number
* Dates need formatting
* Calculations are required

Expressions solve this.

Examples:

* `greater()`
* `equals()`
* `formatDateTime()`

🧠 **Rule**:
Use expressions **only when dynamic content fails**.

---

## 8. Approvals — Human Decision in Automation

Approvals introduce **human judgment**.

Flow behavior:

1. Flow sends approval
2. Flow waits
3. User approves or rejects
4. Flow resumes

Important:

* Flow can wait hours or days
* Approval response controls next steps

🧠 **80/20 insight**:
Most real business automations =
**System logic + Human approval**

---

## 9. SharePoint Automation — The Backbone

SharePoint lists act as:

* Input
* Status tracker
* Audit log

Typical pattern:

* Create item
* Update status
* Store approval decision
* Store comments

🧠 **Golden rule**:
Always update SharePoint after automation completes.

---

## 10. Email Reporting — Communication Layer

Automation without communication = confusion.

Emails are used to:

* Confirm submission
* Notify approval
* Send reports

### HTML Tables:

Used when:

* Multiple records
* Summary reports

🧠 **80/20 win**:
One well-formatted email beats 10 separate emails.

---

## 11. Compose Action — Clean Flow Design

Compose is used to:

* Store intermediate values
* Build email text
* Simplify expressions

🧠 **Pro tip**:
If logic looks ugly, add Compose.

---

## 12. Flow Design Best Practices (HIGH VALUE)

* Rename every step
* Add comments
* Keep flows readable
* Avoid deeply nested conditions

🧠 Flows are **maintained by humans**, not machines.

---

## 13. Error Handling (Often Ignored, Very Important)

Real systems fail:

* Connector fails
* Approval times out
* Data is missing

Use:

* Scope
* Configure run after
* Error emails

🧠 **80/20 rule**:
Error handling separates hobby projects from production flows.

---

## 14. Performance & Stability Tricks

* Filter data at source
* Use Top Count
* Avoid infinite loops
* Don’t update trigger item blindly

🧠 Efficient flows scale better and fail less.

---

## 15. End-to-End Real Flow Pattern (MOST IMPORTANT)

```
Trigger (SharePoint/Form)
 ↓
Read data
 ↓
Condition
 ↓
Approval (if needed)
 ↓
Update SharePoint
 ↓
Send email/report
```

If you can explain this clearly,
you **understand 80% of Power Automate used in real companies**.

---

## 16. One-Line Super Recall (Lock This In)

**Power Automate = Event → Data → Logic → Approval → Update → Notify**
