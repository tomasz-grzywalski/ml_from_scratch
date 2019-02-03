# Solving trivial problem using basic math

## Problem statement

The problem is finding parameters w1 and w2 of following equation:
```
y = x1 * w1 + x2 * w2
```

That will fit following data:
```
x1 = 1.0
x2 = 0.5
y = 20
```

Weights are initialized as:
```
w1 = 0.2
w2 = 0.7
```

## Problem solution - theory

In general the functions we will be working from now on represents solution to some problem we are trying to solve. 
This particular function depends on four parameters: x1,
x2, w1 and w2. x1 and x2 are input variables and y is the estimated solution of our problem (the output). In order for
our equation to work properly, we need to find optimal values of "internal" parameters w1 and w2.

We already know how to find parameters to minimize function value. Let's use that to find optimal values of
w1 and w2.

First we need to define a function that we will be minimizing. This function will represent the error that our
function makes. By minimizing this function (minimizing error), we will make the original function solve the task we
want it to solve.

Typical loss (aka cost) function looks like this:
```
loss = (predicted_value - expected_value)^2
```
If we manage to minimize loss to zero, our function will give perfect answers.

We will optimize the cost function using gradient descent algorithm described in previous lesson.
Our algorithm has just one parameters:   