# gov/acc Governance Audit

Analyze any governance system — DAO, protocol, community, organization — using the [gov/acc](https://gov-acc.metagov.org/) research framework. Not a checklist. Reads real governance data and produces context-specific structural analysis grounded in what practitioners have learned.

Built by [Harmonica](https://harmonica.chat), the AI-facilitated sensemaking platform powering the gov/acc research.

## Why

Vitalik's [d/acc](https://vitalik.eth.limo/general/2025/01/05/dacc2.html) vision — decentralized, democratic, differential, defensive acceleration — requires governance that actually works. Not governance theater, not token-weighted plutocracy, but systems where distributed decision-making produces better outcomes than centralized control.

[Gov/acc](https://gov-acc.metagov.org/) is the governance arm of that vision: a time-bound research initiative (through Devcon 2026) focused on demonstrating that decentralized governance can meaningfully improve ecosystem outcomes. The core question isn't "is governance good?" but **"where does decentralized coordination add clear value, and is it working?"**

This tool applies that lens to a specific governance system.

## How it works

### Data sources

Pulls publicly available governance data:

- **Governance platforms** — proposals, votes, delegates from [Tally](https://www.tally.xyz), [Agora](https://www.agora.xyz), [Snapshot](https://snapshot.org), [Boardroom](https://boardroom.io)
- **Forums** — Discourse, Commonwealth discussion threads
- **Documents** — constitutions, charters, operating manuals
- **Onchain data** — token distribution, treasury flows via block explorers
- **User-provided** — local files, screenshots, pasted content — meeting notes, delegate statements, anything relevant

For major DAOs (ENS, Arbitrum, Optimism, MakerDAO), most governance data is publicly accessible.

### The gov/acc research lens

Every finding is cross-referenced against the gov/acc knowledge base — problems, solutions, and patterns identified by governance practitioners through structured interviews, workshops, and deliberation:

- [gov/acc wiki](https://gov-acc.netlify.app) — structured problems, solutions, and actor profiles
- [gov/acc Priority Leaderboard](https://govacc.net/deliberate/leaderboard) — community-ranked priorities with scores
- [gov/acc Research Dashboard](https://gov-acc-research.netlify.app) — governance patterns across ecosystems

This means the tool doesn't just describe what it sees — it connects evidence from the specific governance system to what practitioners across the ecosystem have learned.

### 5 research domains

| Domain | What it looks for |
|--------|------------------|
| **Participation & Voice** | Is governance applied to the right surfaces? What coordination problems does it actually solve? |
| **Transparency & Accountability** | Where do stated process and actual decisions diverge? Are outcomes implemented? |
| **Resilience & Security** | How does the community resist capture? What happens when key people leave? |
| **Value Creation & Funding** | Does governance drive measurable value or is it overhead? Does capital flow toward priorities? |
| **Deliberation & Culture** | Is there genuine deliberation or just voting? Can newcomers participate meaningfully? |

### Governance surfaces

The key gov/acc question: where does decentralized governance add value, where is it overhead, and where is it missing?

### Experiments, not recommendations

Output is specific, testable experiments framed as hypotheses: "If [change], we expect [outcome], measurable by [metric]."

## Interoperability

Built to be composable with the [Decentralized Deliberation Standard](https://www.dds.xyz/) (DDS) — an open protocol that separates deliberation into Plan, Collect, and Analyze interfaces.

- **As a DDS Analyzer** — if a DAO's deliberation data is in DDS format, the audit gets structured input instead of web scraping
- **Output as DDS Plan** — findings and recommended experiments can be fed back into the governance system as structured deliberation plans
- **Composable with other tools** — any DDS-compatible collection tool (Harmonica, Agora, Snapshot) can feed data in, and any DDS-compatible planning tool can act on the output

## Roadmap

- **gov/acc MCP server** — structured access to the full research corpus: practitioner interviews, workshop outputs, Agora deliberation results, priority leaderboard, solution mappings, case studies. Same pattern as [Lenny's newsletter MCP](https://github.com/LennysNewsletter/lennys-newsletterpodcastdata).
- **[Plurality](https://github.com/pluralitybook/plurality) integration** — Weyl & Tang's collaborative technology principles as an additional analytical lens
- **[Governable Spaces](https://nathanschneider.info/books/governable-spaces/) integration** — Schneider's framework for legitimate governance
- **[Living Structure](https://github.com/zhiganov/claude-living-structure) integration** — Christopher Alexander's 15 Properties applied to governance systems

## Install

Requires [Claude Code](https://claude.ai/code).

```bash
npx skillsadd zhiganov/claude-gov-acc-audit
```

### Usage

```
/gov-acc-audit "ENS DAO"
/gov-acc-audit "Arbitrum governance"
/gov-acc-audit "Optimism" --focus participation
/gov-acc-audit "our community's decision-making process"
```

Focus flags: `participation`, `accountability`, `resilience`, `funding`, `deliberation`, `surfaces`, `all`

## License

MIT
