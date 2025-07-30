1. Defines a function `infiniteNumbers` which generates an infinite list of numbers (starting from 1),
2. Extracts only the **first `n` elements** using `take`.

---

### ✅ Haskell Code:

```haskell
-- Define an infinite list of numbers starting from 1
infiniteNumbers :: [Integer]
infiniteNumbers = [1..]

-- Function to extract the first n numbers from the infinite list
firstN :: Int -> [Integer]
firstN n = take n infiniteNumbers

-- Example usage
main :: IO ()
main = do
    putStrLn "First 10 numbers from the infinite list:"
    print (firstN 10)
```

---

### 💡 Explanation:

* `[1..]` is Haskell's syntax for an infinite list of integers starting from 1.
* `take n` extracts the first `n` elements from any list (including infinite lists).
* `firstN 10` gives the first 10 numbers: `[1,2,3,4,5,6,7,8,9,10]`.

---

### 🧪 Output:

```
First 10 numbers from the infinite list:
[1,2,3,4,5,6,7,8,9,10]
