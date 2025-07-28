```haskell
-- Define maxOfThree function using let bindings
maxOfThree :: Int -> Int -> Int -> Int
maxOfThree a b c =
    let maxAB = max a b
        maxABC = max maxAB c
    in maxABC

-- Main function to test maxOfThree
main :: IO ()
main = do
    putStrLn ("maxOfThree 10 20 15 = " ++ show (maxOfThree 10 20 15))
    putStrLn ("maxOfThree 5 25 10 = " ++ show (maxOfThree 5 25 10))
```

---

### 🔧 How to Run:

1. Save the code as `MaxOfThree.hs`.
2. Compile:

   ```bash
   ghc MaxOfThree.hs
   ```
3. Run:

   ```bash
   ./MaxOfThree
   ```

---

### ✅ Expected Output:

```
maxOfThree 10 20 15 = 20
maxOfThree 5 25 10 = 25
