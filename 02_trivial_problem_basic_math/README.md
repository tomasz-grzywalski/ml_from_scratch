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

In general functions we will be working with from now on represent solutions to some problems we are trying to solve. 
This particular function depends on four parameters: x1, x2, w1 and w2. X1 and x2 are input variables and y is the estimated solution of our problem (the output). In order for our equation to work properly, we need to find optimal values of "internal" parameters w1 and w2.

We already know how to find best parameters to minimize function value. Let's use that to find optimal values of
w1 and w2.

First we need to define a function that we will be minimizing. This function will represent the error that our
function makes. By minimizing this error function (malso called cost function or loss function), we will make the 
original function solve the task we want it to solve. If we manage to minimize loss to zero, our function will give perfect answers.

Typical loss function looks like this:
```
loss = (y - expected_value)^2
```

We will optimize the cost function using gradient descent algorithm described in previous lesson.
Please note that the cost function depends on four variables: x1, x2, w1, w2 and expected_value. The "x" variables paired with expected_value are examples which we will be using for training our model. During the optimization process the "x" variables and expected_value will be fixed and we will be optimizing "w" variables to minimize cost function. This notation might be a bit confusing because in previous lesson we were finding optimal values of "x" variable, but now "x" represents input which is given by the example and therefore it is fixed and only internal parameters "w" are subject of optimization.

## Problem solution - implementation
