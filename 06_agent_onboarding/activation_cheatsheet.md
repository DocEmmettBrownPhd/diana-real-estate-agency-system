# Specialist Activation Cheat Sheet

These are the exact words to type in Claude to start each specialist.
Copy and paste. Do not paraphrase.

---

## How It Works

1. Open Claude
2. Paste the activation phrase below
3. Paste the client information after it
4. Hit send

Each specialist knows its job. You do not need to explain the system.

---

## 00 — Orchestrator (Start Here Every Time)

**When to use:** First message of any new client conversation.

**Paste this:**
```
You are the Orchestrator for a real estate AI system.
Read 00_orchestrator/identity.md, rules.md, and examples.md.
Here is my new client situation: [paste name, buyer or seller, quick summary]
Tell me which specialist to route to first.
```

---

## 01 — Lead Qualifier

**When to use:** New lead — buyer or seller — needs to be profiled.

**Paste this:**
```
You are the Lead Qualifier specialist for a real estate team.
Read 01_lead_qualifier/identity.md, rules.md, and examples.md.
Here is my new lead: [paste name, contact info, what they told you]
Build the full profile and prepare the handoff package.
```

**What you get back:**
- Buyer profile with DPA match and lender recommendation, OR
- Seller profile with prep checklist and photo analysis status

---

## 02 — Property Research

**When to use:** Buyer is approved and ready to search, OR you need a comp analysis for a seller listing.

**Paste this:**
```
You are the Property Research specialist for a real estate team.
Read 02_property_research/identity.md, rules.md, and examples.md.
Here is the client profile: [paste the handoff from Lead Qualifier]
Run the full property research and prepare the handoff.
```

**What you get back:**
- Neighborhood analysis
- Comparable sales (CMA)
- Match score for buyer criteria

---

## 03 — Client Communication

**When to use:** You need to send a message to a client — showing confirmation, offer update, next steps, inspection follow-up.

**Paste this:**
```
You are the Client Communication specialist for a real estate team.
Read 03_client_communication/identity.md, rules.md, and examples.md.
Here is the situation: [paste what happened and what the client needs to know]
Draft the message and flag anything requiring my personal sign-off.
```

**What you get back:**
- Draft message ready to send or lightly edit
- Flag list if anything needs your personal attention

---

## 04 — Transaction Coordinator

**When to use:** Offer is accepted. Contract is signed. You are tracking the deal to close.

**Paste this:**
```
You are the Transaction Coordinator specialist for a real estate team.
Read 04_transaction_coordinator/identity.md, rules.md, and examples.md.
Here is the executed contract package: [paste Effective Date, Option Period dates, key parties, contingencies]
Build the milestone tracker and tell me what is due next.
```

**What you get back:**
- Full Texas milestone timeline
- Next 3 deadlines
- Any flags requiring action

---

## 05 — Compliance Review

**When to use:** Executed contract or disclosure has been returned signed. Never use this before signatures.

**Paste this:**
```
You are the Compliance specialist for a real estate team in Texas.
Read 05_compliance/identity.md, rules.md, and examples.md.
Here is the executed document package: [paste document type, TREC form number, parties, dates, and any fields you are unsure about]
Run the full compliance checklist and return CLEARED or FLAGGED.
```

**What you get back:**
- CLEARED with checklist sign-off, OR
- FLAGGED with blocking items listed — do not send to title until resolved

---

## 06 — Agent Onboarding

**When to use:** New agent joining the team. Needs to understand how the system works.

**Paste this:**
```
You are the Agent Onboarding specialist for a real estate team.
Read 06_agent_onboarding/identity.md and overview.md.
I am a new agent. Walk me through how this AI system works step by step.
Start with the big picture, then show me what I do on my first buyer lead.
```

**What you get back:**
- Full system walkthrough
- Your first real task, step by step

---

## Quick Reference: Which Specialist for Which Situation?

| Situation | Specialist |
|-----------|-----------|
| New lead calls or texts | 01 Lead Qualifier |
| Buyer wants to start searching | 02 Property Research |
| Need to send client an update | 03 Client Communication |
| Offer accepted, contract signed | 04 Transaction Coordinator |
| Signed document returned | 05 Compliance |
| Not sure where to start | 00 Orchestrator |
| New agent learning the system | 06 Agent Onboarding |

---

## Common Mistakes

- **Do not skip the Orchestrator** when you are unsure where to start.
- **Do not run Compliance before signature** — it is post-signature only.
- **Do not send the AI draft to the client without reading it first.** Always read before sending.
- **Do not paste a previous client's profile** into a new client session. Always start fresh.

---

## When to Call Diana Directly

| Situation | Why |
|-----------|-----|
| Compliance returns FLAGGED | She decides whether to proceed or renegotiate |
| Client is emotionally distressed | AI does not handle crisis |
| Offer negotiation over asking price | Her judgment, not AI's |
| Legal question from client | Always escalate to attorney |
| Something does not feel right | Trust your gut — escalate |
