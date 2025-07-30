```haskell
-- Define the Shape data type
data Shape = Circle Double | Rectangle Double Double

-- Implement Show instance
instance Show Shape where
    show (Circle r) = "Circle " ++ show r
    show (Rectangle w h) = "Rectangle " ++ show w ++ " " ++ show h

-- Implement Read instance
instance Read Shape where
    readsPrec _ input =
        case words input of
            ("Circle":r:_) ->
                [(Circle (read r), "")]
            ("Rectangle":w:h:_) ->
                [(Rectangle (read w) (read h), "")]
            _ -> []

-- Example usage
main :: IO ()
main = do
    let shape1 = Circle 5.0
    let shape2 = Rectangle 3.0 4.0

    -- Show examples
    print shape1             -- Circle 5.0
    print shape2             -- Rectangle 3.0 4.0

    -- Read examples
    let shapeStr1 = "Circle 7.5"
    let shapeStr2 = "Rectangle 2.0 6.0"

    print (read shapeStr1 :: Shape)  -- Circle 7.5
    print (read shapeStr2 :: Shape)  -- Rectangle 2.0 6.0
```

---

### 💡 Explanation:

* `Shape` is a custom data type with two constructors:

  * `Circle` takes one `Double` (radius),
  * `Rectangle` takes two `Double`s (width and height).
* `Show` converts `Shape` values to `String`.
* `Read` parses a `String` back into a `Shape`.
* `words` is used to split the input string into components.
* `read` is used to parse `Double` values from the components.

---

This code can be compiled and run with GHC:

```bash
ghc Shape.hs -o shape
./shape
