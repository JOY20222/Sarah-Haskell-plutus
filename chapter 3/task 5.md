* `"Equilateral"` (all sides equal)
* `"Isosceles"` (two sides equal)
* `"Scalene"` (no sides equal)

---

### ✅ Code: `TriangleType.hs`

```haskell
-- Function to classify a triangle by its sides
triangleType :: Float -> Float -> Float -> String
triangleType a b c
    | a == b && b == c = "Equilateral"
    | a == b || b == c || a == c = "Isosceles"
    | otherwise = "Scalene"

-- Main function to test triangleType
main :: IO ()
main = do
    putStrLn ("triangleType 3 3 3 = " ++ triangleType 3 3 3)
    putStrLn ("triangleType 5 5 8 = " ++ triangleType 5 5 8)
    putStrLn ("triangleType 6 7 8 = " ++ triangleType 6 7 8)
```

---

### 🔧 How to Run:

1. Save the file as `TriangleType.hs`.
2. Compile:

   ```bash
   ghc TriangleType.hs
   ```
3. Run:

   ```bash
   ./TriangleType
   ```

---

### ✅ Expected Output:

```
triangleType 3 3 3 = Equilateral
triangleType 5 5 8 = Isosceles
triangleType 6 7 8 = Scalene
