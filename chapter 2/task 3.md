```haskell
-- Define immutable variables
myAge :: Int
myAge = 25

piValue :: Double
piValue = 3.14159

greeting :: String
greeting = "Hello, Haskell!"

isHaskellFun :: Bool
isHaskellFun = True

-- Main function to display the variables
main :: IO ()
main = do
    putStrLn ("myAge = " ++ show myAge)
    putStrLn ("piValue = " ++ show piValue)
    putStrLn ("greeting = " ++ greeting)
    putStrLn ("isHaskellFun = " ++ show isHaskellFun)
```

---

### 🔧 How to Run:

1. Save the code to a file named `ImmutableVars.hs`.
2. Compile using:

   ```bash
   ghc ImmutableVars.hs
   ```
3. Run the compiled program:

   ```bash
   ./ImmutableVars
   ```

---

### ✅ Output:

```
myAge = 25
piValue = 3.14159
greeting = Hello, Haskell!
isHaskellFun = True
```
