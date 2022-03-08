# lecture1 Intro to RL

https://www.davidsilver.uk/teaching/ 

https://www.youtube.com/watch?v=2pWv7GOvuf0 


# Lec 1 intro
- RL problem
    - Rewards
    - Agent and environment
    - History and state
        - Environment state
        - Agent state
        - Information state (Markov state)
        - Full observable environments — Full observability - MDP Markov decision process 
        - Partially observable environments — Partial observability - POMDP partially observable MDP
- Inside an RL agent
    - Components
        - Policy: behavior func
        - Value function: how good
        - Model: agent’s representative of the environment
    - Policy 
        - A map from state to action
        - Deterministic policy: a = pi(s)
        - Stochastic policy: pi(a|s) = P[A_t=a | S_t = s]
    - Value function
        - A prediction of future reward
    - Model
        - Transition model: P predicts the next state
        - Reward model: R predicts he next reward
- Categorizing RL agents 1
    - Value based
        - No policy (implicit)
        - Value function
    - Policy based
        - Policy
        - No value function
    - Actor critic (combine above two)
        - Policy 
        - Value function 
- Categorizing RL agents 2
    - Model free
        - Policy and/or value function
        - No model
    - Model based
        - Policy and/or value function
        - Model
- Problem within RL
    - Learning vs planning
    - Exploration and exploitation 
    - Prediction vs control
