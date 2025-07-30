```haskell
-- Define the Comparable type class
class Comparable a where
    compareWith :: a -> a -> Ordering

-- Define a Blockchain data type
data Blockchain = Blockchain
    { blockHeight :: Int
    , blockHash   :: String
    } deriving (Show)

-- Implement Comparable for Blockchain (based on blockHeight)
instance Comparable Blockchain where
    compareWith b1 b2 = compare (blockHeight b1) (blockHeight b2)

-- Sample data and test
main :: IO ()
main = do
    let block1 = Blockchain 100 "abc123"
    let block2 = Blockchain 150 "def456"
    let block3 = Blockchain 100 "xyz789"

    putStrLn $ "Compare block1 and block2: " ++ show (compareWith block1 block2)
    putStrLn $ "Compare block1 and block3: " ++ show (compareWith block1 block3)
    putStrLn $ "Compare block2 and block1: " ++ show (compareWith block2 block1)
```

### 🔍 Explanation:

* **`Comparable`** is a custom type class with a single method `compareWith`, mimicking the standard `Ord` class.
* **`Blockchain`** is a data type with two fields: `blockHeight` and `blockHash`.
* The instance for `Comparable Blockchain` compares `blockHeight` to determine the ordering.
* The `main` function demonstrates comparison of different `Blockchain` values and prints the results.

### 🧪 Output Example (when running the code):

```
Compare block1 and block2: LT
Compare block1 and block3: EQ
Compare block2 and block1: GT
