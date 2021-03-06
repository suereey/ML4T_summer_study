# Assessing a learning algorithm
## Metric 1: Root mean square (RMS) error 
- What is RMS error
![RMSError](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/11_RMS.PNG)
- In sample vs out of sample: KNN's training sample can have very small error. But measuring the error for Test samples are more important.
- Cross validation: Split data and run different trail. For example: Use the bottom 4 as training data and 1st one as test data (This is 1 trail). In total, this graph can have 5 trails.
![CrossValidation](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/12_CrossValidation.PNG)
- Roll forward corss validation:
        -Cross validation does not fit financial data application (need to predict future).
        - The trial above with test data infront of training data is not okay. (Training data is always before test data!)
        - Rolling forward corss validation:
        ![rollingcrossvalidation](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/13_rollingcrossvalidation.png)

## Metric 2: Correlation
- What is correlation: Y test versus Y predict.
- np.corrcoef():
    - -1:inversely correlated
    - 0: no correlation
    - 1: highly correlated (Good)
![correlation](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/14_Correlation.PNG)
- Most cases, RMS error increases, Correlation decreases; Sometime can be unsure as well.
## Overfitting
- Overfitting: 
    - Polynomial model: In sample error decreasing but out of sample error increasing.
        ![overfitting](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/14_overfitting.PNG)
    - KNN: k is how many data you take to make the prediction.
        ![KNNoverfitting](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/15_KNNOverfitting.PNG)
## Compare Regression and KNN
![COMPARE](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/16_assesslearningalgorithm.PNG)