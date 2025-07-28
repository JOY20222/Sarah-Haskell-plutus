```haskell
-- Function to calculate area of a triangle using Heron's formula
triangleArea :: Float -> Float -> Float -> Float
triangleArea a b c =
    let s = (a + b + c) / 2
    in sqrt (s * (s - a) * (s - b) * (s - c))

-- Main function to test triangleArea
main :: IO ()
main = do
    let area1 = triangleArea 3 4 5
    let area2 = triangleArea 7 8 9

    putStrLn ("triangleArea 3 4 5 = " ++ show area1)
    putStrLn ("triangleArea 7 8 9 = " ++ show area2)
```

---

### 🔧 How to Run:

1. Save the code as `TriangleArea.hs`.
2. Compile with GHC:

   ```bash
   ghc TriangleArea.hs
   ```
3. Run the program:

   ```bash
   ./TriangleArea
   ```

---

### ✅ Expected Output:

```
triangleArea 3 4 5 = 6.0
triangleArea 7 8 9 = 26.832815
```

---

### 📘 Explanation:

* **Semi-perimeter** `s = (a + b + c) / 2`
* **Heron’s formula**:

  $$
  \text{Area} = \sqrt{s(s - a)(s - b)(s - c)}
  $$
