# Lead Intake — Examples

Three scenarios showing the Lead Intake specialist in action: a messy Zillow forward, a phone call with gaps, and a bulk old-contact reactivation.

---

## Example 1: Zillow Email Forward

**Raw input the agent pastes in:**
```
---------- Forwarded message ---------
From: Zillow <noreply@zillow.com>
Subject: New contact from Zillow: Marcus & Priya Okafor

Name: Marcus & Priya Okafor
Phone: (512) 448-2291
Email: mokafor@gmail.com
Message: Hi, we saw the listing at 4802 Tanglewood Ct and wanted to schedule a showing. We are pre-approved and looking to move by August.
Property: 4802 Tanglewood Ct, Austin TX 78731
Received: May 14, 2026 — 9:12am
```

**Lead Intake output:**

```
LEAD PACKAGE — Marcus & Priya Okafor
Date received: 2026-05-14
Source: Portal — Zillow
Status: NEW

RAW CAPTURE
- Name(s): Marcus Okafor, Priya Okafor
- Phone: (512) 448-2291
- Email: mokafor@gmail.com
- Property of interest: 4802 Tanglewood Ct, Austin TX 78731
- Message: Wants to schedule showing. States pre-approved. Target move: August.

GAPS — Agent to collect before or during first contact
- Pre-approval amount: Not captured
- Lender name: Not captured
- Budget ceiling: Not captured
- Current living situation (renting/owns): Not captured
- Specific must-haves: Not captured

LEAD TYPE: Buyer (inferred — showing request, no mention of selling)
URGENCY: Medium — August target is ~10 weeks out

DISTRIBUTION
- Rotation check: [Agent 3] has lowest active count this cycle (4 leads)
- Lead type match: Standard buyer — no specialty override
- ASSIGNED TO: Agent 3
- Assignment logged: 2026-05-14

NEXT STEP: Hand to 01_lead_qualifier with this package. Agent 3 to make first contact within 24 hours.
```

---

## Example 2: Phone Call Notes — Gaps Present

**Raw input the agent pastes in:**
```
Called in around 2pm. Lady named Sandra, wants to sell her house in Mueller. Said she's been thinking about it for a while, doesn't need to move fast. Husband passed away last year so it's just her now. Didn't get her last name or number, she said she'd call back. She mentioned her neighbor sold last spring and got a good price.
```

**Lead Intake output:**

```
LEAD PACKAGE — Sandra [Last name not captured]
Date received: 2026-05-17
Source: Phone call — agent relayed
Status: NEW — INCOMPLETE

RAW CAPTURE
- Name: Sandra (first name only)
- Phone: NOT CAPTURED — client said she would call back
- Email: NOT CAPTURED
- Property: Mueller neighborhood, Austin TX — address unknown
- Intent: Seller — no urgency stated
- Context: Widowed, sole decision-maker, motivated by neighbor's successful sale

GAPS — CRITICAL (lead cannot be fully processed without these)
!! Phone number: Not captured — dependent on client calling back
!! Last name: Not captured
!! Property address: Not captured
!! Timeline: "No rush" stated — needs clarification on actual target date

GAPS — Standard (collect at first full contact)
- Property type and condition: Unknown
- Outstanding liens: Unknown
- Other required signers: None indicated (widowed, sole owner — confirm)
- Target price: Unknown

LEAD TYPE: Seller
URGENCY: Low — client stated no rush. Monitor for call-back.
RED FLAG: No contact info captured. Lead is warm but unreachable until she calls back.

DISTRIBUTION
- Rotation check: Diana is next in rotation for seller leads this cycle
- Lead type: Potential complexity (estate situation, sole decision-maker post-loss) — Diana preferred
- ASSIGNED TO: Diana
- Assignment logged: 2026-05-17

ALERT TO DIANA: This lead has no return contact info. Assign now so Diana is briefed when Sandra calls back. Do not route to qualifier until phone number is captured.

NEXT STEP: Hold at intake. When Sandra calls back, complete the gap fields and hand to 01_lead_qualifier.
```

---

## Example 3: Bulk Old Contact List Reactivation

**Raw input the agent pastes in:**
```
Going through old contacts. Here are 3 people we haven't talked to in a while who might be ready:

1. James Whitfield — (512) 301-4477 — talked to him about buying in 2024, never went anywhere, he was waiting on a job situation
2. Carla Mendes — carla.m@hotmail.com — open house attendee, Buda area, Spring 2025
3. Ron & Tammy Griggs — (512) 558-9102 — referral from the Nguyen deal, wanted to sell in Pflugerville "eventually"
```

**Lead Intake output:**

```
REACTIVATION BATCH — 3 leads
Date received: 2026-05-17
Source: Old contact list — agent review
Status: COLD REACTIVATION

---
LEAD 1 — James Whitfield
- Phone: (512) 301-4477
- Email: Not captured
- Type: Buyer
- Last contact: ~2024 (estimated)
- Context: Was waiting on job situation — unknown if resolved
- Urgency: Unknown — reactivation needed to assess
- ASSIGNED TO: Agent 2 (rotation — lowest buyer count this cycle)
- Assignment logged: 2026-05-17
- Next step: 03_client_communication — reactivation outreach, gentle check-in

---
LEAD 2 — Carla Mendes
- Phone: Not captured
- Email: carla.m@hotmail.com
- Type: Buyer (inferred — open house attendee)
- Last contact: Spring 2025 (~12 months ago)
- Context: Buda area interest — may be Travis County adjacent or Hays County
- Urgency: Unknown
- ASSIGNED TO: Agent 3 (rotation)
- Assignment logged: 2026-05-17
- Next step: 03_client_communication — reactivation outreach

---
LEAD 3 — Ron & Tammy Griggs
- Phone: (512) 558-9102
- Email: Not captured
- Type: Seller
- Last contact: Unknown — referral from Nguyen deal
- Context: Pflugerville seller, "eventually" timeline — now 1+ year later, may be closer
- Urgency: Unknown — warm referral, worth a personal touch
- Referral source: Nguyen deal (note for Diana — personal outreach preferred)
- ASSIGNED TO: Diana (referral from Diana's network — standard rule)
- Assignment logged: 2026-05-17
- Next step: Diana personal outreach, then 03_client_communication if Diana wants a draft

---
BATCH SUMMARY
| Lead | Type | Assigned | Priority |
|------|------|----------|----------|
| James Whitfield | Buyer | Agent 2 | Low — cold |
| Carla Mendes | Buyer | Agent 3 | Low — cold |
| Ron & Tammy Griggs | Seller | Diana | Medium — referral |
```
