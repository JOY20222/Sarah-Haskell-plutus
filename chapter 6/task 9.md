 ### ✅ Haskell Code (`CustomMap.hs`)

```haskell
-- Custom map function implemented using recursion
myMap :: (a -> b) -> [a] -> [b]
myMap _ []     = []
myMap f (x:xs) = f x : myMap f xs

-- Example usage
main :: IO ()
main = do
    let numbers = [1, 2, 3, 4, 5]
    let squared = myMap (\x -> x * x) numbers
    putStrLn ("Original list: " ++ show numbers)
    putStrLn ("Squared list: " ++ show squared)
```

---

### 📘 Explanation:

#### 🔧 Function: `myMap`

```haskell
myMap :: (a -> b) -> [a] -> [b]
```

* Takes:

  * A function `f` that transforms each element (`a -> b`)
  * A list of type `[a]`
* Returns a new list `[b]` with `f` applied to each element.

#### 🔁 How it works:

* **Base case**: If the input list is empty, return an empty list.
* **Recursive case**:

  * Apply `f` to the head `x`
  * Recursively apply `myMap f` to the tail `xs`
  * Combine the results using `:` (cons operator)

#### 🧠 Example:

```haskell
myMap (\x -> x * x) [1,2,3]
= (1*1) : (2*2) : (3*3) : []
= [1,4,9]
```

---

### 🧪 How to run:

1. Save it in a file called `CustomMap.hs`
2. Compile with GHC:

   ```bash
   ghc CustomMap.hs
   ```
3. Run the program:

   ```bash
   ./CustomMap
