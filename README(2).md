# Cars24 Used Car Market Analysis 🚗📊

## 📌 Project Overview

This project analyzes used-car listings collected from Cars24 using
**web scraping** and **exploratory data analysis (EDA)**.

The goal is to understand used-car market patterns by analyzing factors
such as **brand, price, kilometers driven, fuel type, transmission, EMI,
and model year**.

The project is based on a scraped sample of **293 unique car listings
across 17 brands**. The analysis includes data preprocessing,
descriptive statistics, outlier detection, correlation analysis, and
visualizations.

------------------------------------------------------------------------

## 🎯 Objectives

-   Scrape used-car listings from Cars24 across multiple brands.
-   Clean and transform price, EMI, kilometer, and model-year data.
-   Extract brand information from car names.
-   Analyze price patterns by brand, fuel type, transmission, and model
    year.
-   Study the relationship between kilometers driven and car price.
-   Identify price outliers using the IQR method.
-   Generate visualizations and business insights from the dataset.
-   Save the cleaned dataset for further analysis.

------------------------------------------------------------------------

## 🛠️ Technologies Used

-   **Python**
-   **Requests** -- for collecting web pages
-   **BeautifulSoup** -- for HTML parsing and web scraping
-   **Regular Expressions (Regex)** -- for extracting information
-   **Pandas** -- for data cleaning and analysis
-   **NumPy** -- numerical analysis
-   **Matplotlib** -- data visualization
-   **Seaborn** -- visualization
-   **SciPy** -- statistical analysis
-   **Jupyter Notebook** -- development and analysis environment

------------------------------------------------------------------------

## 🌐 Web Scraping

The project collects data from Cars24 used-car listing pages.

### Scraping approach

-   **17 car brands**
-   **2 pages per brand**
-   Requests + BeautifulSoup + Regex
-   Duplicate records are avoided using a unique-record check.

### Brands Covered

Maruti, Hyundai, Tata, Honda, Mahindra, Kia, Toyota, Renault, Ford,
Volkswagen, Skoda, MG, Nissan, Jeep, Audi, BMW, and Mercedes-Benz.

### Data Collected

-   Car Name
-   Brand
-   Kilometers
-   Fuel Type
-   Transmission
-   EMI
-   Price
-   Model Year

------------------------------------------------------------------------

## 📂 Dataset

### Dataset Summary

  Description                            Value
  -------------------- -----------------------
  Total records                            293
  Final dataset          293 rows × 10 columns
  Brands                                    17
  Fuel types                                 3
  Transmission types                         2
  Model years                       2013--2026

The cleaned dataset is saved as:

``` text
cars24_clean.csv
```

------------------------------------------------------------------------

## 🧹 Data Preprocessing

The following preprocessing steps were performed:

1.  Converted price values into numeric format.
2.  Converted EMI values into numeric format.
3.  Extracted brand names from car names.
4.  Converted model year into numeric format.
5.  Cleaned kilometer values and converted them into numeric values.
6.  Checked missing values.
7.  Checked duplicate records.
8.  Created kilometer ranges:
    -   0--20K km
    -   20K--40K km
    -   40K--60K km
    -   60K--80K km
    -   80K--100K km
9.  Detected price outliers using the IQR method.

------------------------------------------------------------------------

## 📊 Exploratory Data Analysis

The project analyzes:

-   Number of cars by brand
-   Fuel-type distribution
-   Transmission distribution
-   Model-year distribution
-   Average price by brand
-   Average price by fuel type
-   Average price by transmission
-   Average price by model year
-   Average price by kilometer range
-   Top 10 most expensive cars
-   Top 10 cheapest cars
-   Brand vs fuel type
-   Brand vs transmission
-   Fuel type vs transmission
-   Brand-wise average kilometers
-   Kilometers vs price correlation

------------------------------------------------------------------------

## 📈 Key Findings

### Fuel Type

Petrol vehicles dominate the scraped dataset:

-   Petrol: **219**
-   Diesel: **60**
-   CNG: **14**

### Transmission

The dataset contains:

-   Manual: **237**
-   Automatic: **56**

Automatic cars have a higher average price in this scraped sample, at
approximately **₹12.26 lakh**, compared with approximately **₹5.69
lakh** for manual cars.

### Price

-   Minimum price: **₹1.58 lakh**
-   Average price: **₹6.95 lakh**
-   Median price: **₹5.68 lakh**
-   Maximum price: **₹41.13 lakh**

### Kilometers vs Price

The correlation between kilometers driven and price is approximately
**-0.19**, indicating a weak negative relationship. This means mileage
alone does not explain used-car prices.

### Brand Analysis

Premium brands such as **Mercedes-Benz, Audi, and BMW** show higher
average prices in this scraped sample.

### Kilometer Range

Cars in the **20K--40K km** range show the highest average price among
the defined kilometer ranges, while average prices generally decrease at
higher mileage ranges.

------------------------------------------------------------------------

## 🔎 Outlier Analysis

The **Interquartile Range (IQR)** method was used to identify price
outliers.

-   Q1: **₹3.85 lakh**
-   Q3: **₹8.13 lakh**
-   IQR: **₹4.28 lakh**
-   Upper limit: **₹14.55 lakh**
-   Price outliers identified: **18**

These outliers represent high-value vehicles and can affect
average-price comparisons.

------------------------------------------------------------------------

## ✅ Data Quality

After preprocessing:

-   Dataset shape: **293 × 10**
-   Duplicate rows: **0**
-   Missing values: **1 in EMI_Amount**
-   Other tracked columns: **0 missing values**
-   Model Year: `int64`
-   Price_Lakh: `float64`

------------------------------------------------------------------------

## 📁 Project Structure

``` text
Cars24-Used-Car-Market-Analysis/
│
├── Web Scrapping Project (1)(1).ipynb
├── cars24_clean.csv
├── Cars24_Used_Car_Market_Analysis.pdf
└── README.md
```

> The CSV file is generated by the notebook after running the scraping
> and preprocessing steps.

------------------------------------------------------------------------

## ▶️ How to Run the Project

### 1. Clone the repository

``` bash
git clone <your-github-repository-url>
cd Cars24-Used-Car-Market-Analysis
```

### 2. Install the required libraries

``` bash
pip install requests beautifulsoup4 pandas numpy matplotlib seaborn scipy jupyter
```

### 3. Open Jupyter Notebook

``` bash
jupyter notebook
```

### 4. Open the notebook

``` text
Web Scrapping Project (1)(1).ipynb
```

### 5. Run the cells

The notebook will:

1.  Scrape Cars24 listing pages.
2.  Create the raw dataset.
3.  Clean and transform the data.
4.  Perform statistical analysis.
5.  Detect outliers.
6.  Generate visualizations.
7.  Save the cleaned dataset as `cars24_clean.csv`.

------------------------------------------------------------------------

## 📌 Project Workflow

``` text
Cars24 Listing Pages
        ↓
Web Scraping
        ↓
Data Collection
        ↓
Data Cleaning & Preprocessing
        ↓
Data Quality Checks
        ↓
Exploratory Data Analysis
        ↓
Statistical Analysis
        ↓
Outlier Detection
        ↓
Visualization
        ↓
Business Insights
```

------------------------------------------------------------------------

## 💡 Conclusion

This project demonstrates how **web scraping and exploratory data
analysis** can be used to extract meaningful insights from used-car
listings.

The analysis shows that used-car prices vary across factors such as
**brand, transmission, fuel type, model year, and mileage**, while no
single factor completely explains resale price.

------------------------------------------------------------------------

## 🚀 Future Enhancements

-   Build a machine-learning model to predict used-car prices.
-   Add more Cars24 cities and listings.
-   Collect data periodically to analyze market changes over time.
-   Create an interactive dashboard using **Power BI or Tableau**.
-   Add more statistical tests and advanced feature engineering.
-   Compare prices across cities and vehicle segments.

------------------------------------------------------------------------

## ⚠️ Note

This analysis is based on a **scraped sample of Cars24 listings** and
should not be treated as a complete representation of the entire
used-car market. Results may change depending on the listings available
at the time of data collection.
