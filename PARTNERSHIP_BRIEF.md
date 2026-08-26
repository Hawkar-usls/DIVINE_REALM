# PLAYGRID / DIVINE_REALM — Science Partnership Brief

> Public evaluation prototype. The current browser build does not yet claim to execute real scientific workloads.

## One-line proposal

**Pair a conventional game surface with an independent, opt-in scientific-compute lane whose work is accepted and verified by a real research Requestor/project.**

## Architecture

```text
PLAYER / TELEGRAM WEBAPP
          |
          +-----------------------> GAME / RNG / PAYOUT
          |
          +--> EXPLICIT CONSENT + DEVICE POLICY
                         |
                         v
                  PLAYGRID GATEWAY
                         |
             approved scientific Requestor
                         |
                  compute provider
                         |
             verified result / receipt
                         |
                    IMPACT LEDGER
```

The compute scheduler is driven by consent, resource caps and available scientific work — **not by spin count, stake size, player losses or session intensity**. The game only visualizes status.

## Golem bridge

Golem can be one compute substrate when a compatible scientific Requestor exists:

```text
SCIENTIFIC REQUESTOR
       ↓
PLAYGRID Gateway / Yagna
       ↓
Golem providers
       ↓
scientific workload
       ↓
result + authoritative upstream receipt
       ↓
Impact Ledger
```

**Truth boundary:** Golem is distributed-compute infrastructure. It is not itself a vaccine-discovery project. DIVINE_REALM only claims scientific contribution after a real workload owner/research partner accepts and verifies the work.

## Player proposition

Before activation the user sees:

- compute is OFF by default;
- workload/project class;
- requested resource cap;
- immediate stop/revoke control;
- verified contribution/impact credits;
- explicit statement that compute does not improve gambling odds.

The product must never say or imply “play longer to help science more”. Compute-only participation must remain possible.

## Partner proposition

For an operator/aggregator:

- differentiation without changing certified game math;
- reusable science/public-good infrastructure across multiple titles;
- independently auditable contribution receipts;
- research/CSR campaigns based on actual accepted compute rather than vague claims.

For a research/cloud/distributed-compute partner:

- a new opt-in compute acquisition channel;
- bounded workloads with visible resource policy;
- public-facing impact reporting tied to upstream evidence;
- no transfer of scientific authority to the game.

## Risk context

JANUS' internal `JANUS_ADDICTIVE_ENGAGEMENT_INDEX` models **Gambling disorder = 82.2/100, EXTREME, model interval 74–90, evidence confidence MODERATE_HIGH**. It explicitly states this is a synthetic evidence-anchored model output, **not prevalence and not an individual probability of addiction**.

Canonical artifact:
`Hawkar-usls/janus-meta-registry/data/AI-LOVER-ADDICTIVE-ENGAGEMENT-INDEX-2026-08-24-v1.0.json`

Therefore DIVINE_REALM forbids:

```text
losses -> more science credit
stake size -> more science credit
more spins -> higher compute rate
charity pressure -> continued wagering
compute -> better RNG/RTP/bonuses
```

## Scale model

The clean first model is compute-based rather than event-based:

```text
verified_science_compute
  = opted_in_compute_hours
  × accepted_compute_units_per_hour
  × upstream_acceptance_rate
```

Scientific impact claims require workload-specific interpretation from the research partner. Compute hours alone are not medical outcomes.

## Minimal receipt

- `task_id`
- `consent_id`
- `campaign_id`
- `workload_id`
- `research_requestor_id`
- `provider_id`
- `started_at`
- `completed_at`
- `input_commitment_hash`
- `output_hash`
- `upstream_acceptance_status`
- `verification_status`
- `game_effect = NONE`

## Pilot

```text
DIVINE_REALM PUBLIC DEMO
 + PLAYGRID Gateway
 + one real scientific Requestor
 + one approved compute provider path
 + authoritative receipt store
```

Success means: explicit consent, actual accepted workload, independently verifiable receipts, acceptable energy/thermal behavior, immediate stop, and zero authority over game mathematics.

Public demo: [`playgrid.html`](playgrid.html)

Golem science model: [`.janus/PLAYGRID_GOLEM_SCIENCE_MODEL.json`](.janus/PLAYGRID_GOLEM_SCIENCE_MODEL.json)

See also: [`LICENSE.md`](LICENSE.md) and [`IP_NOTICE.md`](IP_NOTICE.md).
