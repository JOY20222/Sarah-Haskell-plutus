```haskell
-- Define the grade function using guards
grade :: Int -> String
grade score
    | score >= 90 = "A"
    | score >= 80 = "B"
    | score >= 70 = "C"
    | score >= 60 = "D"
    | otherwise   = "F"

-- Main function to test the grade function
main :: IO ()
main = do
    putStrLn ("grade 95 = " ++ grade 95)
    putStrLn ("grade 72 = " ++ grade 72)
    putStrLn ("grade 50 = " ++ grade 50)
```

---

### 🔧 How to Run:

1. Save the file as `Grading.hs`
2. Compile using GHC:

   ```bash
   ghc Grading.hs
   ```
3. Run the compiled program:

   ```bash
   ./Grading
   ```

---

### ✅ Expected Output:

```
grade 95 = A
grade 72 = C
grade 50 = F
