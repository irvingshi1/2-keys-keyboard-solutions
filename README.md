# 2 Keys Keyboard

The 2 Keys Keyboard problem is a problem where you start off with a string with 1 A ("A") and the goal is to reach n As (e.g. "AAAAAAAAAAA").
There is an empty clipboard. You can either copy the current string to the clipboard, or paste the contents of the clipboard to the current string.

## Solution 1: Brute Force

It is suboptimal to copy the current string to the clipboard twice in a row, since it doesn't change the contents of the clipboard at all. So when
copying to the clipboard, the next step is to paste to the current string. You could try every solution, but that would be long.

## Solution 2: Recursion

See: recursion.txt

Every integer that's at least 2 is a product of prime factors. In the case of n = 1, we have already gotten "A", since that's the initial state.
For the case of a prime number, the solution is n + 1, because you first need to copy to the clipboard once, then paste to the
current string n times, giving you n + 1. In the case of a composite number, divide n by a prime factor and get the answer for the quotient.

## Solution 3: Iteration

See: iteration.txt

Another solution is realizing that the solution for any n is the sum of its prime factors. Simply looping through the prime factors without
recursion reduces the auxiliary space needed.
