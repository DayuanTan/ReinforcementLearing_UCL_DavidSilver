# ReinforcementLearing_UCL_DavidSilver

David Silver's website: https://www.davidsilver.uk/teaching/

## Lectures

### Lecture 1: Introduction to Reinforcement Learning
- [Annotated slide by me](./slides/lec1_intro_RL.pdf), [My note](notes/lec1_intro_RL.md)  
- RL diff form other ML
    - No supervisor, only a reward signal
    - Feedback is delayed, not instantaneous
    - Time reall y matters ( se q uential, non i.i.d data)
    - Agent’s actions affect the subsequent data it receives
- Major Components of an RL Agent
    - Policy: is the agent’s behaviour. It is a map from state to action.
    - Value function: is a prediction of future reward. Used to evaluate the goodness / badness of states.
    - Model: A model predicts what the environment will do next
- Categorizing RL agents
    - Value Based vs Policy Based vs Actor Critic
    - Model free vs Model based
- Problems in RL
    - Learning and Planning
        - Learning: 
            - environment is initially unknown
            - agent interacts with the environment
            - agent improves its policy
        - Planning: 
            - environment is known
            - agent performs computations with its model ( without any external interaction )
            - agent improves its policy
    - Exploration and Exploitation
        - Reinforcement learning is like trial-and-error learning. The agent should discover a good policy. From its experiences of the environment.
    - Prediction and Control
        - Prediction: evaluate the future
            - Given a policy
        - Control: optimise the future
            - Find the best policy

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
    - Solving the Bellman Equation - linear equation
        - Small DRP: solve directly, O(n^3)
        - Large DRP: 
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
    - Bellman Optimality Equation
        - Non-linear, no closed solution
        - iterative solution:
            - Value iteration
            - Policy iteration
            - Q-learning
            - Sarsa
### Lecture 3: Planning by Dynamic Programming
- [Annotated slide by me](./slides/lec3_planning_by_DP.pdf)


### Lecture 4: Model-Free Prediction
- [Annotated slide by me](./slides/lec4_model_free_prediction_MC-TD.pdf)
### Lecture 5: Model-Free Control
- [Annotated slide by me](./slides/lec5_model_free_control.pdf) 
### Lecture 6: Value Function Approximation
- [Annotated slide by me](./slides/lec6_value_Function_Approx.pdf)
### Lecture 7: Policy Gradient Methods
- [Annotated slide by me](./slides/lec7_policy_gradient_pg.pdf) 
### Lecture 8: Integrating Learning and Planning
- [Annotated slide by me](./slides/lec8_integrating_learning_and_planning_dyna.pdf) 
### Lecture 9: Exploration and Exploitation
- [Annotated slide by me](./slides/lec9_exploration_and_exploitation_XX.pdf) 
### Lecture 10: Case Study: RL in Classic Games
- [Annotated slide by me](./slides/lec10_classic_games.pdf) 

## Other resources
- All slides [here](slides/)
- Assignments and Exams and Answers [here](assigns_exams/)