1. Defines a **custom type class** `ShowSimple`, requiring a function `showSimple :: a -> String`
2. Defines a data type `PaymentMethod`
3. Implements an **instance** of `ShowSimple` for `PaymentMethod`

---

### ✅ Full Running Haskell Code

```haskell
-- Define a custom type class ShowSimple
class ShowSimple a where
    showSimple :: a -> String

-- Define a PaymentMethod data type
data PaymentMethod = Cash | CreditCard | BankTransfer
    deriving (Eq)

-- Implement ShowSimple for PaymentMethod
instance ShowSimple PaymentMethod where
    showSimple Cash         = "Cash"
    showSimple CreditCard   = "Credit Card"
    showSimple BankTransfer = "Bank Transfer"

-- Optional: implement Show so that `print` can show the value too
instance Show PaymentMethod where
    show = showSimple

-- Main function to test showSimple
main :: IO ()
main = do
    let method1 = Cash
        method2 = CreditCard
        method3 = BankTransfer

    putStrLn (showSimple method1)   -- Output: "Cash"
    putStrLn (showSimple method2)   -- Output: "Credit Card"
    putStrLn (showSimple method3)   -- Output: "Bank Transfer"

    -- Using print thanks to the Show instance
    print method1
    print method2
    print method3
```

---

### 🔍 Explanation

* `class ShowSimple a where showSimple :: a -> String` defines a **custom type class** for simplified string conversion.
* `PaymentMethod` is a simple sum type with 3 constructors.
* The `instance ShowSimple PaymentMethod` block defines how each constructor maps to a human-readable string.
* We also define a `Show` instance using `showSimple` for convenience (optional but helpful for `print`).

---

### ✅ Sample Output

```
Cash
Credit Card
Bank Transfer
Cash
Credit Card
Bank Transfer
