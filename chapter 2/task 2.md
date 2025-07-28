```haskell
-- Function to add two Int values
add :: Int -> Int -> Int
add x y = x + y

-- Function to check if an Int is even
isEven :: Int -> Bool
isEven n = n `mod` 2 == 0

-- Function to concatenate two Strings
concatStrings :: String -> String -> String
concatStrings str1 str2 = str1 ++ str2

-- Main function to test all three
main :: IO ()
main = do
    -- Test add
    let sumResult = add 5 7
    putStrLn ("add 5 7 = " ++ show sumResult)

    -- Test isEven
    let evenCheck1 = isEven 4
    let evenCheck2 = isEven 5
    putStrLn ("isEven 4 = " ++ show evenCheck1)
    putStrLn ("isEven 5 = " ++ show evenCheck2)

    -- Test concatStrings
    let concatResult = concatStrings "Hello, " "Haskell!"
    putStrLn ("concatStrings \"Hello, \" \"Haskell!\" = " ++ concatResult)
```

---

### 🔧 How to Run

1. Save the code as `Functions.hs`
2. Compile using GHC:

   ```bash
   ghc Functions.hs
   ```
3. Run the program:

   ```bash
   ./Functions
   ```

---

### ✅ Output

```
add 5 7 = 12
isEven 4 = True
isEven 5 = False
concatStrings "Hello, " "Haskell!" = Hello, Haskell!
```
