#Simple algorithms

##Approximate Solutions

Define a good enough solution. Start with a guess and increment by some small value, at which point we have to define what it means whether or not we are close enough.

Steps can be any small number, but if it's too small, we can take an excessive amount of time. If it's too large, we might skip the answer. In other words, we need to find a more efficient way of solving the problem.

##Bisection Search

One example is that we know that the square root of x lies between 1 and x.

Rather than exhaustively trying things starting at 1, what if we instead pick a number in the middle of this range?

If not close enough, we can determine if guess is too big or too small, and then search halfway between whichever side we prefer.

This type of solution would work on any sort of problem that has an "ordering" property.

##Newton-Raphson
General approximation algorithm to find roots of a polynomial

Want to find r such that p(r) = 0

For example, to find the square root of 24, find the root of p(x) = x^2 - 24

Newton showed that if g is an approximation to the root, then g - p(g)/p'(g).
