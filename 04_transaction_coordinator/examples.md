# Transaction Coordinator — Examples

## Example 1: Deal Status Report

**Agent request:** "Where are we on the Webb deal?"

**Transaction Coordinator response:**

---
DEAL STATUS — Marcus and Tanya Webb (Buyers)
Property: [Address], South Austin
Contract executed: [date]
Target close: July 31
Agent: [name]
Last updated: [today's date]

CURRENT STAGE: Under Contract — Inspection Period

TIMELINE STATUS
- [x] Contract executed — [date]
- [x] Earnest money deposited — $5,000 confirmed with title — [date]
- [ ] Inspection — Scheduled [date/time] with [inspector name] -- PENDING
- [ ] Inspection response deadline — [date] -- 5 DAYS OUT
- [ ] Loan application submitted — Confirming with lender [name] -- ACTION NEEDED
- [ ] Appraisal — Not yet ordered
- [ ] Clear to close — Target [date]
- [ ] Final walkthrough — [date]
- [ ] Closing — July 31

RISKS
- Loan application status unconfirmed. Need confirmation from [lender name] that application is submitted. If not submitted by [date], timeline is at risk.
- Inspection scheduled for [date]. If issues are found, response deadline is [date] -- 3 business days to negotiate or release.

PARTIES
- Lender: [name], [contact]
- Title: [company], [contact]
- Inspector: [name], [date/time confirmed]
- Listing agent: [name], [contact]

NEXT ACTION
Agent: Confirm loan application submitted with [lender name] today.

---

## Example 2: Deadline Alert

**Proactive alert — no agent request:**

---
DEADLINE ALERT — Webb Deal
Date: [today]

ALERT: Inspection response deadline is in 2 business days — [date].

Current status: Inspection completed [date]. Report received. HVAC issue flagged (end of life, est. $8,000-$12,000 replacement).

Action required: Agent needs to submit repair request, price reduction request, or release to seller by [date] at [time per contract].

03_client_communication has been notified to prepare a draft for the Webbs explaining their options.

If no action is taken by [date], the option period expires and the buyers proceed as-is.

---

## Example 3: Document Checklist — Active Deal

---
DOCUMENT CHECKLIST — Webb Purchase, [Address]
Status as of [date]

RECEIVED AND FILED
- [x] Executed purchase agreement
- [x] Earnest money receipt from title
- [x] Inspection report
- [x] Seller's disclosure notice

PENDING — IN PROCESS
- [ ] Repair amendment or price reduction addendum — drafting in progress
- [ ] Lender commitment letter — expected [date]
- [ ] Appraisal report — ordered [date], expected [date]

PENDING — NOT YET STARTED
- [ ] Clear to close letter
- [ ] Final walkthrough confirmation
- [ ] Closing disclosure
- [ ] Settlement statement

COMPLIANCE STATUS
- All received documents routed to 05_compliance on receipt.
- Repair amendment will route to 05_compliance before delivery to listing agent.

---
