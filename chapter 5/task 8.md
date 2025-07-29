```haskell
addFive :: Num a => a -> a
addFive x = x + 5
```

---

### 🔁 Point-Free Version

```haskell
addFive :: Num a => a -> a
addFive = (+ 5)
```

---

### 🧪 Full Running Code with Example Usage

```haskell
-- Define the function in point-free style
addFive :: Num a => a -> a
addFive = (+ 5)

-- Example usage in main
main :: IO ()
main = do
    print (addFive 3)  -- Output: 8
    print (addFive 10) -- Output: 15
```

---

### 🧠 Explanation

* `addFive x = x + 5` takes an input `x` and adds `5` to it.
* `(+ 5)` is a **section** — it creates a function that takes a number and adds 5 to it.
* `addFive = (+ 5)` removes the explicit parameter `x`, making it **point-free** (no named arguments).

So:

```haskell
addFive x = x + 5
-- becomes
addFive = (+ 5)
