# Assignment 5: Health Data Classification Results

This file contains your manual interpretations and analysis of the model results from the different parts of the assignment.

## Part 1: Logistic Regression on Imbalanced Data

### Interpretation of Results

In this section, provide your interpretation of the Logistic Regression model's performance on the imbalanced dataset. Consider:

- Which metric performed best and why?
- Which metric performed worst and why?
- How much did the class imbalance affect the results?
- What does the confusion matrix tell you about the model's predictions?

*Your analysis here*
The metric with the best performance is the accuracy with a value of 0.9245 because the nunmber of correct cases, was much higher than the number of incorrect cases. The worst performing metrix is the recall because there was a large number of true positive cases. The class imbalance severely impacted the results because the class imbalance artifically inflates the accuracy, making the model seem that it is performing well, except it does not necessarily reflect good performance on the minority class. The confusion matrix tells us that there is a much larger proportion of true negative cases. However, the number of true positives is very low with only 91 correctly identified cases. 



## Part 2: Tree-Based Models with Time Series Features

### Comparison of Random Forest and XGBoost

In this section, compare the performance of the Random Forest and XGBoost models:

- Which model performed better according to AUC score?
- Why might one model outperform the other on this dataset?
- How did the addition of time-series features (rolling mean and standard deviation) affect model performance?

*Your analysis here...*
According to the AUC score, the XG boost performed better than the random forest with a value of 0.9961. This model outperformed the other because XG boosting uses boosting which builds trees sequentially, and therefore has better control over class imbalances. The addition of time-series features helped to add a temportal factor into the data, which therefore helped the model to predict the general patterns.

## Part 3: Logistic Regression with Balanced Data

### Improvement Analysis

In this section, analyze the improvements gained by addressing class imbalance:

- Which metrics showed the most significant improvement?
- Which metrics showed the least improvement?
- Why might some metrics improve more than others?
- What does this tell you about the importance of addressing class imbalance?

*Your analysis here...*
The recall improved the most by increasing by 91.51% which shows that the model identifies a higher number of true positive cases. Precision had the least improvement because it decreased by 48.03%. This shows that it is important to address class imbalance issues because it can drastically change results. It also shifts the trade-off meaning that som accuracy and precision may need to be sacraficed in order to address the class imbalance.

## Overall Conclusions

Summarize your key findings from all three parts of the assignment:

- What were the most important factors affecting model performance?
- Which techniques provided the most significant improvements?
- What would you recommend for future modeling of this dataset?

*Your conclusions here...*

The most important factors affecting model performance was the class imbalance. This was seen in the logistic model with high accuracy but low recall. Feature engineering such as the rolling features greatly improved the model because by including the time-series features, the model was able to find a general pattern of the data. I would recommend for future modeling, to pay attention to class imbalances because it can greatly affect results, along with incorporating time-series when you can for more complex patterns.