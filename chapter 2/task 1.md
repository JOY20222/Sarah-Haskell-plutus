```haskell
{-# LANGUAGE ScopedTypeVariables #-}

import Data.Typeable (Typeable, typeOf)

main :: IO ()
main = do
    let val1 = 42 :: Int
    let val2 = 3.14 :: Double
    let val3 = "Haskell" :: String
    let val4 = 'Z' :: Char
    let val5 = True && False :: Bool

    putStrLn $ "Type of 42: " ++ show (typeOf val1)
    putStrLn $ "Type of 3.14: " ++ show (typeOf val2)
    putStrLn $ "Type of \"Haskell\": " ++ show (typeOf val3)
    putStrLn $ "Type of 'Z': " ++ show (typeOf val4)
    putStrLn $ "Type of True && False: " ++ show (typeOf val5)
```

---

### 🔧 How to Run:

1. Save the file as `CheckTypes.hs`
2. Compile with GHC:

   ```bash
   ghc CheckTypes.hs
   ```
3. Run the program:

   ```bash
   ./CheckTypes
   ```

---

### ✅ Output:

```
Type of 42: Int
Type of 3.14: Double
Type of "Haskell": [Char]
Type of 'Z': Char
Type of True && False: Bool
```

---

### 🧠 Alternative (GHCi Way – No Code Needed):

You can also do this directly in GHCi:

```haskell
:t 42
:t 3.14
:t "Haskell"
:t 'Z'
:t True && False
```
