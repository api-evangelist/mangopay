# Mangopay

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

European payment infrastructure platform providing REST APIs for marketplace payments, digital wallet management, user KYC/KYB verification, fund transfers, currency conversion, and payment card processing. Mangopay serves multi-party payment flows across product marketplaces, financial platforms, on-demand services, and SaaS companies. The platform has processed over 68 billion euros in transactions across 207 million wallets.

## API

- **Base URL (Production):** https://api.mangopay.com
- **Base URL (Sandbox):** https://api.sandbox.mangopay.com
- **API Version:** v2.01
- **Authentication:** OAuth 2.0 client credentials (ClientId + API Key via Basic Auth to obtain bearer token)
- **Content Type:** application/json (UTF-8)

## Key Capabilities

- **Users** - Natural and legal user creation, KYC/KYB identity verification, SCA enrollment, UBO declarations
- **Wallets** - Multi-currency e-wallet creation, wallet-to-wallet transfers, virtual IBANs, balance management
- **Pay-ins** - Card payments (direct, recurring, preauthorization), Apple Pay, Google Pay, bank transfers, Bancontact, BLIK, Bizum, iDEAL, Klarna, PayPal, Swish
- **Payouts** - Multi-currency transfers to bank accounts in 30+ countries, instant settlement
- **FX** - Foreign exchange conversion with spot and guaranteed rates across 20+ currencies
- **Fraud Prevention** - Custom fraud detection logic, Profiler for Web/iOS/Android
- **Disputes** - Chargeback handling and settlement transfers

## Developer Resources

- [Documentation](https://docs.mangopay.com)
- [API Reference](https://docs.mangopay.com/endpoints/v2.01)
- [Authentication](https://docs.mangopay.com/api-reference/overview/authentication)
- [Rate Limiting](https://docs.mangopay.com/api-reference/overview/rate-limiting)
- [Webhooks](https://docs.mangopay.com/webhooks)
- [SDKs](https://docs.mangopay.com/sdks) - Node.js, PHP, Python, .NET, Java, Ruby
- [Postman Collection](https://docs.mangopay.com/postman)
- [Changelog](https://docs.mangopay.com/release-notes)
- [Status Page](https://hub.mangopay.com/service-status)
- [Sandbox Dashboard](https://hub.mangopay.com)

## SDKs

SDKs are available for Node.js, PHP, Python, .NET, Java, and Ruby. Note: Since November 25, 2025, official SDKs are no longer on GitHub (except PHP). Install via package managers:

- Node.js: `npm install mangopay4-nodejs-sdk`
- PHP: `composer require mangopay4/php-sdk` ([GitHub](https://github.com/Mangopay/mangopay4-php-sdk))

## Rate Limits

Uses a leaky bucket algorithm with four sliding time windows:

| Window | Max Calls |
|--------|-----------|
| 15 min | 2,300 |
| 30 min | 4,500 |
| 1 hour | 8,800 |
| 24 hours | 105,600 |

Exceeding limits returns HTTP 429. Monitor `x-ratelimit`, `x-ratelimit-remaining`, and `x-ratelimit-reset` headers.

## Pricing

Usage-based pricing with volume discounts. No fixed public tiers. Contact Mangopay sales for a custom quote. Billing is monthly with automatic invoice collection.

- [Pricing](https://mangopay.com/pricing)

## Maintainer

**Kin Lane** - kin@apievangelist.com
