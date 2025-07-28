### ✅ Code: `BiggerThan10.hs`

```haskell
-- Define biggerThan10 using a lambda function
biggerThan10 :: Int -> Bool
biggerThan10 = \x -> x > 10

-- Main function to test the behavior
main :: IO ()
main = do
    print $ biggerThan10 5    -- False
    print $ biggerThan10 10   -- False
    print $ biggerThan10 15   -- True
```

---

### 🔧 How to Run

1. Save the code in a file named `BiggerThan10.hs`
2. Compile it using GHC:

   ```bash
   ghc BiggerThan10.hs
   ```
3. Run it:

   ```bash
   ./BiggerThan10
   ```

---

### ✅ Output

```
False
False
True
```

---

### 🧠 Explanation

* **Original version**:

  ```haskell
  biggerThan10 x = x > 10
  ```
* **Lambda version**:

  ```haskell
  biggerThan10 = \x -> x > 10
  ```

You're assigning the function `\x -> x > 10` (a lambda expression) to the name `biggerThan10`.
This expression takes a value `x` and returns `True` if `x > 10`, otherwise `False`.

It's functionally identical to the original, but uses a **lambda** to define the function **anonymously**.
