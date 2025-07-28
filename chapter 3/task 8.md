```haskell
-- Define bmiCategory function
bmiCategory :: Float -> Float -> String
bmiCategory weight height
    | bmi < 18.5 = "Underweight"
    | bmi < 25   = "Normal"
    | bmi < 30   = "Overweight"
    | otherwise  = "Obese"
  where
    bmi = weight / (height ^ 2)

-- Main function to test bmiCategory
main :: IO ()
main = do
    putStrLn ("bmiCategory 70 1.75 = " ++ bmiCategory 70 1.75)
    putStrLn ("bmiCategory 90 1.8 = " ++ bmiCategory 90 1.8)
```

---

### 🔧 How to Run:

1. Save as `BMICategory.hs`.
2. Compile:

   ```bash
   ghc BMICategory.hs
   ```
3. Run:

   ```bash
   ./BMICategory
   ```

---

### ✅ Expected Output:

```
bmiCategory 70 1.75 = Normal
bmiCategory 90 1.8 = Overweight
