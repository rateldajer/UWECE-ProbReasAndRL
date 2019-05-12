---
layout: post
title: Decision Making
---

Now we start the second part of the course which focusses on making *decisions* given complete or partial and uncertain knowledge about the world. 

<!-- todo  use the dmuu and rl book chapter 3 as a basis --> 


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

