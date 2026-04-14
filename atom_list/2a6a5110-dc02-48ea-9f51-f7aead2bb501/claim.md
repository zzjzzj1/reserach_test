## Claim

TRPO is evaluated on 7 Atari 2600 games from the Arcade Learning Environment using a convolutional neural network policy with:
- Two convolutional layers: 16 filters each, $4 \times 4$ kernels, stride 2
- One fully connected hidden layer with 20 units
- Total: $\sim$33,500 parameters
- Softmax output over discrete actions

TRPO achieves performance competitive with Deep Q-Learning (DQN, Mnih et al., 2013) and UCC-I (Guo et al., 2014), despite using a simpler and smaller network architecture. The same architecture and hyperparameters are used across all 7 games.