# PLAYGRID / DIVINE_REALM — Science-Default Amorphous Compute Brief

> Public evaluation prototype. The current browser build does not yet claim real scientific workloads or production provider receipts.

## One-line proposal

**Use DIVINE_REALM as a science-default presentation for a provider-agnostic compute-routing layer whose destination can be changed without changing game mathematics.**

## Architecture

```text
PLAYER / TELEGRAM WEBAPP
          |
          +-----------------------> GAME / RNG / PAYOUT
          |
          +--> EXPLICIT CONSENT + DEVICE POLICY
                         |
                         v
                  PLAYGRID ROUTER
                         |
       ┌─────────────────┼──────────────────┐
       ↓                 ↓                  ↓
   SCIENCE            MARKETPLACE       DATACENTER
   default             e.g. Golem        / OPERATOR
       │                 │                  │
       └─────────────────┼──────────────────┘
                         ↓
                 VERIFIED RECEIPT
                         ↓
       IMPACT / PLAYER EARNINGS / TREASURY
```

The compute scheduler is driven by consent, device policy and provider capacity — **not by spin count, stake size, wins/losses or session intensity**. The game only exposes consent and read-only compute status.

## Science is the default, not a lock-in

DIVINE_REALM keeps its scientific/public-good identity, but the underlying PLAYGRID route can be replaced by a licensed buyer using:

```text
ProviderManifest
+ server adapter
+ authoritative receipt verifier
+ sink/accounting policy
```

No RNG/RTP/wager/bonus code needs to change.

## Reference routes

### Science / public good

A real compatible research Requestor/workload produces `SCIENCE_UPSTREAM_RECEIPT` evidence into an Impact Ledger.

### Golem / compute marketplace

Golem can be a general compute-market route. If the Requestor happens to be scientific, scientific authority still belongs to the real workload owner — not to Golem or the slot.

### Data center / cloud

A buyer can redirect the same routing fabric to approved CPU/GPU/batch workloads on its own infrastructure or a contracted provider.

### Operator / custom

Approved non-sensitive operator jobs or a future provider can be admitted through signed server configuration and a provider-specific verifier.

## Player proposition

Before compute starts the user sees:

- compute is OFF by default;
- selected route/provider class;
- resource cap;
- immediate stop/revoke;
- visible receipt/contribution state;
- explicit statement that compute does not improve gambling odds.

The project forbids “play longer to help science more”. Compute-only participation must remain possible.

## Partner proposition

For an operator/aggregator:

- one compute integration boundary across multiple workload classes;
- provider replacement without changing certified game math;
- verifiable impact/economic reporting;
- a route to research, marketplaces and data-center partners.

For a research/compute partner:

- a new opt-in compute acquisition/distribution channel;
- bounded workloads and explicit resource policy;
- public-facing receipts tied to upstream evidence;
- no transfer of scientific authority to game logic.

## Risk context

JANUS' `JANUS_ADDICTIVE_ENGAGEMENT_INDEX` models **Gambling disorder = 82.2/100, EXTREME, model interval 74–90, evidence confidence MODERATE_HIGH**. The source explicitly states this is a synthetic model output, not prevalence or an individual probability of addiction.

Canonical artifact:
`Hawkar-usls/janus-meta-registry/data/AI-LOVER-ADDICTIVE-ENGAGEMENT-INDEX-2026-08-24-v1.0.json`

Therefore every route forbids:

```text
losses -> more compute reward
stake size -> more compute rate
more spins -> more compute scheduling
charity pressure -> continued wagering
compute -> better RNG/RTP/bonuses
```

## Public handoff

- Route-switchable demo: [`playgrid.html`](playgrid.html)
- Buyer handoff contract: [`OPERATOR_HANDOFF_SPEC.json`](OPERATOR_HANDOFF_SPEC.json)
- Licensing: [`LICENSE.md`](LICENSE.md)
- IP boundary: [`IP_NOTICE.md`](IP_NOTICE.md)

A clean pilot needs one real approved route, one authoritative receipt path and explicit consent. Science remains DIVINE_REALM's default story; PLAYGRID remains the reusable infrastructure underneath.
