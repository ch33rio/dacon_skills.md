# HubSpot-Style CRM Export Cleanup Sample

This is a fictional public sample for the $99 CRM cleanup starter. It shows the kind of small, repeatable cleanup handoff a marketing team might receive after sending one safe sample export or anonymized workflow example.

Do not use real customer records, private emails, credentials, payment details, or confidential CRM exports in public GitHub issues. Use anonymized rows or email `hoonso20@naver.com` for private handoff.

## Messy Input Snapshot

```csv
company,contact,email,lifecycle,source,last note,next step,owner
Acme Dental,Jamie L.,jamie@example.invalid,lead,webinar,"asked for pricing, maybe Q2",send followup?,Sam
Acme Dental,Jamie Lee,jamie@example.invalid,MQL,Webinar,"pricing + ops team loop",book consult,Sam
Northstar Labs,Pat R.,pat@example.invalid,,linkedin,"downloaded checklist",,Ari
Bright Path Co,,ops@example.invalid,subscriber,form,"wants weekly reporting cleanup",qualify,Sam
```

## Cleaned CRM-Ready Rows

```csv
company,contact_name,email,lifecycle_stage,source,next_action,owner,cleanup_note
Acme Dental,Jamie Lee,jamie@example.invalid,MQL,webinar,Book consult with pricing and ops context,Sam,Merged duplicate Acme Dental rows; kept richer lifecycle and next step.
Northstar Labs,Pat R.,pat@example.invalid,lead,linkedin,Send checklist follow-up and ask if CRM cleanup is relevant,Ari,Filled missing lifecycle from source behavior.
Bright Path Co,Unknown,ops@example.invalid,subscriber,form,Qualify weekly reporting cleanup need,Sam,Marked missing contact name; preserve safe email only if approved for private CRM use.
```

## Reusable Cleanup Rules

1. Normalize lifecycle values before import.
2. Merge duplicate company/contact rows only when email or company + contact match.
3. Preserve the richest next action instead of the newest vague note.
4. Flag missing contact names instead of inventing them.
5. Keep source names lowercase and consistent.
6. Add a cleanup note for every row changed.

## Repeatable Prompt

```text
You are cleaning a small marketing CRM export for a human review step.

Input columns:
company, contact, email, lifecycle, source, last note, next step, owner

Return:
company, contact_name, email, lifecycle_stage, source, next_action, owner, cleanup_note

Rules:
- Do not invent missing private data.
- Merge only obvious duplicates.
- Keep one useful next action per row.
- Flag missing fields in cleanup_note.
- Use safe, concise language for handoff notes.
```

## Delivery Handoff

- Use the cleaned rows for review before import.
- Keep the cleanup rules beside the weekly CRM export process.
- If the team repeats this weekly, turn the rules into a checklist or lightweight script.
- Payment and production CRM access should be handled privately after scope is confirmed.

## Need This For Your CRM Workflow?

- CRM cleanup automation page: https://github.com/ch33rio/dacon_skills.md/blob/main/CRM-CLEANUP-AUTOMATION.md
- CRM cleanup buyer listing: https://github.com/ch33rio/dacon_skills.md/issues/3
- Proof sample index: https://github.com/ch33rio/dacon_skills.md/blob/main/samples/README.md
- Email ready-to-buy details, no GitHub sign-in required: hoonso20@naver.com

Work starts only after fit is confirmed, scope is agreed, and payment is received.