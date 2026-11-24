# 06 — Market, go-to-market, competition

## Bottom-up market logic

We do not rely on a top-down cloud market figure. The first-year target is built from clients:

- 30 paying clients × average $1,500 per month of compute = **$45,000 per month** of gross compute revenue.
- This is a planning hypothesis to be replaced with pilot data after M2.

## Buyer and user

- **Buyer:** team lead or founder who owns the compute budget.
- **User:** researcher or engineer who submits jobs.

## Winning the first 10–100 clients

| Channel | Owner | Why it should work |
|---|---|---|
| Direct outreach to research labs and small quant teams (LinkedIn, email) | Pavel | High-intent users with recurring batch jobs |
| Free trial credits (first N core-hours) for pilot clients | Pavel | Lowers the cost of trying |
| Technical content: "Run your Monte Carlo on 1,000 CPUs for $X" with reproducible examples | Pavel | Attracts engineers searching for cheap batch compute |
| Qubic community and ecosystem partners | Pavel | Early miners and ecosystem projects as first users |

## Competition

| Alternative | Strength | QCX advantage |
|---|---|---|
| AWS Batch / GCP spot | Reliability, ecosystem | Lower price, no interruptions to manage, no DevOps |
| Akash | Container hosting market | Focus on simple CPU batch jobs with verified results |
| Golem, iExec | Early decentralized compute | Large existing CPU supply via Qubic pools; feeless micro-payouts |
| BOINC | Huge volunteer base | Paid, commercial, available to any client |

## Defensibility

- Supply side: integration with Qubic pools and a miner base that already exists.
- Verified-results track record and published on-chain receipts.
- Library of ready-made WASM job templates for common workloads.
