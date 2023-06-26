# Reinforcement Learning: Multi Armed Bandit (MAB) Problem
The multi-armed bandit (MAB) problem is like a game where you have to make choices to win the most rewards. It's called "multi-armed bandit" because it's similar to a gambler in a casino with many slot machines (the "armed bandits") and needs to decide which ones to play to win the most money over time.

In the MAB problem, the goal is to figure out which choices (or "arms") will give you the most rewards. The challenge is that you don't know for sure which choices are the best, so you need to try different ones to learn about their rewards. At the same time, you want to focus on the choices that seem to give higher rewards based on what you've learned so far.
The MAB problem is important because it has practical uses in areas like medical studies, online ads, recommendations, and resource management. It helps us understand how to balance exploring new options and exploiting what we already know to make the best decisions when facing uncertainty.

To solve the MAB problem, there are popular algorithms like the epsilon-greedy algorithm, the UCB (Upper Confidence Bound) algorithm, and Thompson sampling. These algorithms help the agent decide which choices to make based on the information it has and the trade-off between exploring new options and exploiting the ones that seem to be better.
In this repository, you'll find a simple version of each of these three algorithms, which can help you understand and apply them in practice.
