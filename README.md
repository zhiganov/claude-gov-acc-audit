# claude-gov-acc-audit

A Claude Code skill that evaluates governance systems against research-backed principles from the [gov/acc](https://gov-acc.metagov.org/) community.

Works on DAOs, protocols, communities, organizations — anything with a governance system.

## Why

The gov/acc initiative (Metagov, 2026) brings together governance practitioners from across web3, civic tech, and institutional design — through structured interviews, workshops, deliberation platforms, and collaborative research. The community has identified core problems that cause governance systems to fail, and the solutions practitioners are building to address them.

This skill turns that ongoing research into a practical audit tool. Point it at a DAO constitution, a community's decision-making process, or a protocol's governance framework and get a research-grounded assessment of where it's healthy and where it's at risk.

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

### 11 Governance Problems

| # | Problem |
|---|---------|
| 1 | Token Voting Failure & Plutocracy |
| 2 | Voting Fatigue & Apathy |
| 3 | Governance Theater & Recentralization |
| 4 | Informal Power & Narrative Capture |
| 5 | Broken Contributor Economies |
| 6 | Lack of Clear Purpose |
| 7 | Delegate Sustainability |
| 8 | Grant System Dysfunction & Capital Misallocation |
| 9 | Technical & Legal Gaps |
| 10 | Over-Reliance on Game Theory |
| 11 | Institutional Amnesia |

### Solutions Assessment

The audit also checks whether the system employs practitioner-recommended solutions: conviction voting, delegation mechanisms, governance memory systems, contributor streams, specialized committees, AI governance assistants, and more.

## Output

For each problem: **Protected**, **Partially addressed**, or **Vulnerable** — with evidence from the governance artifacts. Plus critical gaps with specific recommended solutions from the research.

## Optional MCP integrations

- **living-structure** — does the governance exhibit Alexander's properties?
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's governance framework

## Research

- [gov/acc: Accelerating Governance Innovation in Web3](https://medium.com/@eugene.leventhal/gov-acc-accelerating-governance-innovation-in-web3-31309f06ab63) — Eugene Leventhal, Metagov
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — interactive visualizations of problems, solutions, and actors

## License

MIT
