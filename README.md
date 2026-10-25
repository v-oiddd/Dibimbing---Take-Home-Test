# Dibimbing---Take-Home-Test
Job Connect Project on Data Analytics &amp; Business Intelligence Bootcamp

# Food Delivery Time Analysis
### Data Analyst & Business Intelligence Bootcamp 23 — Take-Home Test

**Author:** Adika Rizqi Irfanto

## Overview

This project analyzes food delivery data to understand delivery performance and identify factors associated with delivery time. The analysis focuses on data cleaning, feature engineering, exploratory data analysis (EDA), and correlation analysis to support data-driven business recommendations.

The project uses Python to explore delivery patterns, examine numerical and categorical features, and prepare a processed dataset for further visualization and analysis.

## Business Questions

This project aims to answer the following questions:

1. How does food delivery perform based on the available data?
2. Which factors are associated with delivery time?
3. What evaluation and improvement strategies could help optimize delivery performance?

## Dataset

**Dataset:** `Food_Delivery_Times.csv`

The dataset contains information about food delivery orders, including:

| Feature | Description |
|---|---|
| `Order_ID` | Unique order identifier |
| `Distance_km` | Delivery distance in kilometers |
| `Weather` | Weather conditions |
| `Traffic_Level` | Traffic congestion level |
| `Time_of_Day` | Time of day |
| `Vehicle_Type` | Type of delivery vehicle |
| `Preparation_Time_min` | Food preparation time in minutes |
| `Courier_Experience_yrs` | Courier experience in years |
| `Delivery_Time_min` | Delivery time in minutes |

*Note: The dataset is referenced by the notebook as `Food_Delivery_Times.csv`. The file itself is not necessarily included in this repository.*

## Tools & Technologies

- **Python** — Data analysis and processing
- **Pandas & NumPy** — Data manipulation and cleaning
- **Matplotlib & Seaborn** — Data visualization
- **Jupyter Notebook / Google Colab** — Analysis environment

## Project Workflow

### 1. Data Preparation & Cleaning
- Inspect dataset structure and data types.
- Identify missing values and examine their distribution across rows and columns.
- Handle missing numerical values using median imputation.
- Handle missing categorical values using mode imputation.

### 2. Feature Engineering
Create additional features to support delivery performance analysis.

**Distance segmentation (`Distance_Group`):**

| Distance | Segment |
|---|---|
| ≤ 5 km | Low Distance |
| > 5–10 km | Medium Distance |
| > 10–15 km | High Distance |
| > 15 km | Very High Distance |

**Delivery time segmentation (`Time_Group`):**

| Delivery Time | Segment |
|---|---|
| ≤ 15 minutes | Early Time |
| > 15–30 minutes | Mid Time |
| > 30–45 minutes | Late Time |
| > 45 minutes | Very Late Time |

### 3. Exploratory Data Analysis (EDA)
Explore delivery performance and distribution patterns through:
- Delivery counts by delivery-time segment.
- Delivery counts by distance segment.
- Distribution of numerical variables.
- Relationships between delivery characteristics and delivery time.

### 4. Correlation Analysis
Evaluate correlations between numerical features and examine encoded categorical features where appropriate. The analysis aims to identify potential relationships with `Delivery_Time_min`.

Correlation is interpreted as an association, not proof of causation.

### 5. Dataset Export
Export the processed dataset to CSV for further visualization and analysis.

**Output file:** `Food_Delivery_Times_2.0.csv`

## Repository Structure

```text
Dibimbing---Take-Home-Test/
├── README.md
├── Take_Home_Test_Adika_Rizqi_Irfanto.ipynb
└── Food_Delivery_Times_2.0.csv  # Optional processed dataset
```

The processed dataset should only be included if it is available and permitted to be shared.

## Key Deliverables

- Data cleaning and preprocessing workflow.
- Engineered distance and delivery-time segments.
- Exploratory visualizations of delivery performance.
- Correlation analysis of delivery-related features.
- Processed dataset for subsequent visualization.

## How to Run

1. Clone or download this repository.
2. Open `Take_Home_Test_Adika_Rizqi_Irfanto.ipynb` in Jupyter Notebook or Google Colab.
3. Upload `Food_Delivery_Times.csv` to the working environment.
4. Update the dataset path in the notebook if necessary.
5. Run the notebook cells sequentially.

Required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

## Further Analysis

Potential next steps include:
- Testing whether delivery time differs significantly across weather and traffic categories.
- Evaluating the relative importance of distance, preparation time, and courier experience.
- Developing a predictive model for delivery time.
- Translating analytical findings into operational recommendations.

---

*Prepared as part of the Data Analyst & Business Intelligence Bootcamp 23 take-home test.*
