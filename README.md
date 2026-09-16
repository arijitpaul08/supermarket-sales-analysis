# supermarket-sales-analysis
An internship data analytics project analyzing supermarket sales using Python, Pandas, Plotly and Streamlit.


## Project Description
This internship project analyzes **500 supermarket sales transactions** from the supplied supermarket-sales PDF. The workflow extracts the PDF into CSV, validates and cleans the data, calculates `Sales = Quantity × Unit Price`, performs exploratory/business analysis with Pandas, creates interactive Plotly visualizations, and provides a Streamlit dashboard.

## Dataset
The source dataset is included in this repository:
- [Supermarket Sales Dataset PDF](data/raw/SUPER%20MARKET%20DATA.pdf)
- [Project Manual PDF](data/raw/Supermarket%20Sales%20Analysis%20DA%20project.pdf)
- [Clean CSV Dataset](data/processed/supermarket_sales_clean.csv)

> The dataset link above is a repository-relative link. After uploading this project to GitHub, it will open directly from the repository.

## Technologies Used
- Python
- Pandas
- NumPy
- PyMuPDF
- Plotly
- Streamlit
- Jupyter Notebook
- Pytest

## Project Files
- `ArijitPaul_SupermarketSalesAnalysis.ipynb` — complete Jupyter Notebook analysis
- `app.py` — interactive Streamlit dashboard
- `run_pipeline.py` — PDF extraction and cleaning pipeline
- `src/extract.py` — PDF-to-table extraction
- `src/clean.py` — validation and cleaning
- `src/analysis.py` — reusable analysis functions
- `src/viz.py` — Plotly visualization helpers
- `requirements.txt` — Python dependencies
- `tests/test_project.py` — automated tests
- `data/raw/` — original PDFs
- `data/processed/` — extracted and cleaned datasets
- `outputs/` — validation and manual-verification outputs

## Setup

### 1. Clone the repository
```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd supermarket_sales_analysis
```

### 2. Create a virtual environment
```bash
python -m venv .venv
```

Windows:
```bash
.venv\\Scripts\\activate
```

macOS/Linux:
```bash
source .venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

## Run the Pipeline
```bash
python run_pipeline.py
```

This extracts the supplied PDF again and recreates the processed CSV. The original PDFs remain unchanged.

## Run the Jupyter Notebook
```bash
jupyter notebook ArijitPaul_SupermarketSalesAnalysis.ipynb
```

Run the cells from top to bottom.

## Run the Streamlit Dashboard
```bash
streamlit run app.py
```

The dashboard supports filters for branch, city, category, product, customer type, gender, payment method and date range.

## Testing
```bash
pytest -q
```

The project includes tests for extraction, validation, Sales arithmetic, benchmark verification and key analytical results.

## Key Results
Calculated directly from the cleaned dataset:

| KPI | Result |
|---|---:|
| Total Sales | ₹244,411.08 |
| Transactions | 500 |
| Units Sold | 2,768 |
| Average Transaction | ₹488.82 |
| Average Rating | 3.99 / 5 |
| Top Product | Cheese — ₹27,906.30 |
| Top Category | Beverages — ₹56,108.24 |
| Top Branch | C / Mumbai — ₹72,469.45 |
| Most-used Payment | UPI — 127 transactions |

## Data Validation
The extracted dataset contains:
- 500 records
- 500 unique invoice IDs
- 0 missing values
- 0 duplicate rows
- 0 duplicate invoice IDs
- 0 invalid ratings
- 0 invalid quantities/unit prices
- Sales arithmetic consistent with `Quantity × Unit Price`

## Manual Verification
The project manual's benchmark results are used only as verification targets. The analytical values are calculated independently from the dataset. All listed manual checks matched within ₹0.01 / 0.01 tolerance.

## Limitations
The source dataset does not contain profit, cost, inventory, discount or customer-ID information. July contains relatively few transactions, so it should not be interpreted as a complete-month seasonal comparison.

## Author
**Arijit Paul**  
BCA — Data Analytics / Machine Learning Project
