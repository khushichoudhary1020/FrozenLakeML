
Machine Learning, as we know there are four different types of machine learning 
Supervised ML
Unsupervised ML
Semisupervised ML
Reinforcement Learning
Here I've worked on Reinforcement learning which is Science of decision making. It is about taking suitable action to maximize reward in a particular situation. 
It is employed by various software and machines to find the best possible behavior or path it should take in a specific situation. 
Reinforcement learning differs from supervised learning in a way that in supervised learning the training data has the answer key with it so the model is trained with the correct answer itself whereas in reinforcement learning, there is no answer but the reinforcement agent decides what to do to perform the given task. 
In the absence of a training dataset, it is bound to learn from its experience. ###Khushi


# FrozenLakeML

**WHAT IS Q-LEARNING**

Q-learning is a machine learning approach that enables a model to iteratively learn and improve over time by taking the correct action. Q-learning is a type of reinforcement learning. With reinforcement learning, a machine learning model is trained to mimic the way animals or children learn. Good actions are rewarded or reinforced, while bad actions are discouraged and penalized.With the state-action-reward-state-action form of reinforcement learning, the training regimen follows a model to take the right actions. Q-learning provides a model-free approach to reinforcement learning. There is no model of the environment to guide the reinforcement learning process. The agent, an AI component that acts in the environment -- iteratively learns and makes predictions about the environment on its own.At each state, the agent selects an action to execute based on an exploration-exploitation tradeoff. Initially, the agent explores different actions randomly to gather information about the environment. Over time, it starts exploiting its knowledge by choosing actions that are known to yield higher rewards according to the Q-table. After executing an action, the agent receives a reward and transitions to a new state. It then updates the Q-table by using the Bellman equation, which combines the immediate reward and the expected rewards from the next state. This update allows the agent to gradually learn the optimal action selection policy. Q-learning also takes an off-policy approach to reinforcement learning. A Q-learning approach aims to determine the optimal action based on its current state. The Q-learning approach can accomplish this by either developing its own set of rules or deviating from the prescribed policy. Because Q-learning may deviate from the given policy, a defined policy is not needed.
In this, we need to train the model or agent using Q-learning technique, in which we provide environment, and a set of rules on the basis of which agent learns. In this game, frozen lake an agent is needed to be trained with the help of reinforcement learning using Q-learning.

**ENVIRONMENT DETAILS:-**
The game initializes with the agent at its start state[0,0] of the frozen lake grid and it needs to reach the goal state. The environment grid holds 16 states(4*4=16). There are holes in the grid(4x4) of lake which are distributed at diff places and if the agent falls in any hole, it will be a punished i.e, no rewards or deduction of reward points (to be specific). The player will play until one of these condition stikes

1) Win the environment
  
2) Falls in the hole/Lake

3) The episode steps finished.

is_slippery is an argument which means that an agent may move perpendicular to the intended direction sometimes ( is_slippery), if you place True in the argument then slippering is a possible condition but if place False agent can't slip. You can import the environmemt from the following link:-**https://gymnasium.farama.org/environments/toy_text/frozen_lake/ **

**ACTIONS IN THIS GAME:-**

_The action shape is (1,) in the range {0, 3} indicating which direction to move the player._
When playing the game you wil notice that the agent is taking 4 possible actions to reach the goal which are listed below:

0: Move left

1: Move down

2: Move right

3: Move up

An agent will take these action to achieve success in the task or to win the game.

**OBSERVATION SPACE:-**
_The observation is a value representing the player’s current position_

The formula used for calculating the observation spaces is current_row * nrows + current_col (where both the row and col start at 0).

**START STATE**:- The initial position of an agent from where it starts the game.

**GOAL STATE**:- The state in which the goal is achieved and the game ends.

**REWARDS**

_This is the vital factor of the game 'rewards'. Any agent learns and hits a trial to get the reward. In this game the reward schedule is:-_

#####Khushi

Reach goal: +1

Reach hole: 0

Reach frozen: 0

**EPISODE TERMINATION:-**
_The episode will be ended when:-_
~ Goal is achieved.

~ Agent falls into the hole.

~ Episode steps ended.

Overall,this is the whole working of this game.
