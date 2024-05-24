<a target="_blank" href="https://colab.research.google.com/github/pierpaolospaziani/Machine-Learning/blob/main/mountain_car.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

# Mountain Car
## Author
* **Pierpaolo Spaziani** (serial number: 0316331)

## Description

The Mountain Car MDP is a deterministic MDP that consists of a car placed stochastically at the bottom of a sinusoidal valley, with the only possible actions being the accelerations that can be applied to the car in either direction.\
The goal of the MDP is to strategically accelerate the car to reach the goal state on top of the right hill.

## Observation Space

| Name | Dimension | Description |
|----------------|:-----------:|-------------------------------------------------|
| Action Space | 3 | Discrete actions: **0** (*push left*), **1** (*no push*), **2** (*push right*). |
| Observation Space | 2 | Continuous values representing position and velocity of the car. **Position**: [-1.2, 0.6], **Velocity**: [-0.07 0.07]|

## Reward

The goal is to reach the flag placed on top of the right hill as quickly as possible, as such the agent is penalised with a reward of -1 for each timestep.

## Starting State

The position of the car is assigned a uniform random value in [-0.6 , -0.4]. The starting velocity of the car is always assigned to 0.

## Episode End

The episode ends if either of the following happens:

- Termination: The position of the car is greater than or equal to 0.5 (the goal position on top of the right hill)
- Truncation: The length of the episode is 200.

## Objective

The objective of this notebook is to solve the problem and compare the results of 2 models:
- **Q-Learning**
- **Sarsa**

<u>**NOTE**</u>: *gym* version 0.26.2 is required to run the code
