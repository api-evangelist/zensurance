# Zensurance (zensurance)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
