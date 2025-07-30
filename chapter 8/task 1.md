```haskell
-- Type synonyms
type Address = String
type Value = Int

-- Function to generate a transaction description
generateTx :: Address -> Address -> Value -> String
generateTx fromAddr toAddr val =
    "Transaction from " ++ fromAddr ++ " to " ++ toAddr ++ " with value " ++ show val

-- Example usage
main :: IO ()
main = do
    let sender = "addr1qxyz..."
    let receiver = "addr1qabc..."
    let amount = 1000

    putStrLn (generateTx sender receiver amount)
```

---

### 💡 Explanation:

* `type Address = String` and `type Value = Int` are **type synonyms**, useful for readability and intent.
* `generateTx` constructs a message like:
  `"Transaction from addr1qxyz... to addr1qabc... with value 1000"`

---

### 🧪 Example Output:

```
Transaction from addr1qxyz... to addr1qabc... with value 1000
