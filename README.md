# solve-BlackJack-problem-with-monte-carlo-prediction-algorithm
Blackjack is a popular card game. in this repository, I've implemented MC prediction algorithm to predict state value function of a selected policy. 
## BlackJack game
![image](https://user-images.githubusercontent.com/74808396/183819119-bc7dabbd-a91f-4f9f-84ce-09f1d7efc483.png)

Blackjack is a popular card game where the goal is to have the sum of cards as close to 21 as possible without exceeding it. The J, K, and Q cards have a points value of 10, and cards from 2 to 10 have values from 2 to 10. The ace card can be either 1 or 11 points; when the latter value is chosen, it is called a usable ace. The player competes against a dealer. At the beginning, both parties are given two random cards, but only one of the dealer's cards is revealed to the player. The player can request additional cards (called hit) or stop receiving any more cards (called stick). After the player sticks, the dealer keeps drawing cards until the sum of cards is greater than or equal to 17. Before the player calls stick, if the sum of their cards exceeds 21 (called going bust), the player loses. Otherwise, if the sum of the dealer's cards exceeds 21, the player wins.
## Monte-Carlo algorithm
Monte-Carlo is an algorithm in the model-free reinforcement learning category. unlike dynamic programming, MC doesn't need a complete model of the environment and learns based on experiences and observed rewards. you can read more about this algorithm in this [medium post](https://medium.com/data-science-in-your-pocket/monte-carlo-for-reinforcement-learning-with-example-1754439dd628)
## environment
for implementing MC algorithm in code we need an environment that simulates a real game for us. we use OpenAi gym ('BlackJack-V1') environment.
this environment takes action and the current state and returns the next state, reward, done (indicates that game ended or not) and information.
- state format:

{the sum of your cards (32 integer numbers) , dealer card (11 integer numbers),usable ace existence (true or false)}
- actions:

stick (stop receiving card): 0
draw (take another card): 1
- game ended if (done = true):

if you select `stick` action or sum of your cards be grather than 21.
## how to run code
- install **numpy** and **gym** libraries.
- run **blackjack** notebook.
- heve fun :wink:
