# SCLM 449: Process Control and Improvement - Happy Cow Ltd. Case Study

## Project Overview 🥛

Happy Cow Ltd., a milk production business, aims to expand into new, more discerning markets. To succeed, they need robust quality management. This project analyzes Happy Cow's milk quality based on seven key variables: **pH, Temperature, Taste, Odor, Fat, Turbidity, and Colour**.

The primary goals are:

1.  Monitor the stability of key production processes using **Statistical Process Control (SPC)**.

2.  Understand the distribution and relationships between quality attributes and the final milk grade (**Low, Medium, High**).

3.  Develop a predictive model using **Multinomial Logistic Regression (MLR)** to classify milk quality based on the measured attributes.

4.  Provide data-driven **strategic recommendations** to Happy Cow Ltd. for improving quality control and consistency.

## Methodology & Analysis 📊

The project employs a multi-faceted approach combining SPC and machine learning:

1.  **Control Charts for Process Monitoring:**

    **X-bar and S charts** were constructed for continuous variables (**pH, Temperature, Colour**) to assess process stability and variability over time. Control limits were calculated, and charts were analyzed for out-of-control signals or non-random patterns.

2.  **Boxplot Analysis for Grade Prediction:**

    Boxplots were generated to visualize the distribution of each predictor variable (**pH, Temperature, Taste, Odor, Fat, Turbidity, Colour**) across the three milk grades (Low, Medium, High). This helps identify differences in central tendency, spread, and potential outliers between grades.

3.  **Distribution and Descriptive Visualizations:**

    A bar chart visualizes the overall distribution of milk samples across the Low, Medium, and High grades, showing the prevalence of each quality category.

4.  **Correlation Analysis:**
 
    A correlation matrix was calculated to examine the linear relationships between the predictor variables. This helps identify potential multicollinearity and understand interdependencies (e.g., Odor and Turbidity, Fat and Taste).

5.  **Multinomial Logistic Regression (MLR):**
 
   MLR was used to model the relationship between the seven predictor variables and the three-category 'Grade' outcome.

   Model fit was assessed using **-2 Log Likelihood** and **Pseudo R-Squares** (Cox & Snell, Nagelkerke, McFadden).

   **Likelihood Ratio Tests** were used to determine the overall model significance and the individual contribution of each predictor variable.

   **Parameter Estimates (B coefficients and Odds Ratios - Exp(B))** were interpreted to understand the direction and magnitude of each predictor's effect on the odds of milk being classified as 'High' or 'Low' relative to the 'Medium' reference category.

6.  **Synthesis:** Findings from boxplots, correlations, and MLR were integrated to create profiles for each milk grade and provide robust insights.

## Key Findings & Recommendations 💡

**Process Stability:** The **pH** and **Colour** processes are statistically in control, but **Temperature** control is unstable and out of control, requiring immediate attention.

**Predictive Factors:** **Temperature, Colour, Taste, Odor, Fat, and Turbidity** were all statistically significant predictors of milk grade in the MLR model. pH was significant in predicting 'Low' vs. 'Medium' but not 'High' vs. 'Medium'. **Temperature** had the largest impact based on Likelihood Ratio Tests.

**Grade Profiles:**

**High Grade:** Strongly associated with good taste, good odor, high fat, high turbidity, higher colour, and *higher* temperature (relative to medium).

**Low Grade:** Strongly associated with *higher* temperature, *higher* colour, *lower* pH, bad taste, bad odor, high fat, and high turbidity (relative to medium).

**Medium Grade:** Tends to have lower colour scores and potentially an optimal temperature range.

**Strategic Recommendations:**
    
    1.  Implement an **automatic classification system** based on key thresholds (Fat, Turbidity, Taste, Odor).
    
    2.  Strictly **control Temperature** around an optimal target (approx. 45°C suggested by boxplots, but needs verification) to reduce variation and improve stability.

    3.  **Standardize sensory evaluation** (Taste, Odor) through training.
    
    4.  Integrate **real-time sensors** for Turbidity, Colour, and Temperature.
    
    5.  Use **pH monitoring** as an early warning for potential low-quality batches.
    
    6.  Optimize production towards **Medium/Low grades** based on market positioning, avoiding costly overproduction of High grade.
