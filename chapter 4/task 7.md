```haskell
-- Define firstAndThird to extract the 1st and 3rd elements of a list
firstAndThird :: [a] -> (a, a)
firstAndThird (x:_:z:_) = (x, z)
firstAndThird _ = error "List must have at least three elements"

-- Main function to test firstAndThird
main :: IO ()
main = do
    print $ firstAndThird [10, 20, 30, 40]
    print $ firstAndThird ["a", "b", "c", "d", "e"]
    -- Uncommenting the line below will cause a runtime error
    -- print $ firstAndThird [1] 
```

---

### 🔧 How to Run

1. Save as `FirstAndThird.hs`
2. Compile:

   ```bash
   ghc FirstAndThird.hs
   ```
3. Run:

   ```bash
   ./FirstAndThird
   ```

---

### ✅ Output

```
(10,30)
("a","c")
```

---

### ⚠️ Note

* The pattern `(x:_:z:_)` means:

  * `x` is the first element
  * `_` ignores the second
  * `z` is the third
  * `_` ignores the rest
