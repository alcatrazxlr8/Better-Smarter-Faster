# Better, Smarter, Faster
Developing and analyzing different optimal strategies and models (Utility based vs Neural Networks) to capture prey efficiently in a dynamic, probabilistic environment.

## Overview

This project, completed as part of the Computer Science course at Rutgers University (Fall 2022), aims to build an agent that can capture prey as efficiently as possible within a probabilistic environment. Building upon the environment from Project 2, this project introduces enhanced strategies and models to optimize the agent's performance under both complete and partial information scenarios.

## Project Structure

### 1. Environment

The environment consists of a circle of 50 nodes, with additional random edges to increase connectivity. It includes three entities:

- **Agent**: The entity controlled by the developed strategies, aiming to capture the prey.
- **Prey**: Moves randomly to neighboring nodes or stays in its current node.
- **Predator**: Follows the Distracted Predator Model, sometimes moving towards the agent and sometimes moving randomly.

### 2. Agent Strategies

#### Complete Information Setting

1. **Optimal Agent (U\*)**:
   - Determines the minimal expected number of rounds (U\*(s)) to catch the prey from any given state \(s\).
   - The algorithm identifies and simulates the optimal action for every state, ensuring the agent captures the prey efficiently.

2. **Comparison with Previous Agents**:
   - Simulates and compares the performance of the optimal agent with Agents 1 and 2 from Project 2.
   - Visualizes states where the optimal agent and previous agents make different choices, explaining the rationale behind these differences.

#### Partial Information Setting

1. **Unknown Prey Position**:
   - Represents the state of the agent with a vector of probabilities for the prey's location.
   - Estimates the utility \(U_{\text{partial}}\) of a state based on the expected utility considering the possible prey locations.

2. **Model \(V\) and \(V_{\text{partial}}\)**:
   - Develops a model \(V\) to predict the value \(U\*(s)\) for complete information states.
   - Trains a model \(V_{\text{partial}}\) to predict \(U_{\text{partial}}\) for partial information states.
   - Simulates agents based on these models and compares their performance against the optimal agent and previous agents.

### Implementation

The project involves writing a program to:

1. Compute \(U\*(s)\) for every state \(s\) and determine the optimal action.
2. Identify states where capturing the prey is impossible and understand the causes.
3. Find and visualize the state with the largest finite \(U\*(s)\) value.
4. Simulate the performance of agents based on \(U\*(s)\) and models \(V\) and \(V_{\text{partial}}\).
5. Address overfitting and accuracy concerns for models \(V\) and \(V_{\text{partial}}\).

### Analysis

Key points of analysis include:

- Performance comparison between the optimal agent, previous agents, and model-based agents.
- Visualization and explanation of states with differing agent decisions.
- Model accuracy and effectiveness in predicting utility values and guiding agent actions.

## Usage

To run the project, open the provided Jupyter Notebook (`Better_Smarter_Faster.ipynb`) in an appropriate environment (e.g., Jupyter Lab, Google Colab). The notebook contains detailed comments and explanations to guide you through the implementation and experimentation process.

### Requirements

- Python 3.x
- Jupyter Notebook
- Required libraries: `numpy`, `matplotlib`, `random`

### Running the Notebook

1. Clone the repository.
   ```bash
   git clone https://github.com/yourusername/Better_Smarter_Faster.git
   cd Better_Smarter_Faster
   ```
2. Open the Jupyter Notebook.
   ```bash
   jupyter notebook Better_Smarter_Faster.ipynb
   ```
3. Follow the instructions in the notebook to run the simulations and analyze the results.

## Conclusion

This project demonstrates advanced strategies for decision-making in uncertain environments. By leveraging probabilistic models and comparing different agent strategies, it provides valuable insights into optimizing agent performance under varying levels of information.
I concluded that even though the utility based approach is quite optimised already, the neural net I built from scratch still beat it and ended up being the better performer


---

**Better, Smarter, Faster: Developing and analyzing optimal strategies and models to capture prey efficiently in a dynamic, probabilistic environment.**
