```haskell
-- Recursive function to check if an element exists in a list
elementExists :: Eq a => a -> [a] -> Bool
elementExists _ [] = False
elementExists x (y:ys)
    | x == y    = True
    | otherwise = elementExists x ys

-- Example usage
main :: IO ()
main = do
    let myList = [10, 20, 30, 40, 50]
    let target1 = 30
    let target2 = 99

    putStrLn ("Does " ++ show target1 ++ " exist in the list? " ++ show (elementExists target1 myList))
    putStrLn ("Does " ++ show target2 ++ " exist in the list? " ++ show (elementExists target2 myList))
```

---

### 📘 Explanation:

#### 🔍 Function: `elementExists`

```haskell
elementExists :: Eq a => a -> [a] -> Bool
```

* **Type Signature**:

  * Takes a value of type `a`, and a list of `a` values.
  * Returns `True` if the element is in the list, `False` otherwise.
  * `Eq a` means that the elements can be compared for equality.

#### 🔁 Logic:

* **Base case**:

  * If the list is empty `[]`, return `False`.
* **Recursive case**:

  * Compare the element `x` with the head `y`.
  * If equal, return `True`; otherwise, continue checking the tail `ys`.

#### 🧠 Example:

```haskell
elementExists 30 [10, 20, 30, 40]
→ compare 30 with 10 → no
→ compare 30 with 20 → no
→ compare 30 with 30 → yes → return True
```

---

### 🧪 How to run:

1. Save the code in a file named `ElementExists.hs`
2. Compile it using GHC:

   ```bash
   ghc ElementExists.hs
   ```
3. Run the compiled program:

   ```bash
   ./ElementExists
