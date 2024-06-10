# UCI Bootcamp Final Project Machine Learning

![dataset-cover](https://github.com/Adykey79/UCI-Bootcamp-Final-Project-ML/assets/149746353/1c9315f7-515a-4cbf-b190-8d212cd82783)


Dataset Resource:
https://www.kaggle.com/datasets/divyansh22/flight-delay-prediction?select=Jan_2020_ontime.csv


U.S Air TraƧc Delays - A Predictive Analysis Perspective
By: Ardavan and Nithya
Project Outline
The project uses a combination of data engineering and supervised Machine Learning (ML) techniques to predict
flight delays for the month of January at specific destination airports in the United States (US) for future years, based
on Jan 2020 US flight data collected from the U.S Bureau of Transportation Statistics. The dataset is first cleaned
and prepared to remove extraneous fields to focus on those relevant for the analysis. An exploratory analysis is
subsequently performed to infer patterns and apply classification methods to predict flight delays. Different ML
modeling techniques are applied to this binary classification problem and the models are evaluated.
Data Source:
Kaggle
Pandas
Framework
Pandas
Dataframe
Data Gathering
Data
Pre-processing &
Cleaning
Exploratory Data
Analysis (EDA)
Modeling -
Machine Learning
Modeling - Neural
Network Model
Logistic Regression
Decision Tree
Random Forest
AdaBoost Classifier
Neural Network (NN)
Model with Keras
Tensorflow
Exploratory Data Analysis (EDA)
Columns with missing values and those that are redundant to the underlying analysis are dropped to cleanup the dataset. The
subsequent cleaned up data is then analyzed to infer basic patterns and insights as below:
❖ Which are the top 10 busiest airports in the US based on Jan 2020 data?
❖ How many flights do we have each day of the week in the US?
❖ How many flights are delayed each day of the week in the US?
❖ Flight delays by various dimensions ( day of month, airline carrier and departure time block )
Key Columns and Description:
❖ DAY_OF_MONTH: Calendar Day of Month
❖ DAY_OF_WEEK: Day of Week
❖ OP_UNIQUE_CARRIER: Unique Scheduled Operating Carrier Code. When multiple carriers have used the same code, a
numeric suffix is used for earlier users, for example, PA, PA(1), PA(2). Use this field for analysis across a range of years.
❖ ORIGIN: Origin Airport
❖ DEST: Destination Airport
❖ DEP_DEL15: Departure Delay Indicator, 15 Minutes or More (1 = Yes)
❖ DEP_TIME_BLK: CRS Departure Time Block, Hourly Intervals
❖ ARR_DEL15: Arrival Delay Indicator, 15 Minutes or More (1 = Yes)
❖ DISTANCE: Distance between airports (miles)
Flight Delays - Data Visualization Summary
Key Insights and Takeaways
● Flight Delay Patterns:
1) The Top 3 busiest airports are all on the
east coast and central portions of the US
(ATL, ORD and DFW). These are prone to
the highest number of delays as a result.
2) Southwest (WN Carrier Code) and Delta
(DL Carrier Code) are the top 2 airlines
with the most delays.
3) Thursday has the maximum number of
flight departures that are delayed.
4) Wednesday has the highest number of
non-delayed flights based on the dataset.
5) Sunday has the highest proportion of
flights with arrival delays despite being
one of the lower volume traffic days in
terms of airplane traffic.
6) The 4th and 11th of the month represent
the days with the maximum proportion of
flights arriving late.
Modeling - Logistic Regression (LR) Analysis
● The AUC, which is the area under the ROC (Receiver Operating Curve) has a high value of 0.90 for this classification.
● The above score underscores the ability of this binary classifier to distinguish between the two classes ( delayed, not delayed )
● The above curve has little overlap pointing to a more discriminating test.
Classification Report Summary:
● The precision for the delayed class is a lot lower (76%) when compared to the not delayed class (96%).
● The above is reinforced with the FPR (False Positive Rate) of the not delayed class higher than that of the delayed class.
● The overall model accuracy is at 93%.

Modeling - Decision Tree Classifier
● The AUC, which is the area under the ROC (Receiver Operating Curve) has a lower value of 0.79 for this classification.
● The above score indicates that this binary classifier is not able to effectively distinguish between the two classes ( delayed, not delayed )
● The above curve has more overlap compared to that of a Logistic Regression (LR) model.
Classification Report Summary:
● The precision for the delayed class is a lot lower (65%) when compared to the not delayed class (94%).
● The above is reinforced with the FPR (False Positive Rate) of the not delayed class higher than that of the delayed class.
● The overall model accuracy is at 90% which is lower than that of the Logistic Regression model (93%).
● The Decision Tree Classifier has slightly lower precision than that of the LR model for the non delayed class
but at much lower precision for the delayed class.

Modeling - Random Forest (RF) Classifier
● The AUC, which is the area under the ROC (Receiver Operating Curve) has an optimal value of 0.90 for this classification.
● This indicates the averaging this binary classifier uses to improve predictive accuracy and control over-fitting in the process.
● The above curve’s slope is also more consistent with that of the Logistic Regression (LR) model with the above optimization.
Classification Report Summary:
● The precision for the delayed class is a lot lower (77%) when compared to the not delayed class (94%).
● The overall model accuracy is at 92% which is closer to that of the Logistic Regression model (93%).
● This classifier improves upon the accuracy of the Decision Tree classifier earlier with a more discriminating test.

Modeling - AdaBoost Classifier
● The AUC, which is the area under the ROC (Receiver Operating Curve) has an optimal value of 0.93 for this classification.
● This indicates the superior classification performance of this model as a meta-estimator.
● The above curve’s slope is also more consistent with that of the LR and RF models with the above optimization.
Classification Report Summary:
● The precision for the delayed class is a lot lower (76%) when compared to the not delayed class (96%).
● The overall model accuracy is at 93% which matches that of the Logistic Regression model.
● This classifier improves upon the accuracy of the Decision Tree classifier earlier with a more discriminating test.

Modeling - Neural Network (NN) Model
● The loss function of the Neural Network (NN) Model, which is a function of the discrepancy between the predicted and targeted
outputs, stabilizes around 20% with subsequent training from the initial 25%.
● The trained and validated datasets also have a high degree of accuracy, around 93% for this model.
Loss and Accuracy Learning Curves:
● It would not help to train the model further as the plot of validation loss decreases to a point in congruence with that of the learning
Loss and then slightly increases again. This could indicate an inflection point of overfitting this model's learning curve.
● The overall model accuracy for the trained datasets saturates around 93%, consistent with other classifier models like RF and LR.

Conclusion
● Predictive Analytics is a powerful tool to analyze impactful datasets like that of flight delays that cause cumulative
losses across the aviation industry with the right balance of focus on accuracy and balancing bias across features.
● Data pre-processing and cleaning is critical to identify and isolate the key categories that increase the predictive
power of the underlying models. This will also help eliminate resource-heavy computations while modeling.
● An Exploratory Data Analysis (EDA) on the cleaned dataset helps to identify key patterns in the data and focus on
relevant areas of research (including classes) for the purposes of supervised machine learning.
● Modeling revolves around identifying a target (flight status, in this case) and defining related features that are
central to the prediction. The subsequent classifiers need to be properly weighed (equal vs. unequal variances)
● Neural Network provides an effective way to further build upon modeling capabilities by normalizing the data.
● Lastly, performance evaluation for each model is paramount with a clear understanding of precision, recall and
accuracy scores and their relative interpretation!

This file contains all the flights starting from 1st January 2020 till 31st January 2020. There are around 400,000 rows in this file and 21 feature columns indicating the features of the flight including information about origin airport, destination airport, airplane information, departure time and arrival time.
