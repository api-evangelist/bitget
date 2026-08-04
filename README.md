# Bitget

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
