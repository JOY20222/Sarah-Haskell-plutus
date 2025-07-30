1. Defines a `Shape` data type with:

   * `Circle Float`
   * `Rectangle Float Float`
2. Implements a function `area :: Shape -> Float` to calculate area.
3. Computes:

   * Area of a **circle with radius 5**
   * Area of a **rectangle with sides 10 and 5**

---

### ✅ Haskell Code:

```haskell
-- Define the Shape data type
data Shape = Circle Float | Rectangle Float Float
    deriving (Show)

-- Define the area function
area :: Shape -> Float
area (Circle r) = pi * r * r
area (Rectangle w h) = w * h

-- Example usage
main :: IO ()
main = do
    let circle = Circle 5
    let rectangle = Rectangle 10 5

    putStrLn $ "Area of circle with radius 5: " ++ show (area circle)
    putStrLn $ "Area of rectangle with sides 10 and 5: " ++ show (area rectangle)
```

---

### 💡 Explanation:

* `Circle r`: Area is `π * r²`
* `Rectangle w h`: Area is `w * h`
* The `main` function demonstrates usage by printing the area of both shapes.

---

### 🧪 Output:

```
Area of circle with radius 5: 78.53982
Area of rectangle with sides 10 and 5: 50.0
