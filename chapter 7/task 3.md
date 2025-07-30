```haskell
-- Define the function
compareValues :: (Eq a, Ord a) => a -> a -> a
compareValues x y
    | x >= y    = x
    | otherwise = y

-- Example usage
main :: IO ()
main = do
    print (compareValues 5 10)       -- 10
    print (compareValues 'a' 'z')    -- 'z'
    print (compareValues 3.5 2.1)    -- 3.5
    print (compareValues "hi" "hello") -- "hi" (because "hi" > "hello" lexicographically)
```

---

### 💡 Explanation:

* The type signature:

  ```haskell
  compareValues :: (Eq a, Ord a) => a -> a -> a
  ```

  says that `a` must be an instance of both `Eq` (for `==`) and `Ord` (for comparison like `>=`).
* The function compares `x` and `y`, and returns the greater one.
* Example usages test the function with integers, characters, floats, and strings.
