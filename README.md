# RL-Continuous-Control

Project to train RL agent for [Udacity Continuous Control Environment](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control)

## About Project

The notebook included in this repository trains a Deep Deterministic Policy Gradient Network to improve the policy ('Actor') and improve the value estimates ('Critic') for an agent in Udacity Continuous Control Environment. 

![Continous Control Environment Gif](udacity_continuous_control_env.gif)

[Gif Source: Udacity DRLND Repository](https://github.com/udacity/deep-reinforcement-learning/tree/master/p2_continuous-control)

In this environment, at each time step, each of the 20 agents is given information about the environment in the form of a 33-dimensional vector, which contains information such as the position, rotation, velocity, and angular velocities of the arm.

Based on this representation of the state, each agent produces a 4-dimensional action vector with each entry being a continuous variable ranging between -1 and 1 (representing torque applicable to two joints) at each timestep to navigate around a large 2D space. 

When each agent's hand is in the goal location (indicated by green sphere), the agent receives a reward of +0.1 at each step. The goal of the agent is to maximize the reward at the end of each episode, by maintaining its position at the target location for as many time steps as possible. 

The environment is considered "solved" when the agents achieve average (over 100 episodes) of the average scores across 20 agents of at least +30. 

## Dependencies

To set up your python environment to run the code in this repository, follow the adapted [instructions from Udacity DRLND repository](https://github.com/udacity/deep-reinforcement-learning) below:

1. Create (and activate) a new environment with Python 3.6.

	- __Linux__ or __Mac__: 
	```bash
	conda create --name drlnd python=3.6
	source activate drlnd
	```
	- __Windows__: 
	```bash
	conda create --name drlnd python=3.6 
	activate drlnd
	```
	
2. If running in **Windows**, ensure you have the "Build Tools for Visual Studio 2019" installed from this [site](https://visualstudio.microsoft.com/downloads/).  This [article](https://towardsdatascience.com/how-to-install-openai-gym-in-a-windows-environment-338969e24d30) may also be very helpful.  This was confirmed to work in Windows 10 Home.  

3. Follow the instructions in [this repository](https://github.com/openai/gym) to perform a minimal install of OpenAI gym.  
	- Next, install the **classic control** environment group by following the instructions [here](https://github.com/openai/gym#classic-control).
	- Then, install the **box2d** environment group by following the instructions [here](https://github.com/openai/gym#box2d).
	
4. Clone the repository (if you haven't already!), and navigate to the `python/` folder.  Then, install several dependencies.  
    ```bash
    git clone git@github.com:jkim222383/RL-Continuous-Control.git
    cd RL-Continuous-Control/python
    pip install .
    ```

5. Create an [IPython kernel](http://ipython.readthedocs.io/en/stable/install/kernel_install.html) for the `drlnd` environment.    
    ```bash
    python -m ipykernel install --user --name drlnd --display-name "drlnd"
    ```

6. Before running code in a notebook, change the kernel to match the `drlnd` environment by using the drop-down `Kernel` menu. 

## Instructions

Follow the instructions on [Continuous Control Jupyter Notebook](p2_continuous-control/Continuous_Control.ipynb).

You can choose to train a new model from scratch while experimenting with different combinations of hyperparameters (in `config_grid`), or simply load the pretrained model weights and observe the agent's policy in the environment. 
