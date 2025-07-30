```haskell
-- Define the Concatenatable type class
class Concatenatable a where
    concatWith :: a -> a -> a

-- Implement Concatenatable for String (which is [Char])
instance Concatenatable String where
    concatWith = (++)

-- Example usage
main :: IO ()
main = do
    let str1 = "Hello, "
    let str2 = "world!"
    let result = concatWith str1 str2
    putStrLn result  -- Output: Hello, world!
```

---

### 🔍 Explanation:

* `String` is just an alias for `[Char]`, so defining the instance for `String` covers `[Char]` too.
* We use the standard `(++)` operator to implement `concatWith`.
* The `main` function demonstrates the usage.

---

### 🧪 Output:

```
Hello, world!
