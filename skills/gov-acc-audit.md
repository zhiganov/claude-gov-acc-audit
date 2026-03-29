---
name: gov/acc Audit
description: Evaluate governance systems against research-backed principles from the gov/acc community. Works on DAOs, communities, organizations, protocols.
---

# gov/acc Audit

Evaluate a governance system against principles surfaced by the gov/acc (governance acceleration) research community — 50+ governance practitioners across web3, civic tech, and institutional design.

**Trigger:** `/gov-acc-audit <subject>` optionally with `--focus <category>`

The subject can be: a DAO constitution, a community's decision-making process, a protocol's governance framework, an organization's bylaws, a forum, or an onchain voting system.

## Background

The gov/acc research (Metagov, 2026) identified 11 core governance problems through structured interviews with governance practitioners. These problems — and the solutions practitioners proposed — form an empirically-grounded checklist for evaluating governance health.

This isn't theoretical — every item was identified by real governance practitioners describing real failures they experienced.

## Process

### Step 1: Understand the system

Gather the governance artifacts:
- **Constitutions / bylaws / charters** — the formal rules
- **Forum posts / proposals** — how decisions are actually discussed
- **Voting records** — who votes, participation rates, outcomes
- **Treasury/funding flows** — how resources are allocated
- **Contributor structures** — who does the work, how they're compensated
- **Communication channels** — where governance happens informally

Read what's available. The audit works with whatever artifacts exist — a DAO with extensive documentation and a small community with just a Discord are both valid subjects.

### Step 2: Evaluate against the 11 governance problems

For each problem, assess whether the governance system is vulnerable to it. Score:
- `[x]` **Protected** — system has mechanisms that prevent or mitigate this
- `[~]` **Partially addressed** — some protections exist but gaps remain
- `[ ]` **Vulnerable** — no meaningful protection; this failure mode is likely
- `[n/a]` — not applicable to this type of governance

#### 1. Token Voting Failure & Plutocracy
*The most widespread problem (28/50 practitioners). Wealth-weighted voting concentrates power.*

- [ ] Voting power is not purely proportional to token holdings
- [ ] Mechanisms exist to amplify smaller holders (quadratic voting, conviction voting, delegation)
- [ ] Large holders cannot unilaterally pass proposals
- [ ] Voting power distribution is transparent and monitored

#### 2. Governance Theater & Recentralization
*Formal governance exists but real decisions happen elsewhere (20/50).*

- [ ] Governance decisions have binding authority — they actually get implemented
- [ ] Core team / foundation cannot override governance outcomes
- [ ] Important decisions go through governance, not just uncontroversial ones
- [ ] There is no "shadow governance" where insiders pre-negotiate outcomes

#### 3. Voting Fatigue & Apathy
*Too many proposals, not enough participation (24/50).*

- [ ] Proposal volume is manageable — not everything requires a vote
- [ ] Delegation or representative mechanisms reduce individual burden
- [ ] Participation incentives exist beyond pure altruism
- [ ] Voter participation rates are tracked and healthy (>10% for major decisions)

#### 4. Informal Power & Narrative Capture
*Influence flows through social capital, not formal authority (17/50).*

- [ ] Decision-making criteria are explicit, not vibes-based
- [ ] Multiple communication channels prevent single-narrative dominance
- [ ] Newcomers can influence decisions, not just established members
- [ ] Power dynamics are discussed openly, not taboo

#### 5. Broken Contributor Economies
*People who do the work aren't fairly compensated or recognized (14/50).*

- [ ] Clear paths from contribution to compensation
- [ ] Compensation is transparent and roughly equitable
- [ ] Non-financial contributions (community building, documentation) are valued
- [ ] Contributors have voice in governance proportional to their involvement

#### 6. Grant System Dysfunction & Capital Misallocation
*Funding goes to the wrong things or the process is broken (10/50).*

- [ ] Grant criteria are clear and aligned with stated goals
- [ ] Follow-up and accountability exist for funded projects
- [ ] Funding decisions aren't dominated by personal networks
- [ ] Treasury management is transparent with regular reporting

#### 7. Lack of Clear Purpose
*The organization doesn't know what it's for (14/50).*

- [ ] Mission / purpose is stated and actually referenced in decisions
- [ ] Strategic priorities exist and guide resource allocation
- [ ] There's a process for revisiting and updating purpose
- [ ] Members can articulate why the organization exists

#### 8. Over-Reliance on Game Theory
*Governance designed around rational actors instead of real humans (8/50, highest depth).*

- [ ] Governance accounts for human behavior (emotion, relationships, trust)
- [ ] Mechanisms don't assume purely self-interested actors
- [ ] Qualitative input (deliberation, discussion) complements quantitative voting
- [ ] Edge cases and gaming are monitored, not just modeled

#### 9. Delegate Sustainability
*Delegates burn out or become captured (11/50).*

- [ ] Delegate roles are compensated or have clear term limits
- [ ] Delegate performance is tracked and transparent
- [ ] Delegation can be easily revoked or reassigned
- [ ] Multiple delegates prevent single-point-of-failure

#### 10. Institutional Amnesia
*Past decisions, context, and rationale are lost (8/50, high depth).*

- [ ] Decision rationale is recorded, not just outcomes
- [ ] New members can understand past decisions and their context
- [ ] Knowledge management system exists (wiki, handbook, archives)
- [ ] Handoff processes preserve institutional knowledge during transitions

#### 11. Technical & Legal Gaps
*Smart contract limitations and legal ambiguity undermine governance (10/50).*

- [ ] Governance has legal standing or clear legal wrapper
- [ ] Smart contract limitations are acknowledged and mitigated
- [ ] Upgrade mechanisms exist for technical governance infrastructure
- [ ] Legal and technical risks are communicated to participants

### Step 3: Assess governance solutions

Check whether the system employs any of the solutions identified by practitioners:

**Participation & Voting:**
- [ ] Conviction voting, quadratic voting, or similar alternatives to token-weighted voting
- [ ] Delegation mechanisms (liquid democracy, steward councils)
- [ ] Optimistic governance (proposals pass unless vetoed)
- [ ] Polis / opinion clustering / sensemaking tools

**Structure & Process:**
- [ ] Specialized committees with delegated authority
- [ ] Clear contributor streams and compensation frameworks
- [ ] Staged proposal process (idea → draft → vote → implementation)
- [ ] Cross-DAO collaboration mechanisms

**Knowledge & Memory:**
- [ ] Governance memory system (searchable decisions, rationale)
- [ ] Onboarding for new governance participants
- [ ] Regular governance health reports / retrospectives

**Technology:**
- [ ] AI governance assistants (summarization, analysis, recommendations)
- [ ] Reputation / soulbound tokens for non-financial contributions
- [ ] Onchain + offchain governance integration

### Step 4: Report

```markdown
# gov/acc Audit: {subject}
Date: {today}

## Summary
- Protected: {count}/11
- Partially addressed: {count}/11
- Vulnerable: {count}/11

## Overall Assessment

{2-3 sentences. What's the governance health? Where is it strong?
Where is it most at risk? How does it compare to what practitioners
described as healthy governance?}

## Problem-by-Problem Analysis

### 1. Token Voting Failure & Plutocracy
**Status: [Protected / Partially / Vulnerable]**

{Evidence from the governance artifacts. What mechanisms exist?
What's missing? How severe is the risk?}

... (repeat for each applicable problem)

## Solutions Deployed
{Which research-backed solutions does this system already use?}

## Critical Gaps
1. {Most urgent vulnerability} — **Recommended:** {specific solution from the research}
2. {Second most urgent} — **Recommended:** {solution}
3. {Third} — **Recommended:** {solution}

## Strengths
{What this governance does well — worth preserving and building on.}

## Connections to Broader Research
{Link findings to Ostrom's commons principles, Plurality concepts,
or Alexander's living structure properties where relevant.}
```

### Step 5: Offer next steps

- "Want me to draft governance proposals to address the critical gaps?"
- "Want to evaluate a specific aspect in more depth? (Use `--focus <category>`)"
- "Want to compare this against another governance system?"

## Focus flags

`voting`, `participation`, `power`, `contributors`, `funding`, `purpose`, `delegation`, `knowledge`, `legal`, `all`

## Optional MCP integrations

- **jtbd-knowledge MCP** — what job are members hiring this governance to do?
- **living-structure** — does the governance exhibit Alexander's properties? (boundaries, gradients, subsidiarity as levels of scale)
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's framework for legitimate governance
