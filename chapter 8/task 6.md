```haskell
-- Define the function
addNumbers :: Int -> Int -> Int
addNumbers x y = x + y

-- Example usage
main :: IO ()
main = do
    let a = 10
    let b = 15
    putStrLn $ "The sum of " ++ show a ++ " and " ++ show b ++ " is " ++ show (addNumbers a b)
```

---

### 💡 Explanation:

* `addNumbers :: Int -> Int -> Int` defines a function that takes two `Int` values and returns their sum.
* `main` demonstrates calling `addNumbers` with example values.

---

### 🧪 Output:

```
The sum of 10 and 15 is 25
