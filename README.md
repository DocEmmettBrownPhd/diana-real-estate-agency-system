# Diana's Real Estate Agency System

An AI operating system for a four-person boutique real estate team in Austin. Six specialists work together, each owning one part of the workflow. Every request enters through the orchestrator and moves forward through explicit handoffs. A new agent can be operational in a day.

---

## System Architecture

```
Incoming Request
      |
      v
00_orchestrator        <-- Every request starts here. Routes to the right specialist.
      |
      |-- New prospect ---------> 01_lead_qualifier      <-- Deep buyer/seller intake
      |                                  |
      |                                  v
      |                          02_property_research    <-- Research briefs per client profile
      |                                  |
      |                                  v
      |                          03_client_communication <-- Drafts in the agent's voice
      |                                  |
      |                                  v
      |                          04_transaction_coordinator <-- Tracks deadlines, docs, risks
      |                                  |
      |                                  v
      +-- Any document ----------> 05_compliance         <-- Flags issues, signs off on docs
```

Work flows left to right. Each specialist receives a structured handoff from the previous one and produces a structured output for the next. The compliance specialist sits outside the linear chain -- it reviews documents at two points: before they go to the client, and after they come back signed.

---

## What Each Specialist Owns

| Folder | Specialist | Owns |
|--------|-----------|------|
| `00_orchestrator/` | Orchestrator | Reads every incoming request. Routes it. Never does the work itself. |
| `01_lead_qualifier/` | Lead Qualifier | Deep buyer and seller intake. Full profile before any showing or listing. |
| `02_property_research/` | Property Researcher | Comparables, neighborhood data, school ratings, market analysis per client profile. |
| `03_client_communication/` | Client Communicator | Emails, texts, follow-ups. Writes in the voice of the agent on the deal. |
| `04_transaction_coordinator/` | Transaction Coordinator | Deadlines, document checklists, who owes what, risk flags once a deal is live. |
| `05_compliance/` | Compliance Reviewer | Reviews all documents before they go out and after they come back signed. Flags issues. Produces sign-off checklist. |

---

## How a Typical Request Flows

**New buyer inquiry:**
1. Request hits `00_orchestrator` -- identified as new buyer lead
2. Routed to `01_lead_qualifier` -- full intake: pre-qualification status, budget, target area, current living situation, eviction history, timeline, must-haves
3. Qualified lead profile handed to `02_property_research` -- research brief built around the specific buyer profile and target area
4. Research brief handed to `03_client_communication` -- agent receives a draft follow-up email with property options and next steps
5. Deal goes live -- `04_transaction_coordinator` takes over, tracks all deadlines and documents
6. Every document routes through `05_compliance` -- flagged for review before delivery, sign-off checklist produced after return

**New seller inquiry:**
1. Orchestrator identifies as seller lead
2. Lead qualifier captures: who is involved in the decision, lowest acceptable price, target price, condition of home, timeline, any outstanding liens
3. Research brief built on comparable sales and current market conditions in their area
4. Client communication drafts listing presentation and follow-up cadence
5. Transaction coordinator manages offer review, contingencies, closing timeline
6. Compliance reviews listing agreement, disclosure forms, purchase contract

---

## Onboarding a New Team Member

**Day 1 -- Read in this order:**

1. This README -- understand the architecture
2. `00_orchestrator/identity.md` -- understand how requests are routed
3. Read the `identity.md` of whichever specialist matches your primary role
4. Read that specialist's `rules.md` -- these are non-negotiable
5. Read `examples.md` -- see the specialist in action
6. Read `handoff.md` -- understand what you receive and what you produce

**That is it. You are operational.**

Every specialist folder is self-contained. You do not need to understand the whole system to do your part. The handoff files tell you exactly what format to expect and what format to produce.

---

## Setup Before Use

1. Open Claude (claude.ai or Claude Code)
2. Create a new Project
3. Upload the specialist folder for your role as Project Knowledge -- or upload all folders if you are Diana managing the whole system
4. The `identity.md` of each folder acts as the system prompt for that specialist
5. Start every session by telling Claude which specialist you are working with: "You are the Lead Qualifier. A new buyer inquiry just came in."

**No software to install. No platform to learn. The folders are the system.**

---

## Design Decisions

**Structured handoffs over free text.** Every specialist passes a labeled field block to the next one -- not a paragraph summary. This means any team member can pick up a deal mid-stream without calling Diana. The newest agent gets the same information the most senior one would.

**Compliance sits outside the linear chain.** It reviews documents at two trigger points: before delivery and after signature. Making it a separate specialist means it never gets skipped when the pipeline moves fast.

**Deep intake upfront.** The lead qualifier captures everything before a showing is scheduled or a listing is taken. Agents were rebuilding context every time. One thorough intake eliminates that entirely.
