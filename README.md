# Diana's Real Estate Agency System

An AI operating system for a four-person boutique real estate team in Austin. Nine specialists work together, each owning one part of the workflow. Every lead enters through a standardized intake and gets assigned to an agent before it moves anywhere. Every new team member starts at 000 before touching a live deal. Every request routes through the orchestrator via explicit handoffs.

---

## System Architecture

```
000_agent_onboarding   <-- Day 1 only. New agents start here before anything else.

Raw Lead Arrives (Zillow, phone, old list, referral, open house)
      |
      v
00a_lead_intake        <-- Standardizes any raw input. Assigns to the right agent.
      |
      v
00_orchestrator        <-- Every qualified request routes here. Never does the work itself.
      |
      |-- Lead ready ---------> 01_lead_qualifier      <-- Deep buyer/seller intake
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
      |                          +-------+-------+
      |                          |               |
      |                          v               v
      +-- Any signed doc --> 05_compliance   06_vendor_team <-- Predicts vendor needs by stage
                                                              (inspector, contractor, surveyor,
                                                               stager, photographer, attorney)
```

Work flows left to right. Each specialist receives a structured handoff from the previous one and produces a structured output for the next. No lead skips intake. No signed document skips compliance. The Vendor Team operates at any deal stage — it predicts who you need before you think to ask.

---

## What Each Specialist Owns

| Folder | Specialist | Owns |
|--------|-----------|------|
| `000_agent_onboarding/` | Agent Onboarding | Visual system overview, day-one orientation. Used once by every new agent before their first live deal. |
| `00a_lead_intake/` | Lead Intake | Catches leads from any source in any format. Standardizes into one consistent Lead Package. Assigns to the right agent using fair rotation and workload balancing. Diana gets full visibility via the Assignment Log. |
| `00_orchestrator/` | Orchestrator | Reads every incoming request. Routes it. Never does the work itself. |
| `01_lead_qualifier/` | Lead Qualifier | Deep buyer and seller intake. Full profile before any showing or listing. DPA matching, lender recommendations, seller prep checklist and photo report. |
| `02_property_research/` | Property Researcher | Comparables, neighborhood data, school ratings, market analysis per client profile. |
| `03_client_communication/` | Client Communicator | Emails, texts, follow-ups. Writes in the voice of the agent on the deal. |
| `04_transaction_coordinator/` | Transaction Coordinator | Deadlines, document checklists, who owes what, risk flags once a deal is live. |
| `05_compliance/` | Compliance Reviewer | Reviews all documents after they come back signed. Flags issues. Produces sign-off checklist. Texas-specific disclosure requirements. Post-signature only. |
| `06_vendor_team/` | Vendor Team | Predicts which vendors are needed based on deal stage and property details. Surfaces inspector, surveyor, contractor, stager, photographer, and attorney contacts before the agent has to ask. |

---

## How a Typical Request Flows

**New buyer inquiry — Zillow email forward:**
1. Agent pastes the raw email into `00a_lead_intake` — standardized Lead Package produced, assigned to the right agent via fair rotation
2. Lead Package handed to `01_lead_qualifier` — full intake: pre-qualification status, budget, target area, current living situation, eviction history, timeline, must-haves. DPA programs and lenders matched to buyer profile.
3. Qualified lead profile handed to `02_property_research` — research brief built around the specific buyer profile and target area
4. Research brief handed to `03_client_communication` — agent receives a draft follow-up email with property options and next steps
5. Deal goes live — `04_transaction_coordinator` takes over, tracks all deadlines and documents
6. `06_vendor_team` activates automatically at Option Period — surfaces inspectors, surveyors, and any vendor flagged by property age or condition
7. Every executed document routes through `05_compliance` — post-signature review and sign-off checklist produced

**New seller inquiry — phone call notes:**
1. Agent types their call notes into `00a_lead_intake` — missing fields flagged, lead assigned to agent
2. Lead Qualifier captures: who is involved in the decision, lowest acceptable price, target price, condition of home, timeline, any outstanding liens. Seller receives pre-listing prep checklist and photo analysis report.
3. `06_vendor_team` activates for pre-listing prep — surfaces stager, photographer, handyman as needed
4. Research brief built on comparable sales and current market conditions in their area
5. Client communication drafts listing presentation and follow-up cadence
6. Transaction coordinator manages offer review, contingencies, closing timeline
7. Compliance reviews all executed documents post-signature

**Old contact list reactivation:**
1. Agent pastes rows into `00a_lead_intake` — each contact gets a Lead Package, assigned in batch
2. Cold reactivation leads route to `03_client_communication` first — outreach drafted before qualifier runs
3. When lead re-engages, qualifier runs the full intake and the deal moves forward normally

**Lead distribution — fair rotation:**
- Intake checks active lead counts across all four agents before assigning
- High-value and referral leads route to Diana unless she is at capacity
- Complex situations (estate, divorce, bankruptcy flag) route to Diana by default
- All assignments logged — Diana sees every assignment and can override any of them

---

## Onboarding a New Team Member

**Day 1 — Read in this order:**

1. This README — understand the architecture
2. `000_agent_onboarding/overview.md` — see the full system as a visual flow chart
3. `00_orchestrator/identity.md` — understand how requests are routed
4. Read the `identity.md` of whichever specialist matches your primary role
5. Read that specialist's `rules.md` — these are non-negotiable
6. Read `examples.md` — see the specialist in action
7. Read `handoff.md` — understand what you receive and what you produce

**That is it. You are operational.**

Every specialist folder is self-contained. You do not need to understand the whole system to do your part. The handoff files tell you exactly what format to expect and what format to produce.

---

## Claude Projects Setup

1. Open Claude (claude.ai)
2. Click **Projects** in the left sidebar
3. Create a new Project — name it "Diana's Real Estate System"
4. Upload all specialist folders as Project Knowledge
5. Every conversation inside this project has all specialists loaded — you never re-upload

**Start every conversation by telling Claude which specialist you need:**
```
You are the Lead Intake specialist. Here is a raw lead that just came in:
[paste the Zillow email / phone call notes / contact list row]
```

No software to install. No platform to learn. The folders are the system.

---

## Design Decisions

**Lead intake as the true front door.** Leads arrive in every format — a forwarded Zillow email, a phone call scribbled on a notepad, a row from an old contact spreadsheet. The intake specialist standardizes all of it before anything else runs. No lead enters the system unformatted.

**Fair distribution built into the architecture.** Four agents, one team. The intake layer tracks who has what, rotates fairly, and surfaces capacity problems to Diana before they become someone's missed opportunity. Diana gets an Assignment Log that shows every lead and every assignment — she can override any of it.

**Agent onboarding first.** The 000 folder exists so no agent touches a live deal without understanding the system. It is the first stop — not an afterthought.

**Buyer and seller prep funnel.** Before the agent is involved, the buyer is matched to down payment assistance programs and lenders. The seller gets a prep checklist and a photo-based staging report. The agent walks in ready to work — not chasing paperwork, not explaining basics.

**Vendor Team as intelligence layer.** The Vendor Team does not wait to be asked. It reads the deal stage, property age, and inspection findings and tells the agent exactly who to call — with name and phone number — before the agent has to think about it.

**Structured handoffs over free text.** Every specialist passes a labeled field block to the next one — not a paragraph summary. Any team member can pick up a deal mid-stream without calling Diana.

**Compliance after signature.** Document review happens when executed documents return. This is where errors and missing signatures actually matter — catching them before filing protects the team from liability.

**Texas-specific compliance.** The compliance specialist knows Texas's required forms by name (TREC forms), understands the Option Period and effective date clock, and flags Texas-specific disclosures — not generic national checklists.
