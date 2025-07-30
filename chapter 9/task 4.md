```haskell
-- Define the Box data type
data Box a = Empty | Has a deriving (Show)

-- Function to extract value from a box or return default if Empty
extract :: a -> Box a -> a
extract defaultVal Empty   = defaultVal
extract _         (Has x)  = x

-- Example usage
box1 :: Box Int
box1 = Has 42

box2 :: Box Int
box2 = Empty

box3 :: Box String
box3 = Has "Hello"

box4 :: Box String
box4 = Empty

-- Main function to test extract
main :: IO ()
main = do
    print (extract 0 box1)              -- Output: 42
    print (extract 0 box2)              -- Output: 0
    print (extract "Default" box3)      -- Output: "Hello"
    print (extract "Default" box4)      -- Output: "Default"
```

---

### 🔍 Explanation

* `extract` pattern matches on the `Box a`:

  * If `Empty`, it returns the default.
  * If `Has x`, it returns `x`.
* Works with any type due to polymorphism.

---

### ✅ Sample Output

```
42
0
"Hello"
"Default"
