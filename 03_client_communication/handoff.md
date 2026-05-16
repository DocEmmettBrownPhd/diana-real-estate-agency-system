# Client Communicator — Handoff Protocol

## What I Receive

From 02_property_research: a research brief plus the client profile from 01_lead_qualifier.
From 04_transaction_coordinator: a situation update (deadline, document status, milestone) requiring client communication.
From 00_orchestrator: a direct communication request with client context.

Minimum required to draft:
- Client name and contact preference (email / text / both)
- Situation type (first follow-up / offer update / inspection / financing / other)
- Agent name (I write as the agent -- I need their name)
- Any specific facts the message must include (address, price, deadline, options)

## What I Produce

One or more of the following, depending on the situation:

- **Email draft** -- subject line + body, ready for agent to review and send
- **Text draft** -- 1-3 sentences, ready for agent to copy and send
- **Both** -- when the situation calls for speed (competing offer, deadline) and follow-up

All drafts are marked DRAFT. The agent reviews and sends. I do not send.

---

## COMMUNICATION HANDOFF FORMAT

```
COMMUNICATION DRAFT — [Client Name]
Date: [date]
Agent: [name]
Situation: [situation type]
Source brief: [what I received -- research brief / transaction update / direct request]

EMAIL DRAFT
Subject: [subject line]
---
[body]
---

TEXT DRAFT (if applicable)
---
[text]
---

Notes for agent:
- [Any fact that needs agent verification before sending]
- [Any decision the agent needs to make before this goes out]
- [Flag if any document is referenced -- route to 05_compliance before sending]
```

---

## Where My Output Goes

- All drafts --> agent for review and send (never sent directly)
- Any draft referencing a document --> flag to orchestrator to route document to 05_compliance
- Offer-related communications --> also notify 04_transaction_coordinator of the update
