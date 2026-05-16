# Compliance Specialist — Handoff Formats

## What Compliance Receives

Compliance accepts two types of inbound routes from the orchestrator:

**Type 1 — Pre-Delivery Review**
```
COMPLIANCE REQUEST — PRE-DELIVERY
Document: [document name and type]
Property: [full address]
Parties: [buyer names] / [seller names]
Routed from: [transaction coordinator / communication / other]
Attached: [list of documents in the package]
Notes: [any known issues or flags from prior specialists]
```

**Type 2 — Post-Signature Audit**
```
COMPLIANCE REQUEST — POST-SIGNATURE
Document: [document name and type]
Property: [full address]
Parties: [buyer names] / [seller names]
Return date: [date document was received back]
Routed from: [transaction coordinator]
Attached: [executed document and all addenda]
Notes: [any known prior flags from pre-delivery review]
```

---

## What Compliance Produces

**Output 1 — Pre-Delivery Review: BLOCKED**
```
COMPLIANCE REVIEW — PRE-DELIVERY
Document: [document name]
Property: [address]
Review date: [date]

FLAGS:
[number]. [BLOCKING or NOTE] — Page [X], [Section or location]
   Issue: [exact description of what is missing or wrong]
   Required action: [what must happen before this clears]

RESULT: BLOCKED — Do not deliver. Resolve flagged items and re-route to compliance.
```

**Output 2 — Pre-Delivery Review: CLEARED**
```
COMPLIANCE REVIEW — PRE-DELIVERY
Document: [document name]
Property: [address]
Review date: [date]

FLAGS: None

RESULT: CLEARED — Document is compliant. Approved for delivery.
```

**Output 3 — Post-Signature Sign-Off Checklist: CLEARED**
```
COMPLIANCE SIGN-OFF CHECKLIST
Document: [document name]
Property: [address]
Executed by: [all signing parties]
Return date: [date]

COMPLETENESS CHECK:
- [x] All signature lines signed
- [x] All date fields filled
- [x] All initialing blocks initialed
- [x] Page count matches — [X] of [X] pages present
- [x] All required addenda attached and signed

CONSISTENCY CHECK:
- [x] Party names consistent throughout
- [x] Property address consistent throughout
- [x] Dollar amounts consistent throughout

FLAGS: None

RESULT: CLEARED — Document is compliant. File in transaction record. Notify transaction coordinator.
```

**Output 4 — Post-Signature Audit: FLAGGED**
```
COMPLIANCE SIGN-OFF CHECKLIST
Document: [document name]
Property: [address]
Return date: [date]

COMPLETENESS CHECK:
- [x or FAIL] [each item]

FLAGS:
[number]. [BLOCKING] — Page [X], [location]
   Issue: [exact description]
   Required action: [what must happen to resolve]

RESULT: FLAGGED — Return to transaction coordinator. Do not file until resolved.
```

---

## Routing After Compliance Output

| Result | Next step |
|--------|-----------|
| Pre-delivery CLEARED | Orchestrator routes back to transaction coordinator for delivery |
| Pre-delivery BLOCKED | Orchestrator returns to originating specialist with flags |
| Post-signature CLEARED | File in transaction record, notify transaction coordinator |
| Post-signature FLAGGED | Return to transaction coordinator for resolution |
