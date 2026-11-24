# 02 — Problem and ICP

## Ideal customer profile (hypothesis)

A small technical team (2–20 people) that:

- runs **embarrassingly parallel CPU batch jobs**: Monte Carlo simulations, parameter sweeps, backtests, bioinformatics pipelines, batch data transformation;
- needs these jobs **a few times per month**, not 24/7;
- spends roughly **$500–$10,000 per month** on this compute;
- has **no dedicated DevOps engineer**;
- can tolerate results arriving in hours, not seconds.

Concrete segments to interview first:

1. Quant and trading teams running backtests and risk simulations.
2. Academic and independent research labs (computational biology, physics, economics).
3. Data and ML teams doing CPU-side preprocessing and hyperparameter sweeps.

## The pain

- **On-demand cloud CPU is expensive** for bursty work.
- **Spot instances are cheaper but unreliable.** Jobs get interrupted, and handling retries needs engineering time.
- **Setup overhead.** For a small team, configuring a batch cluster for an occasional job costs more time than the job itself.
- **University clusters** have queues and allocation limits.

## How they solve it today

| Option | Why it is insufficient |
|---|---|
| AWS / GCP on-demand or spot | Cost, or interruptions plus DevOps work |
| Dedicated servers (e.g. Hetzner) | Fixed monthly cost for bursty needs |
| Own hardware / university cluster | Capacity limits, queues |
| BOINC-style volunteer computing | Only for selected public research projects |
| Decentralized compute (Akash, Golem, iExec) | Mostly GPU or container hosting; little focus on simple paid CPU batch jobs |

## What QCX offers

Upload a WASM job, set a budget, get verified results. No cluster setup, no interruptions to manage, and a price below on-demand cloud CPU.
