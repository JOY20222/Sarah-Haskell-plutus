```haskell
-- Define the function with if-then-else
checkNumber :: Int -> String
checkNumber n =
    if n > 0 then "Positive"
    else if n < 0 then "Negative"
    else "Zero"

-- Main function to test checkNumber
main :: IO ()
main = do
    putStrLn ("checkNumber 5 = " ++ checkNumber 5)
    putStrLn ("checkNumber (-3) = " ++ checkNumber (-3))
    putStrLn ("checkNumber 0 = " ++ checkNumber 0)
```

---

### 🔧 How to Run:

1. Save the file as `CheckNumber.hs`
2. Compile it with:

   ```bash
   ghc CheckNumber.hs
   ```
3. Run the program:

   ```bash
   ./CheckNumber
   ```

---

### ✅ Expected Output:

```
checkNumber 5 = Positive
checkNumber (-3) = Negative
checkNumber 0 = Zero

