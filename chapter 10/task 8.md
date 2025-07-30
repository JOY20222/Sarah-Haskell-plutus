```haskell
-- Define the subclass AdvancedEq of Eq
class Eq a => AdvancedEq a where
    compareEquality :: a -> a -> Bool
    -- Default implementation using (==)
    compareEquality x y = x == y

-- Define a custom data type
data Person = Person
    { name :: String
    , age  :: Int
    } deriving (Show)

-- Make Person an instance of Eq
instance Eq Person where
    (Person name1 age1) == (Person name2 age2) =
        name1 == name2 && age1 == age2

-- Make Person an instance of AdvancedEq
instance AdvancedEq Person where
    -- You can override compareEquality or use default
    compareEquality p1 p2 = name p1 == name p2  -- Custom comparison: only compare names

-- Example usage
main :: IO ()
main = do
    let person1 = Person "Alice" 30
    let person2 = Person "Alice" 40
    let person3 = Person "Bob" 30

    putStrLn $ "person1 == person2: " ++ show (person1 == person2)         -- False
    putStrLn $ "compareEquality person1 person2: " ++ show (compareEquality person1 person2) -- True
    putStrLn $ "compareEquality person1 person3: " ++ show (compareEquality person1 person3) -- False
```

---

### 🔍 Explanation:

* **`AdvancedEq`** is a subclass of `Eq` (note: `class Eq a => AdvancedEq a where ...`).
* We provide a **default implementation** of `compareEquality` using `(==)`, but you can override it as done for `Person`.
* In this example, `compareEquality` compares only the `name` field, while `(==)` compares both `name` and `age`.

---

### 🧪 Sample Output:

```
person1 == person2: False
compareEquality person1 person2: True
compareEquality person1 person3: False
