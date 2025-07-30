```haskell
-- Define the ShowDetailed type class
class ShowDetailed a where
    showDetailed :: a -> String

-- Define the User data type
data User = User
    { username :: String
    , email    :: String
    , age      :: Int
    } deriving (Show)

-- Implement ShowDetailed for User
instance ShowDetailed User where
    showDetailed (User name mail years) =
        "Username: " ++ name ++ "\n" ++
        "Email: " ++ mail ++ "\n" ++
        "Age: " ++ show years

-- Example usage
main :: IO ()
main = do
    let user1 = User "alice" "alice@example.com" 30
    putStrLn "Detailed User Info:"
    putStrLn (showDetailed user1)
```

---

### 🔍 Explanation:

* **`ShowDetailed`** is a custom type class with a method `showDetailed`.
* **`User`** is a record type with fields: `username`, `email`, and `age`.
* The instance for `User` defines how `showDetailed` produces a detailed string description.
* The `main` function demonstrates the output.

---

### 🧪 Output When You Run It:

```
Detailed User Info:
Username: alice
Email: alice@example.com
Age: 30
