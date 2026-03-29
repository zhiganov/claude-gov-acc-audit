---
name: gov/acc Audit
description: Analyze governance systems using research-backed diagnostic lenses from the gov/acc community. Reads actual governance data — proposals, votes, forums, constitutions — and identifies structural patterns.
---

# gov/acc Audit

Analyze a governance system using diagnostic lenses from the gov/acc (governance acceleration) research community. This is not a checklist — it reads actual governance artifacts and identifies structural patterns, divergences between stated values and actual behavior, and conditions that make specific failure modes likely.

**Trigger:** `/gov-acc-audit <subject>` optionally with `--focus <lens>`

The subject can be: a DAO (by name or URL), a protocol's governance framework, a community's decision-making process, an organization's bylaws.

## Background

The gov/acc initiative (Metagov, 2026) brings together governance practitioners through structured interviews, workshops, and deliberation platforms. The community has identified recurring governance failure modes and the structural conditions that produce them.

This skill uses those findings as **diagnostic lenses** — not things to check off, but patterns to look for in real governance data.

## Process

### Step 1: Gather governance artifacts

Collect as much real data as possible about the system. The more data, the better the analysis.

**Onchain / platform data:**
- Proposals and their outcomes (Tally, Agora, Snapshot, Governor contracts)
- Voting records — participation rates, vote distribution, delegate behavior
- Treasury flows — where money goes, who decides
- Token distribution — concentration, delegation patterns

**Offchain artifacts:**
- Constitution, charter, bylaws, operating manual
- Forum discussions (Discourse, Commonwealth) — especially contentious proposals
- Delegate statements and platforms
- Meeting notes, call recordings, governance reports
- Communication channels (Discord governance channels, Telegram groups)

**Use web search and available MCP tools** to fetch current data. For major DAOs, governance platforms (Tally, Agora, Boardroom) have public APIs and dashboards.

### Step 2: Quantitative analysis

Before interpreting, establish the baseline numbers:

- **Participation trends** — voter turnout over time, by proposal type. Is it rising, falling, stable?
- **Power concentration** — what % of voting power is held by top 10/20/50 addresses? How has this changed?
- **Proposal velocity** — how many proposals per month? What % pass? What % are contested?
- **Delegate health** — how many active delegates? Retention rate? Voting consistency?
- **Treasury deployment** — burn rate, allocation categories, accountability mechanisms
- **Time-to-decision** — how long from proposal to execution?

Present these as facts before drawing conclusions.

### Step 3: Structural diagnosis

Using the gov/acc diagnostic lenses, analyze what the data reveals about the system's structural health. For each lens that applies, look for **specific evidence** in the artifacts — not abstract risks, but concrete patterns.

#### Lens 1: Power distribution
*Not "is there plutocracy?" but "what does voting power concentration actually mean for this system's decisions?"*

- Who controls outcomes? Trace the last 20 contested proposals — did the same wallets/delegates decide them?
- What decisions can small holders actually influence?
- Is there a path from participation to power, or is power static?

#### Lens 2: Decision legitimacy
*Not "is there governance theater?" but "where do stated process and actual decision-making diverge?"*

- Which important decisions went through governance vs were made informally?
- Are there patterns of proposals being pre-negotiated before the vote?
- Do governance outcomes actually get implemented? Track execution rate.

#### Lens 3: Participation sustainability
*Not "is there voting fatigue?" but "what is the actual participation trajectory and what's driving it?"*

- Participation trend by proposal type — maybe core protocol votes get turnout but grants don't
- What's the delegate churn rate? Why are delegates leaving?
- Is the system asking too much of participants, or too little?

#### Lens 4: Information asymmetry
*Not "is there narrative capture?" but "who has access to what information and how does that shape decisions?"*

- Are proposal impacts well-communicated before votes?
- Do insiders have context that regular participants lack?
- How accessible is governance information to newcomers?

#### Lens 5: Contributor alignment
*Not "are contributors compensated?" but "does the incentive structure produce the behaviors the system needs?"*

- What gets rewarded? What gets ignored?
- Are the people doing critical work also the people with governance influence?
- Is there a contributor pipeline or just an insider circle?

#### Lens 6: Resource allocation
*Not "are grants dysfunctional?" but "does capital flow toward the system's stated priorities?"*

- Map treasury outflows against stated strategic priorities — do they align?
- What's the accountability chain for funded work?
- How does the system learn from past allocation decisions?

#### Lens 7: Institutional coherence
*Not "is there a clear purpose?" but "does the system act as if it has a coherent purpose?"*

- Do proposals and decisions point in a consistent direction?
- Can members articulate what the system is for — and do they agree?
- When priorities conflict, how are tradeoffs made?

#### Lens 8: Adaptive capacity
*Not "can governance evolve?" but "how has it actually evolved and what drove those changes?"*

- What governance changes have been made in the last year? What triggered them?
- How does the system respond to failures or crises?
- Is there a feedback loop from governance outcomes to governance design?

#### Lens 9: Knowledge continuity
*Not "is there institutional amnesia?" but "what happens when key people leave or context is lost?"*

- Can you reconstruct the rationale for a decision from 6 months ago?
- What happens to a workstream when its lead departs?
- Is governance knowledge in people's heads or in accessible artifacts?

#### Lens 10: Technical-social alignment
*Not "are there legal gaps?" but "where do the technical mechanisms and social reality diverge?"*

- Where do smart contract constraints not match governance intent?
- Are there workarounds that indicate the technical system doesn't fit?
- How are off-chain decisions enforced on-chain?

### Step 3b: Weight by community priorities

Fetch the [Deliberate Priority Leaderboard](https://govacc.net/deliberate/leaderboard) to understand what the broader governance community considers most urgent. Use the priority scores to weight the analysis — lenses aligned with higher-ranked priorities deserve deeper investigation.

For example, if participation/onboarding is the #1 community priority (score 0.40) and the subject DAO has 2.8% voter turnout, that's not just a finding — it's the most critical gap relative to what the community has identified as important.

### Step 4: Comparative context

If data is available, compare against peer governance systems. What do similar DAOs/communities do differently? What's worked? This isn't about copying — it's about understanding the range of viable approaches.

### Step 5: Report

```markdown
# gov/acc Analysis: {subject}
Date: {today}

## Governance at a Glance

{Key numbers: participation rate, power concentration, proposal velocity,
treasury size, active delegates. Just facts.}

## Structural Analysis

### {Lens name}

**What the data shows:** {Specific evidence from artifacts}

**What this means:** {Interpretation — what structural conditions exist
and what they make likely}

**What peers do differently:** {Comparative context if available}

... (repeat for each applicable lens)

## What's Working

{Genuine strengths — not generic praise, but specific structural
features that produce good outcomes. Reference evidence.}

## Structural Risks

{Not "you have problem X" but "these structural conditions make Y likely."
Each risk should be evidence-based and include what would need to change
structurally — not just "add quadratic voting" but why and what it
would change about the specific dynamics observed.}

## Recommendations

{Specific, actionable, grounded in the analysis.
For each recommendation: what to do, why it addresses the
structural condition identified, and what to watch for.}
```

### Step 6: Offer next steps

- "Want me to analyze a specific aspect in more depth?"
- "Want me to draft governance proposals to address the structural risks?"
- "Want to compare this against another governance system?"
- "Want me to evaluate how specific changes would affect the dynamics I identified?"

## Focus flags

`power`, `legitimacy`, `participation`, `information`, `contributors`, `resources`, `coherence`, `adaptation`, `knowledge`, `technical`, `all`

## Optional MCP integrations

- **living-structure** — does the governance exhibit Alexander's properties? (boundaries, gradients, subsidiarity as levels of scale)
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's framework for legitimate governance
