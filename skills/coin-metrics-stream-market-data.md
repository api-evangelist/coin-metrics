---
name: Stream real-time market data over WebSocket
description: >-
  Subscribe to real-time trades, quotes, order books, candles and asset
  metrics over the wss timeseries-stream surface, with reconnect handling.
api: openapi/coin-metrics-timeseries-stream-api-openapi.yml
operations: [getTimeseriesStreamAssetMetrics, getTimeseriesStreamMarketTrades, getTimeseriesStreamMarketOrderbooks]
generated: '2026-07-22'
method: generated
---

# Stream real-time market data over WebSocket

Paid product - requires a Pro API key; the Community tier has no WebSocket
access. Trial/PRO keys allow up to 200 parallel connections.

1. **Connect** to `wss://api.coinmetrics.io/v4` + the stream path with the
   same query parameters as the REST sibling plus `api_key`:
   - `getTimeseriesStreamAssetMetrics` (`/timeseries-stream/asset-metrics?assets=btc&metrics=ReferenceRateUSD&frequency=1s`)
   - `getTimeseriesStreamMarketTrades` (`/timeseries-stream/market-trades?markets=coinbase-btc-usd-spot`)
   - `getTimeseriesStreamMarketOrderbooks` (`/timeseries-stream/market-orderbooks?markets=...`)
2. **Consume** individual JSON messages - one object per event, same
   string-encoded number conventions as REST.
3. **Keep-alive**: the server uses the standard WS ping/pong mechanism;
   respond to pings.
4. **Reconnect logic is mandatory** - connections traverse Cloudflare and
   restart occasionally by design; on close, re-dial and resume. Detect gaps
   by comparing message `time` fields against your last-seen value and
   backfill via the REST sibling (`/timeseries/...`) for the missed window.
5. **Stream vs REST divergence**: stream endpoints mirror REST names but may
   support different parameter sets (real-time vs historical); consult the
   per-operation parameters in the referenced OpenAPI.

The full derived channel catalog (11 channels) is in
`asyncapi/coin-metrics-timeseries-stream-asyncapi.yml`.
