# Analysis of International Tourist Arrivals in Ceará

This project was developed as part of the G707 - Data Mining Topics course at the University of Fortaleza (UNIFOR). The objective is to analyze and predict the flow of international tourists to the state of Ceará, using historical data from the period of 2015 to 2024.

## About the Project

The project analyzes data on international tourist arrivals in Ceará, provided by the [Ministry of Tourism](https://dados.turismo.gov.br/dataset/chegada-de-turistas-internacionais). The analysis includes:

- Data processing and cleaning
- Exploratory Data Analysis (EDA)
- Future arrival predictions

## Project Structure
```
.
├── data/
│   ├── chegadas_[2015-2024].csv  # Raw data files by year
│   └── dados_processados.csv     # Unified and processed dataset
├── analise.ipynb                 # Main notebook with analyses
└── README.md
```

## Dataset

The dataset contains the following information:

- **continente**: Geographical region of origin
- **pais**: Tourist's country of origin
- **ano**: Year of the record
- **mes**: Year of the record
- **chegadas**: Month of the visit

## Analysis and Prediction Methodology

## Exploratory Data Analysis (EDA)

The exploratory data analysis was conducted in several steps:

### 1. Data Preparation
- Merging of annual CSV files (2015-2024)
- Cleaning and standardizing column names
- Filtering specifically for the state of Ceará
- Removing records with zero arrivals
- Aggregating data by continent, country, year, and month

### 2. Temporal Analysis
- Visualization of the complete time series of arrivals
- Identification of seasonal patterns
- Analysis of annual trends
- Detection of high and low season periods
- Impact of special events (such as the COVID-19 pandemic)

### 3. Geographic Analysis
- Distribution of tourists by continent
- Top countries of origin
- Variations in arrivals by geographic region
- Identification of emerging markets

### 4. Statistical Analysis
- Calculation of descriptive statistics
  * Mean of arrivals
  * Median
  * Standard deviation
  * Maximum and minimum values
- Analysis of data distribution
- Identification of outliers

## Forecasting Methodology

### 1. Preparation for Forecasting
- Aggregation of data into a monthly time series
- Handling of missing values
- Normalization of data when necessary

### 2. Forecasting Techniques
- Use of Exponential Smoothing
  * Captures long-term trends
  * Identifies seasonal patterns
  * Adapts to changes in data patterns
  * Weighs recent observations more heavily

### 3. Visualization of Results
- Interactive plots with Plotly
- Comparison between actual and predicted values
- Visualization of confidence intervals
- Decomposition of the time series into components

### 4. Interpretation
- Analysis of predicted trends
- Identification of future seasonal periods
- Assessment of uncertainties in forecasts
- Recommendations based on results

## Tools Used
- Python as the main programming language
- Pandas for data manipulation
- Plotly for interactive visualizations
- Statsmodels for statistical analysis
- Scipy for scientific computing
- Matplotlib and Seaborn for static visualizations

## Limitations and Considerations
- Historical data includes the pandemic period
- Possible structural changes in tourism
- External factors not captured by the model
- Inherent uncertainties in long-term forecasting

## Installation

1. Clone the repository:
```bash
git clone [REPOSITORY_URL]
cd [DIRECTORY_NAME]
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# or
venv\\Scripts\\activate  # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```