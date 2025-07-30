```haskell
-- Define the parametric Shape data type
data Shape a
    = Circle a Float           -- Color and radius
    | Rectangle a Float Float  -- Color, width, and height
    deriving (Show)

-- Example shapes with String as the color type
circle1 :: Shape String
circle1 = Circle "Red" 10.0

rectangle1 :: Shape String
rectangle1 = Rectangle "Blue" 5.0 7.0

-- Function to describe a shape
describeShape :: Show a => Shape a -> String
describeShape (Circle color radius) =
    "Circle with color: " ++ show color ++ " and radius: " ++ show radius
describeShape (Rectangle color width height) =
    "Rectangle with color: " ++ show color ++
    ", width: " ++ show width ++ ", height: " ++ show height

-- Main function to run examples
main :: IO ()
main = do
    putStrLn (describeShape circle1)
    putStrLn (describeShape rectangle1)
```

---

### 🔍 Explanation

* `Shape a` is **parametric**, meaning the color field can be of **any type** `a` (e.g. `String`, `Int`, `Color`, etc.).
* `Circle a Float`: a circle with a color and a radius.
* `Rectangle a Float Float`: a rectangle with a color, width, and height.
* `describeShape` is a helper function to print out shape details.

---

### ✅ Sample Output

```
Circle with color: "Red" and radius: 10.0
Rectangle with color: "Blue", width: 5.0, height: 7.0
