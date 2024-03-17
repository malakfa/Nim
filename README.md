# Nim Game AI using Q-Learning

## Overview

The Nim Game AI is built using Q-learning, a reinforcement learning technique, to learn the optimal strategy for playing the game of Nim. By playing against itself repeatedly and learning from experience, the AI aims to learn which actions to take and which actions to avoid in order to win the game.

## Problem Statement

In the game of Nim, players take turns removing objects from piles. The player who removes the last object loses the game. The AI learns the optimal strategy through reinforcement learning by updating Q-values for each (state, action) pair.

## Representations

- **State:** The state of the Nim game is represented by the current size of all piles. For example, [1, 1, 3, 5] represents a state with 1 object in pile 0, 1 object in pile 1, 3 objects in pile 2, and 5 objects in pile 3.
- **Action:** An action in the Nim game is represented by a pair of integers (i, j), where i is the index of the pile and j is the number of objects to remove from that pile.

## Q-Learning Formula

The Q-value for each (state, action) pair is updated using the following formula:

Q(s, a) <- Q(s, a) + alpha * (new value estimate - old value estimate)

- **alpha:** Learning rate, determining the importance of new information compared to existing knowledge.
- **new value estimate:** Sum of the reward received for the current action and the estimate of all future rewards.
- **old value estimate:** Existing value for Q(s, a).

## Approach

1. **Initialization:** Initialize Q-values for all (state, action) pairs.
2. **Gameplay:** Allow the AI to play against itself or human opponents, selecting actions based on Q-values.
3. **Q-Value Update:** Update Q-values after each action using the Q-learning formula.
4. **Training:** Repeat gameplay and Q-value updates until the AI converges to an optimal strategy.
5. **Evaluation:** Evaluate the performance of the AI by playing against human opponents or other AI agents.

## Future Enhancements

- Implement exploration-exploitation strategies to balance between exploring new actions and exploiting learned knowledge.
- Experiment with different learning rates and discount factors to optimize learning performance.
- Extend the AI to handle more complex variations of the Nim game with additional rules or constraints.

