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

## Example 2: Document Outbound Review

**Incoming request:**
"Can you send the listing agreement to the Nguyens? I think everything is good but just want to make sure."

**Orchestrator response:**

Routing to: 05_compliance (pre-delivery review)

Reason: Outbound document requires compliance review before it goes to the client.

Handoff package:
- Document type: Listing agreement
- Client: Nguyen family
- Agent: [agent name]
- Stage: Pre-signature, ready to send pending compliance review
- Action needed: Flag any issues; clear for delivery if clean

Note to agent: Compliance will return a flagged review or a clear-to-send. Do not deliver to client until compliance sign-off is received.

---

## Example 3: Ambiguous Request

**Incoming request:**
"Can you help me with the Johnson deal?"

**Orchestrator response:**

Before I route this, I need one clarification:

What do you need on the Johnson deal right now -- is this about a document, a deadline, a client communication, or something else?

(One answer routes this immediately to the right specialist.)
