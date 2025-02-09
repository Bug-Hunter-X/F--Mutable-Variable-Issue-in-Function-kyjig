# F# Mutable Variable Issue in Function

This example demonstrates a common mistake when using mutable variables in F# functions.  Mutable variables are updated outside of a function, but changes are not reflected within the function if the function doesn't explicitly use the new values.

## Bug

The `add` function does not use the updated values of `x` and `y`, thus, it always outputs the sum of the initial values of `x` and `y`.

## Solution

The solution involves passing the updated values to the `add` function as arguments.