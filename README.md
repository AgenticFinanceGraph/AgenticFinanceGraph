# Agentic Finance Graph

**The independent ledger of machine money.** We measure which AI agents on Base actually pay, how much of their money was really spent, and what left their control — from receipts on the chain, with every figure defined and timestamped.

> **We have no token.** Any coin using our name is not ours, including "Agentic Finance Graph (AFG)" on Robinhood Chain (`0x3f6dba1b74bf3a8d123ad05f24ddfa952245bac2`), which an unrelated wallet launched on 6 Sep 2026. [How it was launched, traced →](https://dev.to/agenticfinancegraph/someone-launched-a-coin-with-our-name-here-is-the-trail-and-three-fixes-for-launchpads-7f4)

[![agents registered on Base](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dregistrations_minted_total)](https://agenticfinancegraph.com)
[![agents seen paying](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dactors_l7_plus)](https://agenticfinancegraph.com/ranked-ai-agents-observed-paying-l7-liveness)
[![counted agent spending](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dobserved_pay_usd_total)](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)
[![left the agents' control](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dobserved_pay_usd_left_control)](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)

*Live figures, read from [/api/state](https://agenticfinancegraph.com/api/state) each time this page is shown.*

## See it in 30 seconds

https://github.com/user-attachments/assets/ee95c1e9-54c2-49fc-b756-5ab58203861d

*The Desk, recorded on the live site: connect a wallet, your Desk opens, watch any agent, see its history, request the data for 1 cent. Open yours at [agenticfinancegraph.com/desk](https://agenticfinancegraph.com/desk).*

## Latest

- **12 Oct 2026, night** — We measured our own detectors against the literature before trusting them. **Address poisoning:**
  - Compared with the method of Tsuchiya et al. (USENIX Security 2025): of 82,132 plants either rule counts, ours found 80,509 and theirs 80,880.
  - A second read from the chain found every one of 300 sampled plants sent by somebody other than the agent wallet.
  - The watch now uses both rules (`poison.*.v2`), and its loss check reads Base's public nodes when the explorer refuses.

  **Who paid an agent:** [/api/payers](https://agenticfinancegraph.com/api/payers?agent=54261) and the new MCP tool `payer_set` (server 1.5.0, [v0.2.5](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/releases/tag/v0.2.5)) give the reviewer list ERC-8004's `getSummary` asks for. Only 6 of 619 reviewer–agent pairs we can check had paid the agent before rating it.

  **Also:**
  - Our statement roots now form an append-only log in the shape of Certificate Transparency ([/api/statements/log](https://agenticfinancegraph.com/api/statements/log)): keep a signed head, and a consistency proof shows our history was not rewritten.
  - The liveness sweep reads ERC-8004's endpoint-domain proof (about 1 agent in 300 publishes it).
  - A data check flags steps in our own series that no dated change explains ([/api/steps](https://agenticfinancegraph.com/api/steps)).

  Spec [v0.6](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec/releases/tag/v0.6) (303 definitions, 43 checks). [What changed](https://agenticfinancegraph.com/changelog-october-2026)
- **12 Oct 2026, evening** — Every known gap fixed now rather than held for the monthly release. [MCP server](https://agenticfinancegraph.com/mcp-server-connect-your-ai-to-agent-money-data) 1.4.0 ([v0.2.4](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/releases/tag/v0.2.4)): a free `pay_check` before paying an agent (it also reads the payments made after its latest statement), `list_metrics`, a `start_here` prompt, and instructions that let a newly connected AI give the tour itself. What counted spending consists of, in parts that add up to the cent: 52% into lending and vault positions the payer still holds, 17.5% into bridges (most of it back at the payer's own address), 16.8% into a work-escrow marketplace, 9.9% to destinations we have not named. Our own changes of method are dated beside every chart they moved ([/api/changepoints](https://agenticfinancegraph.com/api/changepoints)); `rank.l8plus.v2` corrects a definition that said USDC while the counts used four stablecoins; every paid pack was re-checked and two were fixed. Spec [v0.5](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec/releases/tag/v0.5) (288 definitions). Upstream: [x402-foundation/x402#3784](https://github.com/x402-foundation/x402/pull/3784). [What changed](https://agenticfinancegraph.com/changelog-october-2026)
- **12 Oct 2026, later** — An outside review, checked and fixed: every figure on the site is now written from the latest tape with its measurement time, and dated entries stay frozen to their day; the ranked top 25 and the detection log are readable without JavaScript; x402 is shown as three readings side by side, each saying what it counts; [llms-full.txt](https://agenticfinancegraph.com/llms-full.txt) carries every definition; an [Atom feed](https://agenticfinancegraph.com/feed.xml); OpenAPI 0.11.0; and the [MCP server](https://agenticfinancegraph.com/mcp-server-connect-your-ai-to-agent-money-data) 1.3.0 with four ready-made prompts (daily brief, check before paying, explain an agent, where agents pay). [What changed](https://agenticfinancegraph.com/changelog-october-2026)
- **12 Oct 2026** — Check before you pay: three new evidence packs over x402. `precheck` (5¢) gives an agent's level, last payment, live incidents and statement freshness, plus what the address it gave you is, including whether our poisoning watch saw it planted as a look-alike; `venue` (3¢) says what any address on Base is, with its stablecoin flow over the last 48 hours read live; `builders` (1¢) lists the ERC-8021 Builder Codes on an agent's payments. MCP server 1.2.0 and the bridge [v0.2.2](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/releases/tag/v0.2.2). The bridge follower now covers Mayan and Circle's USDC bridge, our Base registration count now matches The Graph's Agent0 subgraph to the registration (checked daily), and agent pages show the name each agent declares. [Pricing](https://agenticfinancegraph.com/pricing) · [Slow drains](https://agenticfinancegraph.com/slow-drains) · [Article](https://dev.to/agenticfinancegraph/before-your-agent-pays-another-agent-run-a-check-that-costs-cents-34id)
- **11 Oct 2026** — The correction release: retry_storm v2 and mint_burst v2 read runs with a peak (the calendar-hour rules had under-counted storms four to one), every drain detection carries the share of the wallet it took, new kind `layering_fan`, each rule's measured record on the detections page, Research Note 03 "Measured before trusted". Generator and reports: [amlsim-agentic](https://github.com/AgenticFinanceGraph/amlsim-agentic) (hot-wallet population, dominant-share candidate, re-validated reports); spec [0.4](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec). Changelog: [October 2026](https://agenticfinancegraph.com/changelog-october-2026). Evening of the same day: [Builder Codes](https://agenticfinancegraph.com/builder-codes), a page and a free document ([/api/builders](https://agenticfinancegraph.com/api/builders)) grouping counted agent payments by the ERC-8021 code of the app that built the transaction (codes shown as codes; the registry names no one); the "abandoned wallet" slow-drain rule measured on a 90-day synthetic run with victims that stop trading (generator options `victim_silent_share` and drain placement, `measure-november-rule.mjs`, `examples/silence-2026-10-11`), proposed for November and not live; the Telegram group now gets two or three figure posts a day from the free endpoints at random hours, beside the morning digest and the live incident alerts.
- **10 Oct 2026** — [**amlsim-agentic**](https://github.com/AgenticFinanceGraph/amlsim-agentic): IBM's AMLSim adapted for AI-agent wallets. A generator that produces labelled synthetic payment graphs (AMLSim's eight laundering typologies ported, thirteen agent-payment shapes added, each with a near-miss built *not* to be caught) and a validator that runs our production detectors over them and reports precision and recall. First measurements, 2,813 and 22,894 synthetic agents: retry storms, mint bursts and endpoint streaks 100% on both; the drain rule 100% recall with 60–64% precision, every false alarm a first large purchase. The near-misses found two real faults in the live rules (storms split by the calendar-hour bucket, under-reported about 4x on live data; a silent `LIMIT 100`) and the candidate fixes are measured in the same report, held for the monthly correction release. Also today: a Telegram alerts bot ([@AgenticGraphBot](https://t.me/AgenticGraphBot), watch an agent and hear about incidents on it), the MCP server listed on [LobeHub](https://lobehub.com/mcp/agenticfinancegraph-agentic-finance-graph-mcp), and the note to IBM's maintainers at [IBM/AMLSim#93](https://github.com/IBM/AMLSim/issues/93).
- **9 Oct 2026** — MCP bridge [v0.2.1](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/releases/tag/v0.2.1): a Dockerfile, so directories that start servers from source can check it. The server is now listed in the official MCP Registry as `com.agenticfinancegraph/agentic-finance-graph` (publisher verified by our domain), on Smithery and on Glama (health-checked). All nine evidence packs are in the Coinbase x402 Bazaar and on x402scan.
- **5 Oct 2026** — Agent statements: every three hours each paying agent gets a statement (outflow split into spending and routing, what left its control, income, open flags), hash-chained to the previous one and provable against a Merkle root we sign with Ed25519. Also: what changed since the last sweep beside every headline figure; each detector's published record (fired, confirmed, reversed); who paid an address; and binding confidence on every agent page. Spec [v0.3](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec/blob/main/CHANGELOG.md) (276 definitions), MCP [v0.2.0](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/blob/main/CHANGELOG.md) (11 read-only tools).
- **2 Oct 2026** — Security pass on the website: a sign-in signature now works only once, the contact form limits how often one sender can write (by a one-way hash, cleared after 7 days), and two build files are no longer served. Figures from a third-party feed that stopped updating on 23 Sep now carry that date instead of looking current. [Changelog →](https://agenticfinancegraph.com/changelog-september-2026-what-we-added-and-what-it-measures)
- **2 Oct 2026** — [Research Note 02, v1.2](https://agenticfinancegraph.com/research): the $3.2M a fleet of agent Safe accounts sent through bridges reached the same Safes on Arbitrum, 92% straight into lending vaults; and address poisoners planted copies of a thief's address in the victim's history within six minutes. Spec [v0.2](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec/blob/main/CHANGELOG.md) adds 14 definitions; MCP [v0.1.1](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/blob/main/CHANGELOG.md) adds security scanning.
- **30 Sep 2026** — Bridges followed to the other side: every counted agent payment into a bridge, traced to the chain it reached through the bridge's own public record. A correction: our Circle CCTP counter read zero because it watched the wrong contract. [Live data →](https://agenticfinancegraph.com/live-agentic-finance-data-stablecoins-ai-agent-tokens-vault-tvl)
- **28 Sep 2026** — The MCP server and the open accounting spec published here.

All changes, dated: [the changelog](https://agenticfinancegraph.com/changelog-september-2026-what-we-added-and-what-it-measures).

## What we do

- **Rank.** Every ERC-8004 agent registered on Base, walked up a ladder from "registered" to "seen paying" (L7), "still funded" (L8) and "repeat trade" (L9). [The rank →](https://agenticfinancegraph.com/ranked-ai-agents-observed-paying-l7-liveness)
- **Count.** Payments in USDC, USDT, EURC and DAI, split by their receipts into real spending, positions the payer still holds, and routing hops that are not spending at all. [Where agent money goes →](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)
- **Detect.** Drains, retry storms, registrations that changed owner, unknown EIP-7702 delegations, address poisoning. Measured against labelled synthetic data before they are trusted. [Detections →](https://agenticfinancegraph.com/detections-ai-agent-anomaly-log-mint-bursts-retry-storms)
- **Publish.** Dated research notes, a free API, an MCP server, signed three-hourly agent statements, Telegram alerts, and evidence packs about one agent or address for 1 to 25 cents over x402. [Research →](https://agenticfinancegraph.com/research)

## Use it

| | |
|---|---|
| Website | [agenticfinancegraph.com](https://agenticfinancegraph.com) |
| The Desk (watch your agents) | [agenticfinancegraph.com/desk](https://agenticfinancegraph.com/desk) |
| Telegram alerts | [@AgenticGraphBot](https://t.me/AgenticGraphBot) — `/watch 57657` and hear about incidents on that agent; daily figures in [the channel](https://t.me/AgenticFinanceGraph) |
| MCP server | `https://agenticfinancegraph.com/mcp` — [setup guide](https://agenticfinancegraph.com/mcp-server-connect-your-ai-to-agent-money-data) · official MCP Registry: `com.agenticfinancegraph/agentic-finance-graph` |
| CLI | `npx -y github:AgenticFinanceGraph/agentic-finance-graph-mcp state` |
| Free API | [/api/state](https://agenticfinancegraph.com/api/state) · [/api/agents](https://agenticfinancegraph.com/api/agents) · [OpenAPI](https://agenticfinancegraph.com/openapi.json) · [llms.txt](https://agenticfinancegraph.com/llms.txt) |
| Definitions | [Every figure, defined](https://agenticfinancegraph.com/def) |

## How we count

1. **Receipts decide.** A transfer is classified from its transaction receipt, not from a label or a guess.
2. **Routing is not spending.** Hops through bridges, routers and escrow are excluded from the totals and shown separately.
3. **Every figure carries a definition id and the time it was measured.** A definition, once published, is frozen; a change is a new version.
4. **Corrections are public and dated** in the [changelog](https://agenticfinancegraph.com/changelog-september-2026-what-we-added-and-what-it-measures).
5. **Nothing can be bought.** Partnerships, sponsorship and investment never change a rank, a figure or a definition.
6. **Detectors are measured before they are trusted,** on synthetic graphs with known answers ([amlsim-agentic](https://github.com/AgenticFinanceGraph/amlsim-agentic)), and the measurements are published with the rules.

## Open source here

- [**agentic-finance-graph-mcp**](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp) — the MCP bridge and the `afg` CLI. Apache-2.0, no dependencies, read-only, security-scanned on every push.
- [**agentic-finance-graph-spec**](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec) — how we count: the accounting spec, every metric definition, the data checks and test vectors. CC BY 4.0.
- [**amlsim-agentic**](https://github.com/AgenticFinanceGraph/amlsim-agentic) — labelled synthetic agent-payment graphs for testing detectors, adapted from IBM AMLSim, with our detectors' measured precision and recall. Apache-2.0.

## Work with us

- **Builders:** see [where we need help](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/blob/main/CONTRIBUTING.md) — MCP clients, framework adapters, a Python client, recipes. We are open to people who want to join the founding team.
- **Platforms, institutions and investors:** [agenticfinancegraph.com/contact](https://agenticfinancegraph.com/contact)
- **Agents:** `POST https://agenticfinancegraph.com/api/contact` with `{kind, message, reply_to}`.

[X @AgenticGraph](https://x.com/AgenticGraph) · [Telegram](https://t.me/AgenticFinanceGraph) · [agenticfinancegraph@proton.me](mailto:agenticfinancegraph@proton.me) · ERC-8004 agent #95875 on Base
