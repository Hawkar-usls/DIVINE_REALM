# DIVINE_REALM — Scientific/Public-Good Compute Partnership Brief

> Public evaluation prototype. The current browser build does not yet claim to perform real scientific computation.

## Core idea

DIVINE_REALM explores a simple but unusual separation:

```text
REGULATED GAMEPLAY ------------------> RNG / PAYOUT
        |
        +----------------------------> SCIENTIFIC COMPUTE GATEWAY
                                         |
                                         +--> approved workload provider
                                         +--> data center / cloud / research project
                                         +--> verifiable receipt / impact ledger
```

The gambling/game layer and the compute layer are **independent**. A spin can act as an auditable trigger or accounting event for a capped compute contribution, but compute success, speed, output, device power, or scientific result must never affect odds, RTP, payout, bonus eligibility, or RNG.

## What is innovative

The proposed system turns an existing interactive entertainment surface into a gateway for **verifiable, externally useful computation** without pretending that the scientific workload itself is the game.

A production partner could map eligible events to one of two safer models:

1. **Server-funded compute credit:** the operator/sponsor allocates a fixed, capped amount of compute to an approved project or data-center workload.
2. **Explicit opt-in device compute:** technically compatible users separately consent to a bounded worker. This is optional and should be used only if platform, thermal, security, privacy, research, and regulatory review show it is appropriate.

For Telegram/WebView/mobile deployments, the server-funded/server-routed model is the preferred default. A browser demo can show the gateway/API and receipt flow without pretending to be a native BOINC or Folding@home worker.

## Why a casino/platform partner might care

- **Differentiation without altering certified game mathematics.** The compute gateway sits beside RNG rather than inside it.
- **Auditable impact.** Workload ID, provider, compute units, timestamps, hashes, and attestations can be displayed or independently audited.
- **Reusable infrastructure.** Once integrated at platform/aggregation level, multiple games can use the same compute gateway.
- **Research/CSR campaigns.** Operators can sponsor approved workloads with a transparent cap instead of making vague “gaming for good” claims.
- **New B2B relationships.** Gaming platforms, cloud/data-center providers, universities, and distributed-compute projects can participate in one measurable pipeline.

## Why a data-center / cloud / scientific partner might care

- a new channel of prepaid or sponsored compute demand;
- burstable workloads with explicit quotas and scheduling windows;
- a public-facing impact ledger backed by actual task receipts;
- geographically distributed campaign funding without handing control of the scientific result to game logic;
- ability to accept only workload classes that fit the infrastructure and research protocol.

Scientific partners must retain authority over scientific validity. DIVINE_REALM does not decide that a workload is medically/scientifically useful merely because it can execute it.

## Responsible-gaming constraint

The JANUS Addictive Engagement Index (J-AEI) models **Gambling disorder at 82.2/100 (EXTREME; model interval 74–90)**. The source explicitly states that this is a synthetic evidence-anchored model score, **not addiction prevalence and not the probability that an individual player develops a disorder**.

Source: `Hawkar-usls/janus-meta-registry/data/AI-LOVER-ADDICTIVE-ENGAGEMENT-INDEX-2026-08-24-v1.0.json`.

This matters because “help science by gambling more” would create the wrong incentive. A production DIVINE_REALM gate should enforce:

- compute contribution independent of stake size and player losses;
- no contribution acceleration for longer sessions;
- a fixed/time-capped contribution budget;
- responsible-gaming limits override any scientific campaign;
- no guilt, charity pressure, or claim that additional wagering is required to help research;
- clear separation between wager accounting and scientific-compute accounting.

The intended value proposition is: **reuse already-authorized digital activity as a trigger/accounting surface for useful computation — never manufacture additional gambling activity to increase compute.**

## Initial scale model

Use event volume and a predeclared compute credit, not addiction prevalence:

```text
annual_scientific_compute_budget
  = eligible_events_per_day
  × compute_credit_per_event
  × 365
```

Illustrative scenarios for **1,000,000 eligible events/day**:

| Compute credit per eligible event | Daily sponsored compute | Annual sponsored compute |
|---:|---:|---:|
| $0.0001 | $100 | $36,500 |
| $0.001 | $1,000 | $365,000 |
| $0.01 | $10,000 | $3,650,000 |

These figures are **illustrations, not forecasts**. They do not estimate gambling revenue, player losses, scientific output, medical benefit, or partner profit. A real pilot needs workload-specific throughput and cloud/data-center benchmarks.

## Verification contract

A production receipt should be capable of proving at least:

```text
event_receipt_id
campaign_id
workload_id
research_or_provider_id
resource_class
requested_compute_units
started_at
completed_at
input_commitment_hash
output_hash
provider_attestation
compute_credit
status
```

The gaming receipt may be referenced for audit linkage, but never used to contaminate scientific validity or RNG independence.

## Minimal pilot

```text
DIVINE_REALM DEMO
      |
      +--> operator / aggregator sandbox
      |
      +--> compute-gateway API
      |
      +--> one approved workload/provider
      |
      +--> signed receipt + dashboard
```

Pilot success criteria: separation from RNG, auditable receipts, actual workload acceptance, measured cost/throughput, negligible game latency, abuse resistance, responsible-gaming compliance, and independent confirmation from the workload owner.

See [`LICENSE.md`](LICENSE.md) and [`IP_NOTICE.md`](IP_NOTICE.md).
