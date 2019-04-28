---
layout: post
title: Monte Carlo Tree Search 
---

Monte Carlo Tree Search (MCTS) 
{% include sidenote.html id="mctsrefs" note="Kocsis2006,browne2012survey" %}
is another type of RL which can deal with larger state spaces through the use of forward simulation and build upper or lower confidence bounds on the certainty around actions taken. 
The widely discussed AlphaGo competition in 2016 year combined MCTS algorithms with deep learning to learn compact state and value representations {% include sidenote.html note="ref:Silver2016" %}.

Monte Carlo Tree Search(MCTS): This is a heuristic search algorithm most commonly used in game playing. Here a search tree is continuously expanded based on the analysis of the most promising moves.
These are a class of algorithms that perform approximate, but confidence-bounded, RL by performing short roll-outs of the current policy in order to obtain enough statistical information about a state to keep it or discard it as belonging to the optimal path. {% include sidenote.html note="A good survey is provided in ref:browne2012survey" %}.

A related and important research area now is obtaining Bayes-optimal bounds or other statistical guarantees on the quality of the resulting policies {% include sidenote.html note="ref:Guez2013f" %}{% include sidenote.html note="ref:Asmuth2011" %}. 

Other research in this area has sought to provided improved sample complexity for MDP algorithms with PAC guarantees{% include sidenote.html note="ref:2013-aaai" %} {% include sidenote.html note="ref:2015-jmlr" %}. 



## Section
text text 
text text 
text text 
text text 
text text 
text text 
text text 

- {% include marginfigure.html id="bn" url="assets/img/3node-bayesnets.png" description="Bayesian networks over three variables, encoding different types of dependencies: cascade (a,b), common parent (c), and v-structure (d)." %}*Common parent.* If $$G$$ is of the form $$A \leftarrow B \rightarrow C$$, and $$B$$ is observed, then $$A \perp C \mid B$$. However, if $$B$$ is unobserved, then $$A \not\perp C$$. Intuitively this stems from the fact that $$B$$ contains all the information that determines the outcomes of $$A$$ and $$C$$; once it is observed, there is nothing else that affects these variables' outcomes.

Or in the main collumn

{% include maincolumn_img.html src='assets/img/3node-bayesnets.png' caption='Bayesian networks over three variables' %}
<br/>

|[Index](../../) | [Previous](../../preliminaries/applications) | [Next](../undirected)|
