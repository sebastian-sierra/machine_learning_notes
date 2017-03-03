# Week 3

## Classification

Classification problems are like regression problems but the values that y can take are discrete. In the **binary classification problem**, the only values that y can take are either 0 or 1.

Examples:

* Email \(Spam or not\)
* Diseases

## Hypothesis Representation

We just need to adjust our hypothesis function from the linear regression to make values between 0 and 1. This is done by plugging it into the Logistic Function

$$g(z) = {1\over 1+exp^{-z}}$$

$$h(x) = g(\theta^tX)$$

# Decision Boundary

To fit the hypothesis values to our classification we can say:

* $$h(x) ≥ 0.5 \rightarrow y = 1$$

* $$h(x) < 0.5 \rightarrow y = 0$$

g\(z\) ≥ 0.5  when z ≥ 0

So we have

$$\theta^tX ≥ 0 \rightarrow y =1$$

$$\theta^tX < 0 \rightarrow y = 0$$

The **decision boundary** is the line that separates the area where y = 0 from y = 1.

## Logistic Regression Model

The cost function used in linear regression can not be used because the output has mnany local optima so gradient descent is not able to find the global optima.

Insted we used this cost function:

$$J(\theta) = \dfrac{1}{m} \sum_{i=1}^m \mathrm{Cost}(h_\theta(x^{(i)}),y^{(i)})$$

If y is 0, and our hypothesis outputs 0, the cost function would also be 0. But if our hypothesis aproaches 1, then the cost would tend to infinity.

The same reasing works when y = 1.

With this function it can be guaranted that J\(theta\) has only on optima, so it is possible to find it with gradient descent.

## Simplified cost function and gradient descent

The cost function can be written in one simple line:

$$\begin{align*}& J(\theta) = \dfrac{1}{m} \sum_{i=1}^m \mathrm{Cost}(h_\theta(x^{(i)}),y^{(i)}) \newline & \mathrm{Cost}(h_\theta(x),y) = -\log(h_\theta(x)) \; & \text{if y = 1} \newline & \mathrm{Cost}(h_\theta(x),y) = -\log(1-h_\theta(x)) \; & \text{if y = 0}\end{align*}$$

The gradient descent algorithm looks exactly the same that in the linear case. The only thing that has changed is the definition of h\(theta\).

Feature scaling also applies.

## Advanced Optimization

There are more sophisticated and faster algorithms to optimize $$\theta$$. The MATLAB library has its own implementations. In order to use them we just need to provide a function that takes some input $$\theta$$  and produces as output the cost function and the partial derivatives:

  
p.p1 {margin: 0.0px 0.0px 0.0px 0.0px; font: 13.0px Courier; -webkit-text-stroke: \#000000}  
span.s1 {font-kerning: none}  
td.td1 {width: 733.3px; margin: 0.5px 0.5px 0.5px 0.5px; padding: 1.0px 1.0px 1.0px 1.0px}  


| \begin{align\*} & J\(\theta\) \newline & \dfrac{\partial}{\partial \theta\_j}J\(\theta\)\end{align\*} |
| :--- |




