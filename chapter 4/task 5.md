This example assumes the purpose of `specialBirthday` is to print a special message if the person's age is 1 or 18, and a generic message otherwise.

---

### ✅ Code: `SpecialBirthday.hs`

```haskell
-- Define specialBirthday using pattern matching
specialBirthday :: Int -> String
specialBirthday 1  = "Happy 1st Birthday!"
specialBirthday 18 = "Happy 18th Birthday!"
specialBirthday age = "Happy " ++ show age ++ "th Birthday!"

-- Main function to test specialBirthday
main :: IO ()
main = do
    putStrLn (specialBirthday 1)
    putStrLn (specialBirthday 18)
    putStrLn (specialBirthday 25)
```

---

### 🔧 How to Run:

1. Save the file as `SpecialBirthday.hs`
2. Compile:

   ```bash
   ghc SpecialBirthday.hs
   ```
3. Run:

   ```bash
   ./SpecialBirthday
   ```

---

### ✅ Expected Output:

```
Happy 1st Birthday!
Happy 18th Birthday!
Happy 25th Birthday!
