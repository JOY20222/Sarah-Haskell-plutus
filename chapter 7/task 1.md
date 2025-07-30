```haskell
-- Define the Color data type
data Color = Red | Green | Blue

-- Implement the Eq type class
instance Eq Color where
    Red   == Red   = True
    Green == Green = True
    Blue  == Blue  = True
    _     == _     = False

-- Example usage
main :: IO ()
main = do
    print (Red == Red)     -- True
    print (Red == Blue)    -- False
    print (Green == Green) -- True
    print (Blue == Green)  -- False
```

### How it works:

* The `data` declaration defines a custom data type `Color` with three constructors: `Red`, `Green`, and `Blue`.
* The `instance Eq Color where ...` part provides custom logic for comparing two `Color` values using the `==` operator.
* Each constructor is only equal to itself.

### Running:

To run this code:

1. Save it in a file called `ColorEq.hs`.
2. Use `ghc ColorEq.hs` to compile.
3. Run the output executable.
