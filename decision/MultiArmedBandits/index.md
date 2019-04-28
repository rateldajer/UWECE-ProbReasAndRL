---
layout: post
title: Multi-Armed Bandits
---
<!-- TODO  MAB intro text, context --> 
<!-- TODO  MAB flow: does this follow ID or MDP? --> 
## n-Armed Bandits
This is the simplest domain where the exploitation-exploration tradeoff occurs. 
There is simply one state and a $n$ actions which can be taken. Each action has
an independent reward function, which is a distribution. The agent maintains an
estimate of the value of each action and wants to maximize its reward over time
given its uncertainty. The actions don't change the world, you are just trying
to determine the reward model for a single state of a frozen MDP. That's why
they use bandits, since the state is irrelevant, each pull is independent of
the last pull.
The best strategy is to mix some exploration, choosing actions which aren't the
best according to your estimates, in order to increase your certainty and then
to exploit your estiamte of the best action the rest of the time.

More and more complexity can be added by making the rewards drift over time,
causing the bandits to be correlated together, to alter the reward based on as
sequence of actions and of course by adding states to the bandits so that it
becomes a normal MDP again.{% include sidenote.html id="refSutton" note="See Sutton Reinforcement Learning book chapter 2." %}:


## Three Fundamental Pieces of RL in Term of Bandits

- **Reward Model Based on Actions** 
  - Given one bank of n bandits, you need to learn the optimal policy for pulling arms. ie. the reward distirubtion over actions.
  - **(MDP: 1 state, n actions)**
- **Different Reward Model per State** 
  - Multiple sets/banks/rows of bandits.  
  - Each bank has its own reward model for the arms, you don't know any of them.
  - But if you are given a signal about which bank you are at, ie. which state you are in, then you can learn a policy.
  - **(MDP: m states and n actions for m banks of n-armed bandits and a random transition model)**.
- **Actions Affect State Transition** 
  - Finally, if actions influence which state you end up in next then it is a full RL problem. 
  - This is like each arm pull influencing which bank of bandits you will go to next.
  - **(MDP: m states and n actions for m banks of n-armed bandits and transition model $$T(a'\vert a,s)$$.)**



## Section
text text 
text text 
text text 
text text 
text text 
text text 
text text 

- Some text with a margin note(no footnote).{% include marginfigure.html id="bn" url="assets/img/3node-bayesnets.png" description="Bayesian networks over three variables, encoding different types of dependencies: cascade (a,b), common parent (c), and v-structure (d)." %}*Common parent.* If $$G$$ is of the form $$A \leftarrow B \rightarrow C$$, and $$B$$ is observed, then $$A \perp C \mid B$$. However, if $$B$$ is unobserved, then $$A \not\perp C$$. Intuitively this stems from the fact that $$B$$ contains all the information that determines the outcomes of $$A$$ and $$C$$; once it is observed, there is nothing else that affects these variables' outcomes.
- Some text with a side note (footnote included).{% include sidenote.html id="note_imap" note="We will not formally prove this, but the intuition is that if $$X,Y$$ and $$Y,Z$$ are mutually dependent, so are $$X,Z$$. Thus we can look at adjacent nodes and propagate dependencies according to the local dependency structures outlined above." %}:
- Note that printing side notes requires using certain browsers to get the side images, safari seems to work, others?


Or in the main collumn

{% include maincolumn_img.html src='assets/img/3node-bayesnets.png' caption='Bayesian networks over three variables' %}
<br/>

|[Index](../../) | [Previous](../../preliminaries/applications) | [Next](../undirected)|
