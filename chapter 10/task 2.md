```haskell
-- Define the Summable type class
class Summable a where
    sumUp :: [a] -> a

-- Provide an instance for Int
instance Summable Int where
    sumUp = sum

-- Example usage in main
main :: IO ()
main = do
    let numbers = [1, 2, 3, 4, 5] :: [Int]
    print (sumUp numbers)
```

### Explanation:

* **`class Summable a where`** defines a type class named `Summable` with a single function `sumUp`.
* **`instance Summable Int where`** provides an instance of the class for `Int`, using Haskell’s built-in `sum` function.
* In the `main` function, we create a list of `Int`s and use `sumUp` to compute the total, then print the result.

### Output:

```
15
