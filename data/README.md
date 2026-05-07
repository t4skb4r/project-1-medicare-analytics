# Data Source

**Dataset:** CMS Medicare Physician & Other Practitioners PUF
**Year:** 2023
**Source:** https://data.cms.gov
**License:** Public domain — U.S. government data

## Filtering Applied Before Analysis

The full national dataset contains approximately 9–10 million rows.
This project filters to 10 states: TX, CA, NY, FL, IL, OH, PA, GA, WA, CO.
Filtered dataset: approximately 4.6 million rows (2023 single-year file).

CREATE TABLE medicare_puf AS
SELECT * FROM medicare_puf_raw
WHERE Rndrng_Prvdr_State_Abrvtn IN ('TX','CA','NY','FL','IL','OH','PA','GA','WA','CO');

## Data Quality Notes

[Add findings from DQ-1 through DQ-4 here as you run the validation queries.]

## Analytical Limitations

[Add domain constraint notes here — see Part 2C Healthcare Domain Constraints.]

## To Reproduce

1. Download the PUF CSV from data.cms.gov
2. Import into SQLite as medicare_puf_raw using DBeaver
3. Run the filter query above to create medicare_puf
4. Drop medicare_puf_raw

Raw CSV and .db files are excluded from this repo due to file size.
