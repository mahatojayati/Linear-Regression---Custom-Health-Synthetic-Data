# Linear-Regression---Custom-Health-Synthetic-Data

📊 Predicting Human Weight: A Linear Regression Approach. 
Case Study: Age vs. Weight Relationship.

1. Project Objective 
The goal is simple: Can we predict a person's weight based solely on their age? While human growth is complex, this project uses Linear Regression to find the "line of best fit" through age-weight data. We aim to quantify the growth rate (slope) and establish a baseline predictive model.

2. The Tech Stack: Why These?LibraryPurposeThe "Why" Pandas Data Manipulation. Essential for handling DataFrames and CSVs. You can't do data science in Python without it.Matplotlib/SeabornVisualizationHumans are bad at reading rows of numbers; we need to see the trend.Scikit-LearnMachine LearningThe gold standard for robust, reproducible ML algorithms.
  
3. Step-by-Step Execution
   1: Data Inspection. Before building a model, we perform a "Sanity Check."Action: Used df.info() and df.describe().
   Why: To check for null values and understand the distribution (mean, min, max). If your data has massive outliers or missing            entries, your model will be skewed.
   2: Exploratory Data Analysis (EDA)Action: Generated a scatter plot of Age vs. Weight.
   Why: We need to confirm that a linear relationship actually exists. If the data looks like a circle or a random cloud, Linear           Regression is a waste of time.
   3: Train-Test SplitAction: Split data into 80% Training and 20% Testing.
   Why: This is the most critical step. If you train on 100% of your data, you have no way to know if your model actually "learned" or     just "memorised" (overfitting). Testing on unseen data is the only way to prove the model works.
   4: Model TrainingAction: Initialized LinearRegression() and called .fit(X_train, y_train).Why: This is where the math happens. The      algorithm calculates the Ordinary Least Squares (OLS), minimising the distance between the data points and our mathematical line.
   5: Evaluation (The "Brutal Truth")We don't just "hope" the model is good; we prove it with numbers.MetricResultInterpretation$R^2       Score 0.943, 94.3% of the variance is captured by our model.
   MSE 4.80 On average, our squared error is 4.80.
   We want this as low as possible.Slope ($m$)$2.46$For every 1-year increase in age, weight goes up by ~2.46 kg.Note:
   The formula for our model is Weight = 2.46 \times Age + 12.39
   4. Final Visualisation: The Regression Line. Action: Plotted the calculated regression line over the original scatter plot.
   Why: This is the visual proof. It shows exactly how the model "sees" the trend compared to reality.5. Critical Critique (How to         improve)Don't be a "blind" developer. Every model has flaws:Non-Linearity: Human growth isn't perfectly linear.
   It slows down after 18. This model would fail for adults. Missing Features: Weight is influenced by height, gender, and activity.       Adding these would make the model more robust.
   Sample Size: With only 50 data points, the model is sensitive to new, extreme data.
   🛠️ How to Run
    Ensure you have the synthetic_age_weight_data.csv in your directory. Run the cells sequentially. Modify the random_state in the         split if you want to see how different data distributions affect the R^2.
