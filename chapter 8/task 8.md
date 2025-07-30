```haskell
-- Type synonyms
type Name = String
type Age = Int

-- Greeting function
greet :: Name -> Age -> String
greet name age = "Hello, " ++ name ++ "! You are " ++ show age ++ " years old."

-- Example usage
main :: IO ()
main = do
    let personName = "Alice"
    let personAge  = 30
    putStrLn (greet personName personAge)
```

---

### 💡 Explanation:

* `type Name = String` and `type Age = Int` create **aliases** to make type signatures more descriptive and readable.
* `greet` builds a string greeting that includes both the person's name and age.
* `show` is used to convert the `Int` to a `String` for concatenation.

---

### 🧪 Output:

```
Hello, Alice! You are 30 years old.
