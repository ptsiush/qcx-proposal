# 09 — Milestones and budget

**Total ask: USD 55,000 equivalent. Paid per closed milestone. No upfront payment.**
The final milestone (launch) is 27% of the total.

## M1 — Working MVP on a test group ($10,000)

**Deliverables**
- Client portal: sign-up, job upload, budget, progress, results.
- Scheduler and WASM worker with 2-of-3 redundant execution.
- Integration with one pool (or, if no pool has agreed yet, a standalone opt-in worker); a test group of at least 10 miners.
- Benchmark report: throughput and cost per result vs. cloud.

**Acceptance criteria**
- A reviewer can submit the sample Monte Carlo job from the portal and download verified results.
- Recorded walkthrough video plus reproducible instructions in `demo/`.

## M2 — Paid pilot ($15,000)

**Deliverables**
- 3 external clients run paid jobs.
- Miners in the pilot are paid in QUBIC through the pool.
- Public pilot report: jobs, verified tasks, revenue, miner payouts, client feedback.

**Acceptance criteria**
- 3 paying clients, each with at least one completed job.
- Revenue and payout data with period, denominator and source.

## M3 — Automated buyback and on-chain transparency ($15,000)

**Deliverables**
- Automated USDT → QUBIC buyback, pool payouts and surplus burn.
- Job hash, result hash, payout and burn transactions anchored on Qubic.
- Public dashboard with monthly totals.

**Acceptance criteria**
- A reviewer can trace one client payment to the matching buyback, payouts and burn on Qubic.

## M4 — Public launch ($15,000)

**Deliverables**
- Open sign-up for clients, self-serve top-up.
- Documentation and 3 ready-made job templates.
- Onboarding guide for a second pool.

**Acceptance criteria**
- Public launch live; at least 10 paying clients in the first month after launch.
- Fee-share reporting to Qubic Incubation started.

## Use of funds

| Item | Amount |
|---|---|
| Founder development time (portal, API, scheduler, worker, verification, dashboard) and client discovery | $42,000 |
| Infrastructure (servers, storage, monitoring) for 6 months | $5,000 |
| Pilot client trial credits | $4,000 |
| Security review of the WASM worker | $4,000 |
| **Total** | **$55,000** |

A smart contract audit is not budgeted: the MVP does not deploy a custom Qubic smart contract. If one is added later, Qubic Incubation covers one audit per its program rules.

## Timeline (planning)

| Milestone | Target |
|---|---|
| M1 | Month 3 |
| M2 | Month 5 |
| M3 | Month 6 |
| M4 | Month 7 |

The timeline assumes one developer working 4–8 hours per day.
