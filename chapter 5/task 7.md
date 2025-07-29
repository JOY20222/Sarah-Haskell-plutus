
```haskell
-- Original function rewritten using the $ operator
result :: Int
result = sum $ map (*2) $ filter (>3) [1..10]

-- Main function to test the result
main :: IO ()
main = print result  -- Expected output: 84
```

---

### 🔧 How to Run

1. Save as `DollarOperator.hs`
2. Compile:

   ```bash
   ghc DollarOperator.hs
   ```
3. Run:

   ```bash
   ./DollarOperator
   ```

---

### ✅ Output

```
84
```

---

### 🧠 Explanation

#### Original expression:

```haskell
result = sum (map (*2) (filter (>3) [1..10]))
```

This:

1. Filters numbers greater than 3 from `[1..10]` → `[4,5,6,7,8,9,10]`
2. Doubles each number → `[8,10,12,14,16,18,20]`
3. Sums the result → `84`

#### Rewritten with `$`:

```haskell
result = sum $ map (*2) $ filter (>3) [1..10]
```

* `$` is a **function application operator**.
* `f $ x` means the same as `f (x)`, but helps reduce parentheses.
* The expression evaluates **right to left**:

  ```haskell
  result = sum $ map (*2) $ filter (>3) [1..10]
  ```

  is the same as:

  ```haskell
  result = sum (map (*2) (filter (>3) [1..10]))
