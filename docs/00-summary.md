# 00 — Summary

**Problem.** Small teams in research, data and fintech regularly need bursts of CPU compute (simulations, parameter sweeps, batch data processing). Cloud on-demand CPU is expensive. Spot instances are cheaper but get interrupted and still need DevOps work. Decentralized compute networks mostly focus on GPUs.

**User.** A technical team of 2–20 people that runs embarrassingly parallel CPU batch jobs a few times per month, spends roughly $500–$10,000 per month on that compute, and does not have a dedicated DevOps engineer. *(This profile is a hypothesis to be validated, see `05`.)*

**Product.** QCX: a client portal plus job scheduler. The client uploads a job packaged as WebAssembly (WASM), sets a budget and receives results. Jobs run in a WASM sandbox on CPUs of opted-in Qubic miners through an existing Qubic pool. Each task is executed by more than one miner and the results are compared, so the client gets verified output.

**Why Qubic.**
1. Qubic already coordinates a large fleet of modern AVX-512 CPUs with economic incentives and pool infrastructure that switches workloads.
2. Qubic's feeless transfers make thousands of small per-task miner payouts practical.
3. Job and result hashes are anchored on Qubic, so every buyback and burn is publicly auditable.
4. Revenue from QCX creates a buy-side sink for QUBIC funded by real customers. This is the "Outsourced Computations" direction from Qubic's own roadmap, delivered as a product.

**Ask.** USD 55,000 equivalent, paid against 4 milestones. No upfront payment.

| Milestone | Outcome | Amount |
|---|---|---|
| M1 | Client portal + one WASM workload running on a test group of one pool's miners (testnet-level payouts) | $10,000 |
| M2 | Paid pilot with 3 external clients, revenue data published | $15,000 |
| M3 | Automated USDT → QUBIC buyback, miner payouts and burn, with an on-chain public report | $15,000 |
| M4 | Public launch open to all clients and to additional pools | $15,000 |

**Return to Qubic Incubation.** 15% of QCX platform fees until 1.5× the funded amount has been returned, reported monthly. See `08`.

**Biggest risks.** Delivery capacity of a single developer, securing a pool partner after approval, and pricing compute high enough that miners prefer it to their default workload. See `10`.
