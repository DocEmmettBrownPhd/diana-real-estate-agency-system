# Lead Qualifier — Examples

## Example 1: Buyer Profile — Complete

**Incoming handoff from orchestrator:**
Lead: Marcus and Tanya Webb. Buyer. South Austin, ~$450K, before August school start.

**Lead Qualifier output:**

---
BUYER PROFILE — Marcus and Tanya Webb
Date: [date]
Agent assigned: [agent name]

**Intent:** Purchase primary residence
**Type:** Buyer

**Financial**
- Budget: $450,000 maximum
- Pre-qualified: Yes — pre-approval letter from Cornerstone Home Lending, expires August 15
- Down payment: 10% confirmed
- Financing type: Conventional

**Target Area**
- Primary: South Austin (78745, 78748, 78749)
- Secondary: Would consider Buda if under $420K
- Must-haves: Minimum 3 bed / 2 bath, garage or covered parking, yard for dog
- Hard no: HOA communities

**Timeline**
- Target close: On or before July 31 (school enrollment deadline August 15)
- Urgency: High -- date-driven by school calendar

**Current Living Situation**
- Currently renting in North Austin
- Month-to-month lease -- can move with 30-day notice
- No current ownership

**Background Check Items**
- Eviction history: None reported
- Prior ownership: No
- Moving from: Current Austin rental

**Red Flags**
- None. Pre-approval confirmed. Timeline is tight but workable.

**Notes**
- Tanya is the primary decision-maker. Marcus defers on neighborhood but has final say on price.
- They have seen 4 homes with another agent but did not make an offer. Ask why.

---
Route to: 02_property_research
Include: This full profile

---

## Example 2: Seller Profile — With Red Flag

**Incoming handoff from orchestrator:**
Lead: Patricia Odom. Seller. Inherited home in Pflugerville. Wants to list ASAP.

**Lead Qualifier output:**

---
SELLER PROFILE — Patricia Odom
Date: [date]
Agent assigned: [agent name]

**Intent:** List and sell inherited property
**Type:** Seller

**Property**
- Address: [captured from client]
- Type: Single-family residential
- Condition: Unknown -- client has not seen interior in 18 months
- Occupancy: Vacant

**Decision-Making**
- Primary contact: Patricia Odom (daughter, executor of estate)
- Other parties: One sibling (brother, out of state) must co-sign any listing agreement
- Authority: Patricia is executor but sibling signature required on all documents

**Pricing**
- Client target price: $385,000
- Lowest acceptable: $360,000 (stated)
- Market context: Needs comparables -- route to 02_property_research

**Timeline**
- Urgency: High -- client is paying carrying costs (utilities, insurance) and wants out quickly
- Target list date: Within 2 weeks

**Property Issues**
- Outstanding lien: Property tax lien from 2023 -- client says "it should be cleared" but has no documentation
- Disclosure items: Unknown condition of HVAC, roof age unknown

**Red Flags**
- !! LIEN: Unverified property tax lien. Do not proceed to listing agreement until lien status is confirmed in writing.
- !! MULTI-PARTY: Sibling must sign listing agreement. Confirm availability and willingness before scheduling listing appointment.
- !! CONDITION: Interior not inspected in 18 months. Recommend walkthrough before pricing.

---
Route to: 02_property_research (comparables for Pflugerville area)
Also route: Listing agreement to 05_compliance once lien is cleared

---
