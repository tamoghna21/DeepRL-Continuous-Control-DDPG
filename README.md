[//]: # (Image References)

[image1]: https://user-images.githubusercontent.com/10624937/43851024-320ba930-9aff-11e8-8493-ee547c6af349.gif "Trained Agent"

[image2]: score_plot.png "Score Plot"

# Continuous Control - Reacher Environment (Project 2 - Udacity Deep RL)

This project is part of the Udacity [Deep Reinforcement Learning Nanodegree Program](https://www.udacity.com/course/deep-reinforcement-learning-nanodegree--nd893). This project solves the Reacher environmet in Mac OSX. 

The goal is to create and train an Agent to solve the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment.  The Action space is continuous in this environment.

![Trained Agent][image1]

### Environment Details

The envoronment is built using [Unity Machine Learning Agents](https://github.com/Unity-Technologies/ml-agents) (**ML-Agents**), which is an open-source Unity plugin that enables games and simulations to serve as environments for training intelligent agents. 
The project environment, provided by Udacity is similar to, but not identical to the [Reacher](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment. The Udacity provided environment has been downloaded from [here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip) for Mac OSX. 

#### Distributed Training
The [Reacher environment](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip) for Mac OSX provided by Udacity used in this project has 20 identical agents, each with its own copy of the environment.

#### State and Action spaces

In this environment, a double-jointed arm can move to target locations. A reward of +0.1 is provided for each step that the agent's hand is in the goal location. Thus, the goal of your agent is to maintain its position at the target location for as many time steps as possible.

The observation space consists of 33 variables corresponding to position, rotation, velocity, and angular velocities of the arm. Each action is a vector with four numbers, corresponding to torque applicable to two joints. Every entry in the action vector should be a number between -1 and 1.

#### Solving the environment

For solving this version of the environment with twenty identical agents, the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
- This yields an average score for each episode (where the average is over all 20 agents).

The environment is considered solved, when the average (over 100 episodes) of those average scores is at least +30. In the case of the plot above, the environment was solved at episode 63, since the average of the average scores from episodes 64 to 163 (inclusive) was greater than +30.

### Getting Started

1. Follow the instructions [here](https://github.com/udacity/deep-reinforcement-learning#dependencies) to setup the python environment. These instructions can be found in README.md at the root of the repository.
2. Download this repository (only for Mac OSX), it has the environment included. So for Mac OSX, step 3 can be skipped.
3. Download the Udacity provided environment (Twenty Agents version) from one of the links below (For Mac OSX, this step can be skipped as the environment is already included in this repo).  Select the environment corresponding to the required operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

4. Place the file in the repository folder (downloaded in step 2) and unzip (or decompress) the file.


### Instructions

The environment just set up has the files and tools to allow the training of the agent.

Start the Jupyter Notebook server by running the commands below (in Mac OSX). A new browser tab will open with a list of the files in the current folder.

```
$ source activate drlnd
$ jupyter notebook
```

Follow the instructions in `Continious_Control-Reacher.ipynb` to get started with training your own agent!  

The task of solving the Reacher environment with twenty agents was completed using DDPG algorithm with modifications.

```
Environment solved in 182 episodes!	Average Score: 30.05
```
![Score Plot][image2]

For more details see the [Report](https://github.com/tamoghna21/DeepRL-Continuous-Control-DDPG/blob/main/Report.pdf)







