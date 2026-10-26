# Inbound Health

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

Inbound Health was a Minneapolis, Minnesota company that enabled health systems and health plans to
deliver hospital-level and skilled-nursing-level care in patients' homes. It was spun out of Allina
Health's Hospital-at-Home and SNF-at-Home programs in October 2022 with $20 million from Flare
Capital Partners, raised a $30 million Series B led by HealthQuest Capital in September 2023, and in
February 2024 released **Inbound InHome** — a patient-management and analytics platform combining
AI/ML patient identification, device-agnostic biometric monitoring, a virtual care module, episode
workflow automation, supply-chain management, and integration points into multiple EMRs.

**The company is defunct.** Inbound Health ceased operations in December 2025 after regulatory
uncertainty over the federal Acute Hospital Care at Home (AHCAH) waiver stalled its next financing
round, and MedArrive acquired its AI-backed care-navigation technology assets in March 2026.

## API surface

None. Inbound InHome was sold only under signed health-system and health-plan agreements; no public
developer portal, API reference, SDK, or machine-readable specification (OpenAPI, AsyncAPI, GraphQL
SDL, MCP manifest or A2A agent card) was ever published on an Inbound Health host.

Probed 2026-08-23:

| Probe | Result |
|---|---|
| `https://inboundhealth.com/` | `526` — Cloudflare edge is live, origin is gone |
| `https://inboundhealth.com/openapi.json` (and `/swagger.json`, `/api-docs`, `/docs`, `/llms.txt`) | `526` |
| every `https://inboundhealth.com/.well-known/*` path | `526` |
| `http://inboundhealth.com/<any path>` | `404`, byte-identical 1,957-byte "Site is not available" page |
| `api.` / `docs.` / `developer.` / `app.` / `portal.` / `status.inboundhealth.com` | no DNS record |
| `https://github.com/InboundHealth` | organization exists, **0 public repositories** |

The domain is still registered to the company (GoDaddy, registry expiry 2027-01-06) and MX still
routes to Microsoft 365, but nothing is served. Because the site is confirmed dead it is
deliberately **not** wired as a `Website` pointer. The previous `Website` pointer on this profile
(`https://www.nasdaqprivatemarket.com/`) was the secondary-market venue this company was harvested
from — not Inbound Health's own web presence — and has been removed.

## Artifacts

- `well-known/inbound-health-well-known.yml` — the full `/.well-known/` and contract-discovery
  probe, including the negative controls. Records an absence; no `WellKnown` pointer is emitted.
- `security/inbound-health-domain-security.yml` — DNS/TLS posture of the retained domain: no
  DNSSEC, no CAA, no DMARC, no HSTS, and **two conflicting `v=spf1` records**, which makes SPF
  evaluation permerror for the whole domain under RFC 7208.
