```haskell
-- Type synonyms for clarity
type Address = String
type Value = Int

-- Define the Transaction type using record syntax
data Transaction = Transaction
  { from          :: Address
  , to            :: Address
  , amount        :: Value
  , transactionId :: String
  } deriving (Show)

-- Function to create a transaction and return the transaction ID
createTransaction :: Address -> Address -> Value -> String
createTransaction sender receiver val =
  let txId = "tx-" ++ take 6 sender ++ "-" ++ take 6 receiver ++ "-" ++ show val
      tx = Transaction
            { from = sender
            , to = receiver
            , amount = val
            , transactionId = txId
            }
  in transactionId tx

-- Example usage
main :: IO ()
main = do
  let sender = "address123456789"
  let receiver = "address987654321"
  let val = 500
  let txId = createTransaction sender receiver val
  putStrLn $ "Transaction created with ID: " ++ txId
```

---

### 💡 Explanation

* `Transaction` is a record with named fields: `from`, `to`, `amount`, and `transactionId`.
* `createTransaction` builds a basic ID by using parts of the sender and receiver address plus the amount.
* The ID format is: `tx-<first6OfSender>-<first6OfReceiver>-<value>`.

---

### 🧪 Sample Output

```
Transaction created with ID: tx-addres-addres-500
