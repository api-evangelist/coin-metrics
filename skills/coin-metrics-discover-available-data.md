---
name: Discover available Coin Metrics data
description: >-
  Find which assets, exchanges, markets, metrics and time ranges are available
  before querying timeseries data, using reference-data and catalog-v2.
api: openapi/coin-metrics-reference-data-api-openapi.yml
operations: [getReferenceDataAssets, getReferenceDataAssetMetrics, getReferenceDataMarkets, getCatalogV2AssetMetrics]
generated: '2026-07-22'
method: generated
---

# Discover available Coin Metrics data

Use this skill before any timeseries query - guessing asset codes or metric
names is the top cause of 400 "bad_parameter" errors.

1. **Pick a base URL.** Keyless exploration: `https://community-api.coinmetrics.io/v4`
   (free, CC BY-NC 4.0, 10 requests / 6s per IP). Paid coverage:
   `https://api.coinmetrics.io/v4` with `?api_key=<key>`.
2. **List entities** with reference data (the entity handbook):
   - `getReferenceDataAssets` (`GET /reference-data/assets`) for asset codes like `btc`.
   - `getReferenceDataMarkets` (`GET /reference-data/markets`) for market ids like
     `binance-btc-usdt-spot` (`<exchange>-<instrument>-<type>`).
   - `getReferenceDataAssetMetrics` (`GET /reference-data/asset-metrics`) for metric
     definitions (name, unit, data type, product, category).
3. **Check availability** with `getCatalogV2AssetMetrics`
   (`GET /catalog-v2/asset-metrics`): each entry gives per-frequency
   `min_time`/`max_time`. On the paid host, `/catalog-v2/*` reflects only what
   your key licenses; `/catalog-all/*` (full catalog) shows the entire universe.
   `format=json_stream` is supported on catalog-v2 and avoids paging.
4. **Page correctly**: `page_size` defaults to 100 (max 10,000); follow the
   top-level `next_page_url` verbatim when present.
5. **Avoid the deprecated catalog v1** (`/catalog/*`, `/catalog-all/*` v1 family,
   62 deprecated operations) - use catalog-v2 and reference-data instead.

Errors arrive as `{"error": {"type", "message"}}` - branch on `error.type`
only. See `conventions/coin-metrics-conventions.yml` and
`errors/coin-metrics-problem-types.yml`.
