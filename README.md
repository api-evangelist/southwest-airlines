# Southwest Airlines

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

Southwest Airlines is one of the world's most profitable airlines and the largest domestic air carrier in the United States by number of passengers. The company provides scheduled air transportation in the United States and near-international markets, known for its low fares, no baggage fees policy, and customer service. Southwest Airlines is a Fortune 500 company headquartered in Dallas, Texas.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/southwest-airlines/refs/heads/main/apis.yml)

## Scope

- **Type:** Contract
- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- Fortune 500
- Airlines
- Aviation
- Travel

## Timestamps

- **Created:** 2026-03-21
- **Modified:** 2026-05-02

## APIs

### Southwest Airlines Flight API

The Southwest Airlines internal flight booking API powers the southwest.com website for searching and booking flights. It provides flight availability, pricing, schedules, and air booking shopping capabilities.

- [Website](https://www.southwest.com/)
- [JSON Schema - Flight](https://raw.githubusercontent.com/api-evangelist/southwest-airlines/refs/heads/main/json-schema/southwest-airlines-flight-schema.json)
- [JSON Schema - Reservation](https://raw.githubusercontent.com/api-evangelist/southwest-airlines/refs/heads/main/json-schema/southwest-airlines-reservation-schema.json)

### Southwest Airlines Rapid Rewards API

The Rapid Rewards loyalty program API enables management of points balances, redemption, and tier status for Southwest Airlines frequent fliers.

- [Rapid Rewards](https://www.southwest.com/rapid-rewards/)

### Southwest Airlines In-Flight Network API

The Southwest Airlines in-flight network provides a JSON API available at getconnected.southwestwifi.com/current.json while onboard the aircraft. It delivers real-time flight information including speed, altitude, position, weather, and flight status to connected passengers.

- [Blog Post](https://apievangelist.com/2016/10/06/your-southwest-airlines-flight-has-an-api/)

## Common Properties

- [Website](https://www.southwest.com)
- [Investor Relations](https://ir.southwest.com/)
- [GitHub Organization](https://github.com/SouthwestAir)
- [Open Source Initiative](https://github.com/SouthwestAir/.github)
- [LinkedIn](https://www.linkedin.com/company/southwest-airlines)
- [X (Twitter)](https://twitter.com/SouthwestAir)

## Artifacts

### JSON Schemas

| Schema | Description |
|---|---|
| [southwest-airlines-flight-schema.json](json-schema/southwest-airlines-flight-schema.json) | Southwest Airlines scheduled flight with route, timing, and status |
| [southwest-airlines-reservation-schema.json](json-schema/southwest-airlines-reservation-schema.json) | Flight reservation (PNR) with passengers, itinerary, and fare data |

### JSON Structure

| Structure | Description |
|---|---|
| [southwest-airlines-flight-structure.json](json-structure/southwest-airlines-flight-structure.json) | Hierarchical structure of flight, reservation, and loyalty data |

### JSON-LD Context

| Context | Description |
|---|---|
| [southwest-airlines-context.jsonld](json-ld/southwest-airlines-context.jsonld) | Linked data context mapping Southwest Airlines vocabulary to schema.org |

### Examples

| Example | Description |
|---|---|
| [southwest-airlines-flight-example.json](examples/southwest-airlines-flight-example.json) | Sample flight from Dallas Love Field to Chicago Midway |
| [southwest-airlines-reservation-example.json](examples/southwest-airlines-reservation-example.json) | Sample reservation with passenger and itinerary details |

### Vocabulary

| Vocabulary | Description |
|---|---|
| [southwest-airlines-vocabulary.yml](vocabulary/southwest-airlines-vocabulary.yml) | Domain vocabulary for Southwest Airlines flight and loyalty operations |

## Maintainers

**FN:** API Evangelist

**Email:** info@apievangelist.com
