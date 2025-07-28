```haskell
-- Define the function using partial application
multiplyByFive :: Int -> Int
multiplyByFive = (*) 5

-- Main function to test multiplyByFive
main :: IO ()
main = do
    print $ multiplyByFive 2    -- 10
    print $ multiplyByFive 10   -- 50
    print $ multiplyByFive (-3) -- -15
```

---

### 🔧 How to Run

1. Save as `MultiplyByFive.hs`
2. Compile it with:

   ```bash
   ghc MultiplyByFive.hs
   ```
3. Run:

   ```bash
   ./MultiplyByFive
   ```

---

### ✅ Output

```
10
50
-15
```

---

### 🧠 Explanation

* `(*)` is the infix multiplication operator.
* `(*) 5` is a **partially applied function**: it returns a new function that takes one argument and multiplies it by 5.
* So `multiplyByFive x = 5 * x`, but written in a shorter and more functional way.
