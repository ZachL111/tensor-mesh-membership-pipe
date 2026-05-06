# Field Notes

`tensor-mesh-membership-pipe` is easiest to review by starting with the fixture, not the prose.

The domain cases cover `quorum health`, `lease drift`, `replica lag`, and `membership churn`. They sit beside the smaller starter fixture so the project has both a compact scoring check and a domain-flavored review check.

`edge` is the strongest case at 204 on `replica lag`. `stale` is the cautious anchor at 128 on `quorum health`.

The point is not to make the repository bigger. The point is to make the important judgment testable.
