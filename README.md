# Optimizing Customer Engagement through RFM Segmentation and Analysis

In retail, understanding customer behavior and keeping customers engaged is crucial for crafting effective marketing strategies and critical for business success. RFM segmentation is a powerful customer analytics technique that helps businesses understand their customer base and develop targeted marketing strategies to boost engagement and loyalty. This project aims to delve deep into customer data to uncover valuable insights and enhance customer engagement.
The dataset used can be downloaded from [kaggle](https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis)
## Project Goal

The primary goal of this project is to optimize marketing strategies and improve customer engagement for a retail company. This was achieved by conducting hypothesis tests and segmentation analyses to reveal insights into customer behavior and preferences.

## Objectives

1. **Identify Key Factors Influencing Customer Behavior:**
   - Conduct hypothesis tests to explore the impact of factors like education level, marital status, and income on customer spending behavior.
   - Determine which factors significantly influence spending patterns to identify potential areas for targeted marketing efforts.

2. **Segment Customers Based on Behavioral Patterns:**
   - Use findings from hypothesis tests to segment customers into distinct groups based on their spending behavior and preferences.
   - Explore segmentation methods such as RFM (Recency, Frequency, Monetary) analysis to categorize customers into high-value, medium-value, and low-value segments.

3. **Provide Actionable Insights and Recommendations:**
   - Summarize findings from hypothesis tests and segmentation analysis into actionable insights.
   - Provide strategic recommendations for future marketing campaigns, product development, and customer engagement initiatives.

## Data Cleaning and Preprocessing

### Handling Missing Values

- Examined the dataset for missing values, particularly focusing on the 'Income' column.
- Filled missing values with the mean income to ensure data completeness.

### Identifying Outliers

- Identified outliers in the 'Income' column using statistical summaries, histograms, and boxplots.
- Calculated the Interquartile Range (IQR) to set boundaries for outliers and capped values outside these boundaries to minimize their impact.

### Addressing Inconsistencies

- Converted date columns to a consistent datetime format and derived customer age from the 'Year_Birth' column.
- Created new features such as 'Frequency' (total number of purchases per customer) and 'Monetary' (total amount spent across categories).

### Saving the Cleaned Dataset

- Selected relevant columns and saved the cleaned dataset for further analysis.
- Included key features such as age, education, marital status, income, frequency, and monetary value.

## Exploratory Data Analysis (EDA)

- **Monetary Value:** Customers with PhD degrees have the highest average monetary value, followed by those with Graduation, Master's, 2nd Cycle, and Basic education levels.
- **Age and Income:** Higher education levels correlate with older age and higher income.
- **Recency and Frequency:** No significant differences in recency (last purchase) or purchase frequency across education segments.
- **Income and Monetary value:** Positive correlation between income level and monetary value spent.

## Hypothesis Testing

### 1. Impact of Education Level on Total Monetary Value

- **Hypothesis (H01):** Customers with higher education levels tend to spend more.
- **Test Method:** ANOVA (Analysis of Variance)
- **Findings:** The ANOVA test resulted in a p-value of 5.889795808232043e-11, indicating a significant difference in total monetary value spent across different education levels.
- **Post-hoc Analysis (Tukey's HSD test):** Significant differences found between Basic vs. all higher education levels and 2n Cycle vs. PhD.

### 2. Impact of Marital Status on Total Monetary Value

- **Hypothesis (H02):** There is a significant difference in spending based on marital status.
- **Test Method:** ANOVA (Analysis of Variance)
- **Findings:** The ANOVA test resulted in a p-value of 0.38589916683378545, indicating no significant difference in total monetary value spent across different marital statuses.

### 3. Correlation between Income and Total Monetary Value

- **Hypothesis (H03):** Higher income leads to higher total monetary value spent.
- **Test Method:** Pearson Correlation
- **Findings:** The correlation coefficient is 0.8037457806030315 with a p-value of 0.0, indicating a significant positive correlation between income and total monetary value.

## Customer Segmentation

### 1. Education Level Segmentation

Based on the hypothesis testing results, customers were segmented according to their education levels.

#### Key Insights:

- Customers with a "Basic" education spend significantly less compared to other education levels.
- Higher education levels (PhD, MSc, and Graduation) correspond to higher spending.

#### Strategic Recommendations:

- Develop targeted marketing campaigns and premium product offerings for customers with higher education levels (PhD, Master).
- Create educational content and product knowledge initiatives for customers with a "Basic" education to increase engagement and spending.

### 2. RFM Segmentation Analysis

RFM (Recency, Frequency, Monetary) analysis was conducted to categorize customers based on their purchasing behavior.

#### Key Insights:

- **High-Value Customers:** Most frequent purchases, recent purchases, and highest average purchase value.
- **Medium-Value Customers:** Moderate purchase frequency, slightly lower recency, and moderate purchase value.
- **Low-Value Customers:** Least frequent purchases, oldest purchases, and lowest average purchase value.

#### Strategic Recommendations:

- Implement loyalty programs and exclusive offers for high RFM score customers.
- Develop re-engagement campaigns and personalized offers for low RFM score customers to increase their engagement and spending.

## Conclusion

By leveraging data analysis, hypothesis testing, and segmentation techniques, we have identified key factors influencing customer behavior and provided actionable insights for improving marketing strategies, product development, and customer engagement. Implementing these recommendations will help the retail company optimize its efforts and enhance customer satisfaction and loyalty.

## Repository Structure

- `data/`: Contains the raw and cleaned datasets.
- `notebooks/`: Jupyter notebooks for data cleaning, EDA, hypothesis testing, and segmentation analysis.
- `results/`: Outputs and visualizations from the analysis.
- `README.md`: Project overview and documentation (this file).
