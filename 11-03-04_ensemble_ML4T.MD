# Ensemble learners-bagging and boosting
## Ensemble
- What is ensemble
    ![ensemble](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/17_EnsembleLearner.PNG)
- How to build an ensemble
    ![buildensemble](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/18_EnsembleLearner.PNG)
- Bootstrap aggregating-bagging
    ![bootstrap](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/19_Bootstrap.PNG)
- Overfit
    - most likely to overfit:
    ![overfit](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/20_ensembleOverfit.PNG)
    - Bagging example
    ![baggingexample](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/21_ensembleOverfit.PNG)
- Boosting: Ada boost
    - After D1, when select data to D2, data with high error are weighted to have high chance to go into D2. Following D2 to D3, D3 to D4... as well.
    ![adaboost](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/22_Adaboost.PNG)
    - Which is more likely to overfit as m increases: m is the number of bags we are using

        - simple bagging
        - Adaboost (Yes, adaboost)
- Summary: ensemble learners: bagging and boosting
    ![SUMMARY](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/23_boostsummary.PNG)



