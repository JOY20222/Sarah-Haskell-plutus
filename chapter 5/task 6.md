```haskell
-- Define a function that filters even squares using function composition
evenSquares :: [Int] -> [Int]
evenSquares = filter even . map (^2)

-- Main function to test it
main :: IO ()
main = do
    print $ evenSquares [1..10]      -- [4,16,36,64,100]
    print $ evenSquares [3,5,7]      -- []
    print $ evenSquares [2,4,6,8]    -- [4,16,36,64]
```

---

### 🔧 How to Run

1. Save this as `EvenSquares.hs`
2. Compile:

   ```bash
   ghc EvenSquares.hs
   ```
3. Run:

   ```bash
   ./EvenSquares
   ```

---

### ✅ Output

```
[4,16,36,64,100]
[]
[4,16,36,64]
```

---

### 🧠 Explanation

* `map (^2)` squares each number in the list.
* `filter even` keeps only the even numbers.
* `evenSquares = filter even . map (^2)` composes the two:

  * It’s equivalent to:

    ```haskell
    evenSquares xs = filter even (map (^2) xs)
    ```
  * But written more concisely using function composition.

Function composition `.` connects functions where the output of one becomes the input of the next.
