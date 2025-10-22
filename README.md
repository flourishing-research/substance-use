# Religious/Spiritual Exposure and Substance Use Outcomes

This repository contains the data processing and analysis workflow for a meta-analysis examining the relationship between **religious/spiritual exposure** and **substance use outcomes**. The project involves extracting, cleaning, standardizing, and analyzing data collected from multiple studies.

## 📂 Repository Structure

```
.
├── fetch_data.Rmd      # Fetches and reformats data from Google Sheets (original source)
├── etl.Rmd             # Standardizes effect sizes into logRR and prepares analytic dataset
├── test.Rmd            # Runs meta-analysis tests on the standardized dataset
├── data.csv            # Snapshot of the original Google Sheet (for reproducibility)
├── final.Rdata         # Saved R session data containing final datasets and objects
└── README.md
```

## 🧾 Overview of Workflow

### 1. **Data Fetching and Labeling** – `fetch_data.Rmd`
- Originally, data were stored in a personal Google Sheet. Since deprecated.
- This script fetched the data and applied improved variable labels.
- We’ve saved a copy as `raw_data.csv` and `raw_data.RData` to ensure reproducibility.

### 2. **ETL: Extract, Transform, Load** – `etl.Rmd`
- Standardized effect sizes from individual studies into **log relative risk (logRR)** with point estimates and variances.
- Combined standardized results into a single data frame for downstream analysis.

### 3. **Meta-Analysis Testing** – `test_final.Rmd`
- Runs various meta-analysis models on the standardized dataset.
- These analyses reproduce the reported results used in the project.

## 💾 Reproducibility

To reproduce the results:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/religion-substance-meta.git
   cd religion-substance-meta
   ```

2. **Open R or RStudio**.

3. **Load the saved session data**:
   ```r
   load("data.Rdata")
   ```

4. **Run the analysis notebook**:
   Open and run `test.Rmd` line by line


## 📝 Notes

- `data.Rdata` includes all data and intermediate objects as they were at the time of final submission.
- Some objects in `data.Rdata` may include one-off commands or helper functions.
- The CSV file ensures data availability even if the original Google Sheet is removed.

## 📚 Citation / Attribution

If you use this repository or any part of the analysis, please cite the corresponding paper or acknowledge this project appropriately.
