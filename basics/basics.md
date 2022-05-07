# Basics of ML

The main difference between ML and traditional modeling 
lays in the key concept of ML. When you build traditional model, 
you rely on your own principles of understanding the domain.
When you build machine learning model, you rely on its ability to understand the domain.

# ML areas
1. [**Supervised learning**](#supervised-learning)  
The model is trained to find answers for 
objects with already known answers  
**Examples:** Classification, Regression


2. **Unsupervised learning**  
The model is trained to discover patterns 
or undetected information about data  
**Examples:** Clustering, PCA


3. **Reinforcement learning**  
The model is trained as agent that takes actions 
in the environment to maximize reward  
**Examples:** Q-learning




## Supervised learning
Let <img src="https://render.githubusercontent.com/render/math?math={\color{green}\X^d}"> be object space, <img src="https://render.githubusercontent.com/render/math?math={\color{green}\Y}"> - answers space; 
<img src="https://render.githubusercontent.com/render/math?math={\color{green} (x_i, y_i)^{l}_{i=1}}"> is training set, where 
<img src="https://render.githubusercontent.com/render/math?math={\color{green} x_i = (x^1, ..., x^d) }">

Let's denote a(x) as model and Q(a, x) as function of error on training set

The training itself is an optimization problem 

<img src="https://render.githubusercontent.com/render/math?math={\color{red}a(x) = argmin_{a \in A}(Q(a,x))}">, 
where A is a set of possible models

Possible tasks:
### 1. **Regression**
The task is to predict _(usually)_ the real number 


### 2. **Classification**  


Note: *also **Ranking** belongs to supervised learning, but I'm not sure


## Unsupervised learning
TBD
## Reinforcement learning
TBD

# Quality and error function
**Loss** (error) function is the function to minimize during training.

**Metric** (quality) function is the function used to check is model good enough.

The key difference between these function
