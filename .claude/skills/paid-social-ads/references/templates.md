# Templates

## 1. Campaign Decision (decision.md)

```
# Campaign Decision: [name] [YYYY-MM]

Offer:            [what is sold, price, next step]
Objective:        [Leads | Sales | Messages | Traffic for pool-building]
Primary KPI:      [one metric]
Markets:          [max 2 for a launch]
Pain point:       [one per ad set]
Platforms:        [per market, from market-matrix.md]
Budget total:     [amount] over [days]
Budget math:      target cost per event [x] × 50 ÷ 7 = [y]/day per ad set
                  Real budget per ad set: [z]/day → chosen option: [1 | 2 | 3 | 4] because [reason]
Continue if:      [cost per qualified lead ≤ X by day 28]
Stop if:          [no qualified lead after spend of Y]
Assumptions:      [every number not from real data, labelled as assumption]
Owner:            [who presses publish, who answers leads, response time]
```

## 2. Naming and UTMs

Campaign: `[Brand]_[Obj]_[Launch|Mo]_[YYYY-MM]` → `DXV_LEADS_Launch_2026-12`
Ad set: `[CC]_[lang]_[pain]_[aud]` → `DE_de_service_broad`, `CR_es_visibility_rt30`
Ad: `[fmt]_[hook]_[v]` → `vid916_pain_v1`, `car45_proof_v2`

UTMs (Meta dynamic parameters shown):
```
utm_source={{site_source_name}}
utm_medium=paid_social
utm_campaign={{campaign.name}}
utm_content={{adset.name}}__{{ad.name}}
utm_term=[pain]
```
LinkedIn: write static values matching the same names.

## 3. Ad creative brief (one per ad)

```
Ad name:        [from naming]
Ad set:         [market, language, pain, audience]
Format:         [9:16 video | 4:5 carousel | 4:5 static | Lead form | Click-to-WhatsApp]
Hook (0 to 2s): [the line or visual that stops the scroll]
Pain:           [one, in the audience's own words]
Shift:          [what changes after]
Proof:          [real, on file]
Next step:      [one, small]
Visual:         [what is on screen, safe zones respected]
On-screen text: [max ~7 words per frame]
AI used?:       [yes/no → disclosure on]
Skill hand-off: [hook-writer | reels-script | carousel-writer | canva | image-prompt …]
```

## 4. Ad copy slots

| Platform | Slot | Guidance |
|---|---|---|
| Meta | Primary text | First ~125 characters show before "more". Put hook + who-it's-for there. |
| Meta | Headline | Short, ~40 characters. The outcome, not the brand name. |
| Meta | Description | Often hidden. Never put essential info here. |
| Meta | CTA button | Learn more / Sign up / Book now / Send WhatsApp message. Match the landing page. |
| LinkedIn | Intro text | First ~150 characters visible. Lead with the specific situation. |
| LinkedIn | Headline | ~70 characters max recommended. |
| LinkedIn | Lead Gen Form | 3 to 5 fields max. Every extra field costs leads. |

Write 3 variants of primary text per ad: pain-led, proof-led, founder-voice. Same hook visual, different
words, so the test isolates copy.

## 5. Pre-launch checklist (checklist.md)

Tracking and consent
- [ ] Meta Pixel / LinkedIn Insight Tag installed and firing (test with Events Manager / Tag Helper)
- [ ] Conversions API (server events) set up or explicitly waived
- [ ] Consent banner blocks pixels until opt-in (EU/UK); reject as easy as accept
- [ ] Conversion event defined and tested end to end (submit a real test lead)
- [ ] UTMs on every ad and visible in analytics

Landing page per language
- [ ] Page exists in the ad's language and matches the ad's promise
- [ ] Impressum / company details and privacy notice (market-specific, see market-matrix.md)
- [ ] Loads fast on mobile, form or WhatsApp button above the fold
- [ ] Thank-you page or message states what happens next and when

Ads
- [ ] One objective, one KPI, thresholds written in decision.md
- [ ] Naming convention followed
- [ ] 4:5 and 9:16 versions for every concept, safe zones respected
- [ ] Copy checked against brand voice rules and guardrails file
- [ ] No unsubstantiated claims, no fake urgency, no personal-attribute phrasing
- [ ] AI disclosure on where AI was used
- [ ] Exclusions set (customers, staff, converters)
- [ ] Spending limit set on the account

Operations
- [ ] Named person answers leads/chats, response-time target set, coverage for LatAm hours
- [ ] CRM or sheet ready to log lead → reply → call booked → deal
- [ ] Read dates in the calendar: day 3, 7, 14, 28

## 6. Read report (reads/day-XX.md)

```
# Read: day [XX] — [campaign]
Source: [platform export file / numbers given by human on DATE]

| Ad set | Spend | Primary events | Cost/event | Qualified | Booked | Notes |
|---|---|---|---|---|---|---|

Winners:   [ad names + why]
Kill:      [ad names + rule applied]
Next:      [max 3 actions]
Learning:  [one sentence for ads/learnings.md]
```
Leave cells empty rather than estimate.
