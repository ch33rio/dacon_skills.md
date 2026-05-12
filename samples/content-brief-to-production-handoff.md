# Sample Deliverable: Content Brief To Production Handoff

Use case: A content or creative team turns messy campaign notes into a cleaner production handoff for writers, designers, or editors.

## Workflow Map

Current workflow:

1. Strategy or account notes are collected from a call, dashboard, or planning doc.
2. A producer rewrites those notes into a brief.
3. Missing decisions are discovered late by writers, designers, or editors.
4. Production loses time clarifying audience, deliverable, proof points, and approval needs.

Bottleneck:

The handoff mixes strategy, copy requirements, creative constraints, and open questions in one loose note.

Small fix:

Use a structured prompt that separates the handoff into production-ready sections and flags missing decisions before work starts.

## Input Example

```text
Client wants a mid-funnel white paper and 3 LinkedIn posts from the same research notes. Audience is VP Marketing at B2B SaaS companies. Main angle: teams are wasting time reconciling campaign data across tools. Need proof from CRM reporting, paid media, and content analytics. Mention pipeline visibility but avoid promising revenue lift. Designer needs chart ideas. Client approval needed before Friday. Missing: final title and whether we can mention HubSpot/Salesforce by name.
```

## Prompt Workflow

Paste campaign notes into this prompt:

```text
Turn the notes below into a production handoff.

Rules:
- Do not invent claims, stats, or client approvals.
- Separate confirmed requirements from open questions.
- Keep the handoff useful for writer, designer, and account owner.
- Flag risky wording when notes mention revenue, ROI, or unsupported claims.
- Return exactly this structure:

## Production Brief
- Deliverables:
- Audience:
- Core angle:
- Must include:
- Must avoid:

## Writer Notes
- 
- 
- 

## Designer Notes
- 
- 

## Account Owner Questions
- 
- 

Notes:
{paste notes}
```

## Expected Output

## Production Brief

- Deliverables: one mid-funnel white paper and three LinkedIn posts from the same research notes.
- Audience: VP Marketing at B2B SaaS companies.
- Core angle: teams lose time reconciling campaign data across disconnected tools.
- Must include: CRM reporting, paid media, content analytics, and pipeline visibility as themes.
- Must avoid: unsupported promises about revenue lift.

## Writer Notes

- Position the white paper around operational waste and reporting clarity, not guaranteed performance gains.
- Reuse the same narrative for three LinkedIn posts: data cleanup pain, cross-tool reporting gaps, and pipeline visibility.
- Treat HubSpot/Salesforce mentions as pending until the account owner confirms brand-name approval.

## Designer Notes

- Consider a simple before/after diagram showing scattered campaign inputs becoming one reporting view.
- Use chart placeholders only where the client has approved source data.

## Account Owner Questions

- What is the final approved title or working title for the white paper?
- Can the team mention HubSpot and Salesforce by name, or should the copy use generic CRM language?

## Handoff Notes

Use this for:

- Content brief cleanup.
- Production handoff.
- Turning call notes into writer/designer instructions.
- Catching missing approvals before production starts.

Do not use this for:

- Inventing claims.
- Creating unsupported case-study metrics.
- Publishing confidential client details.

Quality check:

- Every output line should trace back to the input note.
- Open questions should stay questions, not assumptions.
- Risky claims should be softened or flagged before client review.
