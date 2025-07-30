```haskell
-- Define the parameterized Box type
data Box a = Box a deriving (Show)

-- Make Box an instance of Eq (requires a to be Eq)
instance Eq a => Eq (Box a) where
    (Box x) == (Box y) = x == y

-- Example usage
main :: IO ()
main = do
    let box1 = Box 5
    let box2 = Box 5
    let box3 = Box 10

    print (box1 == box2)  -- True
    print (box1 == box3)  -- False
```

---

### 🔍 Explanation:

* `Box a` is a **generic (parameterized) type** holding a value of type `a`.
* The `Eq` instance requires `a` to also be an instance of `Eq` (via `Eq a =>`).
* The `==` function compares the contained values.

---

### 🧪 Output When You Run It:

```
True
False
