```haskell
-- Define specialBirthday using pattern matching and include age in default case
specialBirthday :: Int -> String
specialBirthday 1  = "Happy 1st Birthday!"
specialBirthday 18 = "Happy 18th Birthday!"
specialBirthday age = "Happy " ++ show age ++ "th Birthday!"

-- Main function to test specialBirthday
main :: IO ()
main = do
    putStrLn (specialBirthday 1)
    putStrLn (specialBirthday 18)
    putStrLn (specialBirthday 5)
    putStrLn (specialBirthday 30)
```

---

### 🔧 How to Run:

1. Save the code in a file named `SpecialBirthday.hs`
2. Compile it:

   ```bash
   ghc SpecialBirthday.hs
   ```
3. Run the program:

   ```bash
   ./SpecialBirthday
   ```

---

### ✅ Example Output:

```
Happy 1st Birthday!
Happy 18th Birthday!
Happy 5th Birthday!
Happy 30th Birthday!
