# Algo_Trading

Algorithmic trading is the automated process of buying and selling shares on the stock market. This project presents a deep reinforcement learning approach to algorithmic trading. To tackle this problem, I have developed an automated stock market trading system which uses a Deep Q-Network trader to buy, sell or hold stocks. For this system, I  have collected stock market data for twenty companies from January 3rd, 2017 till January 6th, 2021. The automated algorithmic trader will predict which action should be taken during each point in time.

#### Training
* During training, the agent learns how to take an action based on the observed state.
* Within the training function, the agent observes the state, selects an action based on epsilon-greedy strategy and updates its memory.
* During training, the loss function is executed and loss values are logged.
* For each epoch, the logged values are displayed. The training function output consists of the running epochs, value of balance, and loss values.

#### Trade Function
* During trading, the system takes the test data set as input.
* Within the trading function, two arrays named as buying_days and selling_days are updated based on the action taken (buy/sell respectively).
* The balance is also updated and tracked. The output of the trading function is displayed which shows on which days the shares are bought or sold.

#### Q-learning
* Q-learning is an off policy reinforcement learning algorithm that finds the best action for a state based on Q-values.
* Q-values are tabulated in the Q-table, which consists of states as rows and actions as columns.
* In Deep Q-learning, the core of the system is not the Q-table, but rather the deep neural network that will be used to update the Q-table values and consequently to pick actions.
* In Deep Q-Learning, the state is fed into the neural network and it returns the Q-table values.
* For this system, the agent picks each action based on the epsilon greedy policy.

  > Reward = Reward + [discount_factor * estimate of optimal future value]
