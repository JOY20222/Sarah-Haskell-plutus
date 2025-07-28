```haskell
-- Define dayType using pattern matching
dayType :: String -> String
dayType "Saturday" = "It's a weekend!"
dayType "Sunday"   = "It's a weekend!"
dayType "Monday"   = "It's a weekday."
dayType "Tuesday"  = "It's a weekday."
dayType "Wednesday"= "It's a weekday."
dayType "Thursday" = "It's a weekday."
dayType "Friday"   = "It's a weekday."
dayType _          = "Invalid day"

-- Main function to test dayType
main :: IO ()
main = do
    putStrLn ("dayType \"Saturday\" = " ++ dayType "Saturday")
    putStrLn ("dayType \"Wednesday\" = " ++ dayType "Wednesday")
    putStrLn ("dayType \"Funday\" = " ++ dayType "Funday")
```

---

### 🔧 How to Run:

1. Save the code in a file named `DayType.hs`
2. Compile it using GHC:

   ```bash
   ghc DayType.hs
   ```
3. Run the program:

   ```bash
   ./DayType
   ```

---

### ✅ Expected Output:

```
dayType "Saturday" = It's a weekend!
dayType "Wednesday" = It's a weekday.
dayType "Funday" = Invalid day
