# DeepLearning_2020
This repository contains reinforcement learning models that are able to play 3 enviroments from the library OpenAI-Gym. The enviroments currently available are: CartPole, LunarLander and Breakout.

The code has been developed to run using Google Colab, however if you want to run it on your PCs you can set the variable "colab" to False so that the model can be stored and loaded from your PC. Take into account that OpenAI Gym doesn't support Windows OS so you might run into problems when running the code using Windows.

That is why we chose to implement the code in a notebook format so that it can install all the required dependencies and run as intended by using Google Colab no matter which OS you are using.


## CartPole
The code contained in the CartPole folder uses DQN reinforcement learning in order to learn how to play the game. The architecture of the network consists on a CNN, given that the input provided to the network is a frame of the game screen.


## LunarLander
The notebook contained in the LunarLander folder uses DQN reinforcement learning by using the state provided by the gym enviroment as input for the network. In this case, a fully connected layer is used, as the size of the input (the state) will be vectors of size (8,1).

The code contains every class needed to do the DQN reinforcement learning and also contains train and test functions. The train function trains the agent and stores the model whenever the game is won (avg score higher than 200 in 100 consecutive episodes). The test function, allows the user to load a previously stored model and make it play a number of times. Then it renders a video showing how the agent has played.

## Breakout
In the folder Breakout, many codes can be found. BreakoutAI.ipynb contains an AI algorithm which basically makes the paddle do the correct action so that it is always below the ball. This algorithm is used to generate a dataset so that we can do a Supervised Learning approach.

The code BreakoutSL.ipynb is a Supervised Learning approach, that uses the data previously generated by the AI algorithm to do the training and the testing of the model.

Finally, the code BreakoutReinforcement.ipynb is a DQN reinforcement learning approach. In this code, the network is formed by fully connected layers as the input (the state) will be the position of the ball and the paddle. This state that we will use as input is not the one returned by gym library. We decided to modify the state as we empirically found out that it gave us better results.

