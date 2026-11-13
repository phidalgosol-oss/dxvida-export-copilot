---
name: paid-social-ads
description: Plan, build, launch and read paid social ad campaigns (Meta = Instagram + Facebook, LinkedIn, TikTok) for B2B SMB audiences across multiple countries and languages. Use when someone says "ads", "paid campaign", "boost", "Meta Ads Manager", "LinkedIn ads", "ad budget", "ad creative", "launch push", "retargeting", "lead ads", "CPA/CPL/ROAS", or wants a launch or monthly campaign that spends money. Covers the decision layer the organic skills skip: one objective, budget math against the learning phase, campaign architecture, market and language split, creative testing matrix, tracking and consent, per-country ad compliance, kill and scale rules, and the day 7/14/28 read. Hands organic content, hooks, captions and visuals to the installed social-media-skills. Never fabricates metrics or benchmarks.
version: '1.0.0'
---

# paid-social-ads

Organic content earns attention slowly. Paid ads buy it fast and send a bill. This skill exists so the bill
buys **learning first and leads second**, and never pays for vanity reach.

The agent plans, writes, checks and reads. The human owns the ad account, the card, the final click on
"Publish" and every claim that goes live.

## Read these first (stop if missing)

1. **Brand files in the repo.** Search for `brand-profile*`, `*strategy*`, `*voice*`, `*icp*`, `*pricing*`.
   If no brand profile exists, run `social-media-skills:brand-profile` before anything else.
2. **The offer.** What exactly does the ad sell, at what price, with what next step (demo call, free audit,
   training seat, lead magnet). No offer = no ad. Say so and stop.
3. **The landing page per language.** An ad without a matching landing page in the ad's language wastes
   the click. Check it exists and has an Impressum/legal notice and a consent banner (see
   `references/market-matrix.md`).
4. **Any guardrails file** (phrasing rules, banned claims, approved numbers). Treat it as binding.

## Hard rules

- **One campaign, one objective, one primary KPI.** Never "awareness and leads and followers."
- **Never invent numbers.** No benchmark CPMs, CTRs or CPAs presented as fact. Use the human's own past
  data or label figures as planning assumptions to replace after day 7.
- **No claim the business can't prove.** No "guaranteed", no fake scarcity, no fake testimonials, no
  invented client logos. Results claims need substantiation on file.
- **AI-generated or AI-edited visuals and voices get disclosed** (Meta "AI info" label, platform toggles,
  EU AI Act Art. 50 transparency applies from 2 Aug 2026).
- **Tracking before spend.** Pixel/Insight Tag firing, consent working, UTMs set. Otherwise the money buys
  no learning.
- **Write copy in the brand's voice rules.** If the repo has style rules (e.g. no Oxford commas, no
  em-dashes, short declarative sentences), they apply to ad copy too.

## The workflow: AIM, BUILD, RUN, READ

### 1. AIM: decide before you design

Produce a one-page **Campaign Decision** (template in `references/templates.md`):

| Decision | Rule |
|---|---|
| Objective | Pick the deepest event the budget can feed (see budget math). Usually Leads or Sales. Awareness only if a retargeting pool is the explicit goal. |
| Primary KPI | One of: cost per qualified lead, cost per booked call, cost per landing page view (only for pool-building). |
| Markets in the launch | Max 2 for a first launch. More markets split the budget and nobody learns. Expand after the read. |
| Pain point | One per ad set. Three pains in one ad = no pain. |
| Platform per market | Use `references/market-matrix.md`. Do not default to Instagram for every country. |
| Success threshold | Write the number that means "continue monthly" and the number that means "stop" before launch. |

### 2. Budget math: the part most SMB campaigns get wrong

Ad platforms optimise in a **learning phase** (Lernphase). Meta's long-standing guidance is roughly
**50 optimisation events per ad set per week** to exit it. Fewer events = unstable delivery and noisy data.

```
min daily budget per ad set ≈ (target cost per event × 50) ÷ 7
```

Example as a planning assumption: target cost per lead €25 → €25 × 50 ÷ 7 ≈ **€179/day per ad set**.

If the real budget is far below that, do **not** spread it thin. Pick one of these, in this order:

1. **Fewer ad sets.** One ad set per market, broad targeting, creatives carry the targeting.
2. **Optimise for a shallower event** that happens 5 to 10 times more often (landing page view, lead form
   open, video 50% view) and build a retargeting pool, then run a small conversion campaign on the pool.
3. **Fewer markets.** Drop to one market until the funnel is proven.
4. **Accept "learning limited"** and judge on a longer window (14 to 28 days), stated up front.

Always show the human the math with their numbers. Always state which option you chose and why.

### 3. BUILD: campaign architecture

Default structure for a multi-market B2B SMB launch on Meta:

```
Campaign: [Brand]_[Objective]_[Launch|Monthly]_[YYYY-MM]
  Ad set: [Market]_[Lang]_[Pain]_[Audience: Broad|LAL|Retarget]
    Ad: [Format]_[Hook angle]_[v1..vN]
```

- **Separate ad sets by language**, never mix languages in one ad set.
- **Broad or Advantage+ audience** as default for prospecting. Interest stacks narrow the algorithm and
  rarely beat creative-led targeting. Use interests only as a test arm.
- **Retargeting ad set** for site visitors, video viewers and IG/FB engagers (30 to 90 days). Different
  copy: answer the objection, show proof, make the next step smaller.
- **Exclusions:** existing customers, employees, recent converters.
- **Placements:** Advantage+ placements unless creative only exists in one ratio. Supply 4:5 (feed) and
  9:16 (Reels/Stories) for every concept. Keep text and logos out of the top ~14% and bottom ~35% of 9:16.
- **LinkedIn:** Lead Gen Form or Thought Leader Ad (boosting the founder's post). Target by company size
  (2 to 200), job function and country. Expect higher cost per click than Meta and plan budget for it.
- **WhatsApp / Messenger click-to-chat** (Meta) for LatAm markets where buyers prefer chat over forms.
  Someone must answer within business hours or the lead dies.

Naming convention and UTM scheme in `references/templates.md`. Use them exactly so the read is possible.

### 4. Creative: concept matrix, not random posts

Creative is the targeting now. Build a **concept matrix**:

| | Hook A: pain | Hook B: proof | Hook C: founder |
|---|---|---|---|
| Format 1: 9:16 video 15 to 30s | | | |
| Format 2: 4:5 carousel | | | |
| Format 3: 4:5 static | | | |

- 3 to 5 ads per ad set at launch. Test **one variable at a time** (hook angle first, then format).
- Every ad answers in the first 2 seconds or first line: who it's for, what pain, what changes.
- Hand production to installed skills: `social-media-skills:hook-writer`, `short-form-video-script`,
  `reels-script`, `carousel-writer`, `talking-head-and-piece-to-camera`, `canva`, `image-prompt`,
  `ai-video`, `captions-and-clipping`, `platform-specs-and-validation`.
- Ad copy slots and character guidance in `references/templates.md`.
- Translate by **transcreation**, not translation. German SMB copy ≠ Mexican SMB copy. Use local
  examples, local currency, local formality (Sie vs. du, usted vs. tú).

### 5. RUN: launch checklist

Run `references/templates.md → Pre-launch checklist`. Do not mark ready until every box is ticked or
explicitly waived by the human with a reason.

### 6. READ: decision points, not dashboards

| When | Look at | Decide |
|---|---|---|
| Day 2 to 3 | Delivery, CTR (link), hook rate (3s views ÷ impressions), comments for objections | Fix broken ads only. Do not touch budgets. |
| Day 7 | Cost per primary event per ad and per ad set | **Kill** ads that spent ~2× target cost with zero events. Keep the rest. Add 1 to 2 new ads built on the winning hook. |
| Day 14 | Cost per event, lead quality (did leads book? reply?) | **Scale** winners by 20 to 30% per step, not doubling. Pause losing markets. |
| Day 28 | Cost per qualified lead or booked call vs. the pre-set threshold | **Go / no go** for monthly plan. Write it down. |

Lead quality beats lead price. A €15 lead that never answers loses to a €60 lead that books. Always ask the
human for the downstream outcome (calls booked, deals) before declaring a winner.

Never report a number the human did not give you or the platform export does not show. Use
`social-media-skills:analytics-and-reporting` for the report format.

### 7. Monthly cadence (if the launch passes)

- Week 1: read last month, retire fatigued ads (frequency > ~3 to 4 on prospecting, or falling CTR).
- Week 2: ship 3 to 5 new ads on the winning angle plus one wild-card angle.
- Week 3: expand one variable (new market OR new pain OR new format, never two at once).
- Week 4: read, decide, log learnings in `ads/learnings.md` so next month starts smarter.

## Outputs this skill produces

Save to the repo under `ads/[YYYY-MM]-[campaign]/`:

1. `decision.md` — the Campaign Decision page with budget math.
2. `structure.md` — campaigns, ad sets, ads, naming, UTMs, audiences, exclusions.
3. `creative-briefs.md` — concept matrix plus one brief per ad, per language.
4. `copy.md` — final ad copy per ad and language, ready to paste.
5. `checklist.md` — pre-launch checklist with status.
6. `reads/day-07.md`, `day-14.md`, `day-28.md` — filled only from real numbers.

## Hand-offs

- Organic launch arc around the ads: `social-media-skills:campaign-and-launch-planning`
- Lead magnet and funnel behind the ad: `social-media-skills:lead-magnets-and-funnels`
- DM and chat follow-up: `social-media-skills:social-selling-and-dm`
- Testing method: `social-media-skills:experimentation-and-ab-testing`
- Targets: `social-media-skills:goals-and-kpis`
