```haskell
-- Define applyThreeTimes: applies a function three times to an integer
applyThreeTimes :: (Int -> Int) -> Int -> Int
applyThreeTimes f x = f (f (f x))

-- Main function to test applyThreeTimes
main :: IO ()
main = do
    print $ applyThreeTimes (+1) 5        -- Expected: 8
    print $ applyThreeTimes (*2) 1        -- Expected: 8 (1 → 2 → 4 → 8)
    print $ applyThreeTimes (`div` 2) 64  -- Expected: 8 (64 → 32 → 16 → 8)
```

---

### 🔧 How to Run

1. Save the code as `ApplyThreeTimes.hs`
2. Compile it:

   ```bash
   ghc ApplyThreeTimes.hs
   ```
3. Run the program:

   ```bash
   ./ApplyThreeTimes
   ```

---

### ✅ Output

```
8
8
8
```

---

This demonstrates **higher-order functions** in Haskell—`applyThreeTimes` takes a function and an integer and applies the function three times to the value.
