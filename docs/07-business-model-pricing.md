# 07 — Business model and pricing

## Pricing

- Clients pay **per verified core-hour** (or per result for standard templates), in USDT.
- Target client price: **at least 30% below on-demand cloud CPU** for comparable throughput. The exact number will be set from the M1 benchmark.
- Free trial credits for pilot clients.

## Where each client dollar goes (planning model)

| Share | Destination |
|---|---|
| 70% | Buy QUBIC on the market → paid to miners through the pool |
| 15% | QCX platform fee (operations, development, return to Qubic Incubation) |
| 10% | Redundant execution: buys QUBIC paid to the second (verifying) miner per task |
| 5% | Buyback surplus burned |

The split is a starting hypothesis. The two hard constraints are:

1. Miners must earn more per CPU-hour from QCX than from their default workload, otherwise they will not opt in.
2. The client price must stay clearly below cloud alternatives.

The M1 benchmark and M2 pilot will show whether both constraints can hold at the same time. If they cannot, this is a kill criterion (see `05`).

## Why the pricing metric fits delivered value

Clients care about completed, correct results. Charging per verified core-hour or per result means they never pay for failed or unverified tasks.

## Unit economics example (illustrative)

A client buys $1,000 of compute:
- $700 buys QUBIC that is paid to miners;
- $100 buys QUBIC paid to verifying miners;
- $50 of QUBIC is bought and burned;
- $150 is QCX revenue, of which 15% ($22.50) goes to Qubic Incubation as the return (see `08`).

So every $1,000 of client spend creates about $850 of QUBIC buy pressure.
