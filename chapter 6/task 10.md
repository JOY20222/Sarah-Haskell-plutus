```haskell
-- Recursive function to convert a number to a list of its digits
digits :: Int -> [Int]
digits n
    | n < 10    = [n]
    | otherwise = digits (n `div` 10) ++ [n `mod` 10]

-- Example usage
main :: IO ()
main = do
    let number = 12345
    let digitList = digits number
    putStrLn ("Digits of " ++ show number ++ ": " ++ show digitList)
```

---

### 📘 Explanation:

#### 🔧 Function: `digits`

```haskell
digits :: Int -> [Int]
```

* Takes an `Int` and returns a list of `Int` representing its digits.

#### 🔁 How it works:

* **Base case**:
  If `n < 10`, return `[n]` (a single-digit number).
* **Recursive case**:

  * `digits (n `div` 10)` recursively processes all digits **except the last**
  * `n `mod` 10` gets the **last digit**
  * Combine them using `++` to preserve the correct order

#### 🧠 Example:

```haskell
digits 123
= digits 12 ++ [3]
= (digits 1 ++ [2]) ++ [3]
= ([1] ++ [2]) ++ [3]
= [1,2,3]
```

---

### 🧪 How to run:

1. Save the code in a file named `DigitsList.hs`
2. Compile it using GHC:

   ```bash
   ghc DigitsList.hs
   ```
3. Run the program:

   ```bash
   ./DigitsList
