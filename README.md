# Tech Layoffs Analysis | Python · Power BI

An analysis of global company layoffs, covering data cleaning in a Jupyter notebook and an interactive Power BI dashboard. It explores which industries, countries, company stages and time periods were hit hardest.

## Business Questions
- Which industries and countries saw the most layoffs?
- How did layoffs change over time?
- Are late-stage or well-funded companies affected more than early-stage startups?
- Which companies laid off the largest share of their workforce?
- How are layoffs distributed across size categories?

## Tools Used
| Tool | Purpose |
|------|---------|
| Python (Jupyter Notebook) | Data cleaning and exploratory analysis libraries: pandas, numpy |
| Power BI | Interactive dashboard |
| GitHub | Version control and documentation |

## Dataset
- **File:** `layoffs_cleaned.csv`, about 4,600 layoff records

| Column | Description |
|--------|-------------|
| company | Company name |
| location | City/region of the company |
| total_laid_off | Number of employees laid off |
| date | Date of the layoff event |
| percentage_laid_off | Share of the workforce laid off |
| industry | Industry of the company |
| stage | Funding stage (e.g. Seed, Series B, Post-IPO) |
| funds_raised | Total funds raised by the company |
| country | Country of the company |
| date_added | Date the record was added to the source dataset |
| layoff_category | Derived: layoff size bucket created during cleaning |

## Project Workflow
Full code is in [`Layoff_project.ipynb`](Layoff_project.ipynb).

### 1. Data Cleaning (Python)
- Removed duplicate records
- Handled missing values in `total_laid_off`, `percentage_laid_off`,`Country`, `industry` and `funds_raised`
- Drop the `Source` column for better analysis
- Standardised data types (dates, numeric fields)
- Standardised text values in columns such as industry and country
- Created a `layoff_category` column to group layoffs by size
- Exported the result as `layoffs_cleaned.csv`

### 2. Exploratory Data Analysis
- Layoffs by industry, country and funding stage
- Trend of layoffs over time
- Companies with the highest layoff counts

### 3. Dashboard (Power BI)
File: [`layoff_project.pbix`](layoff_project.pbix)
- Interactive dashboard built on the cleaned dataset

## Key Insights
- Others had the highest total layoffs, followed by Retail
- Layoffs peaked in Quarterly 1 with 0.34M employees affected
- Post-IPO companies were hit hardest, with 592.03K total layoffs
- Amazon had the single largest layoff event, with 592k employees

## Dashboard Preview
> Add a screenshot: upload an image to the repo and link it, e.g. <img width="1185" height="676" alt="Layoff_project" src="https://github.com/user-attachments/assets/232dff58-5b64-403d-9885-493646d96783" />

`

## Repository Structure
```
Layoff_Analysis/
├── Layoff_project.ipynb     # Data cleaning and EDA notebook
├── layoffs_cleaned.csv      # Cleaned dataset
├── layoff_project.pbix      # Power BI dashboard
└── README.md
```

## How to Run
1. Install the libraries: `pip install pandas numpy jupyter` 
2. Open `Layoff_project.ipynb` in Jupyter Notebook and run all cells
3. Open `layoff_project.pbix` in Power BI Desktop (it uses `layoffs_cleaned.csv`)

## Author
**Varatharaj S.**, Data Research Analyst
[LinkedIn](#) · [GitHub](https://github.com/Varatha1)
