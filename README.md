# COVID-and-the-Impact-on-GDP
Documentation and project files for analysis and cleaning of UN GDP data from Kaggle

# Global GDP & Economic Indicators (1970–2021) | Data Cleaning & EDA

A data engineering and exploratory project focused on standardizing, auditing, and preparing historical macro-economic data spanning 220 countries and 50+ years. The primary focus of this project is resolving structural missingness, enforcing schema integrity, and analyzing sector-level economic trends.

---

## Key Features & Workflow

* **Schema Standardization**: Cleaned extra whitespace from column names and string fields across 10,512 rows, establishing consistent `snake_case` variable naming.
* **Missingness Diagnosis & Domain Imputation**: Isolated country-specific gaps in macro indicators—such as `Agriculture_Hunting_Forestry_Fishing_(ISIC A-B)`—and applied domain-appropriate zero-imputation for urbanized micro-states (e.g., Macao SAR, Monaco, Sint Maarten).
* **Integrity Validation**: Verified composite key uniqueness on `(Country, Year)` pairs and filtered out low-density aggregate fields to streamline analytical models.
* **Visual Explorations**: Modularized economic analysis with reusable Python functions (`plot_GDP_top15(n)`) using `matplotlib` and `seaborn` under the `fivethirtyeight` styling theme.

---

## Tech Stack & Dependencies

* **Language**: Python 3.x
* **Core Libraries**: `pandas`, `numpy`
* **Visualization**: `matplotlib`, `seaborn`

---

## Repository Structure

```text
├── data/
│   └── UN_GDP_Indicators_1970_2021.csv    # Raw dataset
├── notebooks/
│   └── GDP_Data_Cleaning_and_EDA.ipynb    # Main Jupyter Notebook
├── README.md                              # Project documentation
