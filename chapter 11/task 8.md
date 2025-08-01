```haskell
main :: IO ()
main = do
    putStrLn "Enter a number:"
    input <- getLine
    let number = read input :: Int
    if even number
        then putStrLn "The number is even."
        else putStrLn "The number is odd."
```

---

### 🧠 Explanation:

* `getLine` reads the input as a `String`.
* `read input :: Int` converts the string to an integer.
* `even` is a built-in function that checks if a number is even.
* `if ... then ... else` chooses the appropriate message to print.

---

### ✅ Example:

**Input:**

```
Enter a number:
7
```

**Output:**

```
The number is odd.
```

---

### ▶️ How to Run:

1. Save as `Main.hs`
2. Compile and run:

   ```bash
   ghc Main.hs -o evenOdd
   ./evenOdd
   ```

Or run in GHCi:

```bash
ghci Main.hs
main
