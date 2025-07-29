```haskell
-- Recursive function to compute the length of a list
listLength :: [a] -> Int
listLength []     = 0
listLength (_:xs) = 1 + listLength xs

-- Example usage
main :: IO ()
main = do
    let myList = [5, 10, 15, 20, 25]
    let len = listLength myList
    putStrLn ("The length of the list is: " ++ show len)
```

---

### 📘 Explanation:

#### 🔧 Function: `listLength`

```haskell
listLength :: [a] -> Int
```

* Takes a list of any type `[a]` and returns its length as an `Int`.

#### 🔁 How it works:

* **Base case**:

  * If the list is empty (`[]`), the length is `0`.
* **Recursive case**:

  * If the list has at least one element (`_ : xs`), count `1` for the head, and recursively compute the length of the tail `xs`.

#### 🧠 Example step-by-step:

```haskell
listLength [5, 10, 15]
= 1 + listLength [10, 15]
= 1 + (1 + listLength [15])
= 1 + (1 + (1 + listLength []))
= 1 + (1 + (1 + 0))
= 3
```

---

### 🧪 How to run:

1. Save the code in a file called `ListLength.hs`
2. Compile it using GHC:

   ```bash
   ghc ListLength.hs
   ```
3. Run the program:

   ```bash
   ./ListLength
