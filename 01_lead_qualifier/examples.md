# Lead Qualifier — Examples

## Example 1: Buyer Profile — Complete with DPA and Lender Match

**Incoming handoff from orchestrator:**
Lead: Marcus and Tanya Webb. Buyer. South Atlanta area, ~$450K, before August school start.

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
- Primary: South Atlanta (30310, 30311, 30315)
- Secondary: Would consider College Park or East Point if under $420K
- Must-haves: Minimum 3 bed / 2 bath, garage or covered parking, yard for dog
- Hard no: HOA communities

**Timeline**
- Target close: On or before July 31 (school enrollment deadline August 15)
- Urgency: High — date-driven by school calendar

**Current Living Situation**
- Currently renting in North Atlanta
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

- Program: Georgia Dream Homeownership Program
  Assistance: Up to $10,000 toward down payment and closing costs
  Match reason: First-time buyers, conventional loan, income likely within limits for Atlanta MSA
  Next step: Confirm household income against Georgia Dream limits; buyer must complete homebuyer education course before closing

- Program: Invest Atlanta — HOME Investment Partnership Program
  Assistance: Up to $10,000 forgivable loan
  Match reason: First-time buyers purchasing within City of Atlanta limits; income eligibility likely met
  Next step: Confirm property address falls within City of Atlanta boundaries; apply through Invest Atlanta

Note: If both programs are stackable (confirm with lender), total DPA could reach $20,000 — significantly reducing out-of-pocket at close.

**Preferred Lenders — Matched**

- Lender: Movement Mortgage — Atlanta
  Specialty match: Conventional loans, Georgia Dream approved, fast closing model (strong fit for tight timeline)

- Lender: Ameris Bank — Atlanta
  Specialty match: Georgia Dream approved, local decision-making — good backup if Movement cannot close by July 31

---
Route to: 02_property_research
Include: This full profile

---

## Example 2: Seller Profile — With Red Flag and Prep Checklist

**Incoming handoff from orchestrator:**
Lead: Patricia Odom. Seller. Inherited home in southwest Atlanta. Wants to list ASAP.

**Lead Qualifier output:**

---
SELLER PROFILE — Patricia Odom
Date: [date]
Agent assigned: [agent name]

**Intent:** List and sell inherited property
**Type:** Seller

**Property**
- Address: [captured from client — southwest Atlanta area]
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
- HVAC service and documentation before listing (disclosure requirement)
- Deep clean entire interior — vacant homes accumulate dust and odor quickly
- Check for vandalism or damage from extended vacancy

Full checklist attached (agent reviews with client after walkthrough):
[ ] Curb appeal — lawn, walkway, front door, house numbers
[ ] Deep clean entire home
[ ] Touch-up interior paint
[ ] Replace burned-out bulbs
[ ] Service HVAC — have receipt ready for disclosure
[ ] Check roof for visible damage
[ ] Repair any leaky faucets
[ ] Gather documentation: survey, utility history, any warranty paperwork

**Photo Analysis**
Status: Not yet submitted
Next step: Send photo submission form to Patricia Odom once interior walkthrough is complete and basic cleanup is done. Do not send form before walkthrough — current condition may produce a misleading baseline report.

---
Route to: 02_property_research (comparables for southwest Atlanta area)
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
- Repaint front door (current color is faded) — a fresh dark color (navy, black, charcoal) photographs well and adds instant curb appeal
- Remove the broken planter on left side of porch before any photos
- Add two matching potted plants flanking the front door

PRIORITY: High — first exterior photo is the listing thumbnail; this is the most important room in the report

---
ROOM: Living Room
PHOTO COUNT: 4

WHAT WORKS:
- Good natural light from front windows — keep curtains fully open for listing photos
- Hardwood floors are a strong feature — make sure they are clean and polished

RECOMMENDED BEFORE PHOTOS / SHOWINGS:
- Remove the remaining furniture (one chair, one side table) — room shows larger empty
- Clean all windows inside and out before photos
- Touch-up the baseboard paint on the north wall — visible scuff marks in photo 3

PRIORITY: Medium — good bones; small cleanup gets this room photo-ready

---
ROOM: Kitchen
PHOTO COUNT: 2

WHAT WORKS:
- Cabinet layout is functional and will photograph well with counters clear

RECOMMENDED BEFORE PHOTOS / SHOWINGS:
- Deep clean inside and outside of all appliances — refrigerator is still in place and has visible grime
- Clean grout lines on countertop tile — discoloration visible in photo 1
- Replace the under-cabinet light fixture — visible in photo 2 with broken cover

PRIORITY: High — kitchens sell homes; this one needs cleaning before any photos

---
ROOM: Primary Bedroom
PHOTO COUNT: 2

WHAT WORKS:
- Room size reads well — good proportions for the price point

RECOMMENDED BEFORE PHOTOS / SHOWINGS:
- Patch and paint the wall behind where the bed was — bracket holes visible
- Clean and stage with minimal furniture if possible (agent to advise)

PRIORITY: Medium

---
END OF REPORT

Agent note: Review this report with Patricia before sharing. Prioritize front exterior and kitchen — those two rooms will have the most impact on buyer first impressions and online clicks.
