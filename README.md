# Agentic Finance Graph

**The independent ledger of machine money.** We measure which AI agents on Base actually pay, how much of their money was really spent, and what left their control — from receipts on the chain, with every figure defined and timestamped.

[![agents registered on Base](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dregistrations_minted_total)](https://agenticfinancegraph.com)
[![agents seen paying](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dactors_l7_plus)](https://agenticfinancegraph.com/ranked-ai-agents-observed-paying-l7-liveness)
[![counted agent spending](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dobserved_pay_usd_total)](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)
[![left the agents' control](https://img.shields.io/endpoint?url=https%3A%2F%2Fagenticfinancegraph.com%2Fapi%2Fstate%3Fview%3Dshields%26key%3Dobserved_pay_usd_left_control)](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)

*Live figures, read from [/api/state](https://agenticfinancegraph.com/api/state) each time this page is shown.*

## Latest

- **2 Oct 2026** — [Research Note 02, v1.2](https://agenticfinancegraph.com/research): the $3.2M a fleet of agent Safe accounts sent through bridges reached the same Safes on Arbitrum, 92% straight into lending vaults; and address poisoners planted copies of a thief's address in the victim's history within six minutes. Spec [v0.2](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec/blob/main/CHANGELOG.md) adds 14 definitions; MCP [v0.1.1](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/blob/main/CHANGELOG.md) adds security scanning.
- **30 Sep 2026** — Bridges followed to the other side: every counted agent payment into a bridge, traced to the chain it reached through the bridge's own public record. A correction: our Circle CCTP counter read zero because it watched the wrong contract. [Live data →](https://agenticfinancegraph.com/live-agentic-finance-data-stablecoins-ai-agent-tokens-vault-tvl)
- **28 Sep 2026** — The MCP server and the open accounting spec published here.

All changes, dated: [the changelog](https://agenticfinancegraph.com/changelog-september-2026-what-we-added-and-what-it-measures).

## What we do

- **Rank.** Every ERC-8004 agent registered on Base, walked up a ladder from "registered" to "seen paying" (L7), "still funded" (L8) and "repeat trade" (L9). [The rank →](https://agenticfinancegraph.com/ranked-ai-agents-observed-paying-l7-liveness)
- **Count.** Payments in USDC, USDT, EURC and DAI, split by their receipts into real spending, positions the payer still holds, and routing hops that are not spending at all. [Where agent money goes →](https://agenticfinancegraph.com/where-ai-agent-money-goes-real-spending-vs-routing-2026)
- **Detect.** Drains, retry storms, registrations that changed owner, unknown EIP-7702 delegations. [Detections →](https://agenticfinancegraph.com/detections-ai-agent-anomaly-log-mint-bursts-retry-storms)
- **Publish.** Dated research notes, a free API, an MCP server, and evidence packs about one agent for 1 to 25 cents over x402. [Research →](https://agenticfinancegraph.com/research)

## Use it

| | |
|---|---|
| Website | [agenticfinancegraph.com](https://agenticfinancegraph.com) |
| The Desk (watch your agents) | [agenticfinancegraph.com/desk](https://agenticfinancegraph.com/desk) |
| MCP server | `https://agenticfinancegraph.com/mcp` — [setup guide](https://agenticfinancegraph.com/mcp-server-connect-your-ai-to-agent-money-data) |
| CLI | `npx -y github:AgenticFinanceGraph/agentic-finance-graph-mcp state` |
| Free API | [/api/state](https://agenticfinancegraph.com/api/state) · [/api/agents](https://agenticfinancegraph.com/api/agents) · [OpenAPI](https://agenticfinancegraph.com/openapi.json) · [llms.txt](https://agenticfinancegraph.com/llms.txt) |
| Definitions | [Every figure, defined](https://agenticfinancegraph.com/def) |

## How we count

1. **Receipts decide.** A transfer is classified from its transaction receipt, not from a label or a guess.
2. **Routing is not spending.** Hops through bridges, routers and escrow are excluded from the totals and shown separately.
3. **Every figure carries a definition id and the time it was measured.** A definition, once published, is frozen; a change is a new version.
4. **Corrections are public and dated** in the [changelog](https://agenticfinancegraph.com/changelog-september-2026-what-we-added-and-what-it-measures).
5. **Nothing can be bought.** Partnerships, sponsorship and investment never change a rank, a figure or a definition.

## Open source here

- [**agentic-finance-graph-mcp**](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp) — the MCP bridge and the `afg` CLI. Apache-2.0, no dependencies, read-only, security-scanned on every push.
- [**agentic-finance-graph-spec**](https://github.com/AgenticFinanceGraph/agentic-finance-graph-spec) — how we count: the accounting spec, every metric definition, the data checks and test vectors. CC BY 4.0.

## Work with us

- **Builders:** see [where we need help](https://github.com/AgenticFinanceGraph/agentic-finance-graph-mcp/blob/main/CONTRIBUTING.md) — MCP clients, framework adapters, a Python client, recipes. We are open to people who want to join the founding team.
- **Platforms, institutions and investors:** [agenticfinancegraph.com/contact](https://agenticfinancegraph.com/contact)
- **Agents:** `POST https://agenticfinancegraph.com/api/contact` with `{kind, message, reply_to}`.

[X @AgenticGraph](https://x.com/AgenticGraph) · [Telegram](https://t.me/AgenticFinanceGraph) · [agenticfinancegraph@proton.me](mailto:agenticfinancegraph@proton.me) · ERC-8004 agent #95875 on Base

<sub>Research, not investment advice.</sub>
