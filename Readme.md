# collaboration-competition-rl
A Multi Agent RL agent that solves Unity's Tennis environment for a collaboration task 

## Project Details:
**Overview:** 
Broad goal is to train an agent to successfully solve Unity's Tennis environment.

**Goal & Rewards:** 
In this environment, two agents control rackets to bounce a ball over a net. If an agent hits the ball over the net, it receives a reward of +0.1. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play.

**State Space:** 
The state space consists of 8 variables corresponding to the position and velocity of the ball and racket. Each agent receives its own, local observation. 

**Action Space:**
Actions are continuous. Each action is a vector with 2 numbers, corresponding to moves toward (or away from) the net, and jumping.

**Solving condition:**
The task is episodic, and in order to solve the environment, agents must get an average score of +0.5 (over 100 consecutive episodes, after taking the maximum over both agents). Specifically,

- After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 2 (potentially different) scores. We then take the maximum of these 2 scores.
- This yields a single score for each episode.

The environment is considered solved when the average (over 100 episodes) of those scores is at least +0.5.

## Getting Started:
### Setting up the python environment and installing dependencies
 1. Create (and activate) a new environment with Python 3.6.

   - Linux or Mac:
 
      `conda create --name continuous_control python=3.6`
      `source activate continous_control`
      
   - Windows:
   
     `conda create --name continuous_control python=3.6`  
     
     `activate continuous_control`
  
 2. Clone the repository, Then, install several dependencies.
 
     `git clone https://github.com/ramanshrivastava/continuous-control-rl.git`
     
     `pip install -r requirements.txt`
     
     
 3. Create an IPython kernel for the `continuous_control` environment.
 
    `python -m ipykernel install --user --name continuous_control --display-name "continuous_control"`
   

 4. Before running code in a notebook, change the kernel to match the `continuous_control` environment by using the drop-down Kernel menu.

### Download the Unity Environment 
1. Download the environment from one of the links below. You need only select the environment that matches your operating system:

  - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux.zip)
  - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher.app.zip)
  - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86.zip)
  - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Windows_x86_64.zip)

(For Windows users) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

(For AWS) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/one_agent/Reacher_Linux_NoVis.zip) to obtain the environment.

2. Place the file in the `multi-agent-rl-tennis` GitHub repository, in the root folder, and unzip (or decompress) the file.


## Instructions:
1. Open the `Tennis.ipynb` jupyter notebook and execute each code cell to train the agent. 
2. Once the necessary packages are imported as a next step provide the `file_name` for the `UnityEnvironment`
3. Execute the rest of the cells as it is there after 
4. provide the `PATH` for `.pth` files in the code cell 8 to save actor and critic model weights. 

