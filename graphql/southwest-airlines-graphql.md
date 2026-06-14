# Southwest Airlines GraphQL Schema

This directory contains a conceptual GraphQL schema for Southwest Airlines covering the airline's core flight, booking, loyalty, and ancillary service domains.

## Overview

Southwest Airlines operates one of the largest domestic air networks in the United States, distinguishing itself through low fares, a no-baggage-fee policy, open seating, and the Rapid Rewards loyalty program. While Southwest does not publish a public GraphQL API, this schema models the full breadth of business concepts exposed across southwest.com, the Rapid Rewards program, and partner integrations.

The schema is structured around five primary domains:

- **Flights** — schedules, routes, status, delays, and cancellations
- **Booking** — reservations, itineraries, PNRs, confirmations, and hold policies
- **Boarding** — open seating, boarding groups, positions, and boarding passes
- **Rapid Rewards** — points, tiers, companion pass, earning categories, and bonuses
- **Ancillaries** — EarlyBird Check-In, Upgraded Boarding, baggage policy, vouchers, and travel funds

## Schema File

`southwest-airlines-schema.graphql`

## Named Types

### Aircraft and Airports

| Type | Description |
|------|-------------|
| `Airport` | A commercial airport served by Southwest, identified by IATA code |
| `Terminal` | A terminal or concourse within an airport |
| `Gate` | A departure or arrival gate |
| `Aircraft` | Interface for Southwest fleet aircraft |
| `Boeing737` | Boeing 737 aircraft — the only aircraft type in Southwest's all-737 fleet |

### Flights

| Type | Description |
|------|-------------|
| `Flight` | A scheduled flight between two airports |
| `FlightNumber` | Carrier + number identifier for a Southwest service |
| `FlightSchedule` | Recurring service pattern on given days of the week |
| `FlightRoute` | City-pair route served by Southwest |
| `FlightStatus` | Real-time operational status (on-time, delayed, cancelled, diverted) |
| `DirectFlight` | A nonstop flight with no intermediate stops |
| `Connection` | A connecting itinerary with layovers |
| `Layover` | An intermediate stop between two flight segments |
| `Departure` | Departure airport, gate, and time details |
| `Arrival` | Arrival airport, gate, baggage claim, and time details |
| `Delay` | Delay details including reason and new departure time |
| `Cancel` | Cancellation details and rebooking options |

### Seating and Boarding

| Type | Description |
|------|-------------|
| `OpenSeating` | Southwest's open seating model — no assigned seats |
| `Seat` | A physical seat row and position on an aircraft |
| `BoardingGroup` | One of three boarding groups (A, B, C) |
| `BoardingPosition` | A specific position within a boarding group (e.g., A32) |
| `BoardingPass` | An issued boarding pass for a passenger on a flight |
| `MobileBoarding` | Mobile boarding pass with wallet and deep link URLs |
| `Checkin` | A passenger check-in event with method and timestamp |

### Fare Products

| Type | Description |
|------|-------------|
| `WannaGetAway` | Southwest's lowest restricted fare |
| `WannaGetAwayPlus` | Enhanced low fare with added flexibility |
| `Anytime` | Fully flexible, refundable fare |
| `BusinessSelect` | Premium fare with A1-A15 boarding, drink coupon, and priority security |

### Booking and Reservations

| Type | Description |
|------|-------------|
| `Booking` | A completed flight booking |
| `Reservation` | Reservation record tied to a booking |
| `PNR` | Passenger Name Record — the airline booking reference |
| `Confirmation` | Booking confirmation sent to the customer |
| `Itinerary` | Full travel itinerary including outbound and return segments |
| `HoldPolicy` | Rules for holding a fare price before purchase |

### Passengers

| Type | Description |
|------|-------------|
| `Passenger` | A traveler booked on a Southwest flight |

### Rapid Rewards Loyalty

| Type | Description |
|------|-------------|
| `RapidRewards` | The Southwest loyalty program |
| `RapidRewardsAccount` | A member's loyalty account |
| `Tier` | A loyalty tier level with benefits and requirements |
| `TierRequirements` | Annual points and flight requirements to qualify for a tier |
| `AList` | Entry-level elite status — 25% points bonus and priority check-in |
| `AListPreferred` | Top elite status — 100% points bonus and complimentary Wi-Fi |
| `Companion` | A designated companion for a Companion Pass holder |
| `CompanionPass` | Benefit allowing one companion to fly free on every booked flight |
| `Points` | A member's Rapid Rewards points balance |
| `PointsBonus` | A bonus earning promotion available on eligible fares |
| `EarningCategory` | A category for earning points (flights, partners, credit card) |

### Ancillaries

| Type | Description |
|------|-------------|
| `EarlyBird` | Purchased automatic 36-hour check-in for an improved boarding position |
| `CheckInEarlyBird` | EarlyBird check-in result with assigned boarding position |
| `UpgradeBoarding` | Purchased A1-A15 boarding position at the gate |
| `Voucher` | A travel voucher or credit |
| `LUVVoucher` | Dollar-denominated Southwest gift certificate |
| `TravelFund` | Credit held from a cancelled reservation |
| `CancellationCredit` | Credit issued from a cancelled non-refundable booking |

### Policies and Fees

| Type | Description |
|------|-------------|
| `BaggagePolicy` | Southwest's two-free-bags checked baggage policy |
| `FreeBaggage` | Details of the free checked bag allowance |
| `OverweightBag` | Fees for bags exceeding weight limits |
| `ChangeFee` | Southwest's no-change-fee policy details |
| `Refundable` | Refundable fare details |
| `NonRefundable` | Non-refundable fare details with travel fund issuance |

### API Access

| Type | Description |
|------|-------------|
| `APIKey` | An API key for partner or developer access |
| `Token` | An authentication bearer token |

## Enumerations

| Enum | Values |
|------|--------|
| `FareClass` | WANNA_GET_AWAY, WANNA_GET_AWAY_PLUS, ANYTIME, BUSINESS_SELECT |
| `BoardingGroupLabel` | A, B, C |
| `FlightStatusCode` | ON_TIME, DELAYED, CANCELLED, DIVERTED, LANDED, DEPARTED, SCHEDULED |
| `TierLevel` | A_LIST, A_LIST_PREFERRED, COMPANION_PASS, STANDARD |
| `BaggageStatus` | INCLUDED, FEE_APPLIES, OVERSIZED |
| `SeatZone` | FORWARD_CABIN, MIDDLE_CABIN, AFT_CABIN |
| `CheckInMethod` | MOBILE, WEB, KIOSK, AGENT |
| `RefundPolicy` | REFUNDABLE, NON_REFUNDABLE, TRAVEL_FUND |
| `VoucherType` | LUV_VOUCHER, TRAVEL_FUND, POINTS_CREDIT |
| `DelayReason` | WEATHER, AIR_TRAFFIC_CONTROL, MECHANICAL, CREW, LATE_AIRCRAFT, SECURITY |

## Root Operations

### Queries
- `airport` — look up an airport by IATA code
- `airports` — list all Southwest-served airports
- `flight` — retrieve a flight by ID
- `searchFlights` — search available flights by route and date
- `flightStatus` — real-time status for a flight number and date
- `booking` — retrieve a booking by confirmation number
- `rapidRewardsAccount` — retrieve a member's loyalty account
- `points` — current points balance for a member
- `vouchers` — active vouchers and travel funds for a passenger
- `baggagePolicy` — Southwest's baggage policy details
- `earlyBirdAvailability` — check EarlyBird purchase eligibility
- `upgradeBoardingAvailability` — check gate-purchased upgrade availability

### Mutations
- `bookFlight` — book a flight for one or more passengers
- `cancelBooking` — cancel a booking and receive a cancellation credit
- `purchaseEarlyBird` — add EarlyBird Check-In to a booking
- `purchaseUpgradeBoarding` — buy an A1-A15 boarding position at the gate
- `checkIn` — check in a passenger for a flight
- `designateCompanion` — set or change the Companion Pass companion
- `redeemVoucher` — apply a LUV Voucher to a booking
- `issueAPIKey` — provision an API key for partner access
- `refreshToken` — refresh an authentication token

### Subscriptions
- `flightStatusUpdates` — real-time flight status stream
- `gateChanges` — gate change notifications
- `boardingPositionAssigned` — boarding position assignment events

## Source

Schema developed from public knowledge of Southwest Airlines products and policies including southwest.com, the Rapid Rewards program terms, and publicly documented API behavior from third-party aggregators.

- Human URL: https://www.southwest.com/
- Developer URL: https://developer.southwest.com/
