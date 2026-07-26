# Three UK (three-uk)

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
