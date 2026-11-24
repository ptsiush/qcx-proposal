# 05 — Validation and traction

## Honest status

QCX is at the pre-build stage. There are no users, interviews or revenue yet, and no pool has been contacted. This document lists what will be checked, in what order, and what would make us stop.

## Validation plan

**Weeks 1–3 (in parallel with review and the start of M1)**
1. Interview 10 potential clients from the three ICP segments in `02`. Questions: what jobs they run, how often, what they pay today, what would make them switch.
2. Ask in the Qubic Discord mining channels whether miners would allocate part of their CPU to paid jobs, and at what price.
3. Run a sample WASM Monte Carlo job on a modern AVX-512 CPU and record throughput and cost per result.

**After approval**
4. Approach pool operators with the approved proposal and agree on a pilot.

## Success criteria to continue past M1

- At least 3 clients agree to a paid pilot (letter of intent).
- One pool agrees to the pilot, or enough miners opt in to the standalone worker (at least 10).
- Measured cost per result allows a client price at least 30% below on-demand cloud while paying miners more than their default workload.

## Kill criteria

- Fewer than 2 of 10 interviewed clients would try QCX at the target price.
- Miners require a price that makes QCX more expensive than cloud spot instances.

If a kill criterion is hit, the project stops before M2 and Qubic pays nothing beyond closed milestones.

## Metrics we will report

All metrics will state the period, the denominator and the source, for example: "verified tasks per week, from the QCX scheduler log, weeks 1–4". Interview notes and benchmark results will be added to `data/` in this repository as they come in.
