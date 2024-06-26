

# Reinforcement Learning Agent: True Online Sarsa(λ)
## CSE 571 - Artificial Intelligence (2022) | Team 3643

### Team Members
- Aasish Tammana (1225545568)
- Akhilesh Udayashankar (1225622476)
- Devadutt Sanka (1225362138)
- Prem Suresh Kumar (1225492151)

### Project Overview
The primary objective of this project is to implement and evaluate the performance of a True Online Sarsa(λ) agent with linear function approximation. We aim to compare its effectiveness against the Q-learning agent, also implemented with linear function approximation, in various environments within the Pacman domain. All performance data generated during the project are stored and documented in the `modelperformance` file.

### Files Description
- `layoutGenerator.py`: Generates new layouts for the Pacman domain for use in testing both agents.
- `generatettestresults.py`: Conducts the Student T-Test to statistically compare the performance of True Online Sarsa(λ) against Approximate Q-learning agents.
- `generategraphsforallmodelruns.py`: Produces plots for all tested layouts, comparing the performance of True Online Sarsa(λ) agents (with various λ values) against the Q-learning agent.
- `game.py`: Modified to integrate the True Online Sarsa(λ) algorithm during runtime.
- `pacman.py`: Updated to include an additional function call for saving model training information.
- `qlearningAgents.py`: Contains the implementation for both the True Online Sarsa(λ) and Approximate Q-learning agents.
- `trainmodelsforalllayouts.py`: Facilitates training of both the Approximate Q Learning and True Online Sarsa(λ) models with a trace decay of 0.3 across all available layouts.
- `Plots.ipynb`: Contains sample code snippets from several of the scripts mentioned above for quick reference and understanding.

### Execution Commands
#### For the Approximate Q Learning Agent:
```shell
python pacman.py -p ApproximateQAgent -a extractor=SimpleExtractor -x 2000 -n 2000 -l layoutname
```

#### For the True Online Sarsa(λ) Agent:
- For a trace decay rate of 0.3:
```shell
python pacman.py -p TOSarsaAgent -a extractor=SimpleExtractor,tDRate=0.3 -x 2000 -n 2000 -l layoutname
```

#### To Automate Model Training Across All Layouts:
```shell
python trainmodelsforalllayouts.py
```

#### To Conduct the Student T-Test:
```shell
python generatettestresults.py
```

#### To Generate Comparative Graphs:
```shell
python generategraphsforallmodelruns.py
```