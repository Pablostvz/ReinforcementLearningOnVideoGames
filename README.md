# DeepLearning_2020
This repository contains reinforcement learning models that are able to play 3 enviroments from the library OpenAI-Gym. The enviroments currently available are: CartPole, LunarLander and Breakout.

## Installation
To execute the notebooks create a folder named DeepLearning_2020 in the base directory of Google Drive. Then download this repository as a zip and put the uncompressed reposity into the Drive folder DeepLearning_2020.

The code has been developed to run using Google Colab, however some codes allows you if you to run it on your PCs setting the variable "colab" to False so that the model can be stored and loaded from your PC. Take into account that OpenAI Gym doesn't support some Windows OS so you might run into problems when running the code using Windows.

That is why we chose to implement the code in a notebook format so that it can install all the required dependencies and run as intended by using Google Colab no matter which OS you are using.


## CartPole
The code contained in the CartPole folder uses DQN reinforcement learning in order to learn how to play the game. The architecture of the network consists on a CNN, given that the input provided to the network is a frame of the game screen.


## LunarLander
The notebook contained in the LunarLander folder uses DQN reinforcement learning by using the state provided by the gym enviroment as input for the network. In this case, a fully connected layer is used, as the size of the input (the state) will be vectors of size (8,1).

The code contains every class needed to do the DQN reinforcement learning and also contains train and test functions. The train function trains the agent and stores the model whenever the game is won (avg score higher than 200 in 100 consecutive episodes). The test function, allows the user to load a previously stored model and make it play a number of times. Then it renders a video showing how the agent has played.

## Breakout
In the folder Breakout, many codes can be found. The code Breakout_SL.ipynb is a Supervised Learning approach, that uses the data previously generated by an AI algorithm to do the training and the testing of the model. The AI algorithm basically calculates the position of the paddle and ball and with this information chooses the action to make. This algorithm is used to generate a dataset so that we can do a Supervised Learning approach.

Finally, the code BreakoutReinforcement.ipynb is a DQN reinforcement learning approach. In this code, the network is formed by fully connected layers as the input (the state) will be the position of the ball and the paddle. This state that we will use as input is not the one returned by gym library. We decided to modify the state as we empirically found out that it gave us better results.

The dataset breakout_balanced.npy for the supervised learning cannot be uploaded because it's too large. In case you want to train it with our dataset you can do it by inserting the file in the folder ReinforcementLearningOnVideoGames/data/. We also provide the code to generate a new dataset and the trained model.
Link:
https://drive.google.com/file/d/1PvOt8ACSEvMPCj9XHlwQdz0iMrcf7tBp/view?usp=sharing

