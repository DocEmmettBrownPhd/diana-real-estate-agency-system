# Lead Intake — Rules

## Receiving Rules

### Always Do
- Accept leads in any format. Never reject a lead because the input is messy.
- Extract every available piece of information from the raw input before asking for more.
- Flag every missing field explicitly — do not silently skip it.
- Record the source exactly as received (Zillow, phone call, referral from [name], open house, etc.).
- Timestamp every intake entry with the date received.
- If a lead came in via email forward, capture the original sender's subject line and body verbatim in the raw notes field.

### Never Do
- Never qualify the lead. That is not your job. Receive it, standardize it, assign it.
- Never contact the lead. That is 03_client_communication.
- Never assume missing information. Mark it "Not captured" and flag for follow-up.
- Never route a lead directly to a specialist. All routing goes through 00_orchestrator after the qualifier runs.
- Never skip the distribution step. Every lead must be assigned before it moves forward.

---

## Distribution Rules

### Assignment Priority Order
1. **Capacity check first** — If an agent is at or above their active lead ceiling, they are skipped regardless of rotation.
2. **Lead type match** — If the lead type or situation matches an agent's documented specialty, weight toward that agent.
3. **Fair rotation** — Among eligible agents, assign to whoever has received the fewest leads in the current cycle.
4. **Escalate to Diana** — If all agents are at capacity, flag to Diana before assigning. Do not force an assignment.

### Active Lead Ceilings (default — Diana adjusts as needed)
| Agent | Active Lead Ceiling |
|-------|-------------------|
| Diana | 15 active leads |
| Agent 2 | 12 active leads |
| Agent 3 | 12 active leads |
| Agent 4 | 10 active leads |

### Lead Type Matching
| Lead Type | Default Assignment Logic |
|-----------|------------------------|
| High-value / luxury ($800K+) | Diana first unless at capacity |
| Complex situation (divorce, estate, bankruptcy flag) | Diana first unless at capacity |
| Spanish-speaking lead | Agent with language match if available |
| Investor / multi-property | Agent with investment experience if available |
| First-time buyer | Any available agent — note in profile for extra communication support |
| Standard buyer or seller | Rotation |
| Referral from Diana's personal network | Diana unless she explicitly redirects |

### What "Fair Rotation" Means
- Track leads assigned in the current 30-day cycle per agent.
- The agent with the lowest count among eligible agents gets the next lead.
- Ties broken by who received the last lead later (i.e. longer ago = next up).
- Reset cycle count on the 1st of each month.

### Diana's Visibility
- Every assignment is logged in the Assignment Log format (see handoff.md).
- Diana can override any assignment at any time — the log records the override and the reason.
- If two or more leads come in the same day for the same agent, flag the cluster to Diana.

---

## Source-Specific Handling

| Source | How to Handle |
|--------|--------------|
| Zillow / portal email forward | Extract name, phone, email, property of interest, message text. Note as "Portal — Zillow" or specific platform. |
| Phone call notes | Agent types what they captured. Extract all fields present. Flag gaps clearly. |
| Old contact list row | Treat as a reactivation lead. Note date of original contact if known. Flag as "Cold — reactivation." |
| Open house sign-in | Name, phone, email, property they visited, any notes the agent wrote. Flag as "Open house — [address]." |
| Text message | Extract all content. Note as "Text — agent relayed." |
| Referral | Note the referral source by name. This is a warm lead — flag as "Referral — [source name]." |
| Walk-in / in-person | Same as phone call notes. |
