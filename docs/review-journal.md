# Review Journal

The cases below are the review handles I would use before changing the implementation.

The local checks classify each case as `ship`, `watch`, or `hold`. That gives the project a small review vocabulary that matches its distributed systems focus without claiming live deployment or external usage.

## Cases

- `baseline`: `quorum health`, score 132, lane `watch`
- `stress`: `lease drift`, score 137, lane `watch`
- `edge`: `replica lag`, score 204, lane `ship`
- `recovery`: `membership churn`, score 192, lane `ship`
- `stale`: `quorum health`, score 128, lane `watch`

## Note

The repository should be understandable without pretending it is larger than it is.
