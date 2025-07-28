```haskell
-- Use filter to extract all odd numbers from 1 to 30
filterOdds :: [Int]
filterOdds = filter odd [1..30]

-- Main function to display the result
main :: IO ()
main = print filterOdds
```

---

### 🔧 How to Run

1. Save the code in a file named `FilterOdds.hs`
2. Compile it:

   ```bash
   ghc FilterOdds.hs
   ```
3. Run the executable:

   ```bash
   ./FilterOdds
   ```

---

### ✅ Output

```
[1,3,5,7,9,11,13,15,17,19,21,23,25,27,29]
```

---

The `filter odd [1..30]` expression returns only the elements in the list `[1..30]` that satisfy the `odd` predicate.
