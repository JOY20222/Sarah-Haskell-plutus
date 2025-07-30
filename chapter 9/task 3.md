```haskell
-- Define the Box data type
data Box a = Empty | Has a deriving (Show)

-- Function to add a number to the value inside the box (if it exists)
addN :: Num a => a -> Box a -> Box a
addN n (Has x) = Has (n + x)
addN _ Empty   = Empty

-- Example usage
box1 :: Box Int
box1 = Has 10

box2 :: Box Int
box2 = Empty

-- Main function to test addN
main :: IO ()
main = do
    print (addN 5 box1)  -- Output: Has 15
    print (addN 7 box2)  -- Output: Empty
```

---

### 🔍 Explanation

* `data Box a = Empty | Has a`: A generic container type.
* `addN :: Num a => a -> Box a -> Box a`: Adds the given number only if the box contains a number (`Has x`); otherwise returns `Empty`.
* `box1` and `box2` demonstrate usage with an `Int` box.

---

### ✅ Sample Output

```
Has 15
Empty
