# F# Mutable Variable Swap Bug

This repository demonstrates a common error in F# related to the behavior of mutable variables when passed to functions. The `swap` function, as initially written, does not swap values in the expected manner due to pass-by-reference semantics. This readme explains the issue and provides a corrected version.

## Bug Description

The `bug.fs` file contains a function intended to swap the values of two mutable variables. However, due to the pass-by-reference nature of mutable variables in F#, the function modifies the original variables directly, leading to unexpected output.

## Solution

The `bugSolution.fs` file provides the corrected implementation. Instead of modifying the input variables directly, the corrected function returns a new tuple containing the swapped values.  This approach respects the immutability principles of F# while achieving the desired swapping effect. 

## How to Run

1. Clone this repository.
2. Open the `bug.fs` and `bugSolution.fs` files in an F# environment (e.g., Visual Studio, Ionide).
3. Compile and run each file to observe the different behaviors.