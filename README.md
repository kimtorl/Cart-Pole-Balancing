# Cart-Pole-Balancing
Balancing cartpole-v1 using Q learning

# Overview:
Welcome to CartPole Balancing with Q-Learning! This project showcases the power of Reinforcement Learning (RL) through Q-learning, a classic RL algorithm, to teach an agent how to balance a pole on a moving cart. Witness the magic of artificial intelligence as the agent learns to perform this seemingly simple task through trial and error.

A summary of the pole cart environment is given below:

1. Action Space:
The action is an ndarray with shape (1,) which can take values {0, 1} indicating pushing the cart to the left or right, respectively. Note that the velocity that is reduced or increased by the applied force is not fixed and it depends on the angle the pole is pointing. The center of gravity of the pole varies the amount of energy needed to move the cart underneath it.

2. Observation Space:
The observation is an ndarray with shape (4,) with the values corresponding to the following positions and velocities:
![image](https://github.com/kimtorl/Cart-Pole-Balancing/assets/98906571/91b1d93b-1fec-4f7c-aed3-5d225bbc168c)

3. Reward
Since the goal is to keep the pole upright for as long as possible, a reward of +1 for every step taken, including the termination step, is allotted.

4. Starting State
All observations are assigned a uniformly random value in (-0.05, 0.05).

5. Episode End
The episode ends if any one of the following occurs:
Termination: Pole Angle is greater than ±12°
Termination: Cart Position is greater than ±2.4 (center of the cart reaches the edge of the display)
Truncation: Episode length is greater than 500.
