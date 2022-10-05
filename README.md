# Deep Q-learning for Playing Parser-based Text-based Games
In this project, I use deep reinforcemnt learning to train an intelligent RL agent to play parser-based text-based games.

I specifically leverage and implement ideas from the following two papers:
1. [Language Understanding for Text-based Games Using Deep Reinforcement Learning](https://arxiv.org/abs/1506.08941)
2. [Counting to Explore and Generalize in Text-based Games](https://arxiv.org/abs/1806.11525)

Before discussion the results and other nitty-gritty details about the project, I would like to briefly describe text-based games in general so that we are all up-to-date:

## Text-based Games
In text-based games, a player has to issue a series of text commands to win a game. At every stage/level of the game, the player receives a description of the current state of the game and has to issue an appropriate command based on the description. The player moves to the next level and receives a reward (depending on the specific game) if it issues a correct command. The player eins the game if it can successfully complete the primary objective (specified at the start of the game) withing the specified number of steps.

![Types of Text-based Games](images/background/types_of_tbg.png)
There are 3 types of text-based games:
1. Parser-based games: The player issues command by generating a sequence of tokens.
2. Choice-based games: The player issues commands by choosing from a given list.
3. Hypertext-based games: The player issues commands by pointing to the words in the state description.

In this project, we will play a parser-based game: The Coin Collector game available in the [Textworld Learning Environment](https://arxiv.org/abs/1806.11532))

