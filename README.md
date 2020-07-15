<h1 align="center">Solving Cartpole Using Reinforcement Learning
</h1>
<p align="center">
    <a href="https://jupyter.org/"><img src="https://img.shields.io/badge/Made with-Jupyter Notebook-Orange.svg"></a>
    <a href="https://github.com/luowensheng/DIP-Image-Restoration-Homomorphic-filtering-/pulse"><img src="https://img.shields.io/badge/Maintained%3F-yes-green.svg"></a>
    <a href="https://github.com/luowensheng"><img src="https://badges.frapsoft.com/os/v2/open-source.svg?v=103"></a>


[Goal & To Do](#Goal-&-To-Do) • [Step by Step](#Step-by-Step) • [Implementation](#Implementation) • [Results](#Results) • [Questions](#Questions)

</center>
<br>
<br>
<br>


# Goal and To Do
The goal of this test is **to solve a classic control problem by implementing multiple reinforcement learning methods**.

In this test, we have to implement the algorithms all by our own.

# Step by Step
* **Environment**
    - We’ll use Cartpole-v1 (OpenAI Gym library) as our environment. To use this environment, we should install it on your machine. Run the command (We’ll need Python 3.5+):
        ```
        pip install gym
        ```
    - We can also build it from source:
        ```
        git clone https://github.com/openai/gym
        cd gym
        pip install –e.
        ```

* **Interact with OpenAI Gym environments**
* **The observation space (state space) is:**
    - Cart position (max: 4.8, min: -4.8)
    - Cart velocity (max: Inf, min: -Inf)
    - Pole Angle (max: 24 deg, min: -24 deg)
    - Pole velocity at tip (max: Inf, min: -Inf)

* **The action space is:**
    - Push cart to left (0)
    - Push cart to right (1)

* **Taking each step would earn reward +1**

![step](https://i.ibb.co/kqm7W2K/1.jpg)

<br>

Visit https://gym.openai.com/docs/ for more detail.

# Implementation
### **What to implement:**
* Tabular Q-learning method (How to transform continuous state to discrete state?)
* Policy Gradient method
* Actor-Critic method

>***Google colab** was used for this project.*

# Results
### **Tabular Q-learning method**
![tabular](https://i.ibb.co/FXd1wGz/2.jpg)

### **Policy Gradient method**
Due to the continuous nature of this problem, **Keras** was used to train the agent. The algorithm was taken from the book.

The number of hidden states was 250 and the learning rate of 0.1.

![policy gradient](https://i.ibb.co/rxRS820/3.jpg)

It has one input layer which are the four observation values the we get after each action, and also 2 dense layers, with the second having 250 components to be able to extract more information. With a batch of 1, we get the following result:

![results](https://i.ibb.co/f8zwY27/4.jpg)

The agent was able to perform much faster than the q-learning agent and it reached its optimal policy at about 100 steps.

![results](https://i.ibb.co/PT63LMZ/5.jpg)

### **Actor-Critic method**
![results](https://i.ibb.co/myMdBRF/6.jpg)



# Questions
Submit your questions and bug reports [here](https://github.com/luowensheng/Natural-Language-Processing-Grammatical-Error-Correction-/issues).

