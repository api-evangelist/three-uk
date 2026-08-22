# Three UK (three-uk)

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

Three UK (Hutchison 3G UK Limited, Reading, England) is a United Kingdom mobile network operator that launched in 2003 as the country's first 3G-only carrier and grew into a consumer and business mobile, 5G, and home broadband provider, also operating the SMARTY sub-brand. Since 31 May 2025 Three UK has been a wholly owned subsidiary of VodafoneThree, the merged Vodafone UK / Three UK joint venture that is 51% Vodafone Group and 49% CK Hutchison Holdings, serving roughly 27 million UK customers. In the telecom value chain Three UK is a network owner and access provider, not a developer platform — it sells connectivity, coverage, wholesale and MVNO capacity, and business connectivity, while its group-level enterprise, IoT, private-network and wholesale propositions are marketed through CK Hutchison's CKH IOD and Three Group Solutions.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/three-uk/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/three-uk/refs/heads/main/apis.yml)

## Tags

- Telecommunications
- United Kingdom
- Mobile Network Operator
- Network APIs
- CAMARA
- GSMA Open Gateway
- 5G
- Broadband
- Roaming
- SIM Swap
- Identity Verification
- Age Verification
- Wholesale
- MVNO
- Partner Gated

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## APIs

**None listed.** Three UK publishes no public API.

This is an honest finding, not a gap in the research. As of 25 July 2026:

- There is no first-party developer portal. `developer.three.co.uk`, `developers.three.co.uk`, `docs.three.co.uk`, `apis.three.co.uk`, `sandbox.three.co.uk`, `opengateway.three.co.uk` and `developers.opengateway.three.co.uk` all resolve through a wildcard DNS record to the same Akamai edge address, whose TLS certificate (`O=Hutchison 3G UK Limited, CN=three.co.uk`) does not cover any of them — the handshake fails. `api.three.co.uk` resolves to a separate address that times out on port 443.
- `www.three.co.uk/developer`, `/developers`, `/api`, `/business/api` and `/opengateway` all return **404**. The homepage and `/business` page contain no occurrence of "developer" or "api".
- The Wayback Machine holds **no** archived snapshot of a Three UK developer portal. This is not an abandoned developer programme — Three UK appears never to have run one.
- No OpenAPI, Swagger, AsyncAPI, GraphQL SDL, or `.proto` is published. `/openapi.json`, `/swagger.json`, `/api-docs`, `/graphql` and both OAuth/OIDC `.well-known` documents return 404.
- No first-party SDKs on npm, PyPI, Maven or NuGet. No public Postman workspace.

## CAMARA and GSMA Open Gateway

Three UK is a genuine participant in the telecom sector's standards layer, and this is the finding that matters for this provider:

- **CAMARA participant.** The CAMARA Project's own governance roster lists `Three UK | Jason Tesh`, with four further named participants under `Hutchison`. Parent CK Hutchison Holdings is catalogued in the CAMARA landscape under *Operation / Operators*.
- **GSMA Open Gateway member**, via CK Hutchison Group Telecom.
- **CAMARA APIs with real evidence:** SIM Swap (already available across the UK operators), **KYC Age Verification** and **KYC Tenure** (commercially launched 23 September 2025 alongside BT/EE, Virgin Media O2 and Vodafone Group), with **KYC Match** committed.
- **Not merely a press release** — GSMA describes this as a commercial launch. But none of it is callable from anything Three UK publishes. There is no Three UK base URL, no API reference, no sandbox, no credentials flow.

## How developers actually reach Three UK

Only through somebody else. GSMA names **JT Group (Jersey Telecom)** and **TMT.ID** as already processing hundreds of thousands of UK operator network API calls per month. Three UK's 51% owner **Vodafone Group** is a founding venture partner in **Aduna**, the Ericsson-led network-API joint venture — Three UK itself is not an Aduna partner.

That is the split this sector shows in its purest form: the carrier owns the network capability and helps write the standard, while the entire developer-facing surface — documentation, credentials, sandbox, SDKs, billing — belongs to aggregators and channel partners.

## Auth

None published. CAMARA specifies OpenID Connect and **CIBA** (Client-Initiated Backchannel Authentication) for network-based authorization; **no CIBA reference, OIDC discovery document, or authorization endpoint appears on any Three UK surface.** Authorization for Three UK's CAMARA APIs happens inside the channel partner's platform.

## TM Forum

No TM Forum Open API conformance certification could be confirmed for Three UK or Hutchison 3G UK Limited. The TM Forum certification leaderboard blocks anonymous fetch (HTTP 403), so this is recorded as **unverified**, not as absent.

## Links

- Website — [https://www.three.co.uk/](https://www.three.co.uk/)
- Business — [https://www.three.co.uk/business](https://www.three.co.uk/business)
- Three Group Solutions — [https://groupsolutions.three.com/](https://groupsolutions.three.com/)
- CKH IOD — [https://ckhiod.com/](https://ckhiod.com/)
- CAMARA Project — [https://camaraproject.org/](https://camaraproject.org/)
- CAMARA participants — [https://github.com/camaraproject/Governance/blob/main/PARTICIPANTS.MD](https://github.com/camaraproject/Governance/blob/main/PARTICIPANTS.MD)
- GSMA Open Gateway — [https://www.gsma.com/solutions-and-impact/gsma-open-gateway/](https://www.gsma.com/solutions-and-impact/gsma-open-gateway/)
- GSMA UK launch release (2025-09-23) — [https://www.gsma.com/newsroom/press-release/uk-mobile-operators-launch-age-verification-and-anti-fraud-apis-through-gsma-open-gateway-initiative/](https://www.gsma.com/newsroom/press-release/uk-mobile-operators-launch-age-verification-and-anti-fraud-apis-through-gsma-open-gateway-initiative/)

## Artifacts

The enrichment round of 2026-07-25 re-ran contract discovery against every Three UK, Three Group Solutions, CKH IOD and SMARTY host — `/openapi.json`, `/openapi.yaml`, `/swagger.json`, `/v1/openapi.json`, `/api-docs`, `/docs`, `/redoc`, `/graphql`, `/llms.txt` and the full `/.well-known/` discovery set — and confirmed the original finding: no machine-readable contract exists anywhere. What it did capture is real:

- [`conformance/three-uk-conformance.yml`](conformance/three-uk-conformance.yml) — the CAMARA / GSMA Open Gateway posture, split explicitly between the **organisational** layer (where Three genuinely conforms: named participant, commercially launched SIM Swap / KYC Age Verification / KYC Tenure) and the **publication** layer (where it conforms to nothing, because it publishes nothing).
- [`lifecycle/three-uk-lifecycle.yml`](lifecycle/three-uk-lifecycle.yml) — a network-service lifecycle, not an API one: the live "affected areas" status page, the coverage/network-status checker, and the completed 3G switch-off. No API versioning, deprecation policy, Sunset header support, developer SLA or changelog exists.
- [`well-known/three-uk-well-known.yml`](well-known/three-uk-well-known.yml) — every `/.well-known/` path probed with its status. The only two documents Three UK serves there are the My3 iOS/Android app-association files, saved verbatim.
- [`security/three-uk-domain-security.yml`](security/three-uk-domain-security.yml) — probed: TLS 1.3, HSTS `max-age=31536000`, a five-issuer CAA set, SPF and DMARC (`p=quarantine`), no DNSSEC. No security.txt, no vulnerability-disclosure programme, and no trust centre could be verified.
- [`packages/three-uk-packages.yml`](packages/three-uk-packages.yml) — the eight registries searched and the empty result, plus the unverified `github.com/ThreeUK` organisation (one 2015 SEO repo, no company metadata) recorded as a candidate that is **not** claimed as first-party.
- [`llms/three-uk-llms.txt`](llms/three-uk-llms.txt) — generated, since `https://www.three.co.uk/llms.txt` returns 404. It tells an agent plainly that there is nothing here to call and points it at the aggregators instead.

## Review

See [review.yml](review.yml) for the full reviewer finding, every URL probed with its HTTP status, and the CAMARA / Open Gateway evidence trail.
