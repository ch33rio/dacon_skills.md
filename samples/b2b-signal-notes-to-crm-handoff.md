# Sample Deliverable: B2B Signal Notes To CRM Handoff

Use case: A B2B growth team collects account signals and needs a clean CRM handoff for sales or customer-facing follow-up.

## Workflow Map

Current workflow:

1. Signal notes arrive from campaigns, content engagement, LinkedIn activity, CRM updates, or sales context.
2. Someone turns those notes into an account summary.
3. Sales or account teams need the likely pain, next step, and missing context.
4. Handoffs vary by person and often include speculation.

Bottleneck:

Signal notes mix facts, guesses, and action ideas. The next owner needs a concise handoff without invented intent.

Small fix:

Use a structured prompt that separates observed signals, possible pain, confidence level, and next action.

## Input Example

```text
Account: Northstar Analytics. VP Demand Gen downloaded attribution checklist and attended webinar on campaign reporting. CRM has open renewal discussion in 60 days. Paid search campaign had high CPL last quarter. SDR note says team uses HubSpot and Salesforce but reporting is manual. No direct request yet. Need a clean handoff for AE before Thursday.
```

## Prompt Workflow

Paste signal notes into this prompt:

```text
Convert the signal notes below into a CRM handoff.

Rules:
- Do not infer buying intent beyond the notes.
- Separate observed facts from possible pain.
- Use a confidence level: High, Medium, or Low.
- Suggest one next action that is useful and low-pressure.
- Return exactly this structure:

| Account | Observed Signals | Possible Pain | Confidence | Suggested Next Step | Missing Context |

Signal notes:
{paste notes}
```

## Expected Output

| Account | Observed Signals | Possible Pain | Confidence | Suggested Next Step | Missing Context |
|---|---|---|---|---|---|
| Northstar Analytics | VP Demand Gen downloaded attribution checklist, attended campaign reporting webinar, renewal discussion in 60 days, prior high CPL, manual HubSpot/Salesforce reporting noted by SDR | Campaign reporting and attribution cleanup may be a current operational pain | Medium | AE should ask whether reporting cleanup is part of the renewal planning conversation and offer a short workflow review | Whether the VP requested help, who owns reporting, and what manual reporting steps are most painful |

## Handoff Notes

Use this for:

- CRM handoff cleanup.
- Signal triage.
- Account planning notes.
- Low-pressure follow-up preparation.

Do not use this for:

- Claiming intent that is not in the notes.
- Automated outreach at scale.
- Regulated lead scoring or eligibility decisions.
- Storing private customer data in public tools.

Quality check:

- Observed signals should be factual.
- Possible pain should be phrased as a possibility.
- Suggested next step should be specific and non-pushy.

## Need This For Your Workflow?

This sample is part of the $99 AI Workflow Audit + One Automation Fix starter.

- Email ready-to-buy details, no GitHub sign-in required: hoonso20@naver.com
- Landing preview: https://rawcdn.githack.com/ch33rio/dacon_skills.md/1745b44d4ed8db7ab4132ef18b831f718b0c9216/public/index.html
- Buy form for signed-in GitHub buyers: https://github.com/ch33rio/dacon_skills.md/issues/new?template=buy-workflow-audit.yml
- Offer scope: https://github.com/ch33rio/dacon_skills.md/blob/main/offers/ai-workflow-audit.md

Do not post private customer data, credentials, production secrets, or payment details in public GitHub issues.
