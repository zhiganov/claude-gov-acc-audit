---
name: gov/acc Audit
description: Analyze governance systems using the gov/acc research framework. Reads actual governance data — proposals, votes, forums, constitutions — and identifies what's working, what isn't, and what experiments could help.
---

# gov/acc Audit

Analyze a governance system through the lens of the gov/acc (governance acceleration) initiative. Not a checklist — reads actual governance artifacts and produces context-specific analysis grounded in what practitioners and researchers have learned.

**Trigger:** `/gov-acc-audit <subject>` optionally with `--focus <domain>`

The subject can be: a DAO (by name or URL), a protocol's governance framework, a community's decision-making process, an organization's bylaws.

## Background

Gov/acc is a time-bound research initiative (through Devcon 2026) focused on demonstrating that decentralized governance can meaningfully improve ecosystem outcomes. The core thesis: there's a critical window to prove governance's value. Without demonstrable success, ecosystems will abandon decentralization.

The initiative rejects governance maximalism — not everything should be governed decentrally. The question isn't "is governance good?" but "where does decentralized coordination add clear value, and is it working?"

This skill applies the gov/acc framework to a specific governance system: what's working, what isn't, where governance is applied to the right problems, and what experiments could improve outcomes.

Source: [gov/acc: Accelerating Governance Innovation in Web3](https://gov-acc.metagov.org/) — Eugene Leventhal, Metagov

## Process

### Step 1: Gather governance artifacts

Collect real data about the system. The more data, the better the analysis.

**Onchain / platform data:**
- Proposals and outcomes (Tally, Agora, Snapshot, Governor contracts)
- Voting records — participation rates, vote distribution, delegate behavior
- Treasury flows — where money goes, who decides
- Token distribution — concentration, delegation patterns

**Offchain artifacts:**
- Constitution, charter, bylaws, operating manual
- Forum discussions (Discourse, Commonwealth) — especially contentious proposals
- Delegate statements and platforms
- Meeting notes, governance reports, retrospectives
- Communication channels (Discord governance channels, Telegram groups)

**Use web search and available MCP tools** to fetch current data. For major DAOs, governance platforms (Tally, Agora, Boardroom) have public dashboards.

### Step 2: Establish baselines

Before interpreting, establish the numbers:

- **Participation trends** — voter turnout over time, by proposal type
- **Power concentration** — % of voting power in top 10/20/50 addresses
- **Proposal velocity** — proposals per month, pass rate, contested vs rubber-stamped
- **Delegate health** — active delegates, retention, voting consistency
- **Treasury deployment** — burn rate, allocation categories, accountability
- **Time-to-decision** — proposal to execution

Present facts before drawing conclusions.

### Step 2b: Load gov/acc research context

Fetch the gov/acc knowledge base to ground the analysis in practitioner research:

1. **[gov/acc Priority Leaderboard](https://govacc.net/deliberate/leaderboard)** — community-ranked priorities with scores. Use to weight which domains deserve deeper investigation.
2. **[gov/acc wiki](https://gov-acc.netlify.app)** — structured problems, solutions, and actor profiles. Fetch pages relevant to the patterns observed in Step 2 (e.g., if participation is low, fetch the wiki's "Voting Fatigue & Apathy" page for practitioner-identified causes and solutions).
3. **[gov/acc Research Dashboard](https://gov-acc-research.netlify.app)** — interactive data on problem breadth/depth, solution maturity, and actor networks.

**If the gov/acc MCP server is available** (planned, HAR-562): use structured queries instead of web fetching — `get_problem()`, `search_content()`, `get_solutions_for_problem()`.

This means the analysis can cite specific practitioner experiences: "28 practitioners identified token voting failure as the most prevalent governance problem — your system shows the same pattern with 85% of voting power in 15 wallets."

### Step 3: Analyze through the five gov/acc research domains

These domains come directly from the gov/acc initiative's research agenda. For each, analyze what the data reveals about this specific system. Look for evidence, not abstractions.

#### Domain 1: Participation & Voice

*What coordination problems does decentralized governance actually solve here? Is governance applied to the right surfaces?*

- What decisions go through governance? Are these the ones that *should*?
- Is there governance happening where centralized decision-making would be more effective? (governance maximalism)
- Are there decisions made centrally that the community should have voice in?
- What does the participation trajectory look like, and what's driving it?
- Do tools and processes increase participation while improving (not just legitimizing) outcomes?
- Is the community scoped to people who actually sustain the system, or is it open to drive-by voting?

#### Domain 2: Transparency & Accountability

*What does functional accountability actually look like in this system, operationally?*

- Where do stated process and actual decision-making diverge?
- Are governance outcomes implemented? Track the execution rate.
- Is proposal impact well-communicated before votes, or are people voting blind?
- Can you trace a decision from proposal to rationale to outcome to evaluation?
- Is there accountability for funded work, or just allocation?
- Where is information asymmetry — who has context that shapes decisions?

#### Domain 3: Resilience & Security

*How does this community resist capture? What operational structures enable or undermine it?*

- Can a small group of actors control outcomes? Trace contested proposals.
- What happens when key people leave? Has this been tested?
- Are there mechanisms for the community to override decisions by insiders?
- What are the attack surfaces — flash loan voting, bribery, social engineering?
- How does the system handle crises? Any past examples?

#### Domain 4: Value Creation & Funding

*Does governance drive measurable value, or is it overhead?*

- Does capital flow toward the system's stated priorities? Map treasury outflows against strategy.
- Which governance mechanisms produce specific, measurable outcomes?
- What's the cost of governance (time, attention, resources) vs the value it creates?
- Are contributors — the people doing critical work — aligned with governance incentives?
- How does the system learn from past funding decisions?

#### Domain 5: Deliberation & Culture

*Which deliberative forms produce the best outcomes here? What's the governance culture?*

- Is there genuine deliberation, or just voting on pre-formed positions?
- What's the culture around disagreement — constructive, adversarial, suppressed?
- Do newcomers have a path to meaningful governance participation?
- Is institutional knowledge preserved or lost when people leave?
- How has governance itself evolved? What triggered changes?

### Step 4: Identify appropriate governance surfaces

This is the key gov/acc question. Based on the analysis, evaluate:

- **Where governance adds value** — decisions where decentralized input genuinely improves outcomes
- **Where governance is overhead** — decisions that would be better made by a smaller group or automated
- **Where governance is missing** — important decisions made without community input that should have it

### Step 5: Report

```markdown
# gov/acc Analysis: {subject}
Date: {today}

## At a Glance

{Key numbers: participation rate, power concentration, proposal velocity,
treasury size, active delegates. Just facts.}

## Governance Surfaces

**Where governance adds value:** {evidence-based}
**Where governance is overhead:** {evidence-based}
**Where governance is missing:** {evidence-based}

## Domain Analysis

### Participation & Voice
{What the data shows, what it means, what peers do differently}

### Transparency & Accountability
{...}

### Resilience & Security
{...}

### Value Creation & Funding
{...}

### Deliberation & Culture
{...}

## What's Working

{Specific structural features producing good outcomes. Reference evidence.}

## Structural Risks

{Evidence-based risks with structural conditions that produce them.}

## Experiments to Consider

{Not generic recommendations but specific, testable experiments
this system could run. Frame as hypotheses:
"If [change], we expect [outcome], measurable by [metric]."}
```

### Step 6: Offer next steps

- "Want me to analyze a specific domain in more depth?"
- "Want me to draft governance proposals for any of the experiments?"
- "Want to compare this against another governance system?"
- "Want me to design a Harmonica deliberation session to explore these findings with the community?"

## Focus flags

`participation`, `accountability`, `resilience`, `funding`, `deliberation`, `surfaces`, `all`

## Optional MCP integrations

- **living-structure** — does the governance exhibit Alexander's properties? (boundaries, gradients, subsidiarity as levels of scale)
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's framework for legitimate governance
