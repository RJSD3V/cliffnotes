Start reading Lils Blog referenced in Stablebaselines3 Documentation

### Key Concepts: 

An agent acts in an environment. the environment gives feedback and reacts based on the model which we may or may not know. 

The agent can stay in one of multiple states of the environment. What states the agent stays in depends on the actions that the agent takes, and the Transition probabilities between those states. When the action is taken, the environment delivers a reward. 


The model defines the Reward function and the transition probabilities. We may or may not know how the model works and this differentiate two circumstances. 

- Know the model: planning with perfect information, do model based RL.
- Don't know the model: Learn the model as you go as a part of the algorithm. 

#### Model: 
The descriptor of the environment. We can learn or infer how the environment will react or provide feedback to the agent. A model has two major parts, A probability funciton and a Reward function. 


#### Policy
Policy is an agent's behavior function, tells us which action to take in state s.Its a mapping from s --> a, state to action, which tells us which action to take in each state. This can be deterministic or stochastic. 

Deterministic: pi (s) = a
Stochastic: pi (s) = P [ A = a | S = s ]

