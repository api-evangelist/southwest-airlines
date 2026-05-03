# Southwest Airlines

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
