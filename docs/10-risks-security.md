# 10 — Risks and security

## Security assumptions

- Miner machines are untrusted by clients, and client code is untrusted by miners.
- WASM sandbox (wasmtime) with no file system or network access by default; strict CPU, memory and time limits per task.
- Client inputs are visible to miners. QCX does not accept confidential data in the MVP, and clients are told this before upload.
- Results are verified by redundant execution: 2 miners per task, a 3rd on mismatch. Miners with repeated mismatches are excluded.

## Dependencies

| Dependency | Risk | Mitigation |
|---|---|---|
| Pool partner | No pool agrees after approval, or a partner withdraws | Pool-agnostic connector; fallback standalone opt-in worker for miners; onboard a second pool in M4 |
| QUBIC liquidity | Buybacks move the price or are hard to execute | Spread buybacks over time; use several venues; publish execution log |
| Miner supply | Miners prefer their default workload | Price must beat the default reward per CPU-hour (kill criterion in `05`) |
| Single developer | Delivery slower than planned | Narrow MVP (one job type, one pool); payments only on closed milestones, so Qubic carries no schedule risk; external security review of the worker |

## Operational risks

- **Determinism failures** in client jobs: test-run every job on two machines before accepting it.
- **Abuse** (e.g. someone using QCX for cryptomining or illegal workloads): job review for new clients, KYB for large clients, the sandbox blocks network access.
- **Regulation:** clients pay in USDT and miners in QUBIC. The legal structure and jurisdiction for accepting client payments will be chosen and set up before M2, when the first paid pilot starts.

## Audit plan

- External security review of the WASM worker and the sandbox configuration before M2 (budgeted in `09`).
- If a custom Qubic smart contract is added later (e.g. on-chain escrow), it will be audited before mainnet, using the one audit covered by Qubic Incubation.
