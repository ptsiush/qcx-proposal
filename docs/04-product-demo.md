# 04 — Product and demo

## Main user flow (client)

1. Sign up on the QCX portal and top up a balance in USDT.
2. Upload a job: a WASM module plus an input manifest (a list of input chunks).
3. Set a budget and a deadline. See a price estimate.
4. QCX splits the job into tasks and sends them to miners.
5. Watch progress live. Download the verified results.
6. Get an invoice plus a public link to the job's on-chain receipt.

## Main flow (miner)

1. Opt in to QCX jobs in the pool settings and choose how much CPU to allocate.
2. The pool's miner client downloads tasks and runs them in a WASM sandbox.
3. The miner is paid in QUBIC per verified task through the pool.

## MVP scope (M1–M2)

**In scope**
- One job type: deterministic WASM jobs with chunked input (e.g. Monte Carlo simulation, parameter sweep).
- One pool integration.
- Redundant execution: each task runs on 2 miners; on mismatch, a 3rd miner decides.
- Client portal (TypeScript): upload, budget, progress, results, invoices.
- Manual USDT → QUBIC conversion during the pilot, with a public log.

**Out of scope for MVP**
- GPU jobs, long-running services, jobs needing network access.
- Confidential data (inputs are visible to miners; clients are told so).
- Automated buyback and on-chain reporting (M3).

## Architecture

```
Client portal (TS) ──> QCX API / Scheduler ──> Pool connector ──> Miners (WASM worker)
                              │                                        │
                              │<──────────── results + hashes ─────────┘
                              │
                     Verification (2-of-3 hash match)
                              │
                     Treasury: USDT → QUBIC buyback → pool payouts, surplus burn
                              │
                     Qubic: job hash, result hash, payout and burn tx (public report)
```

## Why WASM

- **Sandbox.** WASM modules cannot touch the miner's file system or network unless explicitly allowed. This protects miners.
- **Determinism.** The same module and input give the same output on any CPU, which makes result verification by hash comparison possible.
- **Portability.** One package runs on Windows and Linux miners alike.

## Key technical risks

| Risk | Mitigation |
|---|---|
| Non-deterministic jobs break verification | Restrict to deterministic WASM; validate with a test run before accepting a job |
| WASM is slower than native code | Benchmark in M1; price per useful result, not per core-hour, if needed |
| Pool connector complexity | Start with a single pool partner and reuse its existing workload-switching; fallback: standalone opt-in worker |
| Miners cheat by returning fake results | Redundant execution plus reputation; miners with mismatches are excluded |

## Demo

Planned for M1: a reproducible walkthrough (video + script) of a Monte Carlo job running on a test group of miners, with results verified and an on-chain receipt.
