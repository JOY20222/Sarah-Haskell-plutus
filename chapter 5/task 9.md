```haskell
-- Define the higher-order function
transformList :: (a -> a) -> [a] -> [a]
transformList f = map (f . f)

-- Example usage in main
main :: IO ()
main = do
    print (transformList (+1) [1, 2, 3])    -- Output: [3,4,5]
    print (transformList (*2) [1, 2, 3])    -- Output: [4,8,12]
    print (transformList reverse ["ab", "cd"]) -- Output: ["ab","cd"]
```

---

### 🧠 **Explanation**

* `transformList :: (a -> a) -> [a] -> [a]`
  This function takes:

  * a function from `a` to `a` (e.g., `(+1)`, `(*2)`, etc.)
  * a list of `a`s (`[a]`)
  * and returns a new list where each element has the function applied **twice**.

* `map (f . f)` uses function composition:

  * `f . f` means "apply `f` twice": i.e., `f (f x)`
  * `map (f . f)` applies that to **each element** in the list.

---

### ✅ Example Breakdown

```haskell
transformList (+1) [1,2,3]
-- becomes map ((+1) . (+1)) [1,2,3]
-- => map (\x -> (+1) ((+1) x)) [1,2,3]
-- => map (\x -> x + 1 + 1) [1,2,3]
-- => [3,4,5]
