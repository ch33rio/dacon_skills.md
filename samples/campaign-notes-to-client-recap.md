# Sample Deliverable: Campaign Notes to Client Recap

Use case: A marketing agency reviews weekly campaign observations and needs a concise client-ready recap plus internal next actions.

## Workflow Map

Current workflow:

1. Campaign manager checks dashboard notes, ad platform observations, search terms, CRM signals, or content performance notes.
2. Notes are copied into a doc or Slack thread.
3. Someone rewrites them into client-friendly bullets.
4. Internal follow-up tasks are written separately.

Bottleneck: the rewrite step is repetitive and easy to make either too vague for the client or too detailed for a weekly recap.

Small fix: use a structured prompt that separates client-facing recap, risks, next actions, and missing data.

## Input Example

```text
Client: Northstar Dental. Week of May 4. Google Ads leads up 18% WoW, but CPL rose from $42 to $51. Branded search stable. Nonbrand emergency dentist terms got clicks but low form completion. Landing page mobile speed looks slow from PageSpeed note. CRM says 7 calls marked missed after 5pm. SEO blog on dental implants got 22% more organic sessions but no tracked conversions yet. Need client update and internal next steps.
```

## Prompt Workflow

Paste weekly notes into this prompt:

```text
Turn the campaign notes below into a client-ready weekly recap and internal action list.

Rules:
- Do not invent metrics or causes.
- Separate client-facing summary from internal tasks.
- Keep client bullets clear and non-technical unless a technical issue affects results.
- Call out missing data as a question, not a conclusion.
- Include exactly 3 client recap bullets, 3 internal next actions, and 2 follow-up questions.

Return this structure:
## Client Recap
- 
- 
- 

## Internal Next Actions
- 
- 
- 

## Follow-up Questions
- 
- 

Campaign notes:
{paste notes}
```

## Expected Output

## Client Recap

- Lead volume improved this week, with Google Ads leads up 18% week over week, while cost per lead also increased from $42 to $51.
- Nonbrand emergency dentist traffic is getting clicks but is not completing forms at the same rate, so that segment needs landing page and intent review.
- Organic traffic to the dental implants blog increased 22%, but conversion impact is not confirmed yet because tracked conversions are not showing.

## Internal Next Actions

- Review emergency dentist search terms, landing page alignment, and mobile form behavior before the next client update.
- Check mobile speed issues flagged by PageSpeed and identify one practical fix for the landing page.
- Compare missed calls after 5pm with ad schedule and call-routing coverage before recommending budget or schedule changes.

## Follow-up Questions

- Are the 7 missed after-hours calls included in lead counts, and should call handling be part of this week's action plan?
- Is conversion tracking configured for the dental implants blog path, or do we need to add/verify tracking before drawing conclusions?

## Handoff Notes

Use this for:

- Weekly paid search recaps.
- SEO/content performance notes.
- CRM signal triage.
- Turning dashboard observations into client update bullets.

Do not use this for:

- Inventing attribution.
- Hiding negative performance.
- Making budget recommendations without enough data.
- Sharing confidential client data in public tools.

Quality check:

- Every metric should trace back to the input notes.
- Internal tasks should be action-oriented.
- Client recap bullets should be readable without ad-platform context.
