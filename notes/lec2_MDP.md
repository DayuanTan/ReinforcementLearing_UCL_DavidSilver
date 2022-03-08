# lecture2 MDP

https://www.youtube.com/watch?v=lfHX2hHRMVQ


# Lec 2 Markov decision process MDP

- Markov Processes
    - Intro
    - Almost all RL problems can be formalized as MDPs
        - Optimal control 
    - Markov Property
        - The future is independent of the past, given the present
        - State transition Matrix
    - Markov chains
        - Markov process (or Markov chain) is a memoryless random process, with Markov property
        - Is a tuple <S, P>
            - S is a set of states
            - P is state transition probability matrix
        - E.g.: Student Markov chain 
            - Student Markov chain Episodes, transition matrix
- Markov Reward Processes
    - Markov reward process (MRP) is a Markov chain with values
        - Is a tuple <S, P, R, gamma>
            - R is a reward function R_s = E[ R_(t+1) | S_t = s ] 
    - Return
        - G_t is the total discounted reward from time step t. G stands for goal.
        - G_t = R_t+1 + gamma * R_t+2 + gamma^2 * R_t+3 + …
        - Why discount?
            - Most Markov reward and decision process are discounted.
    - Value function
        - Value function v(s) gives the long term value of state s
        - The state value function v(s) of an MRP is the expected return starting from state s
            - v(s) = E[ G_t | S_t = s ]
        - E.g.: Student MRP returns
- Markov Decision Processes
- Extensions to MDPs

