# DIVINE_REALM — Positive Compute Gate Roadmap

## Mission

DIVINE_REALM becomes the **positive gateway** of the paired slot ecosystem.

With explicit, revocable user consent, spare CPU/GPU capacity may be contributed to legitimate distributed-science workloads while the game is open or while a standalone compute mode is active. The game may visualize that contribution as part of its narrative/animation layer, but **scientific compute must never influence RNG, RTP, payout probability, bet size, or spin timing**.

The target is not “gambling justified by charity.” The target is a system where an entertainment surface can optionally carry a verifiable public-benefit compute payload without exploiting the player.

Paired repository: `Hawkar-usls/SSlot`.

---

## Non-negotiable invariants

1. **Explicit opt-in only.** No mining/science workload may begin before a clear consent action.
2. **Instant pause/stop.** The user can stop compute without losing game access, balance, eligibility, or status.
3. **No RNG coupling.** Compute contribution can never alter odds, RTP, reel result, bonus probability, jackpot probability, or payout.
4. **No wagering coercion.** “Compute more to win more,” “spin to cure disease,” “loss equals contribution,” or similar framing is forbidden.
5. **No hidden utilization.** CPU/GPU/RAM/network use must be visible and bounded.
6. **Thermal/power guard.** Idle-only is the default; battery, temperature, load, and user activity can automatically suspend compute.
7. **Scientific provenance.** Only allowlisted projects/adapters with documented provenance and terms may receive work.
8. **Result integrity.** Contribution claims are accepted only after project-side validation or an equivalent verifiable receipt.
9. **Privacy minimization.** No personal files, browsing data, wallet secrets, Telegram content, or unrelated telemetry may enter work units.
10. **Standalone usefulness.** A user who does not gamble must still be able to use the public-benefit compute layer where deployment policy permits it.

---

## Concept: “the cartoon is the window, not the work”

The visual/narrative sequence shown during a spin may **represent** real compute progress, but the animation itself must not be falsely described as scientific computation.

Preferred model:

```text
approved science project
        ↓
 signed/validated work unit
        ↓
 low-priority local compute
        ↓
 contribution receipt
        ↓
 narrative visualization
        ↓
 public impact ledger
```

Examples of eligible adapter classes include:

- Folding@home-style protein/molecular simulation clients;
- BOINC-compatible projects such as World Community Grid tasks;
- future university/laboratory workloads that satisfy the same provenance and validation gates.

The first implementation should use official project clients or documented APIs/adapters rather than reimplementing scientific kernels inside the slot.

---

## Architecture

### 1. `ComputeConsentGate`

Stores a revocable consent record:

- enabled/disabled;
- CPU percentage cap;
- GPU enabled/disabled;
- idle-only policy;
- network cap;
- battery policy;
- thermal policy;
- selected project(s);
- timestamp and consent version.

No valid consent = no external compute.

### 2. `ScienceComputeBroker`

A narrow broker between DIVINE_REALM and allowlisted compute clients.

Responsibilities:

- discover available official client;
- request/observe work units;
- never inspect unrelated user data;
- throttle resources;
- pause instantly;
- surface status only.

It must not generate reel outcomes or touch gambling balances.

### 3. `ContributionReceipt`

Each accepted unit produces a receipt containing only the minimum useful evidence:

```json
{
  "project_id": "...",
  "work_unit_ref_hash": "...",
  "validation_status": "ACCEPTED",
  "cpu_seconds": 0,
  "gpu_seconds": 0,
  "energy_estimate_wh": 0,
  "completed_at": "...",
  "receipt_hash": "..."
}
```

Where project policies permit, receipts should be independently verifiable without exposing the player's identity.

### 4. `ImpactVisualizer`

Maps validated compute progress into cosmetic/narrative state.

Allowed:

- show completed work units;
- show aggregate CPU/GPU time;
- visualize a protein, molecule, grid, constellation, temple, etc. as a metaphor for progress;
- award non-wagering badges or cosmetic milestones.

Forbidden:

- better odds for more compute;
- bonus spins for compute;
- hiding losses behind “you helped science” messaging;
- claiming a scientific discovery before the upstream project validates it.

### 5. `PublicImpactLedger`

Publish aggregate, privacy-preserving metrics:

- validated work units;
- project distribution;
- total compute time;
- estimated energy use;
- rejected/invalid work;
- timestamped receipt roots/hashes;
- any operator-funded donations associated with the program.

Do not publish individual gambling losses beside scientific contribution.

---

## Two-mode UX

### Mode A — Play + Compute

User explicitly enables compute. Low-priority work may continue while the slot UI is open.

The visual spin can display compute progress, but the spin result is precommitted/independent from compute completion.

### Mode B — Compute Only

No wagering interface is required. The user can contribute spare compute and view the same impact dashboard without placing bets.

This mode is important because the public-benefit layer must not require gambling.

---

## Resource policy v0.1

Default proposal for prototype testing, not production defaults:

- compute OFF by default;
- idle-only ON by default;
- CPU cap configurable, low default;
- GPU OFF until explicitly enabled;
- suspend on battery unless user explicitly allows it;
- suspend on thermal threshold;
- suspend immediately on active gameplay if frame time or input latency degrades;
- display estimated power/energy consumption rather than implying compute is free.

---

## Scientific project admission gate

Before an adapter becomes `ENABLED`, record:

- project owner/institution;
- official client/API source;
- license/terms;
- workload purpose;
- validation mechanism;
- data/privacy model;
- supported platforms;
- security review status;
- current operational status;
- external contact/maintainer if available.

Initial research candidates:

- Folding@home;
- BOINC / World Community Grid;
- other verified academic BOINC projects.

No project is enabled solely because it has a medical-sounding name.

---

## Milestones

### P0 — Contract freeze

- [ ] Freeze consent schema.
- [ ] Freeze strict RNG/compute separation.
- [ ] Freeze resource and thermal limits.
- [ ] Freeze public receipt schema.
- [ ] Add tests proving compute cannot alter payout state.

**Gate:** `COMPUTE_CANNOT_CHANGE_GAMBLING_OUTCOME = PASS`.

### P1 — Local simulator

- [ ] Build fake work-unit adapter.
- [ ] Implement pause/resume/throttle.
- [ ] Generate signed local receipts.
- [ ] Drive narrative visuals from fake progress only.

**Gate:** no real external workload yet.

### P2 — First real science adapter

- [ ] Integrate one official distributed-compute client in sandboxed/sidecar form.
- [ ] Read only documented status/progress APIs.
- [ ] Verify completion/acceptance.
- [ ] Store receipt hash.

**Gate:** `REAL_SCIENCE_RECEIPT_VERIFIED = PASS`.

### P3 — Impact dashboard

- [ ] Add compute-only mode.
- [ ] Show validated units, compute time, estimated energy and project provenance.
- [ ] Separate impact metrics from gambling metrics.

### P4 — Narrative integration

- [ ] Bind progress to visual storytelling.
- [ ] Keep game outcome independent.
- [ ] Add accessibility/reduced-motion path.
- [ ] Prohibit celebration of losses or break-even results.

### P5 — Security and privacy review

- [ ] Signed client binaries / provenance checks.
- [ ] Sandboxing.
- [ ] Network allowlist.
- [ ] No arbitrary remote code execution.
- [ ] No access to wallet secrets or unrelated files.
- [ ] Abuse/replay/forged-receipt tests.

### P6 — Energy and environmental accounting

- [ ] Estimate Wh per validated task.
- [ ] Show user-level estimate locally.
- [ ] Publish aggregate energy metrics.
- [ ] Add optional carbon-intensity-aware scheduling where reliable data exists.

### P7 — Non-money public pilot

- [ ] Run with play-money/demo mode only.
- [ ] Measure opt-in rate, thermal impact, false receipts, user understanding, and actual validated science contribution.
- [ ] Independent review of coercion and consent UX.

### P8 — Real-money deployment gate

Blocked until separate legal/licensing, gambling-safety, privacy, security, payment, AML/KYC where applicable, accessibility, scientific-project terms, and independent RNG/math reviews pass.

---

## Success metrics

The positive gateway succeeds when it can prove all of the following at once:

```text
VALIDATED_SCIENCE_COMPUTE > 0
USER_CONSENT = EXPLICIT_AND_REVOCABLE
HIDDEN_COMPUTE = 0
RNG_DEPENDENCE_ON_COMPUTE = 0
WAGERING_ADVANTAGE_FROM_COMPUTE = 0
PUBLIC_RECEIPT_AUDIT = PASS
THERMAL_AND_ENERGY_GUARDS = PASS
COMPUTE_ONLY_MODE = AVAILABLE
```

The core metric is **verified public-benefit computation per unit of voluntarily donated resource**, not spins, losses, ARPU, or time-on-device.
