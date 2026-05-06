# Tensor Mesh Membership Pipe Walkthrough

This walk-through keeps the domain vocabulary close to the data instead of burying it in prose.

| Case | Focus | Score | Lane |
| --- | --- | ---: | --- |
| baseline | quorum health | 132 | watch |
| stress | lease drift | 137 | watch |
| edge | replica lag | 204 | ship |
| recovery | membership churn | 192 | ship |
| stale | quorum health | 128 | watch |

Start with `edge` and `stale`. They create the widest contrast in this repository's fixture set, which makes them better review anchors than the middle cases.

If `stale` becomes less cautious without a clear reason, I would inspect the drag input first.
