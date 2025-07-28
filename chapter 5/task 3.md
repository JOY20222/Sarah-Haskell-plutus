```haskell
import Data.Char (isUpper)

-- Define the function
anyStartsWithUpper :: [String] -> Bool
anyStartsWithUpper = any (\word -> not (null word) && isUpper (head word))

-- Main function to test the behavior
main :: IO ()
main = do
    print $ anyStartsWithUpper ["hello", "world"]         -- False
    print $ anyStartsWithUpper ["hello", "World"]         -- True
    print $ anyStartsWithUpper ["Apple", "banana", "Car"] -- True
    print $ anyStartsWithUpper [""]                       -- False
    print $ anyStartsWithUpper []                         -- False
```

---

### 🔧 How to Run

1. Save the code in a file named `AnyStartsWithUpper.hs`
2. Compile it:

   ```bash
   ghc AnyStartsWithUpper.hs
   ```
3. Run the program:

   ```bash
   ./AnyStartsWithUpper
   ```

---

### ✅ Example Output

```
False
True
True
False
False
```

---

### 🧠 Explanation

* `any` checks whether **any element** of the list satisfies the given predicate.
* The lambda `\word -> not (null word) && isUpper (head word)` ensures:

  * The word is not empty.
  * The first character is uppercase.
