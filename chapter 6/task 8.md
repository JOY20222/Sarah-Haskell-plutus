```haskell
-- Function to filter even numbers from a list
filterEven :: [Int] -> [Int]
filterEven [] = []
filterEven (x:xs)
    | even x    = x : filterEven xs
    | otherwise = filterEven xs

-- Example usage
main :: IO ()
main = do
    let myList = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
    let evens = filterEven myList
    putStrLn ("Original list: " ++ show myList)
    putStrLn ("Even numbers: " ++ show evens)
```

---

### 📘 Explanation:

#### 🔧 Function: `filterEven`

* **Type**: `[Int] -> [Int]`
* Filters only even numbers from an input list of integers.

#### 🔁 How it works:

* **Base case**: If the list is empty, return an empty list.
* **Recursive case**:

  * If the head `x` is even, include it in the result and recurse on the tail `xs`.
  * If it's odd, skip it and continue.

#### 🧠 Example:

```haskell
filterEven [1,2,3,4]
→ 2 : 4 : []
→ [2,4]
```

---

### 🧪 How to run:

1. Save the code to a file named `FilterEven.hs`
2. Compile it:

   ```bash
   ghc FilterEven.hs
   ```
3. Run it:

   ```bash
   ./FilterEven
