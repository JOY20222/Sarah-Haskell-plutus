HC1T3 - Task 3: Checking if a Number is Greater than 18

---

### ✅ Full Haskell Code

```haskell
-- File: GreaterThan18.hs

-- A pure function that checks if a number is greater than 18
greaterThan18 :: (Ord a, Num a) => a -> Bool
greaterThan18 x = x > 18

-- Main function to demonstrate usage
main :: IO ()
main = do
    let testNumber1 = 20
    let testNumber2 = 15
    putStrLn $ "Is " ++ show testNumber1 ++ " greater than 18? " ++ show (greaterThan18 testNumber1)
    putStrLn $ "Is " ++ show testNumber2 ++ " greater than 18? " ++ show (greaterThan18 testNumber2)
```

---

### 🔧 How to Run:

1. Save the code in a file named `GreaterThan18.hs`.
2. Compile and run with GHC:

```bash
ghc GreaterThan18.hs -o greaterThan18
./greaterThan18
```

Or run interactively in GHCi:

```bash
ghci GreaterThan18.hs
*Main> main
Is 20 greater than 18? True  
Is 15 greater than 18? False
```

---

### ✅ Function Characteristics:

* **Pure**: `greaterThan18` has no side effects and always returns the same output for the same input.
* **Simple**: Uses standard comparison.
* **General**: Works with any numeric type that supports ordering (`Ord` and `Num`).


