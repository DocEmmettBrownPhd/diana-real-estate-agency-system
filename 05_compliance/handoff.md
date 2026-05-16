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
Document: [document name and GAR form number]
Property: [address]
Executed by: [all signing parties]
Return date: [date]

REQUIRED FIELDS CHECK:
- [x] All signature lines signed
- [x] All date fields filled — including Binding Agreement Date
- [x] All initialing blocks initialed
- [x] Page count matches — [X] of [X] pages present

GEORGIA DISCLOSURES CHECK:
- [x] GAR Form F510 (Agency Disclosure / BRRETA) — present and signed
- [x] GAR Form F301 (Seller's Property Disclosure) — present and complete [or N/A]
- [x] GAR Form F316 (Lead-Based Paint) — present and signed [or N/A — property post-1978]
- [x] GAR Form F322 (Community Association) — present and signed [or N/A — no HOA]

BINDING AGREEMENT DATE CHECK:
- [x] Binding Agreement Date: [date] — confirmed
- [x] Due Diligence Period end date: [date] — correctly calculated
- [x] Earnest money receipt confirmed

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
Document: [document name and GAR form number]
Property: [address]
Return date: [date]

REQUIRED FIELDS CHECK:
- [x or FAIL] [each item with page number if failed]

GEORGIA DISCLOSURES CHECK:
- [x or FAIL] [each required form]

BINDING AGREEMENT DATE CHECK:
- [x or FAIL] [each item]

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
