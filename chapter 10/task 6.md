```haskell
-- Define a Blockchain data type
data Blockchain = Blockchain
    { blockHeight :: Int
    , blockHash   :: String
    } deriving (Show)

-- Implement Eq with mutual recursion between (==) and (/=)
instance Eq Blockchain where
    x == y = not (x /= y)
    x /= y = not (x == y)

-- Example usage
main :: IO ()
main = do
    let b1 = Blockchain 100 "abc"
    let b2 = Blockchain 100 "abc"
    let b3 = Blockchain 101 "def"

    print (b1 == b2)  -- Should be True
    print (b1 /= b3)  -- Should be True
```

---

### ⚠️ Note:

This code **compiles and runs** because Haskell allows mutual recursion between `(==)` and `(/=)`.
However, this instance will cause **infinite recursion** at runtime unless one of them is overridden with a base case or actual logic.

To avoid **infinite loops**, you must implement **one of them directly**. Here's a **correct version** with actual logic, still showing mutual dependency:

---

### ✅ Safe and Working Mutual Recursion Example:

```haskell
-- Define a Blockchain data type
data Blockchain = Blockchain
    { blockHeight :: Int
    , blockHash   :: String
    } deriving (Show)

-- Implement Eq with mutual recursion (one direction is concrete)
instance Eq Blockchain where
    x == y = blockHeight x == blockHeight y && blockHash x == blockHash y
    x /= y = not (x == y)

-- Example usage
main :: IO ()
main = do
    let b1 = Blockchain 100 "abc"
    let b2 = Blockchain 100 "abc"
    let b3 = Blockchain 101 "def"

    print (b1 == b2)  -- True
    print (b1 /= b3)  -- True
```

---

### 🧪 Output:

```
True
True
