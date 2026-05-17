# Lead Intake — Handoff Protocol

## What I Receive

Raw lead input in any of the following forms:
- Zillow or portal email forward (paste the full email)
- Phone call notes (agent types what they captured)
- Old contact list row (name, phone, email, any notes)
- Open house sign-in entry
- Text message relay
- Referral mention ("someone told me their neighbor wants to sell")
- Any other unstructured lead information

No format required on input. That is the point.

---

## What I Produce

Every lead exits as a **Lead Package** in the format below, plus an entry in the **Assignment Log**.

---

## LEAD PACKAGE FORMAT

```
LEAD PACKAGE — [Full Name(s) or "Unknown" if not captured]
Date received: [YYYY-MM-DD]
Source: [Portal — Zillow / Phone call — agent relayed / Old contact list / Open house — [address] / Referral — [source name] / Text / Other]
Status: [NEW / INCOMPLETE / COLD REACTIVATION]

RAW CAPTURE
- Name(s): [as received]
- Phone: [number or "Not captured"]
- Email: [address or "Not captured"]
- Property of interest: [address or area, or "Not captured"]
- Message / notes: [verbatim or summarized from raw input]

GAPS — [list every field not captured, mark CRITICAL if it blocks first contact]
- [Field]: [Not captured / Needs confirmation]
!! [Critical field]: [Not captured — blocks routing]

LEAD TYPE: [Buyer / Seller / Both / Unknown]
URGENCY: [Low / Medium / High] — [reason if stated]
RED FLAGS: [None / list with !! prefix]

DISTRIBUTION
- Rotation check: [which agent is next in rotation]
- Lead type match: [any specialty override applied — explain if so]
- ASSIGNED TO: [Agent name]
- Assignment logged: [YYYY-MM-DD]

NEXT STEP: [Hand to 01_lead_qualifier with this package / Hold at intake — [reason] / Escalate to Diana — [reason]]
```

---

## ASSIGNMENT LOG FORMAT

One row per lead. Diana reviews this log to see pipeline balance across the team.

```
ASSIGNMENT LOG — [Month YYYY]

| Date       | Lead Name              | Type   | Source          | Assigned To | Notes                        |
|------------|------------------------|--------|-----------------|-------------|------------------------------|
| 2026-05-14 | Marcus & Priya Okafor  | Buyer  | Zillow          | Agent 3     | Standard rotation            |
| 2026-05-17 | Sandra [unknown]       | Seller | Phone call      | Diana       | Estate complexity; no contact info yet |
| 2026-05-17 | James Whitfield        | Buyer  | Old contact     | Agent 2     | Reactivation — cold          |
| 2026-05-17 | Carla Mendes           | Buyer  | Old contact     | Agent 3     | Reactivation — cold          |
| 2026-05-17 | Ron & Tammy Griggs     | Seller | Referral        | Diana       | Nguyen referral — personal touch |
```

---

## Where the Lead Package Goes

```
Lead Package produced
        ↓
01_lead_qualifier       ← receives the full Lead Package as its starting input
        ↓
00_orchestrator         ← routes the qualified profile to the right specialist
```

- If the lead is **INCOMPLETE** (critical fields missing): Hold at intake. Note what is needed. Do not route to qualifier until critical gaps are filled.
- If the lead is **COLD REACTIVATION**: Route to 03_client_communication first for outreach, then to 01_lead_qualifier once the lead re-engages.
- If all agents are **at capacity**: Escalate to Diana with the lead package before assigning. Do not force an assignment.
- If Diana **overrides** an assignment: Log the override and the reason in the Assignment Log.

---

## Connection to the Lead Qualifier

The Lead Qualifier (01_lead_qualifier) receives the Lead Package as its starting point. It does not re-ask questions already captured here — it picks up where intake left off and fills in the deeper qualification fields (financial details, must-haves, timeline specifics, red flag investigation).

The Lead Package is not a duplicate of the qualifier profile. It is the raw standardized input. The qualifier profile is the finished, fully qualified output.
