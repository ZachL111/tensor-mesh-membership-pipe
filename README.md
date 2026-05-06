# tensor-mesh-membership-pipe

`tensor-mesh-membership-pipe` explores distributed systems with a small SQL codebase and local fixtures. The technical goal is to implement an SQL distributed systems project for membership constraint solving, using bounded scenario files and conflict explanations.

## Reason For The Project

I want this repository to be useful as a quick reading exercise: fixtures first, implementation second, verifier last.

## Tensor Mesh Membership Pipe Review Notes

The first comparison I would make is `replica lag` against `quorum health` because it shows where the rule is most opinionated.

## What It Does

- `fixtures/domain_review.csv` adds cases for quorum health and lease drift.
- `metadata/domain-review.json` records the same cases in structured form.
- `config/review-profile.json` captures the read order and the two review questions.
- `examples/tensor-mesh-membership-walkthrough.md` walks through the case spread.
- The SQL code includes a review path for `replica lag` and `quorum health`.
- `docs/field-notes.md` explains the strongest and weakest cases.

## How It Is Put Together

The core code exposes a scoring path and the added review layer uses `signal`, `slack`, `drag`, and `confidence`. The domain terms are `quorum health`, `lease drift`, `replica lag`, and `membership churn`.

The SQL checks add a separate view over the domain review fixture.

## Run It

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File scripts/verify.ps1
```

## Check It

The check exercises the source code and the review fixture. `edge` is the high score at 204; `stale` is the low score at 128.

## Boundaries

No external service is required. A deeper version would add more negative cases and a clearer boundary around invalid input.
