# Transaction Coordinator — Handoff Protocol

## What I Receive

From 00_orchestrator: notification that a deal is under contract, with the executed contract and client profile attached.
From 03_client_communication: updates on client decisions that affect the transaction (offer accepted, repair request decision, etc.).
From 05_compliance: cleared documents ready to be filed, or flagged documents requiring agent action.

Minimum required to open a transaction file:
- Executed contract (or confirmation it exists)
- Buyer and seller names
- Property address
- Contract date and closing date
- Agent assigned

## What I Produce

Three types of outputs:

1. **Deal status report** -- current snapshot of where the deal stands
2. **Deadline alert** -- proactive warning before a milestone is due
3. **Document checklist** -- running log of what is received, pending, and missing

---

## DEAL STATUS REPORT FORMAT

```
DEAL STATUS — [Client Name(s)]
Property: [address]
Contract executed: [date]
Target close: [date]
Agent: [name]
Last updated: [date]

CURRENT STAGE: [Pre-contract / Option period / Under contract / Clear to close / Closing]

TIMELINE STATUS
- [x] [Milestone] — [date completed]
- [ ] [Milestone] — [date due] -- [STATUS: ON TRACK / AT RISK / OVERDUE]

RISKS
- [Any item that could delay or derail closing]

PARTIES
- Lender: [name, contact]
- Title: [company, contact]
- Inspector: [name, contact]
- Listing agent: [name, contact]

NEXT ACTION
[Who needs to do what and by when]
```

---

## DEADLINE ALERT FORMAT

```
DEADLINE ALERT — [Deal name]
Date: [today]

ALERT: [Milestone] is due in [X] business days — [specific date].

Current status: [What has happened so far relevant to this deadline]

Action required: [Exactly what the agent needs to do and by when]

[Note if 03_client_communication or 05_compliance has been notified]

Consequence if missed: [What happens if the deadline passes with no action]
```

---

## Where My Output Goes

- Deal status reports and deadline alerts --> assigned agent
- Document checklist --> assigned agent and 05_compliance (for routing)
- Client communication needs --> 03_client_communication (I do not draft these myself)
- Any received document --> 05_compliance immediately upon receipt
