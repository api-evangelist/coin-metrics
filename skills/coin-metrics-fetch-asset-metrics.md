---
name: Fetch asset metric timeseries
description: >-
  Pull historical metric timeseries (reference rates, prices, on-chain
  metrics) for one or more assets, with correct pagination, time windows and
  rate-limit handling.
api: openapi/coin-metrics-timeseries-api-openapi.yml
operations: [getTimeseriesAssetMetrics, getTimeseriesMarketCandles]
generated: '2026-07-22'
method: generated
---

# Fetch asset metric timeseries

1. **Call `getTimeseriesAssetMetrics`** (`GET /timeseries/asset-metrics`) with
   `assets` (comma-separated, e.g. `btc,eth`) and `metrics`
   (e.g. `ReferenceRateUSD`). Keyless try-it:
   `https://community-api.coinmetrics.io/v4/timeseries/asset-metrics?assets=btc&metrics=ReferenceRateUSD`.
2. **Scope the window** with `start_time`/`end_time` (ISO 8601, UTC default;
   `timezone` accepted for parsing) and `frequency` (e.g. `1d`, `1h`, `1m`).
3. **Latest-value pattern**: `limit_per_asset=1` with `page_size >= assets x limit`
   returns just the most recent observation per asset.
4. **Handle values as strings** - all numbers are quoted strings (arbitrary
   precision); parse with a decimal type, never float-truncate. Missing fields
   are omitted; nulls appear only where mathematically meaningful
   (`null_as_zero=true` converts them).
5. **Paginate** via top-level `next_page_url` - fetch it unmodified until absent.
6. **Respect rate limits**: community 10 req/6s per IP; PRO 6,000 req/20s per
   key; on 429 back off using `X-RateLimit-*` headers. Max 10 parallel requests.
7. For OHLCV use `getTimeseriesMarketCandles` (`GET /timeseries/market-candles`)
   with `markets` (e.g. `coinbase-btc-usd-spot`, wildcards like `*-btc-usd-spot`
   supported) and `frequency`.

Errors: 400 bad parameter (validate via reference-data/catalog-v2 first),
401 missing/invalid key, 403 not licensed (check https://coverage.coinmetrics.io/),
414 URI too long (chunk your asset list). Envelope:
`{"error": {"type", "message"}}`.
