# Lead Qualifier — Handoff Protocol

## What I Receive

An orchestrator handoff containing:
- Lead name(s)
- Lead type (buyer / seller / both)
- Source (Zillow, referral, open house, cold call, etc.)
- Any initial details already captured
- Agent assigned

## What I Produce

A completed lead profile in one of the two formats below. Every field must be filled or marked "Not yet captured."

---

## BUYER PROFILE FORMAT

```
BUYER PROFILE — [Full Name(s)]
Date: [date]
Agent assigned: [name]

Intent: [Primary residence / Investment / Second home]
Type: Buyer

FINANCIAL
- Budget: $[amount]
- Pre-qualified: [Yes / No / In process] — Lender: [name], Expires: [date]
- Down payment: [amount or %]
- Financing type: [Conventional / FHA / VA / Cash / Other]

TARGET AREA
- Primary area: [neighborhoods or zip codes]
- Secondary area: [if any]
- Must-haves: [list]
- Hard no: [list]

TIMELINE
- Target close date: [month/year or specific date]
- Urgency level: [Low / Medium / High] — Reason: [why]

CURRENT LIVING SITUATION
- Currently: [Renting / Owns / Other]
- Lease end or flexibility: [details]
- Moving from: [city/area]

BACKGROUND
- Eviction history: [None / Yes — details]
- Prior ownership: [Yes / No]
- Active bankruptcy: [None / Yes — details]

RED FLAGS
- [None] or [list each flag with !! prefix]

NOTES
- [Any additional context relevant to the agent]

DOWN PAYMENT ASSISTANCE — MATCHED PROGRAMS
[List 2–3 programs from the Austin/Texas DPA list that match this buyer's income, loan type,
and first-time buyer status. If no match, state why.]
- Program name: [name]
  Assistance: [amount]
  Match reason: [why this buyer qualifies]
  Next step: [what buyer needs to do]

PREFERRED LENDERS — MATCHED
[List 2–3 Austin/Texas lenders matched to this buyer's loan type and situation.]
- Lender: [name]
  Specialty match: [why recommended for this buyer]
```

---

## SELLER PROFILE FORMAT

```
SELLER PROFILE — [Full Name(s)]
Date: [date]
Agent assigned: [name]

Intent: [Primary sale / Investment property / Estate / Relocation]
Type: Seller

PROPERTY
- Address: [address]
- Type: [Single-family / Condo / Multi-family / Land]
- Condition: [Good / Fair / Unknown — details]
- Occupancy: [Owner-occupied / Tenant-occupied / Vacant]

DECISION-MAKING
- Primary contact: [name, relationship]
- Other required signers: [names and roles]
- Signing authority confirmed: [Yes / No / Pending]

PRICING
- Client target price: $[amount]
- Lowest acceptable: $[amount]
- Market context: [Needs comparables / Client has data / Overpriced — flag]

TIMELINE
- Urgency: [Low / Medium / High] — Reason: [why]
- Target list date: [date]
- Target close: [date or timeframe]

PROPERTY ISSUES
- Outstanding liens: [None / Yes — type and status]
- Known repairs needed: [list or None]
- Disclosure items: [list or None]

RED FLAGS
- [None] or [list each flag with !! prefix]

NOTES
- [Any additional context]

PRE-LISTING PREP CHECKLIST
Priority items based on intake (agent to confirm):
- [High-priority item 1 based on what seller shared]
- [High-priority item 2]
Full checklist attached.

PHOTO ANALYSIS
Status: [Not yet submitted / Photos received — report attached / Pending seller submission]
Next step: [Send photo submission form / Review submitted photos / Deliver report to agent]
```

---

## Where the Profile Goes

- Buyer profile → 02_property_research (include full profile)
- Seller profile → 02_property_research (comparables) and flag for listing preparation
- Any profile with a red flag → notify assigned agent immediately before routing forward
- Seller photo report → agent review first, then share with seller
