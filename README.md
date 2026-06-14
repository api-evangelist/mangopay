# Mangopay

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
