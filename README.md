# Coin Metrics (coin-metrics)

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
