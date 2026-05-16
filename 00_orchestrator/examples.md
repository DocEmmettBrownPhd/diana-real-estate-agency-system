# Orchestrator — Examples

## Example 1: New Buyer Inquiry

**Incoming request:**
"Got a new lead from Zillow. Marcus and Tanya Webb. Looking to buy in South Austin, budget around $450K, want to move in before school starts in August."

**Orchestrator response:**

Routing to: 01_lead_qualifier

Reason: New buyer inquiry requiring full intake before any research or communication.

Handoff package:
- Lead names: Marcus and Tanya Webb
- Source: Zillow inquiry
- Type: Buyer
- Initial details provided: South Austin, budget ~$450K, timeline before August school start
- Agent assigned: [agent name]
- Status: No prior contact on file

Next step after qualification: 02_property_research

---

## Example 2: Signed Document Returned

**Incoming request:**
"The Nguyens just sent back the signed listing agreement."

**Orchestrator response:**

Routing to: 05_compliance (post-signature audit)
Also notifying: 04_transaction_coordinator

Reason: Executed document returned — compliance post-signature audit required before filing.

Handoff package:
- Document type: Listing agreement
- Client: Nguyen family
- Agent: [agent name]
- Stage: Executed — returned signed by sellers
- Action needed: Post-signature audit — verify all signatures, dates, initials, and required Texas disclosures present

Note to transaction coordinator: Compliance will return a sign-off checklist or a flagged review. Do not file until compliance clears it.

---

## Example 3: Ambiguous Request

**Incoming request:**
"Can you help me with the Johnson deal?"

**Orchestrator response:**

Before I route this, I need one clarification:

What do you need on the Johnson deal right now — is this about a document that came back signed, a deadline, a client communication, or something else?

(One answer routes this immediately to the right specialist.)
