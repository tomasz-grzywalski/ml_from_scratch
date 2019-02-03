# Short theoretical introduction

## Finding minimum of a function using gradient descent

This algorithm is at the core of all neural network training processes, so it is very important to understand it before
we move forward.

Let's say we have a function y = f(x) and for
that function we want to find value of parameter "x" for which the function has minimal value.

The algorithm looks like this:

![alt text](finding_minimum.png "gradient descent")

1. We start from random point (1).
2. In this point we check how the value of the function changes in nearest neighborhood of current point, this is in 
fact the definition of a derivative (marked red on the chart). The sign of the derivative tels us in which direction 
we should go to find the minimum of our function. The absolute value of the derivative (slope of the read line) tells us
how fast the functions changes in near proximity of our selected point and therefore determined by how much do we need
to move.
3. The derivative tells us we should move left and since the slope is quite steep, we take a large jump to point (2).
More technically speaking, we subtracted portion of the derivative from our current value of "x" (the derivative had a
positive value indicating the function value increases with increased value of "x", but we want to find the minimum so
we are moving in the other direction)
4. In point (2) we again calculate the derivative and find out that we overdid and this time we need to move right.
Because slope is less steep, we move by smaller value than we did last time. Technically: derivative is now a negative
number so by subtracting it from our current "x" we will actually increase value of "x". This way we have moved to point
(3)
5. We repeat this procedure until our steps become very small. We arrived at point (4) where derivative is near or 
equal to zero. We have found the value of "x" for which the function has minimal value.