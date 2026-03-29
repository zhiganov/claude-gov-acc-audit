# claude-gov-acc-audit

A [Claude Code](https://claude.ai/code) skill that analyzes governance systems using the [gov/acc](https://gov-acc.metagov.org/) research framework.

Not a checklist — reads actual governance data (proposals, votes, forums, constitutions) and produces context-specific analysis grounded in what practitioners and researchers have learned.

## Why

Vitalik's [d/acc](https://vitalik.eth.limo/general/2025/01/05/dacc2.html) vision — decentralized, democratic, differential, defensive acceleration — requires governance that actually works. Not governance theater, not token-weighted plutocracy, but systems where distributed decision-making produces better outcomes than centralized control.

[Gov/acc](https://gov-acc.metagov.org/) is the governance arm of that vision: a time-bound research initiative (through Devcon 2026) focused on demonstrating that decentralized governance can meaningfully improve ecosystem outcomes. The core question isn't "is governance good?" but "where does decentralized coordination add clear value, and is it working?"

This skill applies that lens to a specific governance system — reading real data, not running a checklist.

## Install

```bash
npx skillsadd zhiganov/claude-gov-acc-audit
```

## Usage

```
/gov-acc-audit <subject>
/gov-acc-audit <subject> --focus <domain>
```

### Examples

```
/gov-acc-audit "ENS DAO"
/gov-acc-audit "Arbitrum governance"
/gov-acc-audit "our community's decision-making process"
/gov-acc-audit "Optimism" --focus participation
```

### Focus flags

`participation`, `accountability`, `resilience`, `funding`, `deliberation`, `surfaces`, `all`

## What it does

### 1. Gathers real data

Proposals and outcomes (Tally, Agora, Snapshot), voting records, token distribution, forum discussions, constitutions, delegate statements, treasury flows.

### 2. Analyzes through 5 gov/acc research domains

| Domain | What it looks for |
|--------|------------------|
| **Participation & Voice** | Is governance applied to the right surfaces? What coordination problems does it actually solve? |
| **Transparency & Accountability** | Where do stated process and actual decisions diverge? Are outcomes implemented? |
| **Resilience & Security** | How does the community resist capture? What happens when key people leave? |
| **Value Creation & Funding** | Does governance drive measurable value or is it overhead? Does capital flow toward priorities? |
| **Deliberation & Culture** | Is there genuine deliberation or just voting? Can newcomers participate meaningfully? |

### 3. Identifies appropriate governance surfaces

The key gov/acc question: where does decentralized governance add value, where is it overhead, and where is it missing?

### 4. Recommends experiments

Not generic advice — specific, testable experiments framed as hypotheses: "If [change], we expect [outcome], measurable by [metric]."

## MCP server (planned)

The skill will be powered by a dedicated **gov/acc MCP server** — structured access to the full research corpus: practitioner interviews, workshop outputs, Agora deliberation results, priority leaderboard, solution mappings, case studies. Same pattern as [Lenny's newsletter MCP](https://github.com/LennysNewsletter/lennys-newsletterpodcastdata).

Until then, the skill works by web fetching governance platform data and the priority leaderboard.

## Other MCP integrations

- **living-structure** — does the governance exhibit Alexander's properties?
- **Plurality MCP** (planned) — Weyl & Tang's collaborative technology principles
- **Governable Spaces MCP** (planned) — Schneider's governance framework

## Research

- [gov/acc](https://gov-acc.metagov.org/) — governance acceleration initiative by Metagov
- [gov/acc Priority Leaderboard](https://govacc.net/deliberate/leaderboard) — community-ranked governance priorities
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — interactive visualizations of problems, solutions, and actors

## License

MIT
