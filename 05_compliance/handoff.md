# Compliance Specialist — Handoff Formats

## What Compliance Receives

Compliance accepts one type of inbound route from the orchestrator:

**Post-Signature Audit Request**
```
COMPLIANCE REQUEST — POST-SIGNATURE
Document: [document name and type]
Property: [full address]
Parties: [buyer names] / [seller names]
Return date: [date document was received back]
Routed from: [transaction coordinator]
Attached: [executed document and all addenda]
Notes: [any known issues flagged during the deal — liens, multi-party signing requirements, etc.]
```

---

## What Compliance Produces

**Output 1 — Post-Signature Sign-Off Checklist: CLEARED**
```
COMPLIANCE SIGN-OFF CHECKLIST
Document: [document name and TREC form number]
Property: [address]
Executed by: [all signing parties]
Return date: [date]

REQUIRED FIELDS CHECK:
- [x] All signature lines signed
- [x] All date fields filled — including Effective Date
- [x] All initialing blocks initialed
- [x] Page count matches — [X] of [X] pages present

TEXAS DISCLOSURES CHECK:
- [x] TREC IABS 1-0 (Information About Brokerage Services) — provided at first contact
- [x] TREC OP-H (Seller's Disclosure Notice) — present and complete [or N/A]
- [x] HUD/EPA Lead-Based Paint Disclosure — present and signed [or N/A — property post-1978]
- [x] TREC 36-10 (HOA Addendum) — present and signed [or N/A — no HOA]
- [x] MUD Notice — present and signed [or N/A — property not in MUD district]

EFFECTIVE DATE CHECK:
- [x] Effective Date: [date] — confirmed and filled in
- [x] Option Period end date: [date] — correctly calculated from Effective Date
- [x] Option Fee: [amount] — paid directly to seller, receipt confirmed
- [x] Earnest money due date: [date] — 3 days from Effective Date, receipt confirmed

CONSISTENCY CHECK:
- [x] Party names consistent throughout
- [x] Property address consistent throughout
- [x] Dollar amounts consistent throughout

FLAGS: None

RESULT: CLEARED — Document is compliant. File in transaction record. Notify transaction coordinator.
```

**Output 2 — Post-Signature Audit: FLAGGED**
```
COMPLIANCE SIGN-OFF CHECKLIST
Document: [document name and TREC form number]
Property: [address]
Return date: [date]

REQUIRED FIELDS CHECK:
- [x or FAIL] [each item with page number if failed]

TEXAS DISCLOSURES CHECK:
- [x or FAIL] TREC IABS 1-0 — [status]
- [x or FAIL] TREC OP-H (Seller's Disclosure) — [status]
- [x or FAIL] HUD/EPA Lead-Based Paint — [status or N/A]
- [x or FAIL] TREC 36-10 (HOA Addendum) — [status or N/A]
- [x or FAIL] MUD Notice — [status or N/A]

EFFECTIVE DATE CHECK:
- [x or FAIL] Effective Date filled in — [status]
- [x or FAIL] Option Period dates correct — [status]
- [x or FAIL] Earnest money deadline correct — [status]

FLAGS:
[number]. [BLOCKING] — Page [X], [section or location]
   Issue: [exact description of what is missing or wrong]
   Required action: [what must happen to resolve]

RESULT: FLAGGED — Return to transaction coordinator. Do not file until resolved.
```

---

## Routing After Compliance Output

| Result | Next step |
|--------|-----------|
| CLEARED | File in transaction record, notify transaction coordinator |
| FLAGGED | Return to transaction coordinator for resolution — do not file |
