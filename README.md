# 🏢 AmbitionBox Web Scraping and Exploratory Data Analysis

## 📌 Project Overview

This project focuses on extracting company-related information from [AmbitionBox](https://www.ambitionbox.com/) using Python web scraping techniques and performing Exploratory Data Analysis (EDA) to understand company ratings, employee reviews, salary information, job openings, industries, and locations.

The scraped information is cleaned, transformed, and analyzed using Python libraries. Different statistical techniques and visualizations are used to explore patterns in company data and derive useful observations.

## 🎯 Project Objectives

- Scrape company information from AmbitionBox.
- Extract company names, ratings, reviews, salary information, job openings, industry details, and highly rated factors.
- Clean and prepare the scraped data for analysis.
- Handle missing values and duplicate records.
- Convert salary, review, and job-count values into numerical formats.
- Analyze company ratings, salary trends, industries, and locations.
- Visualize relationships between salary, ratings, reviews, and other variables.
- Identify patterns that can support company and employment-related research.

## 🛠️ Tools and Technologies

- **Python** — Programming language
- **Requests** — Sending HTTP requests to retrieve web pages
- **BeautifulSoup** — Parsing HTML and extracting webpage information
- **Regular Expressions (Regex)** — Extracting and cleaning text patterns
- **Pandas** — Data manipulation and analysis
- **NumPy** — Numerical operations
- **Matplotlib** — Data visualization
- **Seaborn** — Statistical visualization
- **Jupyter Notebook** — Development and analysis environment

## 📂 Project Structure

```text
AmbitionBox-Web-Scraping/
│
├── README.md
├── Web Scraping Project.ipynb
├── Visualization_for_ambition_box.ipynb
└── Ambition_box_data.csv
```

*Note: The CSV file should be included if you choose to share the processed dataset. The filenames in the repository may differ slightly from this example.*

## 🔍 Project Workflow

### 1. Web Scraping

- Sent HTTP requests to the AmbitionBox company-listing pages using Python Requests.
- Parsed HTML content using BeautifulSoup.
- Extracted company information using HTML tags and CSS classes.
- Used loops to process multiple company-listing pages.
- Collected company names, ratings, review counts, salary information, job openings, industry details, and highly rated factors.
- Stored extracted information in Python lists and combined it into a Pandas DataFrame.

### 2. Data Extraction and Storage

The extracted data was organized into a structured dataset with the following fields:

| Column | Description |
|---|---|
| Company | Company name |
| Rating | Company rating |
| Review | Number of employee reviews |
| Salary | Salary information |
| Job | Job-opening count |
| Industry | Industry classification |
| Highly_rated_for | Highly rated workplace factors |
| Location | Company location |

The dataset was exported to CSV format for further processing and analysis.

### 3. Data Cleaning and Preparation

- Inspected dataset structure, column names, and data types.
- Checked missing values and handled them using median, mode, or an `Unknown` label as appropriate to the field.
- Checked for duplicate records and removed duplicates.
- Extracted industry and location information from combined text using regular expressions.
- Converted salary, review, and job-count values into numerical formats.
- Reordered columns for easier analysis.
- Reviewed descriptive statistics and dataset information.

**Dataset size:** The visualization notebook records 1,000 rows and 8 columns initially, and 996 rows and 8 columns after duplicate removal.

### 4. Exploratory Data Analysis (EDA)

The cleaned dataset was analyzed using statistical summaries and visualizations.

#### Univariate Analysis
- Company rating distribution using histograms.
- Review-count distribution using KDE plots.
- Top industries using count plots and pie charts.
- Salary distribution using boxplots.
- Job-opening distribution using violin plots.
- Highly rated workplace factors.
- Company locations by number of listings.

#### Bivariate Analysis
- Average salary by industry.
- Average salary by industry and location.
- Industry versus highly rated workplace factors.
- Company rating versus salary.
- Industry versus company rating.
- Company locations versus ratings.
- Industry and location comparisons using grouped summaries and heatmaps.

#### Multivariate Analysis
- Correlation heatmap for numerical variables.
- Review count, salary, and rating comparison using a scatter plot.
- Salary patterns across industry and location combinations.
- Pairplot to examine relationships among numerical features.

## 📊 Key Observations

The notebook observations indicate the following patterns:

- IT Services & Consulting is prominently represented in the dataset.
- Company salary levels vary across industries.
- Company listings are concentrated in major employment locations.
- Review count and salary show a relatively stronger positive relationship than rating and salary.
- Company ratings are generally concentrated within a moderate-to-positive range.
- Highly rated workplace factors vary across industries.
- Salary patterns differ across industry and location combinations.

These are exploratory observations from the notebook. They should not be interpreted as proof of causation or as representative of every company on the platform.

## 📈 Business Value

This project demonstrates how web scraping and data analysis can help organize publicly available company information into a structured dataset.

Potential applications include:

- Comparing company ratings and review activity.
- Exploring salary differences across industries.
- Understanding the geographic distribution of company listings.
- Examining workplace factors highlighted in company information.
- Preparing datasets for further reporting and visualization.

## ▶️ How to Run the Project

### Prerequisites

Install Python and Jupyter Notebook or JupyterLab.

Install the required libraries:

```bash
pip install pandas numpy requests beautifulsoup4 matplotlib seaborn
```

### Run the Scraping Notebook

1. Clone or download this repository.
2. Open `Web Scraping Project.ipynb` in Jupyter Notebook.
3. Run the cells in sequence to retrieve, extract, clean, and export the company data.
4. Review the generated `Ambition_box_data.csv` file.

### Run the Visualization Notebook

1. Keep `Visualization_for_ambition_box.ipynb` and `Ambition_box_data.csv` in the same project directory.
2. Update the CSV-loading code to use a relative path:

```python
df = pd.read_csv("Ambition_box_data.csv")
```

3. Run the notebook cells in order to perform data cleaning, statistical analysis, and visualization.

**Important:** Website HTML structures and access restrictions may change. The scraping code may need updates if the website layout changes. Run the notebook against the current website and verify its output before relying on the results.


## 👨‍💻 Author

**Harish Patil**

Aspiring Data Analyst | Python | SQL | Data Visualization

