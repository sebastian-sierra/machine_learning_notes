# Week 2

## Gradient Descent for Multiple Variables

The equation takes the same form but this time it goes from 1 to n features.

We update each feature with it's own equation until convergence

## Gradient Descent In Practice

### Feature Scaling

Different ranges between features can cause slow convergence. It's better to scale all the features in order to have them in the same range. Ex: between -1 and 1.

Being close it's enought.

We can do this by mean normalization.

### Debugging gradient descent

Plotting $$J\(\theta\)$$ every hundred iterations, each iteration J\(theta\) should decrease.

Convertion can also be check in this graph.

If J\(theta\) is increasing, it's probally because alpha is to big.

If alpha is too small, convergence may be slow.

To choose alpha:

Start at 0.001 increase by 3x until found.

### Features and Polynomial Regression

Features can be combined into one. Ex: We have x1 and x2 as length and width, so x3 area.

The hypothesis function's curve can be changed into various forms \(quadratic, cubic, square root, etc...\).

For this we can define new features like x2 = x^2

We should be carefull with ranges as they change.

## Normal Equation

It consits of solving the system of equations of all the derivatives with respect to theta-j equal to zero. We end up with the equation:  
theta = \(X'X\)^-1 _ X'_ y

The normal equation has some advantages like:

* No alpha to choose
* No need to iterate

But some clear disadvantages:

* Calculating X'\* X is O\(n^3\)

So gradient descent is better when we have many features \(n\) like 10,000

### X'X singularity

Sometimes the matrix X'X is non-invertible. This is probally due to:

* Redundant features \(They are linearly dependent\) ex: x1 size in feet, x2 size in m.
* We have too many features \(m ≤ n\)



