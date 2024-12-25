# Sales Prediction and Customer Segmentation

## Project Overview
This project focuses on leveraging sales data to gain actionable business insights and improve decision-making processes. The analysis involves customer segmentation using RFM metrics and clustering techniques, and sales prediction using a Random Forest model. The key outcomes include identifying customer segments, predicting sales, and providing strategic business recommendations.

---

## Table of Contents
1. [Project Workflow](#project-workflow)
2. [Data Used](#data-used)
3. [Implementation Details](#implementation-details)
4. [Results and Insights](#results-and-insights)
5. [How to Run the Project](#how-to-run-the-project)

---

## Project Workflow
1. **Data Loading & Cleaning**:
   - Removed duplicate records and handled missing values.
   - Created a clean dataset for analysis and modeling.

2. **Exploratory Data Analysis (EDA)**:
   - Analyzed sales trends and customer behavior across time, geography, and product categories.
   - Visualized patterns in purchasing behaviors and churned customers.

3. **Feature Engineering**:
   - Derived Recency, Frequency, and Monetary (RFM) metrics.
   - Categorized customers based on RFM scores and segmented them into groups.
   - Engineered additional features such as TotalPrice, WeekDay, and Hour.

4. **Clustering Analysis**:
   - Applied K-Means clustering to segment customers into meaningful groups.
   - Used PCA for dimensionality reduction and better visualization of clusters.

5. **Model Building**:
   - Trained a Random Forest model to predict sales using selected features.
   - Included customer behavior, product categories, and temporal features in the model.

6. **Model Evaluation**:
   - Evaluated the Random Forest model using RMSE.
   - Identified important features contributing to sales predictions.

7. **Final Model Adjustment**:
   - Refined clustering and predictive models for improved performance.
   - Validated the robustness of insights derived.

8. **Business Recommendations**:
   - Provided actionable recommendations based on customer segmentation and sales trends.

---

## Data Used
- **Main Dataset**:
  - Columns: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`, `TotalPrice`, `WeekDay`, `Day`, `Month`, `Year`, `Hour`, `PriceCategory`.

- **RFM Metrics**:
  - Columns: `CustomerID`, `Recency`, `Frequency`, `Monetary`, `R_Score`, `F_Score`, `M_Score`, `RFM_Score`, `Segment`, `Churn`, `Cluster`.

---

## Implementation Details

### Data Preprocessing
- Cleaned missing values in `CustomerID` and invalid entries in `Quantity` and `UnitPrice`.
- Capped outliers in RFM metrics to ensure robust clustering.

### Exploratory Data Analysis
- Visualized sales trends by time, day, and geography.
- Analyzed characteristics of churned customers and purchasing trends.

### RFM Analysis
- Segmented customers into groups using Recency, Frequency, and Monetary values.
- Assigned RFM scores and mapped them to meaningful customer segments.

### K-Means Clustering
- Performed clustering based on RFM metrics.
- Used PCA to visualize clusters and interpret segment distributions.

### Random Forest Sales Prediction
- Selected important features through correlation analysis and domain knowledge.
- Trained a Random Forest model to predict `TotalPrice`.
- Evaluated model performance using RMSE and identified key predictors.

### Insights and Recommendations
- Highlighted key segments such as `Loyal Customers` and `At-Risk Customers`.
- Provided strategic insights to optimize marketing campaigns and sales strategies.

---

## Results and Insights
1. **Customer Segmentation**:
   - Segmented customers into actionable groups like `Champions`, `Hibernating`, and `At-Risk`.
   - Identified characteristics and purchasing behaviors of each segment.

2. **Sales Prediction**:
   - Achieved a robust predictive model with key features like `Recency`, `Frequency`, and `PriceCategory`.
   - Derived actionable insights from feature importance analysis.

3. **Business Recommendations**:
   - Focus on `Loyal Customers` for retention and `Promising Customers` for upselling opportunities.
   - Adjust inventory management based on top-selling products.
   - Target `At-Risk Customers` with personalized re-engagement campaigns.

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter Notebook or Python scripts for each step of the analysis.

4. View visualizations and reports generated in the `output/` folder.

---

### Contributions
Feel free to contribute to the project by suggesting improvements or adding features. Submit a pull request or open an issue for discussions.

### License
This project is open-source and available under the [MIT License](LICENSE).

