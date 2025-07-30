```haskell
-- Define the Color data type
data Color = Red | Green | Blue deriving (Show, Eq)

-- Implement the Ord type class
instance Ord Color where
    compare Red   Red   = EQ
    compare Red   _     = LT
    compare Green Red   = GT
    compare Green Green = EQ
    compare Green Blue  = LT
    compare Blue  Blue  = EQ
    compare Blue  _     = GT

-- Example usage
main :: IO ()
main = do
    print (Red < Green)     -- True
    print (Green < Blue)    -- True
    print (Blue > Red)      -- True
    print (Red >= Blue)     -- False
    print (compare Green Red)  -- GT
    print (compare Red Blue)   -- LT
```

---

### 💡 Explanation:

* `data Color = Red | Green | Blue` defines the `Color` type.
* `deriving (Show, Eq)` automatically implements `Show` (for printing) and `Eq` (for equality).
* `instance Ord Color` provides the custom ordering:

  * `Red < Green < Blue`
  * `compare` is used to define how any two `Color` values are ordered.
