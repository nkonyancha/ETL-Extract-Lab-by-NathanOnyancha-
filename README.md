# ETL-Extract-Lab-by-NathanOnyancha


## Description
This notebook extracts air quality data from a CSV file, filters the data for new entries since the last extraction, and updates the last extraction timestamp. It helps in incremental data processing by only working with new records.

## Tools Used
- Python
- pandas
- Jupyter Notebook

## How to Reproduce

1. **Run the notebook in Jupyter**:
   - Make sure you have the file `Air_Quality.csv` in the same directory.
   - Ensure you have `last_extraction.txt` file initialized (or the notebook will create/update it).
   - Run the cells from top to bottom.

2. **Data Source**:
   - The data is loaded from the local file `Air_Quality.csv`.
   - The file contains air quality measurements with a `Start_Date` column that records when each measurement started.

---

## Explanation of Key Steps in Code

- The notebook reads the CSV file and parses `Start_Date` as datetime.
- It reads the last extraction timestamp from `last_extraction.txt`.
- Filters rows newer than the last extraction.
- Writes the latest `Start_Date` from the filtered data back to `last_extraction.txt` for next runs.
