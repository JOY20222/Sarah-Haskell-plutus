```haskell
-- Define the function
circleCircumference :: (Real a, Floating b) => a -> b
circleCircumference r = 2 * pi * realToFrac r

-- Example usage
main :: IO ()
main = do
    print (circleCircumference (5 :: Int))       -- 31.41592653589793
    print (circleCircumference (7.5 :: Double))  -- 47.12388980384689
    print (circleCircumference (10 :: Integer))  -- 62.83185307179586
```

---

### 💡 Explanation:

* **Type signature**:

  ```haskell
  circleCircumference :: (Real a, Floating b) => a -> b
  ```

  * `a` is any type that belongs to the `Real` class (includes `Int`, `Integer`, `Double`, etc.),
  * `b` is any type in the `Floating` class (`Float`, `Double`),
  * `realToFrac` converts from `Real` type to `Floating` type.

* **Formula used**:
  Circumference = `2 × π × radius`

* This function can accept both integer and floating-point values as input and still return a precise floating-point result.

---

### 🧪 Example Output:

```haskell
31.41592653589793
47.12388980384689
62.83185307179586
