# Golden Cases

The golden files are not a benchmark. They are a stable review surface for distributed systems.

The main golden fixture is `fixtures/golden/scoreboard.csv`. The matrix fixture is `fixtures/golden/lane-matrix.csv`. Together they cover `quorum health`, `lease drift`, `replica lag`, and `membership churn` with different score ranges.

The purpose is to make intentional rule changes show up in review.
