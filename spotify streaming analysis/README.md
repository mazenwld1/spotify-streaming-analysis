# Spotify Streaming Performance Analysis

An Excel-based data analysis project exploring artist streaming performance using **Power Query, PivotTables, PivotCharts, Excel Slicers, and an interactive dashboard**.

## Project Objective

Analyze Spotify artist streaming performance and answer practical business questions about:

- Top-performing artists
- Genre performance
- Geographic concentration
- Artist type
- Sex and language distribution
- Collaboration vs. solo performance
- Debut era and streaming performance

## Dataset

**Source file:** `Spotify Streaming Performance Dataset.csv`

The dataset contains:

- **500 artists**
- **43 countries**
- **23 genres**
- **11 languages**

## Business Questions

1. Who are the top 10 artists by total streams?
2. Which genres generate the most streams?
3. Which countries produce the most streaming volume?
4. Do solo artists or groups generate more streams?
5. How does streaming performance differ by sex?
6. Which languages have the highest streaming volume?
7. Which artists have the strongest collaboration share?
8. Which artists have the strongest solo share?
9. Does debut era appear related to streaming performance?
10. Which genres have the strongest collaboration contribution?

## Data Cleaning — Power Query

The raw CSV was imported into Excel Power Query and transformed before analysis.

Main cleaning steps:

1. Imported the CSV using **Data → Get Data → From Text/CSV**
2. Standardized column headers
3. Removed unwanted leading spaces from field names
4. Trimmed text fields
5. Corrected/enforced data types
6. Checked missing values
7. Checked duplicate rows and duplicate artist names
8. Validated negative values and stream relationships
9. Created derived analytical fields

### Derived Fields

- `Career Era`
- `Stream Performance Tier`
- `Collaboration Preference`

The cleaned query output is loaded into the `PQ_Cleaned` worksheet.

## Analysis

PivotTables were created for:

- Top Artists
- Genres
- Countries
- Artist Type
- Collaboration
- Career Era

These PivotTables feed the dashboard visuals.

## Dashboard

The Excel dashboard contains:

- KPI cards
- Top 10 Artists chart
- Genre streaming chart
- Country streaming chart
- Solo vs. Collaboration chart
- Interactive slicers for:
  - Primary Genre
  - Country of Origin
  - Artist Type
  - Primary Language
  - Career Era
  - Sex

The slicers are connected to the PivotTables so the dashboard can be filtered interactively.

## Key Findings

- **Drake** is the highest-streamed artist in the dataset.
- **Hip-Hop** has the highest total streaming volume.
- The **United States** has the highest streaming volume and contains 265 of the 500 artists.
- **English** is the dominant language, with 340 artists.
- **Solo artists** generate more total streams than groups in this dataset.
- The collaboration and solo stream components reconcile to total streams, making them suitable for collaboration analysis.

## Data Quality & Limitations

The project documentation reports no missing values, duplicate rows, or duplicate artist names.

One important source-data limitation was identified:

> Lead Streams + Feature Streams do not consistently reconcile to Total Streams.

Therefore, the project uses the solo/collaborative stream relationship for the collaboration analysis rather than assuming lead + feature streams equal total streams.

## Excel Workbook Structure

| Sheet | Purpose |
|---|---|
| `Raw_Data` | Original/raw dataset |
| `PQ_Cleaned` | Power Query cleaned dataset |
| `Clean_Data` | Cleaned-data reference |
| `PT_Top_Artists` | Top artist PivotTable |
| `PT_Genres` | Genre PivotTable |
| `PT_Countries` | Country PivotTable |
| `PT_Artist_Type` | Artist type PivotTable |
| `PT_Collaboration` | Collaboration PivotTable |
| `PT_Career_Era` | Career era PivotTable |
| `Dashboard` | Interactive Excel dashboard |
| `Questions` | Business questions and answers |
| `Analysis` | KPI analysis and interpretation |
| `Documentation` | Project methodology |
| `Power_Query_Guide` | Power Query cleaning steps |

## Tools Used

- Microsoft Excel
- Power Query
- PivotTables
- PivotCharts
- Excel Slicers
- GitHub

## How to Use

1. Open the Excel workbook in **Microsoft Excel desktop**.
2. Open the `Dashboard` sheet.
3. Use the slicers to filter the analysis.
4. Explore the charts and KPI cards.
5. Review `Questions`, `Analysis`, and `Documentation` for the methodology and findings.

## Project Structure

Spotify-Streaming-Analysis/
│
├── README.md
├── Spotify_Streaming_Analysis_Dashboard_FINAL_FIXED.xlsx
└── data/
    └── Spotify Streaming Performance Dataset.csv
```

## Author

Mazen Waleed — Excel Data Analysis Portfolio Project
