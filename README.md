# claude-gov-acc-audit

A [Claude Code](https://claude.ai/code) skill that analyzes governance systems using research-backed diagnostic lenses from the [gov/acc](https://gov-acc.metagov.org/) community.

Not a checklist — it reads actual governance data (proposals, votes, forums, constitutions) and identifies structural patterns.

## Why

Governance leads don't need a tool that tells them "voting fatigue exists." They need analysis of *their* specific governance data: participation trends, power concentration patterns, divergences between stated process and actual behavior, structural conditions that make failure modes likely.

The gov/acc initiative (Metagov, 2026) identified recurring governance failure modes through practitioner interviews, workshops, and deliberation platforms. This skill uses those findings as **diagnostic lenses** to analyze real governance artifacts.

## Install

```bash
npx skillsadd zhiganov/claude-gov-acc-audit
```

## Usage

```
/gov-acc-audit <subject>
/gov-acc-audit <subject> --focus <lens>
```

### Examples

```
/gov-acc-audit "ENS DAO"
/gov-acc-audit "Arbitrum governance"
/gov-acc-audit "our community's decision-making process"
/gov-acc-audit "Optimism" --focus participation
```

### Focus flags

`power`, `legitimacy`, `participation`, `information`, `contributors`, `resources`, `coherence`, `adaptation`, `knowledge`, `technical`, `all`

## What it does

### 1. Gathers real data

Fetches governance artifacts: proposals and outcomes (Tally, Agora, Snapshot), voting records, token distribution, forum discussions, constitutions, delegate statements, treasury flows.

### 2. Establishes baselines

Quantitative analysis first: participation trends over time, power concentration (top 10/20/50 wallets), proposal velocity and pass rates, delegate health and retention, treasury deployment vs stated priorities.

### 3. Applies diagnostic lenses

10 structural lenses from the gov/acc research:

| Lens | What it looks for |
|------|------------------|
| Power distribution | Who actually controls outcomes? Trace contested proposals. |
| Decision legitimacy | Where do stated process and actual decisions diverge? |
| Participation sustainability | What's the participation trajectory and what's driving it? |
| Information asymmetry | Who has context that shapes decisions? |
| Contributor alignment | Does the incentive structure produce needed behaviors? |
| Resource allocation | Does capital flow toward stated priorities? |
| Institutional coherence | Does the system act as if it has a coherent purpose? |
| Adaptive capacity | How has governance actually evolved and what drove changes? |
| Knowledge continuity | What happens when key people leave? |
| Technical-social alignment | Where do mechanisms and social reality diverge? |

Each lens produces evidence-based findings, not abstract risk flags.

### 4. Reports with recommendations

Structural risks grounded in evidence, comparative context from peer systems, and specific actionable recommendations tied to the dynamics observed.

## Optional MCP integrations

- **living-structure** — does the governance exhibit Alexander's properties?
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's governance framework

## Research

- [gov/acc](https://gov-acc.metagov.org/) — governance acceleration initiative by Metagov
- [Deliberate Priority Leaderboard](https://govacc.net/deliberate/leaderboard) — community-ranked governance priorities with scores from practitioner deliberation
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — interactive visualizations of problems, solutions, and actors

## License

MIT
