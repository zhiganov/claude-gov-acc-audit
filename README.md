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

The skill uses web search and web fetch to pull publicly available governance data:

- **Governance platforms** — proposal history, voting records, and delegate info from [Tally](https://www.tally.xyz), [Agora](https://www.agora.xyz), [Snapshot](https://snapshot.org), [Boardroom](https://boardroom.io)
- **Forums** — discussion threads from Discourse, Commonwealth, or governance-specific forums (fetched via URL)
- **Documents** — constitutions, charters, operating manuals published on the DAO's docs site or GitHub
- **Onchain data** — token distribution and treasury flows via block explorers (Etherscan, etc.)
- **The user can also provide** local files, screenshots, or paste content directly — forum posts, meeting notes, delegate statements, anything relevant

**gov/acc research as diagnostic context:**

The skill cross-references findings against the gov/acc knowledge base — problems, solutions, and actors mapped by 50+ governance practitioners:

- [gov/acc wiki](https://gov-acc.netlify.app) — structured problems, solutions, and actor profiles with relationships
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — interactive visualizations of governance patterns across ecosystems
- [gov/acc Priority Leaderboard](https://govacc.net/deliberate/leaderboard) — community-ranked priorities with scores from practitioner deliberation

This means the skill doesn't just describe what it sees — it can say "this pattern matches what 28 practitioners identified as token voting failure" or "practitioners working on similar problems recommend conviction voting and delegation mechanisms."

The more data available, the better the analysis. For major DAOs (ENS, Arbitrum, Optimism, MakerDAO), most governance data is publicly accessible.

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

## Standards

- **[DDS](https://www.dds.xyz/)** (Decentralized Deliberation Standard) — open protocol for sovereign, verifiable, interoperable deliberation. The audit checks whether the governance system uses open standards for deliberation data, and recommends DDS-compatible tools when gaps are found.

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
