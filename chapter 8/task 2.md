

1. Defines a `PaymentMethod` type with constructors: `Cash`, `Card`, `Cryptocurrency`.
2. Defines a `Person` type with:

   * a `name` (`String`),
   * an `address` (a tuple of `String` and `Int`),
   * a `paymentMethod` (`PaymentMethod`).
3. Creates a `Person` named `bob` who pays with `Cash`.

---

### ✅ Haskell Code:

```haskell
-- Define PaymentMethod data type
data PaymentMethod = Cash | Card | Cryptocurrency
    deriving (Show)

-- Define Person data type
data Person = Person
    { name          :: String
    , address       :: (String, Int)  -- (Street name, house number)
    , paymentMethod :: PaymentMethod
    } deriving (Show)

-- Create a person named Bob who pays with cash
bob :: Person
bob = Person
    { name = "Bob"
    , address = ("Main Street", 42)
    , paymentMethod = Cash
    }

-- Example usage
main :: IO ()
main = print bob
```

---

### 💡 Explanation:

* `PaymentMethod` is a simple enumeration with three options.
* `Person` is a **record type**, which makes the fields clearly named and accessible.
* `bob` is a value of type `Person` initialized with sample data.
* `deriving (Show)` allows printing both `Person` and `PaymentMethod`.

---

### 🧪 Example Output:

```
Person {name = "Bob", address = ("Main Street",42), paymentMethod = Cash}
