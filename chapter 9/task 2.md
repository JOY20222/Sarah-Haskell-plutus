```haskell
-- Define the Box data type
data Box a = Empty | Has a deriving (Show)

-- Example usage with different types
boxInt :: Box Int
boxInt = Has 42

boxString :: Box String
boxString = Has "Hello, Haskell!"

emptyBox :: Box a
emptyBox = Empty

-- Function to check if the box is empty
isEmpty :: Box a -> Bool
isEmpty Empty = True
isEmpty _     = False

-- Function to extract value from the box with default
getOrElse :: a -> Box a -> a
getOrElse defaultVal Empty   = defaultVal
getOrElse _         (Has x)  = x

-- Main function
main :: IO ()
main = do
    print boxInt
    print boxString
    print (isEmpty emptyBox)
    print (getOrElse 0 boxInt)
    print (getOrElse "Default" (Empty :: Box String))
```

---

### 🔍 Explanation

* `data Box a = Empty | Has a` defines a type that may hold a value of type `a` (`Has a`) or nothing (`Empty`).
* `deriving (Show)` allows automatic printing using `print`.
* `boxInt`, `boxString`, and `emptyBox` are examples with different types.
* `isEmpty` checks whether the box is empty.
* `getOrElse` returns the value inside the box or a default value if it's `Empty`.

---

### ✅ Sample Output

```
Has 42
Has "Hello, Haskell!"
True
42
"Default"
