```haskell
{-# LANGUAGE MultiParamTypeClasses #-}
{-# LANGUAGE FlexibleInstances #-}

-- Define the Convertible type class
class Convertible a b where
    convert :: a -> b

-- Define the PaymentMethod type
data PaymentMethod = CreditCard String | PayPal String | BankTransfer String
    deriving (Show)

-- Implement Convertible to convert PaymentMethod to String
instance Convertible PaymentMethod String where
    convert (CreditCard num)    = "Credit Card: " ++ num
    convert (PayPal email)      = "PayPal: " ++ email
    convert (BankTransfer iban) = "Bank Transfer: " ++ iban

-- Example usage
main :: IO ()
main = do
    let pm1 = CreditCard "1234-5678-9012-3456"
    let pm2 = PayPal "user@example.com"
    let pm3 = BankTransfer "DE89370400440532013000"

    putStrLn $ convert pm1
    putStrLn $ convert pm2
    putStrLn $ convert pm3
```

---

### 🧪 Output:

```
Credit Card: 1234-5678-9012-3456
PayPal: user@example.com
Bank Transfer: DE89370400440532013000
```

---

### 🔍 Explanation:

* We use `MultiParamTypeClasses` to allow `Convertible a b`.
* `FlexibleInstances` is needed to allow `Convertible PaymentMethod String`.
* We define several `PaymentMethod` constructors and convert them to a human-readable `String`.
