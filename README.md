# Zensurance (zensurance)

Zensurance is a Toronto-based digital commercial insurance brokerage founded in 2016 that sells small-business and freelancer coverage online across every Canadian province, placing risk with Canadian carriers rather than underwriting it. Its book is commercial property and casualty — general and commercial general liability, professional liability and errors and omissions, cyber liability, directors and officers, commercial property, commercial auto, builder's risk, and a long tail of trade- and profession-specific packages — sold through a quote-to-bind web flow with licensed broker support and claims advocacy behind it.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/zensurance/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/zensurance/refs/heads/main/apis.yml)

## API Posture

Zensurance publishes **no public, self-serve developer portal and no machine-readable API definitions**. Every candidate developer host was probed on 2026-07-25:

- `developer.zensurance.com`, `developers.zensurance.com`, `docs.zensurance.com`, `partners.zensurance.com` — do not resolve
- `www.zensurance.com/developers`, `/developer`, `/api`, `/docs`, `/partners`, `/integrations` — HTTP 404
- `api.zensurance.com` — HTTP 200, but it is the undocumented backend for the company's own application (root returns the version string `4.0.0`, `/health` returns `{"ok":true}`, every documentation and specification path returns the app's own JSON 404)
- `app.zensurance.com` — HTTP 200, customer login wall

The only public API claim is on the [partnership page](https://www.zensurance.com/zensurance-partnerships) (HTTP 200): *"Seamless API integrations and co-branded white-label tools that align with your systems."* No endpoint, base URL, auth scheme, sandbox, or reference documentation accompanies it — the entry point is a partnership application form. The integration is **partner-gated and privately negotiated**.

- **OpenAPI/Swagger specs harvested:** 0
- **ACORD posture:** no ACORD reference found — zero matches for ACORD, AL3, ACORD XML, NGDS, IVANS, Applied Epic, Vertafore, or AMS360 across the site and its 357-page sitemap
- **Quote / bind / issue / FNOL:** none exposed as an API; all four run through the first-party web application or licensed broker staff
- **Auth model:** none published; the first-party backend uses a session cookie, and neither `/.well-known/openid-configuration` nor `/.well-known/oauth-authorization-server` is served
- **Webhooks / AsyncAPI:** none documented
- **Public Postman workspace:** none
- **GraphQL / gRPC:** none

This is a correct and expected outcome for the sector. Canada has no open-insurance mandate: OSFI supervises federally-regulated insurers prudentially while FSRA, the AMF, and the other provincial regulators own market conduct, and Consumer-Driven Banking excludes insurance outright. Zensurance sits in the thin digital-broker layer beneath a Big-Few carrier oligopoly, and — unlike the traditional Canadian brokerage channel — never touched the ACORD/AL3 agency-download rails at all.

See [review.yml](review.yml) for the full probe log, HTTP statuses, and provenance.

## Tags

- Insurance
- Canada
- Insurtech
- Broker
- Property and Casualty
- Commercial Insurance
- Small Business Insurance
- Cyber Insurance
- Digital Brokerage
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

No public, self-serve APIs are documented. `apis[]` is intentionally empty.

## Links

- [Website](https://www.zensurance.com/)
- [Blog](https://www.zensurance.com/blog)
- [Partnership Program](https://www.zensurance.com/zensurance-partnerships)
- [Customer Application](https://app.zensurance.com/)
- [GitHub Organization](https://github.com/zensurance)
- [Careers](https://www.zensurance.com/careers)
- [Privacy Policy](https://www.zensurance.com/privacy-policy)

## Maintainers

- Kin Lane — kin@apievangelist.com
