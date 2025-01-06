# Haskell Type Error: IO () not an instance of Show

This repository demonstrates a common type error in Haskell: attempting to use a value of type `IO ()` with a function that requires an instance of the `Show` typeclass. The `IO ()` type represents a side effect (an action that interacts with the outside world) and does not have a `Show` instance. Therefore, the compiler will report an error.

The `bug.hs` file contains the erroneous code, while `bugSolution.hs` offers a correction.

**Error:**
The code attempts to apply `mysteryFunction` to a value of type `IO ()`, which causes a type error because `IO ()` doesn't implement the `Show` typeclass.

**Solution:**
The solution involves refactoring the code to avoid trying to display the `IO ()` result directly.  Instead, the side-effects are managed within the `IO` monad.