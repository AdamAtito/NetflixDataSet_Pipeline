# NetflixDataSet_Pipeline

##  project Overview

This project demonstrates a complete end-to-end data engineering and analysis workflow using the Netflix Movies & TV Shows dataset. The primary objective was to take a raw, messy dataset and build a small ETL (Extract, Transform, Load) pipeline to clean, process, and prepare it for insightful exploratory data analysis (EDA).

The project is structured to showcase the following key skills:
1.  **Data Cleaning & Preprocessing:** Systematically handling missing values, correcting data types, and ensuring data quality.
2.  **Feature Engineering:** Creating new, valuable features from existing columns using techniques like regular expressions (Regex).
3.  **Exploratory Data Analysis (EDA):** Uncovering patterns and insights from the clean data.
4.  **Data Visualization:** Presenting the findings through clear and effective charts using Matplotlib & Seaborn.

---

## Tools and Libraries Used

* **Language:** Python
* **Libraries:**
    * **Pandas:** For data manipulation, cleaning, and the core ETL process.
    * **Matplotlib & Seaborn:** For creating static and informative visualizations.
* **Environment:** Jupyter Notebook

---

## Data Engineering Pipeline (ETL)

The initial dataset contained several quality issues typical of real-world data. A pipeline was built to perform the following transformations:

* **Handling Missing Values:** A heatmap was used to visualize the extent of null values in columns like `director`, `country`, and `cast`. These were then strategically filled with "Unknown" to maintain data integrity.
* **Correcting Data Types:** The `date_added` column, originally a string, was converted into a proper `datetime` object for time-series analysis. The `errors='coerce'` parameter was used to handle any non-conforming entries gracefully.
* **Feature Engineering with Regex:** The unstructured `duration` column (containing values like "90 min" or "2 Seasons") was intelligently parsed using **regular expressions**. This created two new, clean numerical columns: `movie_min_duration` and `TV_show_Seasons`, making the data ready for quantitative analysis.

---

## Key Findings & Visualizations

### 1. Missing Data Landscape
The initial step was to identify the data quality gaps. The heatmap below clearly shows the columns that required cleaning.


### 2. Top 10 Content Producing Countries
After cleaning the `country` column, the analysis revealed that the United States is the largest content producer, followed by India.


### 3. Most Common Genres on Netflix
By processing the `listed_in` column, it was found that "Dramas," "Comedies," and "International Movies" are the most dominant genres, highlighting Netflix's content strategy.


---

## How to Run This Project

1.  Clone the repository to your local machine:
    ```bash
    git clone [https://github.com/AdamAtito/NetflixDataSet_Pipeline.git](https://github.com/AdamAtito/NetflixDataSet_Pipeline.git)
    ```
2.  Ensure you have Python and the required libraries (Pandas, Seaborn, Matplotlib) installed.
3.  Open the `Project_Netflix.ipynb` file in a Jupyter environment.
4.  Run the cells sequentially to execute the pipeline and view the complete analysis.
