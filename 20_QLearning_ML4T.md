# Q-Learning
## What is Q-learning
- Q is a table with 2 dimenssions, s (state) and a (action).
- How to use Q? 
    - pi(s) represents the policy take at state s.
    - The equation is: find the maximize Q[s,a]with different a value.
    - The * symbol means optimized value.
    -![WhatisQ](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/31_WhatisQ.PNG)
## Procedures for Q-learning
![procedures](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/32_QlearningProcedure.PNG)
## Update the Rule (Q value)
- Alpha: learning rate: Bigger, learn faster
- Gamma: discount rate: Lower, value the later rewards less
- ![udpaterule](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/33_updaterule.PNG)
- ![updaterule](https://raw.githubusercontent.com/suereey/ML4T_summer_study/main/03_screenshot/34_udpaterule.PNG)

## Two finer points
- Success depends on exploration
- Choose random action with prob C.

# How to use Q-Learning solve stock trade problm. 
## In order to do that, we need to define:
- Actions
- State
- Rewards
## The trading problem: Actions
- Buy
- Sell
- Nohting
- ![Action]()
## The trading problem: Rewards
- Daily return better than cumulative return: A reward at each step allows the learning agent get feedback on each individual action it takes (including doing nothing).


