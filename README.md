# Coin Metrics (coin-metrics)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Coin Metrics is a Boston-based crypto financial intelligence provider founded in 2017, selling institutional-grade cryptoasset network (on-chain) data, exchange market data (trades, quotes, order books, candles, derivatives), CMBI indexes, reference rates, and reference/security-master data. Everything is delivered through a single documented API v4 - REST at api.coinmetrics.io/v4 and WebSocket streaming at wss://api.coinmetrics.io/v4 as paid, API-key products - plus a free, keyless Community API at community-api.coinmetrics.io/v4 under a CC BY-NC 4.0 license, with flat files, Python and R clients, and Google Sheets as additional delivery channels.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/coin-metrics/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/coin-metrics/refs/heads/main/apis.yml)

## Tags

- Financial
- Market Data
- Crypto
- Blockchain
- On-Chain Data
- Indexes
- Reference Rates
- Order Book
- Real-Time

## Timestamps

- **Created:** 2026-07-21
- **Modified:** 2026-07-21

## APIs

### Coin Metrics Market Data API

Timeseries endpoints for exchange market data - trades, quotes, order book snapshots and depth, candles, open interest, liquidations, funding rates, and contract prices - across spot and derivatives markets, served from the API v4 REST root with API-key authentication.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://api.coinmetrics.io/v4`

#### Tags

- Market Data
- Trades
- Quotes
- Order Book
- Derivatives

#### Properties

- [Documentation](https://coinmetrics.io/market-data-feed/)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Network Data API

Network Data Pro on-chain asset metrics - supply, addresses, fees, transactions, miner flows, exchange flows, and hundreds of other per-asset timeseries metrics - via the timeseries/asset-metrics family of API v4 endpoints.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://api.coinmetrics.io/v4`

#### Tags

- On-Chain Data
- Asset Metrics
- Blockchain

#### Properties

- [Documentation](https://coinmetrics.io/network-data-pro/)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Index and Reference Rates API

CMBI index levels and candles, index constituent snapshots and timeframes, and CM Prices reference rates delivered as API v4 timeseries endpoints for benchmark and valuation use cases.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://api.coinmetrics.io/v4`

#### Tags

- Indexes
- Reference Rates
- Benchmarks

#### Properties

- [Documentation](https://coinmetrics.io/indexes/)
- [Documentation](https://coinmetrics.io/reference-rates/)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Timeseries Stream WebSocket API

Real-time WebSocket streaming under /timeseries-stream for asset metrics, market trades, quotes, order books, candles, open interest, liquidations, contract prices, pair and asset quotes, and index levels. Documented as a paid product in the same OpenAPI definition as the REST API.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `wss://api.coinmetrics.io/v4`

#### Tags

- WebSocket
- Streaming
- Real-Time

#### Properties

- [Documentation](https://docs.coinmetrics.io/access-our-data/api)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Community API

Free, keyless subset of API v4 at community-api.coinmetrics.io/v4 offering community network data and market data under a Creative Commons BY-NC 4.0 license. Confirmed live with HTTP 200 responses to catalog and timeseries requests without authentication.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://community-api.coinmetrics.io/v4`

#### Tags

- Community
- Free Tier
- Market Data
- On-Chain Data

#### Properties

- [Documentation](https://coinmetrics.io/community-network-data/)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Atlas Blockchain Explorer API

Atlas blockchain search - blockchain entities (accounts, transactions, blocks, balance updates), asynchronous blockchain explorer jobs and job results, and blockchain metadata endpoints within API v4.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://api.coinmetrics.io/v4`

#### Tags

- Blockchain Explorer
- Transactions
- Balances

#### Properties

- [Documentation](https://coinmetrics.io/atlas/)
- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### Coin Metrics Reference Data and Catalog API

Reference data endpoints for assets, markets, exchanges, indexes, and metrics, catalog and catalog-v2 coverage discovery, security master, profiles, and the datonomy taxonomy - the metadata layer for the rest of API v4.

- **Human URL:** [https://docs.coinmetrics.io/api/v4](https://docs.coinmetrics.io/api/v4)
- **Base URL:** `https://api.coinmetrics.io/v4`

#### Tags

- Reference Data
- Catalog
- Security Master
- Taxonomy

#### Properties

- [API Reference](https://docs.coinmetrics.io/api/v4)
- [OpenAPI](openapi/coin-metrics-api-v4-openapi.json) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [Website](https://coinmetrics.io/)
- [Portal](https://docs.coinmetrics.io/)
- [Documentation](https://docs.coinmetrics.io/access-our-data/api)
- [GitHub Organization](https://github.com/coinmetrics)
- [LinkedIn](https://www.linkedin.com/company/coinmetrics)
- [Blog](https://coinmetrics.io/insights/)
- [Pricing](https://coinmetrics.io/pricing/)
- [Terms of Service](https://coinmetrics.io/terms-of-service/)
- [Privacy Policy](https://coinmetrics.io/privacy-policy/)
- [Support](https://coinmetrics.io/contact/)
- [Status Page](https://status.coinmetrics.io/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
