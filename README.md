# coupang-mountainview-mar-2026

Hands-on Temporal exercises for the Mountain View workshop — March 2026.

## Prerequisites

- Java 11+ (tested with Java 17)
- Maven 3.8+
- Temporal CLI — [install guide](https://docs.temporal.io/cli)
- Git

## Getting Started

Start a local Temporal server before running any exercise:

```bash
temporal server start-dev
```

Each exercise lives in its own numbered directory with:
- `practice/` — your working copy (look for `// TODO` comments)
- `solution/` — reference implementation

To run any exercise, `cd` into `practice/` or `solution/` and use:

```bash
# Terminal 1 — compile and start the Worker
mvn compile exec:java -Dexec.mainClass="fulfillment.FulfillmentWorker"

# Terminal 2 — run the Starter
mvn exec:java -Dexec.mainClass="fulfillment.Starter"
```

## Exercises

| # | Topic | Concept |
|---|-------|---------|
| 1 | [Converting a Workflow](./1_converting/) | Replace ad-hoc retry logic with Temporal activities |
| 2 | [Child Workflows](./2_child_workflows/) | Decompose inventory reservation into a child workflow |
| 3 | [Parallel Activities](./3_parallel_activities/) | Run warehouse checks concurrently with `Async.function()` |
| 4 | [Cost Optimization](./4_cost_optimization/) | Move fast, non-network steps to Local Activities |
