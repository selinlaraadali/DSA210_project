# DSA210_project
# Sleep and Walking Speed Analysis

## Description
This project examines the correlation between sleep duration and walking speed using personal health data collected from the iOS Health app. By analyzing daily sleep and walking metrics, the project seeks to uncover trends and test hypotheses about the impact of sleep on walking metrics.

### Hypotheses:
- Null Hypothesis (H₀): Sleep duration has no significant effect on walking speed.

- Alternative Hypothesis (Hₐ): Sleep duration has a significant effect on walking speed.

The project uses data cleaning, exploratory data analysis (EDA), visualizations, and a simple linear regression model to analyze the relationship and test the hypotheses.

## Motivation
As someone who values maintaining a balanced and active lifestyle, I’ve always been interested in understanding how sleep impacts my physical performance and overall well-being. Sleep is not just a time for rest but a cornerstone of both physical and cognitive health, which are also considered to be correlated with walking speed. Through this project, I aim to explore the relationship between sleep duration and walking speed, uncovering how my daily habits may influence my energy levels and physical activity. 

## Data Source
The dataset used in this project is collected through the iOS Health app on my iPhone, which tracks daily health metrics. The data includes:

- Sleep duration: Total hours of sleep per day as recorded by the Health app.
- Walking speed: Average walking speed (km/h) per day.

## Plan
### Data Cleaning and Preparation:

- Loading Data:

Daily sleep data was loaded and aggregated into weekly sleep duration using the start and end times. Daily walking speed data was similarly aggregated into weekly averages.

- Handling Missing Data:

Missing values were identified and removed to ensure data consistency.

- Aligning Weekly Data:

Weekly datasets for sleep and walking speed were merged on the common week column to retain only matching weeks.

- Normalization:

Data columns were verified to ensure proper formats and consistent scales.

### Exploratory Data Analysis (EDA) and Visualizations:

1) Univariate Analysis

- Sleep Duration:

The histogram showed a right-skewed distribution with most weekly sleep durations between 6 to 8 hours. The boxplot highlighted outliers in sleep durations exceeding 10 hours.

- Walking Speed:

The walking speed data followed a nearly normal distribution, with the majority of values clustering around 3.8 to 4.2 km/h. The boxplot showed minimal variability, with no significant outliers.

2) Bivariate Analysis

- Correlation Analysis:

Scatterplot visualizations depicted a weak positive correlation between sleep duration and walking speed. The linear regression line was overlaid on the scatterplot to observe the relationship visually.

3) Outlier Detection:

Z-Score Analysis: Sleep duration outliers were detected using a z-score threshold of 3 and one significant outlier (11.03 hours) was removed. No outliers were found in walking speed data.

### Hypothesis Testing:

Pearson Correlation Test is conducted to evaluate the relationship between sleep duration and walking speed.

Correlation Coefficient: 0.34

P-Value: 0.0011

Interpretation:

The p-value is less than 0.05, leading to the rejection of the null hypothesis (H₀). This indicates that sleep duration has a statistically significant effect on walking speed, though the correlation is weak.

### Modeling:

A linear regression model was implemented to predict walking speed based on sleep duration.

Steps:

1) Split the data into training (70%), validation (15%), and testing (15%) sets.

2) Train the model using the training set.

3) Evaluate the model on validation and test sets.

- Evaluation Metrics:

1) Validation Set:

Mean Squared Error (MSE): 0.04

Mean Absolute Error (MAE): 0.18

R-squared (R²): 0.08

2) Test Set:

Mean Squared Error (MSE): 0.07

Mean Absolute Error (MAE): 0.23

R-squared (R²): 0.26


Interpretation:

The model shows a weak predictive power (low R² values), indicating that other factors beyond sleep duration may contribute to walking speed.



### Findings and Insights:

- Correlation Analysis: A weak positive correlation exists between weekly sleep duration and walking speed, supported by the Pearson correlation coefficient.

- Hypothesis Testing: The null hypothesis was rejected, confirming a statistically significant relationship.

- Modeling Performance: The linear regression model demonstrated limited predictive power, suggesting the need for additional features or more complex models.

### Limitations and Future Work:

- Data Limitations:

The dataset is limited to weekly aggregated data, potentially missing day-to-day variations. Potential confounding variables (e.g., physical activity levels, health conditions) were not included.

- Modeling Improvements:

Explore multivariate models incorporating additional features such as physical activity or heart rate. Experiment with non-linear models can be done to capture complex relationships.

- Expanded Analysis:

Analysis can be extended to daily data with larger sample sizes. Seasonal or temporal trends in sleep and walking metrics can be investigated.

### Conclusion

This project explored the relationship between sleep duration and walking speed using weekly aggregated data. While a statistically significant relationship was identified, the correlation was weak, and predictive modeling highlighted the need for additional factors to improve accuracy. These findings emphasize the complexity of the relationship between sleep and physical performance, paving the way for further research.


