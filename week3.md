# Week 3

## Classification

Classification problems are like regression problems but the values that y can take are discrete. In the **binary classification problem**, the only values that y can take are either 0 or 1.

Examples:
    * Email (Spam or not)
    * Diseases

## Hypothesis Representation

We just need to adjust our hypothesis function from the linear regression to make values between 0 and 1. This is done by plugging it into the Logistic Function
g(z) = 1/(1+e^-z)
h(x) = g(theta'*X)

# Decision Boundary

To fit the hypothesis values to our classification we can say:
* h(x) ≥ 0.5 -> y = 1
* h(x) < 0.5 -> y = 0

g(z) ≥ 0.5  when z ≥ 0

So we have 

theta'*x ≥ 0 -> y = 1
theta'*x < 0 -> y = 0

The **decision boundary** is the line that separates the area where y = 0 from y = 1.

## Logistic Regression Model

The cost function used in linear regression can not be used because the output has mnany local optima so gradient descent is not able to find the global optima.

Insted we used this cost function:

![Cost function](week3_images/cost_function.png)

If y is 0, and our hypothesis outputs 0, the cost function would also be 0. But if our hypothesis aproaches 1, then the cost would tend to infinity.

The same reasing works when y = 1.

With this function it can be guaranted that J(theta) has only on optima, so it is possible to find it with gradient descent.

## Simplified cost function and gradient descent

The cost function can be written in one simple line:

![Simplified Cost Function](week3_images/simplified_cost_fun.png)

The gradient descent algorithm looks exactly the same that in the linear case. The only thing that has changed is the definition of h(theta).

Feature scaling also applies.
