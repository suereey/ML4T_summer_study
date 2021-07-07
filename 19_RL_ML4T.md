# Reinforcement learning
## Overview
- Reinforce learner provide policies that provide specific direction on which action to take.
- The RL Problem:
    - s: state of the environment
    - a: action
    - T: Transiction function
    - pi: policy
    - r: reward
    - ![RLProblem](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/24_RLProblem.PNG)
- Mapping trading to RL:
    - ![practice](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/25_TradingRL.PNG)
    - ![mapping](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/26_MappingTradingtoRL.PNG)
- Markov decision problems: How to find the best pi (policy)?
    - ![MarkovDecision](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/27_MarkovDecisionProblem.PNG)
    - Under the condition of **Unkown trasation and reward**:
        - Model based
        - Model free **Q-Learning**
        -![model1](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/28_Model_01.PNG) 
    - What is optimize?
        - The 0.95 value means $1 worth $0.95 after take a step.
        - ![optimize](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/29_optimize.PNG)
        -![example](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/30_optimize.PNG)
## RL Summary
![RLSummary](https://github.com/suereey/ML4T_summer_study/blob/main/03_screenshot/31_RLSummary.PNG)