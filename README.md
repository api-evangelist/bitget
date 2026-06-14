# Bitget

Bitget is a cryptocurrency exchange and copy trading platform with REST and
WebSocket APIs for spot trading, futures (USDT-M, USDC-M, and Coin-M perpetual
contracts), margin trading, copy trading, broker services, and earn products.
The platform serves individual traders, algorithmic traders, copy trading leaders
and followers, and third-party brokers building white-label trading platforms.

## APIs

| API | Description |
|-----|-------------|
| [Spot Trading API](https://www.bitget.com/api-doc/spot/intro) | Market data, order management, wallet operations |
| [Futures Trading API](https://www.bitget.com/api-doc/contract/intro) | USDT-M, USDC-M, Coin-M perpetual contracts |
| [Copy Trading API](https://www.bitget.com/api-doc/copytrading/intro) | Futures and spot copy trade for leaders/followers |
| [Broker API](https://www.bitget.com/api-doc/broker/intro) | Sub-account management for white-label platforms |
| [WebSocket API](https://www.bitget.com/api-doc/common/websocket-intro) | Real-time market data and account event streaming |
| [Earn API](https://www.bitget.com/api-doc/common/intro) | Staking and savings product management |
| [Margin Trading API](https://www.bitget.com/api-doc/margin/intro) | Cross and isolated margin leveraged trading |

## Base URLs

- REST: `https://api.bitget.com`
- WebSocket Public: `wss://ws.bitget.com/v2/ws/public`
- WebSocket Private: `wss://ws.bitget.com/v2/ws/private`

## Authentication

All private endpoints require HMAC SHA256 or RSA authentication using:
- `ACCESS-KEY` — API key identifier
- `ACCESS-SIGN` — Base64-encoded HMAC SHA256 or RSA signature
- `ACCESS-TIMESTAMP` — Unix timestamp in milliseconds
- `ACCESS-PASSPHRASE` — User-defined passphrase

## Resources

- [API Documentation](https://www.bitget.com/api-doc/common/intro)
- [Rate Limits](rate-limits/rate-limits.md)
- [Plans](plans/plans.md)
- [FinOps](finops/finops.md)
- [Fee Schedule](https://www.bitget.com/fee)
- [Changelog](https://www.bitget.com/api-doc/common/changelog)
- [Support Center](https://www.bitget.com/support)
- [Telegram (@bitgetOpenapi)](https://t.me/bitgetOpenapi)
- [GitHub SDKs](https://github.com/BitgetLimited)
