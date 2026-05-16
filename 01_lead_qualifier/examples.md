# Lead Qualifier — Examples

## Example 1: Buyer Profile — Complete with DPA and Lender Match

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
- Down payment: 10% confirmed ($45,000)
- Financing type: Conventional

**Target Area**
- Primary: South Austin (78745, 78748, 78749)
- Secondary: Would consider Buda or Kyle if under $420K
- Must-haves: Minimum 3 bed / 2 bath, garage or covered parking, yard for dog
- Hard no: HOA communities

**Timeline**
- Target close: On or before July 31 (school enrollment deadline August 15)
- Urgency: High — date-driven by school calendar

**Current Living Situation**
- Currently renting in North Austin
- Month-to-month lease — can move with 30-day notice
- No current ownership

**Background**
- Eviction history: None reported
- Prior ownership: No — first-time homebuyers
- Active bankruptcy: None

**Red Flags**
- None. Pre-approval confirmed. Timeline is tight but workable.

**Notes**
- Tanya is the primary decision-maker. Marcus defers on neighborhood but has final say on price.
- They have seen 4 homes with another agent but did not make an offer. Ask why.

**Down Payment Assistance — Matched Programs**

- Program: My First Texas Home (TDHCA)
  Assistance: Up to 5% of loan amount (~$21,875 on $437,500 loan) toward down payment and closing costs
  Match reason: First-time buyers, conventional loan, income likely within TDHCA limits for Austin MSA
  Next step: Confirm household income against TDHCA limits; buyer must complete homebuyer education course before closing

- Program: Texas Mortgage Credit Certificate (MCC)
  Assistance: Federal tax credit up to 40% of annual mortgage interest (up to $2,000/year)
  Match reason: First-time buyers — stackable with My First Texas Home for maximum benefit
  Next step: Apply through TDHCA-approved lender at same time as My First Texas Home

Note: Both programs are stackable — confirm with lender. Combined benefit significantly reduces first-year cost of ownership.

**Preferred Lenders — Matched**

- Lender: Cornerstone Home Lending — Austin
  Specialty match: Already pre-approved here; TDHCA approved lender; strong local market knowledge

- Lender: Movement Mortgage — Austin
  Specialty match: Fast closing model — strong backup if timeline is at risk

---
Route to: 02_property_research
Include: This full profile

---

## Example 2: Seller Profile — With Red Flag and Prep Checklist

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
- Address: 412 Millbrook Ln, Pflugerville TX 78660
- Type: Single-family residential
- Condition: Unknown — client has not seen interior in 18 months
- Occupancy: Vacant

**Decision-Making**
- Primary contact: Patricia Odom (daughter, executor of estate)
- Other parties: One sibling (brother, out of state) must co-sign any listing agreement
- Authority: Patricia is executor but sibling signature required on all documents

**Pricing**
- Client target price: $385,000
- Lowest acceptable: $360,000 (stated)
- Market context: Needs comparables — route to 02_property_research

**Timeline**
- Urgency: High — client is paying carrying costs (utilities, insurance) and wants out quickly
- Target list date: Within 2 weeks

**Property Issues**
- Outstanding lien: Property tax lien from 2023 — client says "it should be cleared" but has no documentation
- Disclosure items: Unknown condition of HVAC, roof age unknown

**Red Flags**
- !! LIEN: Unverified property tax lien. Do not proceed to listing agreement until lien status is confirmed in writing.
- !! MULTI-PARTY: Sibling must sign listing agreement. Confirm availability and willingness before scheduling listing appointment.
- !! CONDITION: Interior not inspected in 18 months. Recommend walkthrough before pricing.

**Notes**
- Patricia is motivated but may be emotionally attached to the home. Handle pricing conversation with care.

**Pre-Listing Prep Checklist — Priority Items Based on Intake**

Priority items (agent to confirm at walkthrough):
- Address exterior condition first — vacant property sitting 18 months likely needs curb appeal work
- HVAC service and documentation before listing (Texas disclosure requirement)
- Deep clean entire interior — vacant homes accumulate dust and odor quickly
- Check for vandalism or damage from extended vacancy

Full checklist attached (agent reviews with client after walkthrough).

**Photo Analysis**
Status: Not yet submitted
Next step: Send photo submission form to Patricia Odom once interior walkthrough is complete and basic cleanup is done.

---
Route to: 02_property_research (comparables for Pflugerville area)
Also route: Listing agreement to 05_compliance once lien is cleared

---

## Example 3: Seller Photo Prep Report

**Trigger:** Patricia Odom submits photos via mobile form after interior walkthrough and basic cleanup. Agent routes photos to lead qualifier for AI review.

**Seller Photo Prep Report — Odom Property**
Date: [date]
Prepared for: Agent review (share with seller after agent review)

---
ROOM: Front Exterior
PHOTO COUNT: 3

WHAT WORKS:
- Mature trees provide good shade and curb appeal potential
- Covered front porch is a selling feature — visible in photos

RECOMMENDED BEFORE PHOTOS / SHOWINGS:
- Power wash the front walkway and driveway — visible staining in photos
- Repaint front door — a fresh dark color (navy, black, charcoal) photographs well
- Remove the broken planter on left side of porch before any photos
- Add two matching potted plants flanking the front door

PRIORITY: High — first exterior photo is the listing thumbnail

---
ROOM: Kitchen
PHOTO COUNT: 2

WHAT WORKS:
- Cabinet layout is functional and will photograph well with counters clear

RECOMMENDED BEFORE PHOTOS / SHOWINGS:
- Deep clean inside and outside of all appliances
- Clean grout lines on countertop tile — discoloration visible in photo 1
- Replace the under-cabinet light fixture — broken cover visible in photo 2

PRIORITY: High — kitchens sell homes; this one needs cleaning before any photos

---
END OF REPORT

Agent note: Prioritize front exterior and kitchen — those two rooms will have the most impact on buyer first impressions and online clicks.
