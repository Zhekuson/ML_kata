
# Linear regression  
  
### Definition  
  
The simple linear model    
let $1..d$ be features of the object (real numbers)    
**Linear model** is $a(x) = w_0 + w_1 * x_1 + ... + w_d * x_d$  
  
### Geometry  
It's a **line** in 2D case, **plane** in 3D case, or a **hyperplane** in many dims cases   
  
### Matrix form  
  
$X  w = y$  
  
### Pros and cons  
**Pros**: Easy, simple, interpretable.    
**Cons**: May be too simple, works well in linear cases (or in cases reduced to linear cases).  
  
## Other useful things  
### Regularization  
  
### Analytical solution (optima)  
  
In matrix form the best solution (for MSE) is:    
$w = (X^T X)^{-1} X^T y = X^+ y$  
How to get this:
Lets write out our MSE Loss in matrix form: 
$L(w) = (Xw-y)^T (Xw-y)$ will be a vector of errors (for each object).  
Let's take the derivative (with respect to $w$):  
$$ \frac{\partial L}{\partial w} =  \frac{\partial((w^TX^T -y^T)(Xw-y))}{\partial w} = \frac{\partial (w^T X^TXw - 2 y^TXw + y^Ty)}{\partial w}  =  \frac{\partial(\langle Xw, Xw\rangle)}{\partial w} - 2X^Ty = 2 X^T X \frac{\langle \partial w, w \rangle}{\partial w} - 2X^Ty = \underbrace{2 X^T X w - 2X^Ty}_{result}$$  
Because the MSE function is *convex*, for us would be enough to find the extremum place and that will be the minimum.  
$$\frac{\partial L}{\partial w} =2 X^T X w - 2y^TX = 0  
\Rightarrow\\ w = (X^TX)^{-1}X^Ty$$




  
## Questions from interviews  
   
1) **Q:** Why don't we use the best solution for MSE, if it's calculated?    
**A:** There are several reasons. Inverse matrix is not cheap to calculate, and sometimes just cannot exist (dependencies between features cause linear dependence).   
2) **Q:** How can we use linear regression for another types of dependencies?  And why not?    
**A:** That causes significant increase in dimensions, if we take exponents or square roots of the features (or something different). So it's possible in case of other dependencies, but there are more appropriate models for that.    
3) **Q:** Get the optima analytic solution in matrix form?    
**A:** See the solution [**here**](#analytical-solution-optima)