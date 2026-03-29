# claude-gov-acc-audit

A [Claude Code](https://claude.ai/code) skill that evaluates governance systems against research-backed principles from the [gov/acc](https://medium.com/@eugene.leventhal/gov-acc-accelerating-governance-innovation-in-web3-31309f06ab63) community.

Works on DAOs, protocols, communities, organizations — anything with a governance system.

## Why

The gov/acc research (Metagov, 2026) interviewed 50+ governance practitioners and identified 11 core problems that cause governance systems to fail. These aren't theoretical — every problem was described by people who experienced it firsthand: token voting plutocracy, governance theater, voting fatigue, institutional amnesia, broken contributor economies, and more.

This skill turns that research into a practical audit tool. Point it at a DAO constitution, a community's decision-making process, or a protocol's governance framework and get a research-grounded assessment of where it's healthy and where it's at risk.

## Install

```bash
npx skillsadd zhiganov/claude-gov-acc-audit
```

## Usage

```
/gov-acc-audit <subject>
/gov-acc-audit <subject> --focus <category>
```

### Examples

```
/gov-acc-audit "Arbitrum DAO constitution"
/gov-acc-audit "our community decision-making process"
/gov-acc-audit "Optimism governance" --focus delegation
/gov-acc-audit "MakerDAO" --focus voting
```

### Focus flags

`voting`, `participation`, `power`, `contributors`, `funding`, `purpose`, `delegation`, `knowledge`, `legal`, `all`

## What it checks

### The 11 Governance Problems (from 50+ practitioner interviews)

| # | Problem | Prevalence | Depth |
|---|---------|-----------|-------|
| 1 | Token Voting Failure & Plutocracy | 28/50 | High |
| 2 | Voting Fatigue & Apathy | 24/50 | Medium |
| 3 | Governance Theater & Recentralization | 20/50 | High |
| 4 | Informal Power & Narrative Capture | 17/50 | High |
| 5 | Broken Contributor Economies | 14/50 | Very High |
| 6 | Lack of Clear Purpose | 14/50 | Medium |
| 7 | Delegate Sustainability | 11/50 | High |
| 8 | Grant System Dysfunction | 10/50 | High |
| 9 | Technical & Legal Gaps | 10/50 | Very High |
| 10 | Over-Reliance on Game Theory | 8/50 | Very High |
| 11 | Institutional Amnesia | 8/50 | Very High |

### Solutions Assessment

The audit also checks whether the system employs practitioner-recommended solutions: conviction voting, delegation mechanisms, governance memory systems, contributor streams, specialized committees, AI governance assistants, and more.

## Output

For each of the 11 problems: **Protected**, **Partially addressed**, or **Vulnerable** — with evidence from the governance artifacts. Plus critical gaps with specific recommended solutions from the research.

## Optional MCP integrations

- **jtbd-knowledge** — what job are members hiring this governance to do?
- **living-structure** — does the governance exhibit Alexander's properties?
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's governance framework

## Research

- [gov/acc: Accelerating Governance Innovation in Web3](https://medium.com/@eugene.leventhal/gov-acc-accelerating-governance-innovation-in-web3-31309f06ab63) — Eugene Leventhal, Metagov
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — interactive visualizations of problems, solutions, and actors
- Data collected via [Harmonica](https://harmonica.chat) structured interviews (39 completed sessions, 50 participants engaged)

## License

MIT
