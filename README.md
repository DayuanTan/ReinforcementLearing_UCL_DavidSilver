# ReinforcementLearing_UCL_DavidSilver

David Silver's website: https://www.davidsilver.uk/teaching/

## Lectures

### Lecture 1: Introduction to Reinforcement Learning
- [My note](notes/lec1_intro_RL.md)  
### Lecture 2: Markov Decision Processes
- [Annotated slide by me](./slides/lec2_markov_decision_process_MDP.pdf), [My note](notes/lec2_MDP.md)  
- Markov Process 
    - Markov Chain <S, P>
        - S is a set of states
        - P is state transition probability matrix
        - P_ss' = P[ S_t+1 = s' | S_t = s ]
- Markov Reward Process MRP
    - is Markov Chain with values
    - <S, P, R, gamma>
        - R is a reward function, R_s = E[ R_(t+1) | S_t = s ]. R_s means, for time t and state s, how much reward we can get in t+1, i.e. R_(t+1).
        - gamma is a discount factor. gamma \in [0, 1]
    - Value function
        - Value function v(s) gives the long term value of state s
        - The state value function v(s) of an MRP is the expected return starting from state s
            - v(s) = E[ G_t | S_t = s ]
    - Solving the Bellman Equation
        - solve directly, O(n^3)
        - Dynamic programming
        - Monte-Carlo evaluation
        - Temporal-Difference learning
- Markov Decision Processes MDP
    - is a Markov Reward Process with decisions
    - <S, A, P, R, gamma>
        - A is a finite set of actions
        - P^a_ss' = P[ S_t+1 = s' | S_t = s, A_t = a ]
        - R is a reward function, R^a_s = E[ R_(t+1) | S_t = s, A_t = a ]. R_s means, for time t and state s, how much reward we can get in t+1, i.e. R_(t+1).
    - Value Function
        - State-value function: tell us how good to be a specific state s
            - v_pi(s) = E_pi[ G_t | S_t = s ]
        - Action-value funtion: tell us how good to take a specific action from a specific state
            - q_pi(s, a) = E_pi[ G_t | S_t = s, A_t = a ]
    - Optimal Value Function
        - Solve q_*(s, a)
        - Finding an optimal policy 
### Lecture 3: Planning by Dynamic Programming
  - [My note](notes)
### Lecture 4: Model-Free Prediction
  - [My note](notes)
### Lecture 5: Model-Free Control
  - [My note](notes) 
### Lecture 6: Value Function Approximation
  - [My note](notes)
### Lecture 7: Policy Gradient Methods
  - [My note](notes) 
### Lecture 8: Integrating Learning and Planning
  - [My note](notes) 
### Lecture 9: Exploration and Exploitation
  - [My note](notes) 
### Lecture 10: Case Study: RL in Classic Games
  - [My note](notes) 

## Other resources
- All slides [here](slides/)
- Assignments and Exams and Answers [here](assigns_exams/)