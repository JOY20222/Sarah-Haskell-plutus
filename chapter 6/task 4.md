```haskell
-- Product function using foldl
productList :: [Int] -> Int
productList = foldl (*) 1

-- Example usage in main
main :: IO ()
main = do
    let numbers = [1, 2, 3, 4, 5]
    putStrLn ("The product of the list is: " ++ show (productList numbers))
```

---

### 📘 Explanation:

#### 🔧 `foldl` definition:

```haskell
foldl :: (b -> a -> b) -> b -> [a] -> b
```

* It takes:

  * A **binary function** (e.g., `*`) that combines the accumulator with each element
  * An **initial accumulator value**
  * A **list** to process

#### 🧠 How `foldl (*) 1 [1,2,3,4,5]` works:

```
((((1 * 1) * 2) * 3) * 4) * 5 = 120
```

It **accumulates from the left**, starting with `1` as the neutral element for multiplication.

---

### 🧪 How to run:

1. Save the code in a file, for example `ProductList.hs`
2. Compile using GHC:

   ```
   ghc ProductList.hs
   ```
3. Run the compiled program:

   ```
   ./ProductList
