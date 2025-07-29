```haskell
-- Sum function using foldr
sumList :: [Int] -> Int
sumList = foldr (+) 0

-- Example usage in main
main :: IO ()
main = do
    let numbers = [1, 2, 3, 4, 5]
    putStrLn ("The sum of the list is: " ++ show (sumList numbers))
```

---

### 📘 Explanation:

#### 🔧 `foldr` definition:

```haskell
foldr :: (a -> b -> b) -> b -> [a] -> b
```

* It takes:

  * A **function** that combines an element with the result (e.g., `+`)
  * An **initial value** (also called the accumulator)
  * A **list** to process

#### 🧠 How `foldr` works:

For the list `[1, 2, 3, 4, 5]`, `foldr (+) 0` evaluates like this:

```
1 + (2 + (3 + (4 + (5 + 0))))
```

So it **recursively adds** elements from **right to left**.

---

### 🧪 How to run:

1. Save this in a file, for example `SumList.hs`
2. Compile it with GHC:

   ```
   ghc SumList.hs
   ```
3. Run the output program:

   ```
   ./SumList
