```haskell
-- Recursive function to reverse a list
reverseList :: [a] -> [a]
reverseList []     = []
reverseList (x:xs) = reverseList xs ++ [x]

-- Example usage
main :: IO ()
main = do
    let original = [1, 2, 3, 4, 5]
    let reversed = reverseList original
    putStrLn ("Original list: " ++ show original)
    putStrLn ("Reversed list: " ++ show reversed)
```

---

### 📘 Explanation:

#### 🔁 How the `reverseList` function works:

* `reverseList [] = []`
  → An empty list reversed is still an empty list.
* `reverseList (x:xs) = reverseList xs ++ [x]`
  → Recursively reverse the rest of the list `xs`, and then append `x` at the end.

#### 🧠 Example trace:

```haskell
reverseList [1,2,3]
= reverseList [2,3] ++ [1]
= (reverseList [3] ++ [2]) ++ [1]
= ([3] ++ [2]) ++ [1]
= [3,2,1]
```

---

### 🧪 How to run:

1. Save the code in a file named `Reverse.hs`
2. Open a terminal and compile it using GHC:

   ```bash
   ghc Reverse.hs
   ```
3. Run the compiled program:

   ```bash
   ./Reverse
