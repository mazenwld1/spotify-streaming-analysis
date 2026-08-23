# Data Quality Assessment

## Initial checks

- Rows: 500
- Columns: 14
- Missing values: 0
- Duplicate rows: 0
- Duplicate artist names: 0
- Negative numeric values: 0
- Debut year range: 1939–2023
- Countries: 43
- Genres: 23
- Languages: 11

## Reconciliation checks

`Solo Streams + Collaborative Streams = Total Streams` reconciles for all rows within floating-point precision.

`Lead Streams + Feature Streams = Total Streams` does **not** reconcile for many rows. This is treated as a source-data characteristic rather than silently changing the values.

Example: Flo Rida has a 89.2 million-stream difference between Total Streams and Lead + Feature Streams.

## Values requiring review

The genre value `Sertanjeo` looks potentially misspelled and should be verified against the dataset source before changing it.

## Cleaning policy

The project standardizes headers, trims text, enforces data types, removes blank artist names, and creates analysis-ready derived fields. Original source values are preserved unless a correction can be justified from the source.
