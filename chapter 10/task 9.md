```haskell
-- Define the MinMax type class
class MinMax a where
    minValue :: a
    maxValue :: a

-- Provide an instance of MinMax for Int
instance MinMax Int where
    minValue = minBound
    maxValue = maxBound

-- Example usage
main :: IO ()
main = do
    putStrLn $ "Minimum Int value: " ++ show (minValue :: Int)
    putStrLn $ "Maximum Int value: " ++ show (maxValue :: Int)
```

---

### 🧠 Explanation:

* **`MinMax`** is a custom type class with two methods: `minValue` and `maxValue`.
* For `Int`, we use the predefined `minBound` and `maxBound`, since `Int` is already an instance of `Bounded`.
* The `:: Int` annotation in `main` ensures the compiler knows which instance of `MinMax` we're referring to.

---

### 🧪 Sample Output:

```
Minimum Int value: -9223372036854775808
Maximum Int value: 9223372036854775807
```

> Output may vary depending on your machine's architecture (32-bit vs 64-bit), but the logic will work as expected.
