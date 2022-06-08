# Voting-Rule

# Background

In this assignment you will design and implement several voting rules. In a voting setting, we have a set of  agents and a set of  alternatives. Every agent has a preference ordering  where  means that the agent prefers alternative  to alternative . A preference profile is a set of  preference orderings, one for every agent.

For example, if we have a voting setting with 4 agents and 4 alternatives, one possible preference profile could be the following:

![image](https://user-images.githubusercontent.com/99655823/172713804-e545ced8-130f-49f7-9cba-fa137f2b3656.png)

A voting rule is a function that takes as input the preferences of a set of agents and outputs a winning alternative.

Dictatorship:
An agent is selected, and the winner is the alternative that this agent ranks first.

Plurality:
The winner is the alternative that appears the most times in the first position of the agents' preference orderings. In the case of a tie, use a tie-breaking rule to select a single winner.

Veto:
Every agent assigns 0 points to the alternative that they rank in the last place of their preference orderings, and 1 point to every other alternative. The winner is the alternative with the most number of points. In the case of a tie, use a tie-breaking rule to select a single winner.

Borda:
Every agent assigns a score of 0 to the their least-preferred alternative (the one at the bottom of the preference ranking), a score of 1 to the second least-preferred alternative, ... , and a score of m-1 to their favourite alternative. In other words, the alternative ranked at position  receives a score of m-j. The winner is the alternative with the highest score. In the case of a tie, use a tie-breaking rule to select a single winner.

Harmonic:
Every agent assigns a score of 1/m to the their least-preferred alternative (the one at the bottom of the preference ranking), a score of 1/(m-1) to the second least-preferred alternative, ... , and a score of 1 to their favourite alternative. In other words, the alternative ranked at position j receives a score of 1/j. The winner is the alternative with the highest score. In the case of a tie, use a tie-breaking rule to select a single winner.

Single Transferable Vote (STV):
The voting rule works in rounds. In each round, the alternatives that appear the least frequently in the first position of agents' rankings are removed, and the process is repeated. When the final set of alternatives is removed (one or possibly more), then this last set is the set of possible winners. If there are more than one, a tie-breaking rule is used to select a single winner.
