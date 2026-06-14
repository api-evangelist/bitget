# Bitget API Rate Limits

Bitget enforces rate limits at both the IP and user (UID) level across REST and
WebSocket interfaces. Exceeding limits returns HTTP 429 Too Many Requests.

## REST API — IP-Based Limits

| Scope                   | Limit                      |
|-------------------------|----------------------------|
| Global unauthenticated  | 6,000 requests/minute/IP   |
| Public market data      | 20 requests/second/IP      |
| VIP Fee Rate (Spot)     | 10 requests/second/IP      |
| VIP Fee Rate (Futures)  | 10 requests/second/IP      |

## REST API — UID-Based Limits (Authenticated)

| Endpoint Type            | Standard Limit   |
|--------------------------|------------------|
| Order placement (Spot)   | 10 req/s per UID |
| Batch orders             | 5 req/s per UID  |
| Account queries          | 10 req/s per UID |
| Market data              | 20 req/s per UID |

Spot, Margin, and Futures trading share independent rate limit pools. Within
Futures, USDT-M, USDC-M, and Coin-M products share the same quota.

## UID Tier Overrides

Higher VIP tiers receive elevated per-UID limits:

| Account Tier       | Approx. Limit (req/s) |
|--------------------|-----------------------|
| Regular            | 10–20                 |
| VIP 1–5            | 30–100                |
| Professional (PRO) | 120–300               |
| Market Maker (MM)  | Custom / negotiated   |

## WebSocket API Limits

| Constraint                          | Limit                           |
|-------------------------------------|---------------------------------|
| Connection requests                 | 300 connections/IP/5 minutes    |
| Max simultaneous connections        | 100 connections per IP          |
| Subscription requests               | 240 subscriptions/hour/connection |
| Max channel subscriptions           | 1,000 channels per connection   |
| Messages per second                 | 10 messages/second              |
| Recommended subscriptions/connection| < 50 channels (for stability)   |
| Ping-pong interval                  | Every 30 seconds (required)     |
| Idle connection timeout             | 2 minutes without ping          |
| Max message size                    | 4,096 bytes per request         |

## Endpoints

- REST: `https://api.bitget.com`
- WebSocket Public: `wss://ws.bitget.com/v2/ws/public`
- WebSocket Private: `wss://ws.bitget.com/v2/ws/private`

## Error Handling

- HTTP 429 is returned when REST rate limits are exceeded
- The `x-mbx-used-remain-limit` response header indicates remaining capacity
- Implement exponential back-off when handling 429 responses
- WebSocket connections bypass REST rate limits via persistent push messaging

## Authentication Headers (REST)

All authenticated REST requests require:

| Header              | Description                                   |
|---------------------|-----------------------------------------------|
| ACCESS-KEY          | API key identifier                            |
| ACCESS-SIGN         | HMAC SHA256 or RSA signature (Base64-encoded) |
| ACCESS-TIMESTAMP    | Unix timestamp (milliseconds)                 |
| ACCESS-PASSPHRASE   | User-defined passphrase                       |

Signature string format: `{timestamp}{HTTP_METHOD}{request_path}{query_string}{request_body}`

## Additional Resources

- Rate Limits Overview: https://www.bitget.com/wiki/bitget-api-rate-limits
- API Introduction: https://www.bitget.com/api-doc/common/intro
- Telegram Support: https://t.me/bitgetOpenapi
