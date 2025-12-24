# Bank_Marketing_Classifiers_Performance
To gain a better understanding of the data, please read the information provided in the UCI link above, and examine the Materials and Methods section of the paper

1. Business UnderstandingThe objective of this project is to increase the efficiency of a Portuguese bank's direct marketing campaigns. Historically, these campaigns have low success rates. By using machine learning to predict which customers are likely to subscribe to a term deposit, the bank can:Targeted Outreach: Focus human resources on high-potential leads.Cost Reduction: Minimize the time and money spent on customers unlikely to convert.Strategic Timing: Understand how macro-economic factors influence customer behavior.
2. Data SummaryThe dataset includes 41,188 records from 17 campaigns. Key features analyzed include: Demographics: Age, Job, Marital Status, Education.Economic Indicators: Euribor 3-month rate, Consumer Price Index, Employment Variation Rate.Previous Contacts: Outcome of past marketing efforts.
3. Note on "Duration": The "call duration" was excluded from our final predictive models because it is not known until after a call is made, making it unusable for proactive targeting.
4. Modeling Results: We compared four classification models: Logistic Regression, K-Nearest Neighbors (KNN), Decision Trees, and Support Vector Machines (SVM).
-                    Model  Mean Fit Time (s)  Mean Accuracy  Mean ROC AUC
-      Logistic Regression           0.108072       0.887343      0.646573
-            Decision Tree           0.057032       0.887621      0.637406
-                      KNN           0.043281       0.875030      0.583319
-                      SVM          16.231962       0.887309      0.575107
5. Key Finding: Our analysis shows that the bank's marketing is most effective when targeting retired individuals and students. Furthermore, the broader economic environment (specifically interest rates like the Euribor) is a stronger predictor of a client's decision than their previous banking history.
6. Recommendations:
   Prioritize the "Golden Timing": Focus campaign efforts during periods of stable or declining interest rates, as clients are more receptive to long-term deposits then.
   Refine Customer Segments: The sales team should prioritize calls to clients in the "retired" and "student" categories, as they show a significantly higher conversion rate.
   Duration Strategy: While we cannot predict call length, our data shows successful subscriptions involve longer conversations. Agents should be coached on engagement techniques to keep the client on the line.
 7. Next Steps:
    A/B Testing: Before a full rollout, perform an A/B test where one group of agents uses the model's "priority list" and a control group uses the traditional random calling list.
    Feedback Loop: Create a pipeline where the outcome of every call (success or failure) is fed back into the model weekly to retrain and refine predictions as market conditions shift.
