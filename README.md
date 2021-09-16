# Deep-Q-Network-Snake-game-bot-DeepMind-
For games with many states, we use a neural network to get Q Value for a state-action pair. This network is known as Deep Q Network or DQN. We can either of the following architecture of DQN, but the second one is preferred.


![image](https://user-images.githubusercontent.com/42925930/133657909-3d847cd8-799c-4af0-baac-4b3f74eb1eec.png)

If we use first architecture, then for at a given state, we have to iterate through DQN n times, where n is the number of actions available for the agent. If we use second architecture, then we have to iterate through DQN only one time, and we will get Q Values for all actions, among them we will choose the action with the highest Q value.

We want to iterate through DQN only one time because iterating through a Neural Network is a computationally expensive step, and it takes time to get output. Thus less iteration is preferred.

**SNAKE GAME**

In the game of snake, the snake has to eat food to grow, and avoid hitting walls and eating itself. First, we have to define the actions, state, and rewards.

![image](https://user-images.githubusercontent.com/42925930/133658163-18af03d7-9739-4d0b-bd63-333271c44e5d.png)

**Actions**
Snake can only move
**left, forward, or right**.
Snake can't move backward.
![image](https://user-images.githubusercontent.com/42925930/133658246-83593342-8717-4b36-96d1-7b6fc21c6b08.png)


**States**
We can get the state of the game by just answering the following things:
- Is there a wall or snake body on the left? **==> No**
- Is there a wall or snake body in front?   **==>No**
- Is there a wall or snake body on the right?   **==>Yes**
- Was snake moving up?  **==>Yes**
- Was snake moving right?   **==>No**
- Was snake moving down?   **==>No**
- Was snake moving left?   **==>No**
- Is the food left or right?  **==> Left**
- Is the food up or down?   **==>Down**

Reward
The agent will get **+10 rewar**d when the snake eats food, and **-10 (penalty)** when the snake eats itself or hits the wall.
