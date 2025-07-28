```haskell
-- Define season function using guards
season :: Int -> String
season month
    | month == 12 || month == 1 || month == 2 = "Winter"
    | month == 3  || month == 4 || month == 5 = "Spring"
    | month == 6  || month == 7 || month == 8 = "Summer"
    | month == 9  || month == 10 || month == 11 = "Autumn"
    | otherwise = "Invalid month"

-- Main function to test season
main :: IO ()
main = do
    putStrLn ("season 3 = " ++ season 3)
    putStrLn ("season 7 = " ++ season 7)
    putStrLn ("season 11 = " ++ season 11)
```

---

### 🔧 How to Run:

1. Save the code as `Season.hs`.
2. Compile with:

   ```bash
   ghc Season.hs
   ```
3. Run:

   ```bash
   ./Season
   ```

---

### ✅ Expected Output:

```
season 3 = Spring
season 7 = Summer
season 11 = Autumn

