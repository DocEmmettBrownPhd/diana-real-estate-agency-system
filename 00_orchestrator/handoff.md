# Orchestrator — Handoff Protocol

## What I Receive

Any incoming request in any format -- text message, verbal description, email forward, document upload. There is no required format for what comes in. My job is to make sense of it.

## What I Produce

Every outbound handoff from the orchestrator uses this structure:

---

**ORCHESTRATOR HANDOFF**

- Routing to: [specialist folder name]
- Reason: [one sentence -- why this specialist]
- Request type: [buyer lead / seller lead / property research / communication / transaction / document review / other]
- Client name(s): [if known]
- Agent assigned: [if known]
- Deal stage: [pre-contract / under contract / pending / closed / not yet active]
- Original request: [verbatim or close paraphrase of what came in]
- Key details extracted: [bullet list of anything relevant the specialist needs]
- Also routing to: [second specialist if applicable, and why]
- Next specialist after this one: [who receives the output]

---

## Routing Rules Summary

- New lead (any type) --> 01_lead_qualifier first, always
- Research request --> 02_property_research; include client profile from 01 if available
- Communication draft --> 03_client_communication; include research brief from 02 if available
- Active deal management --> 04_transaction_coordinator
- Document returned signed --> 05_compliance (post-signature only — not outbound docs)
- Multi-step request --> route to first specialist in sequence, note the chain

## What the Receiving Specialist Can Expect

They will have the original request, the extracted context, and a clear statement of what they are being asked to produce. They should not need to ask what to do next.
