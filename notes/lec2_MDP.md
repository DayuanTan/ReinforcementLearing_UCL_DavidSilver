# lecture2 MDP

https://www.youtube.com/watch?v=lfHX2hHRMVQ


# Lec 2 Markov decision process MDP

# Markov Processes
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

# Markov Reward Processes
- Markov reward process (MRP) is a Markov chain with values
    - Is a tuple <S, P, R, gamma>
        - S is a set of states
        - P is state transition probability matrix
        - P_ss' = P[ S_t+1 = s' | S_t = s ]
        - R is a reward function, R_s = E[ R_(t+1) | S_t = s ]. R_s means, for time t and state s, how much reward we can get in t+1, i.e. R_(t+1).
        - gamma is a discount factor. gamma \in [0, 1]
- Return
    - G_t is the total discounted reward from time step t. G stands for goal.
    - G_t = R_t+1 + gamma * R_t+2 + gamma^2 * R_t+3 + …
    - This values immediate reward above delayed rewards. (We prefer closer reward.)
    - Why discount?
        - Most Markov reward and decision process are discounted.
        - Because we don't have a perfect model. We may don't trust our plan/model for future. Uncertainty about the future may not be fully represented.
        - Mathematically  convenient to discount rewards.
        - Avoids infinite returns in cyclic Markov processes.
        - Animal/human prefer immediate reward.
- Value function
    - Value function v(s) gives the long term value of state s
    - The state value function v(s) of an MRP is the expected return starting from state s
        - v(s) = E[ G_t | S_t = s ]
    - E.g.: Student MRP returns
        - Starting from S_1 = C1 with gamma = 1/2
        - G_1 = R_2 + gamma*R_3 + ... + gamma^(T-2) * R_T
        - C1 C2 C3 Pass Sleep:
          - v_1  = -2 - 2 * 0.5 - 2 * 0.25 + 10 * 0.125 = -2.25
- Bellman Equation for MRPs
    - The value function can be decomposed into 2 parts:
      - immediate reward R_t+1
      - discounted value of successor state gamma*v(S_t+1)
      - v(s) = E[ G_t | S_t = s ]
            = E[ R_t+1 + gamma*v(S_t+1) | S_t = s]
- Bellman Equation in Matrix Form
- Solving the Bellman Equation
    - Bellman equation is a linear equation
    - For small MRPs: just solve directly, O(n^3)
    - For large MRPs:
        - Dynamic programming
        - Monte-Carlo evaluation
        - Temporal-Difference learning

# Markov Decision Processes
- A Markov Decision Process (MDP) is a Markov Reward Process with decisions. It is an environment in which all states are Markov.
- MDP is a tuple <S, A, P, R, gamma>
    - S is a finite set of states
    - A is a finite set of actions
    - P is state transition probability matrix
    - P^a_ss' = P[ S_t+1 = s' | S_t = s, A_t = a ]
    - R is a reward function, R^a_s = E[ R_(t+1) | S_t = s, A_t = a ]. R_s means, for time t and state s, how much reward we can get in t+1, i.e. R_(t+1).
    - gamma is a discount factor. gamma \in [0, 1]

    - Example: Student MDP

- Policies
    - A policy pi is a distribution over actions given states:
      - pi(a|s) = P[ A_t = a | S_t = s]
    - A policy fully defines the behaviour of an agent
    - MDP policies depend on the current state (not the history)
      - i.e. policies are stationary (time-independent)

- Given an MDP M = <S, A, P, R, gamma> and a policy pi
    - The state sequence S_1, S_2, ... is a Markov process <S, P^pi>
    - The state and reward sequence S_1, R_2, S_2, ... is a Markov Reward Process <S, P^pi, R^pi, gamma>

- Value Function
    - State-value function: tell us how good to be a specific state s
      - The state-value function V_pi(s) of an MDP is the expected return starting from state s, and the following policy pi
      - v_pi(s) = E_pi[ G_t | S_t = s ]
    - Action-value funtion: tell us how good to take a specific action from a specific state
      - The action-value function q_pi(s, a) is the expected return starting from state s, taking action a, and then following policy pi
      - q_pi(s, a) = E_pi[ G_t | S_t = s, A_t = a ]
- Bellman Expectation Equation
    - The state-value function can again be decomposed 
    - The action-value function can similarly be decomposed
    - Example
- Bellman Expectation Equation (Matrix Form)
    - The Bellman expectation equation can be expressed concisely using the included MRP
    - direct solution


- Optimal Value Function
    - How to find the best  possible solution to MDP
    - The optimal state-value function V_*(s) is the maximum value function over all policies.
    - The optimal action-value function q_*(s, a) is the maximum action-value function over all poliies.
    - Goal: solve q_*


# Extensions to MDPs

