```haskell
import Text.Read (readMaybe)

-- Define the Shape data type
data Shape = Circle Double | Rectangle Double Double
    deriving (Show, Read)

-- Define the parseShape function
parseShape :: String -> Maybe Shape
parseShape input = readMaybe input :: Maybe Shape

-- Example usage
main :: IO ()
main = do
    -- Valid inputs
    print (parseShape "Circle 5.0")          -- Just (Circle 5.0)
    print (parseShape "Rectangle 3.0 4.0")   -- Just (Rectangle 3.0 4.0)

    -- Invalid inputs
    print (parseShape "Triangle 3.0 4.0")    -- Nothing
    print (parseShape "Circle five")         -- Nothing
    print (parseShape "")                    -- Nothing
```

---

### 💡 Explanation:

* `Shape` is defined with `deriving (Show, Read)` so we can automatically parse strings using `readMaybe`.
* `parseShape` uses `readMaybe` from `Text.Read` which safely attempts to parse the string.
* If parsing succeeds, it returns `Just shape`; otherwise, `Nothing`.

---

### 🧪 Sample Output:

```haskell
Just (Circle 5.0)
Just (Rectangle 3.0 4.0)
Nothing
Nothing
Nothing
```

---

To run this code:

1. Save it in a file (e.g. `ParseShape.hs`),
2. Compile with `ghc ParseShape.hs`,
3. Run the executable;
