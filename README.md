# AI for management: balance between exploration and exploitation for decision making

# Problem statement

Case 1: As a successful trader, you have additional funds to invest and must decide whether to stick with your proven strategy or explore new strategies. The crucial consideration is how to ensure that a new strategy has the potential to generate higher gains compared to your existing approach. You must determine whether it is worth the effort to incorporate a new strategy or if it is more advantageous to continue with your familiar and well-performing strategy, even though there may be other strategies that perform better.


Case 2: Imagine we have a website and we want to find out which advertisement banner is the most popular among our users. We have five different banners to choose from. The challenge is to figure out which one is liked the best. When a user clicks on a banner, you assign a reward of +1, and if they don't click, the reward is 0. The goal is to find the banner that gets the highest number of clicks or rewards.

# For the case 2, Why not just sum up the rewards?

While summing up the rewards of each banner might seem like a simple approach to determine the best one, it may not always provide accurate results. Here's why:

1.	Lack of exploration: Summing up rewards does not account for exploration. If you solely rely on the accumulated rewards, you might end up favoring banners that have received a few high rewards by chance, while ignoring other banners that could potentially perform better in the long run. Exploration is crucial to discover and exploit better options.
2.	Limited sample size: The sum of rewards approach does not consider the sample size or the number of times each banner has been shown. It treats all rewards equally, regardless of the number of trials. Banners with a smaller sample size may have higher variance in their estimated performance, leading to unreliable conclusions.
4.	Ignoring uncertainty: Summing rewards overlooks the uncertainty associated with each banner's performance. By considering only the rewards, you don't account for the confidence or uncertainty in your estimations. Some banners might have higher rewards, but they may also have a wider confidence interval, indicating less certainty in their actual performance.
6.	Exploitation-only strategy: Summing rewards is purely an exploitation strategy that focuses on maximizing the immediate rewards without considering the potential benefits of exploring other banners. This can lead to suboptimal decisions if there are better options that have not been thoroughly explored.

To make more informed decisions, it is essential to strike a balance between exploration and exploitation. 

# What is "balance between exploration and exploitation"?

The balance between exploration and exploitation refers to finding the optimal trade-off between trying out new options (exploration) and exploiting the current best-known option (exploitation) in a decision-making process. In various problem domains, including reinforcement learning, this balance is crucial for achieving optimal results.

Exploration involves trying out different actions or options to gather more information about their potential rewards or outcomes. It is a process of learning and discovering new possibilities. By exploring, you aim to uncover unknown or potentially better options that can lead to higher rewards in the long run. However, exploration may involve taking risks and initially sacrificing immediate rewards.

Exploitation, on the other hand, involves leveraging the knowledge or experience gained so far to exploit the current best-known option. It focuses on maximizing the immediate rewards based on the available information. Exploitation aims to make the most of what is already known and exploit the option that has shown to be the most promising. However, exploitation may lead to suboptimal outcomes if there are better, unexplored options.

Achieving a balance between exploration and exploitation is essential because:

1.	Exploration is necessary for learning: By exploring new options, you can gather more information about their rewards or outcomes, allowing you to refine your understanding of the problem and potentially discover better solutions.
2.	Exploitation maximizes immediate rewards: Exploiting the current best-known option allows you to maximize immediate rewards based on the available knowledge. It helps you make the most of what you already know.
4.	Overemphasis on exploration or exploitation can lead to suboptimal outcomes: If you solely focus on exploration, you may spend too much time trying out new options and not enough time exploiting the known best option. Conversely, if you only exploit without exploring, you might miss out on potentially better options.
6.	Finding the right balance between exploration and exploitation is often a challenge. 

# What is the best way to solve the problem (finding the best banner)?

we can use one of MAB algorithms to solve the problem. 

In the MAB framework, each banner is like an arm of a slot machine. When a user clicks on a banner, you assign a reward of +1, and if they don't click, the reward is 0. The goal is to find the banner that gets the highest number of clicks or rewards.
By incorporating exploration, these MAB  methods allow you to gather more data, learn about the performance of different banners, and potentially discover better options that can lead to higher rewards in the long term.

# Reinforcement Learning: Multi Armed Bandit (MAB) Problem
The multi-armed bandit (MAB) problem is like a game where you have to make choices to win the most rewards. It's called "multi-armed bandit" because it's similar to a gambler in a casino with many slot machines (the "armed bandits") and needs to decide which ones to play to win the most money over time.

In the MAB problem, the goal is to figure out which choices (or "arms") will give you the most rewards. The challenge is that you don't know for sure which choices are the best, so you need to try different ones to learn about their rewards. At the same time, you want to focus on the choices that seem to give higher rewards based on what you've learned so far.
The MAB problem is important because it has practical uses in areas like medical studies, online ads, recommendations, and resource management. It helps us understand how to balance exploring new options and exploiting what we already know to make the best decisions when facing uncertainty.

To solve the MAB problem, there are popular algorithms like the epsilon-greedy algorithm, Softmax Exploration, the UCB (Upper Confidence Bound) algorithm, and Thompson sampling. These algorithms help the agent decide which choices to make based on the information it has and the trade-off between exploring new options and exploiting the ones that seem to be better.
In this repository, you'll find a simple version of each of these four algorithms, which can help you understand and apply them in practice. You'll also find some pratical study cases.
