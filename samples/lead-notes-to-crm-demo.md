# Sample Deliverable: Lead Notes to CRM Rows

Use case: A small agency receives messy lead notes from calls, email, or forms and needs clean CRM-ready rows.

## Workflow Map

Current workflow:

1. Lead details arrive as free-form notes.
2. Someone rereads the note and extracts name, company, need, urgency, budget, and next step.
3. The data is pasted into a CRM or spreadsheet.
4. Follow-up tasks are written manually.

Bottleneck: manual extraction is slow and inconsistent.

Small fix: use a structured prompt to convert messy notes into a standard CRM row and a follow-up task.

## Input Example

```text
Talked to Mina from BrightDesk. They run a 12-person customer support team and spend too much time rewriting the same refund and onboarding replies. They use Zendesk and Google Sheets. Wants something simple by next week, budget maybe 300-500 if it saves a few hours each week. Send examples and ask for 3 recent anonymized tickets.
```

## Prompt Workflow

Paste one lead note into this prompt:

```text
Convert the lead note below into a CRM-ready row.

Rules:
- Do not invent missing details.
- Use "unknown" when information is not present.
- Keep the pain point specific.
- Make the next step action-oriented.
- Flag the lead as high priority only if urgency, budget, and clear business pain are present.

Return this exact Markdown table:
| Contact | Company | Team / Role | Pain | Tools | Timeline | Budget | Priority | Next Step |

Lead note:
{paste lead note}
```

## Expected Output

| Contact | Company | Team / Role | Pain | Tools | Timeline | Budget | Priority | Next Step |
|---|---|---|---|---|---|---|---|---|
| Mina | BrightDesk | 12-person customer support team | Rewriting repeated refund and onboarding replies takes too much time | Zendesk, Google Sheets | Next week | $300-$500 | High | Send examples and request 3 anonymized recent tickets |

## Handoff Notes

Use this for:

- Lead qualification.
- CRM cleanup.
- Follow-up planning.
- Turning call notes into structured sales data.

Do not use this for:

- Sensitive personal data without approval.
- Automated outreach at scale.
- Guessing budget, urgency, or contact details.

Quality check:

- Every output field should be traceable to the input note.
- Missing fields should say "unknown."
- The next step should be a concrete action.

## Suggested Next Improvement

If this works manually, the next paid milestone could connect a form or spreadsheet to the prompt workflow and write results into a CRM import sheet.

## Need This For Your Workflow?

This sample is part of the $99 AI Workflow Audit + One Automation Fix starter.

- Email ready-to-buy details, no GitHub sign-in required: hoonso20@naver.com
- Landing preview: https://rawcdn.githack.com/ch33rio/dacon_skills.md/1745b44d4ed8db7ab4132ef18b831f718b0c9216/public/index.html
- Buy form for signed-in GitHub buyers: https://github.com/ch33rio/dacon_skills.md/issues/new?template=buy-workflow-audit.yml
- Offer scope: https://github.com/ch33rio/dacon_skills.md/blob/main/offers/ai-workflow-audit.md

Do not post private customer data, credentials, production secrets, or payment details in public GitHub issues.
