# Methodology

## Workflow

Raw CSV → Power Query → Cleaned/typed data → Derived analytical fields → Power BI data model → Measures → Visuals → Dashboard.

## Power Query transformations

1. Import the CSV.
2. Promote the first row to headers.
3. Rename inconsistent column headers.
4. Trim text fields.
5. Apply explicit data types.
6. Remove blank artist records.
7. Create Career Era.
8. Create Stream Performance Tier.
9. Create Collaboration Preference.

The transformation is designed to be repeatable on refresh rather than manually editing individual rows.
