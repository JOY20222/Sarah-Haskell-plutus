```haskell
-- Define the Address type
type Address = String

-- Define a parametric type synonym Entity a
type Entity a = (a, Address)

-- Example usage with a Person entity
type Person = String

-- Example values using the Entity type
john :: Entity Person
john = ("John Doe", "123 Main St, Haskell Town")

-- Function to display an entity
displayEntity :: Show a => Entity a -> String
displayEntity (name, address) = "Entity: " ++ show name ++ ", Address: " ++ address

-- Main function to run the code
main :: IO ()
main = putStrLn (displayEntity john)
```

### 🔍 Explanation

* `type Entity a = (a, Address)` defines a parametric type synonym where `a` can be any data type (like `String`, a custom record, etc.).
* `john` is an `Entity Person`, and since `Person` is defined as a `String`, it's a `(String, Address)`.
* `displayEntity` is a helper function to format the output.

### ✅ Output when run:

```
Entity: "John Doe", Address: 123 Main St, Haskell Town
