```haskell
-- Define the Shape type using record syntax with two constructors
data Shape
  = Circle
      { center :: (Float, Float)
      , radius :: Float
      , color  :: String
      }
  | Rectangle
      { width  :: Float
      , height :: Float
      , color  :: String
      }
  deriving (Show)

-- Create a circle instance of Shape
circleShape :: Shape
circleShape = Circle
  { center = (0.0, 0.0)
  , radius = 5.0
  , color  = "Red"
  }

-- Create a rectangle instance of Shape
rectangleShape :: Shape
rectangleShape = Rectangle
  { width  = 10.0
  , height = 4.0
  , color  = "Blue"
  }

-- Example usage
main :: IO ()
main = do
  putStrLn "Circle shape:"
  print circleShape
  putStrLn "Rectangle shape:"
  print rectangleShape
```

---

### 💡 Explanation:

* We define a **sum type** `Shape` with two **constructors**:

  * `Circle`, which includes `center`, `radius`, and `color`,
  * `Rectangle`, which includes `width`, `height`, and `color`.
* **Each constructor** has its **own record fields**. It’s legal in Haskell for different constructors to reuse field names (e.g., both have `color`).
* `deriving (Show)` lets us print `Shape` values easily.

---

### 🧪 Sample Output:

```
Circle shape:
Circle {center = (0.0,0.0), radius = 5.0, color = "Red"}
Rectangle shape:
Rectangle {width = 10.0, height = 4.0, color = "Blue"}
