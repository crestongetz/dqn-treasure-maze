# Deep-Q-Network-Treasure-Maze
![Python](https://img.shields.io/badge/Python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)

## Overview
This project implements a Deep Reinforcement Learning agent to autonomously navigate a complex, dynamic maze to locate a hidden treasure. By leveraging Q-learning algorithms paired with a deep neural network, the agent learns optimal pathfinding strategies through a balance of exploration and exploitation.

### How it works
1. The pirate starts at the top of the maze. Valid moves yield standard rewards, while invalid moves such as hitting a blocked path or going outside the boundary, yield penalties.
2. The agent chooses to either explore a random adjacent cell or exploit what it knows.
3. The result of the action is stored in the experience replay memory.
4. Periodically, the network trains on a batch of memories, refining its Q-value predictions.
5. Over multiple episodes, the agent optimizes its pathfinding ability.

## Design Defense
You can view the full `design defense` here: [Design Defense (PDF)](https://github.com/crestongetz/dqn-treasure-maze/blob/0c8f60c1e32da9df4e337418a2745a380af3bbe8/Design%20Defense.pdf)

### Architecture 
* **Deep Q-Network (DQN):** Built using Keras, the neural network predicts the best possible action or Q-value for any given state in the maze.
* **Experience Replay Memory:** The agent stores its previous states, actions, and rewards, sampling them as a batch to update the neural network. This breaks the correlation between consecutive states and stabilizes the learning process.
* **Exploration vs. Exploitation:** The agent begins with a 100% exploration rate, which causes it to take random paths, helping it understand the environment. With each training episode, the exploration rate decays by approximately 0.5%, transitioning the agent to do more exploitation, where it relies on its trained neural network to find the most efficient path.

## Tools/Frameworks used
* Python
* Keras / Deep Learning:
* Jupyter Notebook:
* Reinforcement Learning / Deep Q-Learning

## Future Improvements
1. Test the agent on larger, more complex mazes
2. Optimize for faster training



## Reflection

