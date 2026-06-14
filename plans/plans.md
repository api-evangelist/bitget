# Bitget API Plans

Bitget provides API access at no direct cost. Access tiers are tied to account
VIP level and trading volume rather than subscription fees. All registered users
receive API access upon creating API keys through the account dashboard.

## Free Access (All Users)

All Bitget accounts receive API access as part of their trading account:

- REST API access for spot, futures, margin, copy trading, and broker endpoints
- WebSocket API access for real-time data (public and private channels)
- Up to 100 simultaneous WebSocket connections per IP
- 6,000 REST requests per minute per IP (unauthenticated)
- Standard rate limits apply based on account tier

## VIP Tiers

Rate limits and fee discounts scale with VIP level, which is determined by 30-day
trading volume and/or BGB (Bitget Token) holdings:

| Tier      | Approx. Rate Limit | Spot Maker | Spot Taker |
|-----------|--------------------|------------|------------|
| Regular   | 10–20 req/s        | 0.1000%    | 0.1000%    |
| VIP 1     | 30 req/s           | Lower      | Lower      |
| VIP 2     | 50 req/s           | Lower      | Lower      |
| VIP 3     | 70 req/s           | Lower      | Lower      |
| VIP 4     | 100 req/s          | Lower      | Lower      |
| VIP 5     | 150 req/s          | Lower      | Lower      |
| PRO       | 120–300 req/s      | Negotiated | Negotiated |
| Market Maker (MM) | Custom   | Negotiated | Negotiated |

Futures base rates: Maker 0.02%, Taker 0.06% (Standard)

## BGB Token Discount

Users paying trading fees with BGB (Bitget's native token) receive a 20%
discount on both spot and margin trading fees.

## Broker Program

Non-disclosed brokers (ND-brokers) can apply to the Bitget Broker Program to
operate white-label trading platforms built on Bitget's infrastructure. Brokers
receive backend technology and liquidity access with custom API key management
and sub-account capabilities. Apply via the official partner program.

## Additional Resources

- Fee Schedule: https://www.bitget.com/fee
- VIP Program: https://www.bitget.com/vip
- Broker Program: https://www.bitget.com/api-doc/broker/intro
- API Keys Management: Available through account dashboard after registration
