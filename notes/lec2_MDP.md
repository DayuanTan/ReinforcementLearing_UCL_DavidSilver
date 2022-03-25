# lecture2 MDP

https://www.youtube.com/watch?v=lfHX2hHRMVQ


# Lec 2 Markov decision process MDP

- Markov Processes
    - Intro
        - Markov decision  processes formally describe an environment for RL
    - Almost all RL problems can be formalized as MDPs
        - Optimal control primarily deals with continuous MDPs
        - Partially obervable problems can be converted into MDPs
    - Markov Property
        - The future is independent of the past, given the present
          - P[ S_t+1 | S_t ] = P[ S_t+1 | S_1, ..., S_t ]
        - State transition Matrix
          - State transition probability: 
            - from Markov state s to successor state s'
            - P_ss' = P[ S_t+1 = s' | S_t = s ]
          - State transition Matrix: 
            - from all s to all successor states s'
            - P matrix
    - Markov chains
        - Markov process (or Markov chain) is a memoryless random process, i.e. a squeuence of randome states S1, S2, ... with Markov property
        - Is a tuple <S, P>
            - S is a set of states
            - P is state transition probability matrix
            - P_ss' = P[ S_t+1 = s' | S_t = s ]
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
    - s  
- Extensions to MDPs

