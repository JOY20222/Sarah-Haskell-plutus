```haskell
-- Define isLeapYear using if-then-else
isLeapYear :: Int -> Bool
isLeapYear year =
    if year `mod` 400 == 0 then True
    else if year `mod` 100 == 0 then False
    else if year `mod` 4 == 0 then True
    else False

-- Main function to test isLeapYear
main :: IO ()
main = do
    putStrLn ("isLeapYear 2000 = " ++ show (isLeapYear 2000))  -- True
    putStrLn ("isLeapYear 1900 = " ++ show (isLeapYear 1900))  -- False
    putStrLn ("isLeapYear 2024 = " ++ show (isLeapYear 2024))  -- True
```

---

### 🔧 How to Run:

1. Save as `LeapYear.hs`
2. Compile:

   ```bash
   ghc LeapYear.hs
   ```
3. Run:

   ```bash
   ./LeapYear
   ```

---

### ✅ Expected Output:

```
isLeapYear 2000 = True
isLeapYear 1900 = False
isLeapYear 2024 = True
```

---

### 🧠 Leap Year Rules Recap:

* Divisible by **400** → ✅ Leap year
* Divisible by **100** (but not 400) → ❌ Not a leap year
* Divisible by **4** → ✅ Leap year
* Otherwise → ❌ Not a leap year
